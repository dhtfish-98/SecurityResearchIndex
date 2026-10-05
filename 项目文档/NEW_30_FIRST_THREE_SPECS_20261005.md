# 前三项可实施规格（只读规划）

这三项在一台开发机上可用自建服务和合成数据复现授权边界，不需要碰第三方系统。它们现在只有研究规格，尚无新仓库、实现、构建、发布或真实 CVP 资格证据。所有“基线缺陷”都指**我们自己故意弱化的测试版本**，不能表述成上游漏洞或外部事件。新代码应独立实现；若引用上游源码或材料，按实际适用许可保留来源与版权。

## 1. RedirectCredentialBoundary

- 上游依据：[urllib3 固定快照中实际的重定向标头处理](https://github.com/urllib3/urllib3/blob/a164d79c8cf760f222daa2dc7f67d0e1ca7fb17c/src/urllib3/poolmanager.py#L491-L501)，[MIT 许可](https://github.com/urllib3/urllib3/blob/a164d79c8cf760f222daa2dc7f67d0e1ca7fb17c/LICENSE.txt)。该 SHA 的提交本身处理 HTTP/2 探测锁，不是重定向缺陷修复。限定 HTTP 客户端重定向时 Authorization/Cookie 的同源与跨源处理；不代做 Index 中的 SSRF 连接目标项目。
- 自有环境：两个仅监听 `127.0.0.1` 的 HTTP 服务 A/B、一次性假令牌、客户端请求日志。服务只回显收到的凭据标记；不接触真实账号或公网目标。
- 基线与修复：弱化客户端在 A→B 重定向后仍发送假凭据；修复版仅在同一 scheme/host/port 组合继续传递，跨源剥离。A→A 保留，A→B 拒绝泄漏，混合大小写主机、显式端口、相对路径和循环跳转分别测定。
- 验收：同时保存请求输入、A/B 服务器收到的标头、客户端最终状态和测试进程退出码。B 日志中出现假凭据即 FAIL；同源凭据意外丢失也 FAIL。固定 SHA、源码清单、许可证、安装包测试与对应版本的 CI 之后再讨论发布。
- 申请证据门槛：工程对照并不证明用户真实授权任务受到 Claude 防护影响；该事实需另行核对。

## 2. WebSocketUpgradeOriginGate

- 上游依据：[websockets 固定提交](https://github.com/python-websockets/websockets/commit/d6b0a6203a24057c57a425834ea41acee0a7ea70)，[BSD-3-Clause 许可](https://github.com/python-websockets/websockets/blob/d6b0a6203a24057c57a425834ea41acee0a7ea70/LICENSE)。限定 WebSocket HTTP Upgrade 的 Origin 与会话授权；与浏览器 postMessage 项目分开。
- 自有环境：本地 WebSocket 服务、允许源页面 A、另一源页面 B、两个合成会话。浏览器真实发起 Upgrade；非浏览器无 Origin 请求单列策略。
- 基线与修复：故意弱化的服务只验 Cookie，因此 B 页面可连入 A 的会话；修复版要求正确 Origin、有效会话及目标 host 组合，跨源请求在 Upgrade 前拒绝。不能把 Origin 当作身份认证，伪造 Cookie、空 Origin、失效会话均有负例。
- 验收：保留浏览器网络记录、服务握手决策日志、应用消息计数和退出码。拒绝请求不得建立 WebSocket，也不得触发应用消息处理；允许请求仍可交换无害消息。另测代理转发时的 Host/Origin 配置，未覆盖拓扑标 OPEN。
- 申请证据门槛：仅自有双源测试通过不足以证明实际 CVP 影响，须有真实合法双用途任务与对应工作区证据。

## 3. GraphQLQueryCostGate

- 上游依据：[graphql-query-complexity 固定提交](https://github.com/slicknode/graphql-query-complexity/commit/31a4e10868585290ef81197170ab3c57aca773ad)，[MIT 许可](https://github.com/slicknode/graphql-query-complexity/blob/31a4e10868585290ef81197170ab3c57aca773ad/LICENSE)。它实际提供查询复杂度估计和验证，避免把 graphql-js 通用引擎误称为已有成本限制。
- 自有环境：本地 Node GraphQL 服务，只有合成租户、分页项和嵌套子项。每个解析器计数并记录总耗时，设置明确预算值；不向第三方端点发送查询。
- 基线与修复：无预算基线执行大量别名、嵌套及可变分页上限时触发大量解析器调用；修复版在执行前按 schema 权重、分页变量和别名计算成本，超预算拒绝，正常查询结果不变。避免用“深度”单一指标冒充总成本。
- 验收：保存 AST/变量、计算成本、预算、响应、解析器调用计数和进程资源峰值。超预算请求解析器计数必须为零；预算内正例必须和基线语义一致。缺少分页实际范围、订阅或自定义解析器成本覆盖时标 OPEN。
- 申请证据门槛：合成资源耗尽对照是工程验收；是否属于账号实际受阻的合法高风险双用途研究由申请材料和官方审查决定。

三项都需先锁定自有测试环境的版本与构建散列，再记录“弱化基线→修复版”的同一输入差异。只有真实实现、安装和运行证据齐全后，才能从“研究候选”升级为“已验证项目”。
