# 124 个公开仓的精确提交续审

**冻结读取：2026-10-06 03:56:15–03:56:27 UTC，非原子。** [逐仓机器快照](PUBLIC_PORTFOLIO_POST_119_20261006.json)保存了每个公开仓在读取时的默认分支 HEAD、GitHub 作者和提交者账号关联、检查汇总、最新正式 Release 标签及标签解引用提交。原始 GitHub GraphQL 分页结果作为本索引 v1.0.6 的发行附件保存。这个读取发生在索引 v1.0.6 发布前，所以索引自身一行仍是 v1.0.5；发行后应以 v1.0.6 的独立收据核对。

| 冻结范围 | 观察结果 |
| --- | --- |
| 公开仓 | 124：121 个软件、3 个资料或索引 |
| 当前 HEAD 作者与提交者的 GitHub 账号关联 | 124/124 均为 `dhtfish-98`；不证明自然人身份、独立创作或历史对象归属 |
| 软件最新正式 Release 标签解引用到所读 HEAD | 121/121 |
| 软件所读 HEAD 的 GitHub 检查汇总 | 121/121 `SUCCESS`；资料仓不要求软件工作流 |
| 与 [03:18 UTC 的 123 仓机器基线](PUBLIC_123_BASELINE_20261006.json)相比 | 120 仓 HEAD 未变；SshHostCertTrustBoundary、UnixPeerCredentialBoundary、VpnPeerPrefixBindingGate 的 HEAD 更新，WebhookSignatureReplayGate 新增 |
| 改变或新增的文件 | 四仓各自精确 HEAD 的 Git 归档与 Git tree 共 83/83 个文件的 blob SHA-1 相符；无树截断、子模块、缺漏或额外文件 |
| 改变或新增的发行附件 | 四仓共 14 个 Release 资产重新下载，长度与 SHA-256 均等于 GitHub API 公布值 |

[变更源码扫描](PUBLIC_PORTFOLIO_CHANGED_SCANS_20261006.json)只覆盖这四仓当前 83 个跟踪文件；其中 `Build/` 唯一跟踪路径是 SshHostCertTrustBoundary 的 `.gitignore` 占位，未见已识别的编译产物路径或 AI 产品作为作者的文字模式。[资产校验](PUBLIC_PORTFOLIO_CHANGED_ASSETS_20261006.json)记录逐附件名称、大小、SHA-256 和下载地址。其余 120 仓的内容检查依据 [03:18 UTC 的 123 仓冻结](PUBLIC_123_BASELINE_20261006.json)及其[新增仓扫描](PUBLIC_123_CHANGED_SCANS_20261006.json)，旧 119 仓复用前一轮精确 HEAD 基线；因 HEAD 没变，本轮没有重新下载 120 份归档。全组合跟踪路径为 4,562 条，逐仓路径数与复用依据见机器表。上一次 123 仓审计另复下载了当时两个新发行仓的[12 个附件](PUBLIC_123_RELEASE_ASSETS_20261006.json)；本轮新复下载 14 个分别属于 SSH 主机证书、Unix、VPN、Webhook。

四仓的新版本分别为 [SshHostCertTrustBoundary v0.1.1](https://github.com/dhtfish-98/SshHostCertTrustBoundary/releases/tag/v0.1.1)、[UnixPeerCredentialBoundary v0.1.1](https://github.com/dhtfish-98/UnixPeerCredentialBoundary/releases/tag/v0.1.1)、[VpnPeerPrefixBindingGate v0.1.0](https://github.com/dhtfish-98/VpnPeerPrefixBindingGate/releases/tag/v0.1.0)、[WebhookSignatureReplayGate v0.1.0](https://github.com/dhtfish-98/WebhookSignatureReplayGate/releases/tag/v0.1.0)。四项主线及标签同提交成功检查、旧题目替换关系及每项目精确 HEAD 见[修订 30 项矩阵](THIRD_BATCH_30_REVISED_20261006.json)。SSH 主机证书 v0.1.0 和 Unix v0.1.0 的旧出版状态文案已在各自 v0.1.1 修订；VPN 旧失败 CI 属早期提交，不应当作本次发行 HEAD 的检查结论。[第三批公开文档状态终审](THIRD_BATCH_30_DOC_STATUS_20261006.json)尚有 FederatedConnectorIdentityGate 当前公开文档的三处“未发布/CI 未完成”矛盾，由另一聊天维护，勘误 **OPEN**。所有旧记录仍按自身时点留存。

本轮没有对全部 121 个软件仓重新执行测试、逐函数语义审计、历史归属调查或第三方权利法律核验。新写部分可以如实署名 `dhtfish98`，真实引用或依赖的第三方版权、许可证与来源仍保留。仓库数、统一作者字段、绿色 CI 和公开 Release 都不能证明申请人的真实授权高风险双用途任务、保障措施影响、身份/组织条件或 Anthropic CVP 官方资格和批准；这些仍是 **OPEN**。
