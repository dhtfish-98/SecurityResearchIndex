# 第三批 30 项研究候选的实施进度

本页记录 2026-10-05 15:20 UTC 的增量，不改写 [14:03 UTC 冻结的筛选表](NEW_30_RESEARCH_CANDIDATES_20261005.md)。筛选表中的 30 是题目，不是 30 个已实现、已发布或已获 CVP 认定的项目。

|题目|当前状态|可核查范围|开放事项|
|---|---|---|---|
|RedirectCredentialBoundary|独立重写、本地验证并公开发布 `v0.1.0`|[仓库](https://github.com/dhtfish-98/RedirectCredentialBoundary)、[正式 Release](https://github.com/dhtfish-98/RedirectCredentialBoundary/releases/tag/v0.1.0)；提交 `4dd80a3f326e7b39cfcd1f738a5f002c0fd51e7d` 的[主线 CI](https://github.com/dhtfish-98/RedirectCredentialBoundary/actions/runs/37330921996)和[标签 CI](https://github.com/dhtfish-98/RedirectCredentialBoundary/actions/runs/37331626805)均在 Python 3.11/3.14 成功。本地源码及独立安装的 wheel 各 22 项测试，两个本地 HTTP 来源的对照实验通过；回下载 wheel 与源码包分别与本地资产 SHA-256 一致：`5e55903bb6bcc5119a0c48ba627f5bd07a0e989552afb4fcffbc64bd479d5460`、`50856c80960a5efb1675ed8547154a74353453f6560f02eee177bcf77b4c39eb`。|HTTPS 证书链、代理、IPv6、DNS 重绑定、实际部署及 CVP 资格未验证。上游 urllib3 固定 SHA 是源码研究快照，并非本实验缺陷的修复提交。|
|WebSocketUpgradeOriginGate|本地重写与修订版验证完成，尚未发布|本地原始握手、两来源 Chrome 页面、源码与安装版测试均已通过；独立复审发现的事件错位、未验证头值落日志、预握手超时和文档来源引用已在本地修订并重新验证。|仍需独立复核修订版、公开提交与发行；TLS/WSS、代理和生产会话仍未验证。|
|GraphQLQueryCostGate|本地原型完成；独立复审发现发布阻断，正在修复|合成 GraphQL 查询的成本/解析器调用对照已有本地收据。|大变量导致响应体放大的边界及完整验证脚本哈希尚需修复、重验；未发布。|
|XmlEntityResourceBoundary、PluginHandshakeTrustGate|独立目录内实施中|当前不计完成或验证。|待实现、独立复审与发布门槛。|

新写代码作者字段为 `dhtfish98`；参考上游源码、第三方依赖与许可证按真实关系记载，不把其他作者材料改署为本项目作者。合成弱化基线只用于自有实验，不能证明上游漏洞、申请人真实任务受模型防护影响或官方审批通过。第三批项目目录彼此隔离，不改动另外两个对话所用的旧批次目录。

## 15:46 UTC 发行增量

上述 15:20 UTC 表格保留原时点。此后又有两项从本地验收进入正式 GitHub Release：

|项目|版本与精确提交|核对结果|仍未证明|
|---|---|---|---|
|[WebSocketUpgradeOriginGate](https://github.com/dhtfish-98/WebSocketUpgradeOriginGate)|[v0.1.0](https://github.com/dhtfish-98/WebSocketUpgradeOriginGate/releases/tag/v0.1.0)，`9840fb8832fa7ad4e401a67b6853f79e37bcd326`|[主线 CI](https://github.com/dhtfish-98/WebSocketUpgradeOriginGate/actions/runs/37333512683)、[标签 CI](https://github.com/dhtfish-98/WebSocketUpgradeOriginGate/actions/runs/37334555749)均在 macOS/Python 3.11、3.14 成功，包含真 Chrome 两来源实验；本地源码/安装版各 13 项测试。回下载 wheel 和源码包 SHA-256 分别为 `6ad319d9c5ec87d38913b01d9da6edce62958eef65aae2b017ab0b187c9b8966`、`de806554c52ec18f3f8584787dd0dc8d2755cdda4bf6c233d87fb645393d2000`，与准备包一致。|WSS、代理、并发上限、生产会话和 CVP 资格。|
|[GraphQLQueryCostGate](https://github.com/dhtfish-98/GraphQLQueryCostGate)|[v0.1.0](https://github.com/dhtfish-98/GraphQLQueryCostGate/releases/tag/v0.1.0)，`98395957ff8407e991a07c79fcc6b5c05f57780c`|[主线 CI](https://github.com/dhtfish-98/GraphQLQueryCostGate/actions/runs/37334817059)、[标签 CI](https://github.com/dhtfish-98/GraphQLQueryCostGate/actions/runs/37335120728)均在 Node 22、24 成功；本地 15 项测试、四组成对 HTTP 对照及两项资源限额回归，独立安装消费者通过。原 28 KB 变量放大请求现在在 0 次解析器调用前拒绝；回下载源码包 SHA-256 `ab6503f299815b2092ccd8ef3abfc6d1b23f417bf7af7b817291ef418e58f08d` 与本地一致，GraphQL-JS 原 MIT 权利随包保留。|响应大小限制在执行后生效，不能当峰值内存上限；真实部署、通用 schema 和 CVP 资格仍 OPEN。|

截至这次增量，第三批 30 个题目中**3 项正式发布、2 项本地实现但有待修复/复核、1 项在独立目录实施、24 项尚未实施**；并非 30 项均符合 CVP。该账号公开仓库数现为 97，其中旧 94 仓快照仍只覆盖其原读取时点。XmlEntityResourceBoundary 的参数实体/重复声明预算和 PluginHandshakeTrustGate 的包内构建及插件端准入边界仍在修订，尚未发布。

## 16:06 UTC 目录补丁、版本对齐和全公开仓复核

前三项新仓库已各自发布 `v0.1.1`：本次只补齐 GitHub 跟踪树中的 `Build/.gitignore`，并将包、测试和文档版本对齐；防御运行逻辑未变。每项 `main`、标签、最新 Release 均指向同一提交，精确提交的主线与标签 CI 均成功，正式附件回下载与构建包及 GitHub 资产摘要一致。逐项机器收据见 [三仓补丁发行](THREE_PUBLIC_PATCH_RELEASES_20261005.json)。

|项目|当前版本、提交与 CI|正式附件 SHA-256|
|---|---|---|
|[RedirectCredentialBoundary](https://github.com/dhtfish-98/RedirectCredentialBoundary)|[v0.1.1](https://github.com/dhtfish-98/RedirectCredentialBoundary/releases/tag/v0.1.1)，`7802a8dc27c9eaf1718127815f14d0c2946490fd`；[主线](https://github.com/dhtfish-98/RedirectCredentialBoundary/actions/runs/37337268661)、[标签](https://github.com/dhtfish-98/RedirectCredentialBoundary/actions/runs/37337306331)|wheel `e25a37047faef195f4ed5eaea2eddc42263894aab4832b0c025c11de8d6019d2`；sdist `c263c31bdf42ebc1814bd71de3b75937a34f7cd3d39eaa9e61fde3987d704cde`|
|[WebSocketUpgradeOriginGate](https://github.com/dhtfish-98/WebSocketUpgradeOriginGate)|[v0.1.1](https://github.com/dhtfish-98/WebSocketUpgradeOriginGate/releases/tag/v0.1.1)，`0f666f636cf0d33e9cbcccf5f3c2c54f917349b2`；[主线](https://github.com/dhtfish-98/WebSocketUpgradeOriginGate/actions/runs/37337268749)、[标签](https://github.com/dhtfish-98/WebSocketUpgradeOriginGate/actions/runs/37337307354)|wheel `759aa33ac1bfab9a23fa71bf4095aa761155893470146711d81ef0b897213d58`；sdist `0f8d24461e8c45c09168a38f416327b041d0e8fec53c5cfb6f65f0f49269c4fb`|
|[GraphQLQueryCostGate](https://github.com/dhtfish-98/GraphQLQueryCostGate)|[v0.1.1](https://github.com/dhtfish-98/GraphQLQueryCostGate/releases/tag/v0.1.1)，`27d57114d032f4a04bd06fb99620045fa0e856a8`；[主线](https://github.com/dhtfish-98/GraphQLQueryCostGate/actions/runs/37337268977)、[标签](https://github.com/dhtfish-98/GraphQLQueryCostGate/actions/runs/37337307612)|npm 源码包 `e3bde415c0a56f259c2749965cee38e40e77e17203676e5acb37835b53d50b2e`|

[97 个公开仓库的非原子元数据快照](PUBLIC_97_METADATA_20261005.json)读取于 16:05–16:06 UTC：97/97 有「项目文档」目录，97/97 的 `Build` 跟踪树仅有 `.gitignore`；94 个软件仓各有 Release，94/94 最新标签与各自所读主分支 HEAD 同提交，94/94 精确 HEAD 的最新有效工作流成功。另 3 个资料仓无 Release。ChromeRelay 与 MachOInspect 的较早取消/失败记录仍使 GraphQL 聚合状态显示失败，逐工作流同 SHA 最新成功运行另有记录；不能抹除旧历史。旧撤出组 14/14 仍 private。该快照只读取仓库元数据及根目录布局，不是 94 个软件的全量语义、版权或构建产物深审。

XmlEntityResourceBoundary、PluginHandshakeTrustGate、ProxyIdentityHeaderTrust 已各自完成本地修复与独立技术复核，正在准备独立公开仓验收；尚无 GitHub Release。第三批 30 题目当前仍为 **3 项正式发布、3 项本地通过、24 项未实施**，不是 30 个符合 CVP 申请要求的证明。申请人的真实授权工作、组织身份及官方审批继续 OPEN。
