# 30 个防御研究候选的逐项状态（2026-10-05）

此清单把[两批已发布项目的代码级再筛](CVP_CODE_SCOPE_RECHECK_20261004.md)和[未实施题目再筛](PROJECT_30_FIT_RECHECK_20261005.md)合为一个可核对的 30 项队列。它不是 30 个已完成项目：**6 个有代码和发行证据的条件技术案例、24 个尚未实现的研究方向、0 个经 Anthropic 确认的 CVP 合格或获批项目**。另 54 个既有项目归工程背景，不靠改名并入此队列。候选只在真实授权的防御任务与相关防护影响能够对应时才有申请价值，具体资格由官方决定。

| 序号 | 项目或拟议方向 | 当前状态 | 独立验收所需的关键证据 |
| ---: | --- | --- | --- |
| 01 | [WheelNamespaceReview](https://github.com/dhtfish-98/WheelNamespaceReview) | 已实现，条件案例 | 自有包样本的命名空间解析风险、修复前后安装/导入差异；不以离线样例覆盖真实供应链。 |
| 02 | [CITrustBoundaryReview](https://github.com/dhtfish-98/CITrustBoundaryReview) | 已实现，条件案例 | 授权 CI 工作流中不可信输入到执行边界的可复核差异及修复回归。 |
| 03 | [DeserializeCallReview](https://github.com/dhtfish-98/DeserializeCallReview) | 已实现，条件案例 | 自有服务或工件处理路径中危险反序列化调用的实际到达、隔离与回归。 |
| 04 | [DOMSinkReview](https://github.com/dhtfish-98/DOMSinkReview) | 已实现，条件案例 | 自有页面中的输入到 DOM sink 的可达路径、上下文及修复后浏览器行为。 |
| 05 | [YaraRuleDraftReview](https://github.com/dhtfish-98/YaraRuleDraftReview) | 已实现，条件案例 | 授权恶意样本调查中的规则草拟、误报/漏报边界及独立引擎验证。 |
| 06 | [ModelOpcodeReview](https://github.com/dhtfish-98/ModelOpcodeReview) | 已实现，条件案例 | 自有模型处理流程中静态发现与实际加载隔离的对应证据；不能宣称静态检查可证明全模型安全。 |
| 07 | WebSessionDastReview | 未实现，优先研究 | 自有 Web 服务的会话边界缺陷、修复前后会话与权限矩阵。 |
| 08 | ParserCrashBoundaryReview | 未实现，优先研究 | 自有解析器的真实崩溃、最小输入、根因与修复回归。 |
| 09 | HttpDesyncBoundaryReview | 未实现，优先研究 | 自有代理和后端的请求边界差异及修复后双端一致性；不触碰第三方服务。 |
| 10 | JwtVerifierConfusionReview | 未实现，优先研究 | 自有验证器对算法、密钥来源和声明的接受/拒绝矩阵。 |
| 11 | OAuthCodePkceReplayReview | 未实现，优先研究 | 自有授权服务器与客户端的授权码/PKCE 重放边界及修复结果。 |
| 12 | SamlSignatureWrappingReview | 未实现，优先研究 | 自有 SAML 测试环境中签名对象与业务对象的一致性校验。 |
| 13 | ADCSIssuanceAbuseReview | 未实现，优先研究 | 自有 AD CS 实验域的证书模板权限、实际签发限制与修复对照。 |
| 14 | WASIPreopenBoundaryReview | 未实现，优先研究 | 自有 WASI 运行时对预打开目录权限的实际系统调用和拒绝边界。 |
| 15 | WindowsIoctlDispatchReview | 未实现，优先研究 | 自有 Windows 驱动测试 VM 的 IOCTL 授权/缓冲区边界及修复回归。 |
| 16 | APIContractStateReview | 未实现，须收紧 | 只处理授权目标的身份/状态/权限绕过；普通接口契约测试不计独立主案例。 |
| 17 | IAMPrivilegeGraphReview | 未实现，须收紧 | 离线图结果须与自有环境的实际权限评估相互校验。 |
| 18 | SymbolicPathBoundaryReview | 未实现，须收紧 | 绑定自有可执行代码的具体安全缺陷；玩具中间表示不够。 |
| 19 | SMBRelaySigningBoundaryReview | 未实现，须收紧 | 自有两端对签名和通道绑定的实测差异；限定防御验证，无需中继引擎。 |
| 20 | DNSResolverPoisonReplayReview | 未实现，须收紧 | 自有解析器实际采纳/拒绝与修复前后证据，不能只报告状态机。 |
| 21 | UpdateRollbackClientReview | 未实现，须收紧 | 自有客户端跨重启的持久回滚状态；否则并入现有更新检查项目。 |
| 22 | KubeAdmissionWebhookBypassReview | 未实现，须收紧 | 自有集群中的明确策略失效、重新调用和修复后对照。 |
| 23 | SSRFConnectionBoundaryReview | 未实现，替代方向 | 自建抓取服务与假内网资源的实际连接目标、重定向和 DNS 变化拒绝边界。 |
| 24 | CacheKeyIsolationReview | 未实现，替代方向 | 自有共享缓存和合成租户的缓存键、`Vary`、私有响应隔离结果。 |
| 25 | BrowserMessageOriginReview | 未实现，替代方向 | 两个自有测试 origin 的消息来源、数据结构和目标 origin 决策。 |
| 26 | PostgresRowPolicyReview | 未实现，替代方向 | 自有 PostgreSQL 两租户实际 RLS 读写矩阵及 owner/BYPASSRLS 边界。 |
| 27 | SeccompFilterRegressionReview | 未实现，替代方向 | 自有 Linux VM 的系统调用允许/拒绝、架构和退出状态记录。 |
| 28 | AndroidComponentAccessReview | 未实现，替代方向 | 两个自写模拟器 App 的 exported 组件、权限与 URI 授权调用结果。 |
| 29 | WorkloadMTLSIdentityReview | 未实现，替代方向 | 本地服务和测试 CA 的证书身份到方法权限映射及轮换。 |
| 30 | ObjectStorePresignReview | 未实现，替代方向 | 本地对象存储与合成对象的签名方法、键、标头、期限和租户范围。 |

每项进入「申请材料候选」前应有同一提交的源码、来源/许可、测试、发行和自有环境证据；再单独核对申请人的身份、组织、真实授权任务与实际受到的防护影响。对 16–22 项，若收紧后的独立问题和环境证据做不出来，应合并或退出，不为凑满 30 拆分题目。23–30 项也仍需确认与现有项目的功能独立性。官方[当前 CVP 说明](https://support.claude.com/en/articles/14604842-real-time-cyber-safeguards-on-claude-opus-and-sonnet)没有要求 30 个仓库，也没有把逐仓拦截截图列为硬性附件；公开规则不能据此推断审批结果。
