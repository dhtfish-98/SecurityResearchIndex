# 117 个公开仓续审：Headscale 正式发行后

**冻结点：2026-10-05 23:44:35 UTC，非原子读取。**[逐仓矩阵](PUBLIC_117_POST_HEADSCALE_METADATA_20261006.json)重新读取账号下全部公开仓的 HEAD 和最新 Release。与 116 仓矩阵相比，新增 HeadscaleEnrollmentGate，索引仓自身由 v1.0.1 前进到 v1.0.2；其余 115 仓的 HEAD 与最新版本未变。未变仓沿用原提交的树、标签与 CI 细节；这不是 114 个软件仓的全量代码语义复审。

| 范围 | 冻结结果 |
| --- | --- |
| 公开仓 | 117：114 软件、3 资料或索引 |
| 当前 HEAD 作者／提交者账号关联 | 117/117 为 `dhtfish-98`；当前字段不能替代历史权利鉴定 |
| 软件最新正式 Release 与所读 HEAD | 114/114 同提交 |
| 软件所读 HEAD 的主线 CI | 114/114 有成功运行；92 仓另有同提交标签 CI，22 仓只配置主线触发 |
| 文档与构建目录 | 117/117 有「项目文档」；114 仓的 `Build` 仅跟踪 `.gitignore`，HeadscaleEnrollmentGate、LandlockFilesystemGate 与 PgPoolPrincipalIsolation 在运行时创建 Build |
| 当前跟踪树的已识别编译路径 | 0；无扩展名文件的全量逐字节识别仍 OPEN |
| 第三批固定 30 题 | **23/30 正式发行，7 项待完成**；不等于官方 CVP 合格项目数 |

[HeadscaleEnrollmentGate v0.1.0](https://github.com/dhtfish-98/HeadscaleEnrollmentGate/releases/tag/v0.1.0) 绑定提交 `529bac2f1e9b6c577ee3af78f89083131569d06c`。[主线](https://github.com/dhtfish-98/HeadscaleEnrollmentGate/actions/runs/37389115147)和[标签](https://github.com/dhtfish-98/HeadscaleEnrollmentGate/actions/runs/37389721656)均通过 Python 3.11–3.14 的源码、wheel、sdist 检查，以及固定版本 Headscale 的 16 项合成注册实验。五个正式附件回下载与 GitHub 摘要一致；源码包 18 个文件与提交及中央源码／文档逐字节一致，见[发行回执](HEADSCALE_V0_1_0_RELEASE_20261006.json)。最初主线实验因 Go 临时目录未创建而失败，修复后的同提交主线和标签运行才用于发行。这个项目是自有运营侧授权控制，未证明 Headscale 漏洞、设备身份绑定或真实生产部署；Headscale 与 Tailscale 的版权和 BSD-3-Clause 许可保留。

本索引仓 [v1.0.2](https://github.com/dhtfish-98/SecurityResearchIndex/releases/tag/v1.0.2) 的注释标签、五个附件及源码包已独立回验，见[发行回执](SECURITY_RESEARCH_INDEX_V1_0_2_RELEASE_20261006.json)。它是资料仓，没有程序 CI。本矩阵中的索引行记录读取时的 v1.0.2；写入本报告后的版本发布会使索引 HEAD 再次前进。

另一个历史 30 项交付与第三批 30 题互不重名，仍按[历史接管再筛](HISTORICAL_30_CVP_HANDOVER_RECHECK_20261005.md)将 6 项列作有条件技术附件、24 项列作工程背景。[六项独立深审](HISTORICAL_30_SIX_DEEP_AUDIT_20261006.md)已复现 CITrustBoundaryReview v0.1.3 的一处错误 PASS，其旧版不能作为规则正确性证明；其余五项只通过选定边界样例，全部申请用途仍 OPEN。第三批未发行项中，RootlessIdMapBoundary 的本地候选作者提交字段与真实内核 CI 有待修正；XlmFormulaTrace 的 OOXML 宏表实验仅限严格自建输入，未公开发行。另一个活跃对话负责的 FederatedConnectorIdentityGate 与 PEQuarry 未在本轮并行改动。

申请渠道按用户说明为 Claude.ai / Claude Code。[官方 CVP 说明](https://support.claude.com/en/articles/14604842-real-time-cyber-safeguards-on-claude-opus-and-sonnet)没有“30 个 GitHub 仓”或逐项目拒绝记录的硬门槛。真实合法任务、保障措施影响、申请账号与组织条件和官方批准仍 **OPEN**；仓库数量、作者字段、CI 与 Release 只证明各自限定的工程事实。真实第三方版权与许可证不能因重写而删除。
