# 30 题目池适配性再筛（2026-10-05）

本页复核[前版题目池](PROJECT_30_RESEARCH_POOL_R2_20261004.md)的选题边界。原表有 6 个已实现的**条件技术案例**和 24 个未建仓、未实现、未测试、未发布的规格；它从未代表 30 个已完成或已获 CVP 资格的项目。对现有 24 个规格，本轮按最小交付是否能独立说明高风险双用途的合法防御任务、与已有仓库是否重叠、是否有可复核的自有环境证据再筛。以下只是项目选题判断，不能代替申请人的真实授权任务、受保障措施影响的事实、身份核验或官方审批。

## 优先保留的 9 项规格

WebSessionDastReview、ParserCrashBoundaryReview、HttpDesyncBoundaryReview、JwtVerifierConfusionReview、OAuthCodePkceReplayReview、SamlSignatureWrappingReview、ADCSIssuanceAbuseReview、WASIPreopenBoundaryReview、WindowsIoctlDispatchReview。它们只有在自有或明确授权的服务、域、虚拟机或测试驱动中，能留下具体漏洞边界与修复前后结果时，才可能成为有力的防御案例。特别是 AD CS、WASI 与 Windows 驱动题目需要对应环境；只写模拟状态机不能视为完成。

## 须收紧后重评的 7 项规格

| 题目 | 本轮缺口与要求 |
| --- | --- |
| APIContractStateReview | 普通接口契约不足；应限于授权目标的身份、状态或权限绕过及修复回归。 |
| IAMPrivilegeGraphReview | 离线权限图只是近似；需与实际获授权的权限评估结果对照。 |
| SymbolicPathBoundaryReview | 玩具中间表示不足；需绑定自有真实可执行代码中的具体安全缺陷。 |
| SMBRelaySigningBoundaryReview | 离线前提模型不足；需自有两端对签名及通道绑定的实测差异，且无需实现中继引擎。 |
| DNSResolverPoisonReplayReview | 状态机不足；需自有解析器实际采纳/拒绝及修复前后证据。 |
| UpdateRollbackClientReview | 只解析元数据则与现有更新框架检查重叠；需自有客户端跨重启的持久状态验证，否则并入既有项目。 |
| KubeAdmissionWebhookBypassReview | 常规 webhook 功能测试不足；需自有集群中明确策略失效与修复后重调用的对照。 |

## 降为辅助证据或并入的 8 项最小规格

| 题目 | 当前处理 |
| --- | --- |
| NetworkIDSReplayReview | 常规离线 IDS 告警匹配，作为真实调查或漏洞案例的辅助检测证据。 |
| ContainerRuntimeRuleReview | 常规容器事件规则判定，作为有具体缺陷的工作负载调查模块。 |
| RuntimeFlowTraceReview | 分支事件采集是其他漏洞修复的路径证据，优先并入相应案例。 |
| PackageBehaviorSandboxReview | 仅运行自写合成包尚不证明供应链调查，保留为安全测试环境。 |
| KubeProcessLineageReview | 与容器事件规则的采集层重叠，优先并入同一调查项目。 |
| MobileRuntimeEvidenceReview | 只记录自写应用函数调用次数，与高风险双用途任务联系不足。 |
| LinuxMemoryCaptureReview | 采集完整性属于取证基础设施；权限和隐私成本较高，不能单独充作 CVP 主案例。 |
| TLSHandshakeDowngradeReview | 普通握手矩阵与已有握手证据项目重叠，优先并入。 |

## 可替代的 8 个研究方向（仍未实施）

这些只是为真实任务准备的独立选题选项，不把原 8 项弱规格自动变成合格项目。题名已与当时 94 个公开仓名对照，无同名；功能独立性还须在实施前复核。

| 暂定题名 | 限定的自有实验与独立验收 | 研究依据 |
| --- | --- | --- |
| SSRFConnectionBoundaryReview | 自建 URL 抓取服务与假内网资源，核对实际连接目的地址、重定向及 DNS 变化的拒绝边界；不扫描公网。 | [OWASP SSRF 防护](https://cheatsheetseries.owasp.org/cheatsheets/Server_Side_Request_Forgery_Prevention_Cheat_Sheet.html) |
| CacheKeyIsolationReview | 自有 origin/共享缓存和两个合成租户，对账缓存键、`Vary`、私有响应与跨租户错误命中。 | [RFC 9111](https://www.rfc-editor.org/rfc/rfc9111.html) |
| BrowserMessageOriginReview | 两个本地测试 origin 与自写页面，实测消息的 origin、source、数据结构和目标 origin 决策。 | [HTML Web Messaging](https://html.spec.whatwg.org/multipage/web-messaging.html) |
| PostgresRowPolicyReview | 一次性 PostgreSQL 与两名合成租户，比较预期行级读写矩阵和实际 RLS，记明 owner/BYPASSRLS 边界。 | [PostgreSQL RLS](https://www.postgresql.org/docs/current/ddl-rowsecurity.html) |
| SeccompFilterRegressionReview | 自有 Linux VM 与有限 helper，记录允许/拒绝系统调用、架构及退出状态；不把通知接口当安全策略。 | [Linux seccomp 文档](https://www.kernel.org/doc/html/latest/userspace-api/seccomp_filter.html) |
| AndroidComponentAccessReview | 两个自写模拟器 App，核对 exported 组件权限、URI 授权与实际跨应用调用结果。 | [Android exported 组件访问控制](https://developer.android.com/privacy-and-security/risks/access-control-to-exported-components) |
| WorkloadMTLSIdentityReview | 本地两服务和测试 CA，以成熟 TLS 库实测证书身份到允许方法的映射及轮换；不宣称完整标准合规。 | [SPIFFE X.509-SVID](https://spiffe.io/docs/latest/spiffe-specs/x509-svid/) |
| ObjectStorePresignReview | 本地对象存储与合成对象，对账预签名所绑定的方法、键、标头、有效期及租户范围；不连接真实云。 | [S3 SigV4 查询认证](https://docs.aws.amazon.com/AmazonS3/latest/developerguide/sigv4-query-string-auth.html) |

因此原有 24 项里只有 9 项保留为优先研究规格，7 项需重定范围，8 项退出独立主案例队列。新列 8 项只是替代研究方向。连同已实现的 6 个条件案例，**30 个题目槽位**可供真实任务筛选，但现阶段仍只有 6 个已实现的条件案例，不能写成 30 个已重写、已发布或已符合 CVP 要求的项目。未来须先核对真实授权任务、与现有代码的独立性、来源及第三方权利，再分别完成实现、测试、发布和精确版本证据；不要为达到数量而拆分同一任务。

[Anthropic 当前说明](https://support.claude.com/en/articles/14604842-real-time-cyber-safeguards-on-claude-opus-and-sonnet)没有规定 30 个仓库或逐仓拦截截图为硬要求。它说明 CVP 面向有正当防御目的且工作受到相关保障措施影响的高风险双用途场景；Claude.ai / Claude Code 经 Verification Portal 申请，需身份核验且选项只对授权管理员可见。公开规则并不能证明任何上述项目已获资格或批准。
