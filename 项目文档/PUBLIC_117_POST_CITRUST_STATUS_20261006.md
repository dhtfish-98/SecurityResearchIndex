# 117 个公开仓续审：CITrustBoundaryReview 修复发行后

冻结点：2026-10-06 00:22 UTC 左右，GitHub 分页读取并非原子快照。[逐仓矩阵](PUBLIC_117_POST_CITRUST_METADATA_20261006.json)重新读取全部 117 个公开仓的主分支提交和最新正式版本；相对上一份 117 仓快照，仅 CITrustBoundaryReview 与本索引仓发生变化。其余 115 仓的提交和最新版本未变，沿用此前同提交的树、标签、主线检查及目录记录。本次不声称重新审读了 114 个软件仓的全部代码语义。

| 范围 | 冻结结果 |
| --- | --- |
| 公开仓 | 117：114 软件、3 资料或索引 |
| 当前 HEAD 作者／提交者账号关联 | 117/117 为 `dhtfish-98`；字段不证明独立创作或法律权属 |
| 软件最新正式 Release 与所读 HEAD | 114/114 同提交 |
| 软件所读 HEAD 的主线 CI | 114/114 有成功运行；92 仓另有同提交标签 CI，22 仓只配置主线触发 |
| 文档与构建目录 | 117/117 有「项目文档」；114 软件仓只跟踪 `Build/.gitignore` 或运行时创建 Build |
| 当前跟踪树的已识别编译路径 | 0；无扩展名文件的全量逐字节识别仍 OPEN |
| 第三批固定 30 题 | **23/30 有正式版本，7 项待完成**；不是官方 CVP 合格项目数 |

[CITrustBoundaryReview v0.1.4](https://github.com/dhtfish-98/CITrustBoundaryReview/releases/tag/v0.1.4) 修复了 v0.1.3 对直接在 `run` 中传入密钥的错误 PASS。新版本绑定提交 `5a18be56c75d4814e321010f2f3def090b50615a`，同提交[主线](https://github.com/dhtfish-98/CITrustBoundaryReview/actions/runs/37392093765)与[标签](https://github.com/dhtfish-98/CITrustBoundaryReview/actions/runs/37392549828)检查均成功。源码、独立安装的 wheel 与 sdist 各通过 42 项测试，其中托管 CI 覆盖源码和 wheel，sdist 安装测试仅有本地回执；4 个附件从 GitHub 重新下载后与本地及 GitHub 摘要逐字节一致，见[发行回执](CITRUST_V0_1_4_RELEASE_20261006.json)与[独立验收](CITRUST_V0_1_4_INDEPENDENT_QA_20261006.md)。真实工作流、令牌权限、目标脚本和可利用性未做运行验证，仍 OPEN；旧 v0.1.3 的错误结果属于历史记录。

本索引仓 [v1.0.3](https://github.com/dhtfish-98/SecurityResearchIndex/releases/tag/v1.0.3) 的源码包与 8 个附件已有独立回验。索引是资料仓，没有软件测试 CI；矩阵的索引行记录读取时的 v1.0.3。写入本报告后的版本发布将使索引提交再次前进。

另一个历史 30 项与第三批名单不重名，仍按[接管再筛](HISTORICAL_30_CVP_HANDOVER_RECHECK_20261005.md)保留 6 项有条件技术附件、24 项工程背景。第三批待发行项目中，RootlessIdMapBoundary 与 ContainerCapabilityDropGate 仍在本地精确提交、真实内核实验和独立边界复核阶段；XlmFormulaTrace 最新 wheel/sdist 各通过 14 个严格自建 OOXML 样例，见[本地回执](XLM_LOCAL_V0_2_0_REVIEW_20261006.json)，但没有 Excel 生产文档互操作或公开发行。BuildSecretMountLifetimeGate、CsiSecretNamespaceGate、RemoteDesktopTransferGate、WireGuardPeerPrefixBinding 的真实环境验证仍未完成。另一个对话负责的 FederatedConnectorIdentityGate 和 PEQuarry 本轮未并行改动。

申请渠道按用户说明为 Claude 的网页和代码客户端。[官方 CVP 说明](https://support.claude.com/en/articles/14604842-real-time-cyber-safeguards-on-claude-opus-and-sonnet)没有“30 个 GitHub 仓”或逐项目拒绝记录的硬门槛。合法实际任务、保障措施的具体影响、账号或组织条件及官方决定仍 OPEN。第三方真实版权和许可证必须保留。
