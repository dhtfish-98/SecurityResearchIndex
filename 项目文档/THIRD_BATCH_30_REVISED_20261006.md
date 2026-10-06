# 第三批修订 30 个防御工程项目

**2026-10-06 03:56:15–03:56:27 UTC 非原子公开快照：30/30 个修订后的独立槽位有正式工程 Release。** [机器矩阵](THIRD_BATCH_30_REVISED_20261006.json)逐项记录仓库、精确 HEAD、标签解引用提交、主线与标签成功检查，以及 CVP 证据边界。04:10 UTC 的独立发行复核确认 30 个 Release 和 60 个主线/标签运行均对应各仓同一个精确提交且成功；这只是所执行测试的工程结果。[文档与中央镜像状态](THIRD_BATCH_30_DOC_STATUS_20261006.json)分开记录 03:57 UTC 的公开措辞检查（29/30 无矛盾），以及 **04:10:53 UTC 独立重核**的 168/168 份项目文档和 264/264 个限定范围源码/脚本/配置/测试路径镜像。03:57 的中央文档全一致结论尚不成立；04:07 修正 NATS 文档后文档镜像才精确，而当时中央源码仍有 8 仓 17 路差异。这些旧观察保留为历史，不倒填。源码镜像核对排除 GitHub 工作流、`Build`、`.gitignore` 占位和根目录权利/入口文件，不能称为全部路径或运行语义通过。FederatedConnectorIdentityGate 当前公开旧发布措辞仍 OPEN。

原固定题目中四项经过适配审计后由独立项目占用原槽位，不双计：

| 原题目（不计入当前 30） | 当前项目 | 调整原因 |
| --- | --- | --- |
| CsiSecretNamespaceGate | [HTTPMessageFramingGate](https://github.com/dhtfish-98/HTTPMessageFramingGate/releases/tag/v0.1.0) | 固定 CSI 上游已按 Pod 命名空间查询 SecretProviderClass，缺原主张的可重现实例；改为 HTTP/1.1 报文分界实验。 |
| RemoteDesktopTransferGate | [UnixPeerCredentialBoundary](https://github.com/dhtfish-98/UnixPeerCredentialBoundary/releases/tag/v0.1.1) | 缺真实 RDP/Guacamole 行为证据；改为 Linux `SO_PEERCRED` 本机授权边界。 |
| WireGuardPeerPrefixBinding | [VpnPeerPrefixBindingGate](https://github.com/dhtfish-98/VpnPeerPrefixBindingGate/releases/tag/v0.1.0) | WireGuard 自身有 peer/source 与 replay 保护；新项目明确是独立 HMAC/UDP/TUN 合成隧道，不声称修复 WireGuard 漏洞。 |
| XlmFormulaTrace | [WebhookSignatureReplayGate](https://github.com/dhtfish-98/WebhookSignatureReplayGate/releases/tag/v0.1.0) | 缺 Excel 打开与执行证据；改为本机 HTTP/SQLite 签名与持久防重放实验。 |

按已见工程证据暂分层：**13 项有条件技术附件，17 项防御工程背景**。前一组实际运行了固定上游服务/工具或内核边界，包括 Jupyter、NATS、QUIC、OpenSSH、BuildKit、runc、Dex、Headscale、Landlock、PostgreSQL/PgCat、Linux `SO_PEERCRED` 和 user namespace；仍只证明各自有界环境的结果。后一组使用自有回环服务、合成身份与数据、局部解析器或自编译离线样本，不能因“安全”题目直接升为 CVP 主案例。机器矩阵逐项列出证据等级、技术范围和限制；如果申请人的真实授权任务与某项直接对应，材料角色可以重新评估，但不能仅凭仓库、版本或测试推定官方资格。

这份 30 项矩阵与此前接管的**历史 30 个软件仓**名称交集为零。[历史组的 111 仓时点审计](HISTORICAL_30_CVP_HANDOVER_RECHECK_20261005.md)把六项列为有条件技术附件、24 项列为工程背景；它的版本和 CI 行不代表本次 124 仓现况。新组 13 项与历史六项也无重名，**仅这两组 60 个项目**合计 19 项有条件技术附件、41 项工程背景；这不是当前 121 个公开软件仓的逐项材料角色再审，未核对项目仍 OPEN，且两组都无已核实 CVP 资格。另一个 [CVP_30_CANDIDATE_TRACKER_20261005.md](CVP_30_CANDIDATE_TRACKER_20261005.md) 是包含六个重叠旧案例及 24 个研究规格的旧题目队列，不能加成第三组 30 个已实现项目。旧 `HttpDesyncBoundaryReview` 研究题目由现有 HTTP 分界实验覆盖，不另计软件发行。CITrustBoundaryReview v0.1.3 的直接插值误判是历史缺陷，[v0.1.4](https://github.com/dhtfish-98/CITrustBoundaryReview/releases/tag/v0.1.4) 已作定向修复；真实目标安全仍须另证。

部分项目只在自建或合成样例上验证，不能推断固定上游存在漏洞、生产部署安全、真实使用者身份或申请资格。FederatedConnectorIdentityGate 的公开 v0.1.0 HEAD 的 `项目文档/README.md`、`VALIDATION.md`、`DESIGN.md` 仍声称远端出版或公开 CI 未完成，与实际正式 Release 冲突；该仓由另一对话维护，**公开文档勘误 OPEN**，本索引不替它改仓或把过时句子写成现况。新写代码与包作者按真实归属使用 `dhtfish98`；真实第三方代码、依赖、规范和参考材料的权利与许可证仍归原权利人。GitHub 发行数不是 Anthropic CVP 的最低数量要求；没有每项目原始拦截/降级截图的公开硬门槛。Claude.ai / Claude Code 申请仍要按[官方 CVP 说明](https://support.claude.com/en/articles/14604842-real-time-cyber-safeguards-on-claude-opus-and-sonnet)及实际账号核实授权管理员、身份验证、合法高风险双用途工作和保障措施影响。**已核实官方资格：0；已核实官方批准：0；其余均 OPEN。**
