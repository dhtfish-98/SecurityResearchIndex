> 文档集中在「项目文档」，构建与暂存输出集中在「Build」；保留现有源码路径。历史版本与验证按各自提交理解。

# 防御安全项目与 CVP 证据索引

更新日期：2026-10-04 07:41 UTC。最新逐仓 GitHub 状态冻结于 07:40–07:41 UTC；较早的 04:51 UTC 快照及 2026-10-03 23:49 UTC 工程矩阵均保留原时点。

当前范围为 **94 个公开仓（91 软件、3 资料）和 29 个私有仓**。最新[公开项目再审计](PUBLIC_PORTFOLIO_RECHECK_20261004.md)及其[94 仓逐仓冻结记录](PUBLIC_PORTFOLIO_RECHECK_20261004.json)核对目录、当前提交、CI、署名与发布边界；较早的[公开项目与 CVP 材料状态](CURRENT_PORTFOLIO_STATUS_20261004.md)和[旧快照](PUBLIC_PORTFOLIO_STATUS_20261004.json)保留原证据时间。没有重新执行全部项目或完成全量安全代码审计。所有 CVP 申请资格与批准状态仍为 **OPEN**。

| 材料角色 | 数量 | 使用方式 |
| --- | --- | --- |
| 条件技术案例 | 6 | 代码级再筛后保留的条件候选；仍需真实受影响任务 |
| 技术研究暂缓 | 8 | 已记录问题、审计或发布边界仍开放 |
| 防御工程背景 | 71 | 包含从原条件案例降级的 10 个离线检查工具 |
| 派生通用二进制工具 | 2 | ImageQuay、KernelCabinet；保留真实上游权利，移出独立重写主案例 |
| 通用浏览器自动化背景 | 2 | ChromeRelay、TabWeave 不作为主 CVP 资格证据 |
| 非网络安全背景 | 2 | CDTranslator、SILGallery 不作为主 CVP 资格证据 |
| 资料仓库 | 3 | .github、dhtfish-98、SecurityResearchIndex 不计独立软件项目 |

这些分类是材料整理判断，不是官方项目白名单。普通防御工具不是政策违规；合法双用途也不能仅凭名称或功能判断是否符合申请。渠道按申请人说明为 Claude.ai / Claude Code；原始拦截或降级记录是可选佐证，本审核不将其设为硬性门槛。仓库数量、改名、作者字段和 CI 不能代表官方批准。见 [官方说明](https://support.claude.com/en/articles/14604842-real-time-cyber-safeguards-on-claude-opus-and-sonnet)及 [当前规则与证据](CVP_RULES_AND_EVIDENCE_20261004.md)。

[现行30题目研究池 R2](PROJECT_30_RESEARCH_POOL_R2_20261004.md)列出 6 个已有条件候选和 24 个未实现规格；[代码级再筛](CVP_CODE_SCOPE_RECHECK_20261004.md)把原 18 初筛案例中的 10 个降为工程背景、2 个派生工具移出主案例。30 只是选题数量，不是 30 个已重写或已符合 CVP 要求的项目；实施须以真实授权任务为准。

当前逐仓提交、CI、角色与限定用途见[新快照](PUBLIC_PORTFOLIO_STATUS_20261004.json)。较早的 [2026-10-03 工程矩阵](CVP_REVIEW_20261004.md)及其[机器记录](CVP_REVIEW_20261004.json)保留原冻结证据，不应当作最新 HEAD。真实申请材料待补项见 [证据整理表](APPLICATION_EVIDENCE_OPEN.md)，不把空白信息写成已完成事实。

截至 07:40–07:41 UTC 最新冻结，91 个软件仓各自精确 HEAD 的 Actions **91 项成功、0 项失败或运行中**；3 个资料仓没有相应运行。94 个当前提交的显示名与所有者账号关联均核实，当前跟踪树中未见新编译输出；ImageQuay 保留一份测试固定夹具。CI 只验证所执行范围；ArchiveLens 6 项、BranchLoom 1 项、TabWeave 1 项已保存未修观察继续标注，12 个深层项目的完整审核仍 OPEN。

HeaderPolicyReview 已发布 `v0.1.3`，ImageQuay 已发布 `v1.0.5`，SealScope 已发布 `v0.2.1`，KernelCabinet 已发布 `v1.0.2`；ArchiveLens 已发布源码版 `v1.0.3`，SILGallery 已发布源码版 `v1.0.2`。LocalSecretReview 与 PEHardeningReview 的作者字段修订各发布 `v1.0.3`。PEQuarry 的当前源码 1.0.3 仍只有正式 Release v1.0.2；BranchLoom `0.2.1` 和 TabWeave `4.3.1` 的旧准备包也不是已发布的新修复。14 个小仓的自有版权显示名与两处安装包作者字段更新为 `dhtfish98`；真实第三方作者、许可证和来源仍保留。SILGallery 的旧版本标签关联到另一同名 GitHub 账号，发行说明已作勘误，当前 HEAD 归属所有者。文档或署名提交之后，软件 Release 标签不必等于最新文档 HEAD，应按对应程序提交核验。

2026-10-02 的 14 项替补、10 项保留项目、旧测试及固定发布结果是历史子集，不能代表今天的全部软件或最新提交。原文保留在 [历史索引](历史/20261002/README-目录更新时保留.md)，其他原记录见 [源码复核](SOURCE_REVIEW_20261002.md)、[保留项目复核](RETAINED_PROJECT_REVIEW_20261002.md)、[旧规则记录](CVP_RULES_AND_EVIDENCE_20261002.md)和 [历史分组原文件](历史/20261002/GROUPS-20261002.json)。历史撤出项目仍按原处置保留私有；这不是官方对仓库的永久禁止判断。
