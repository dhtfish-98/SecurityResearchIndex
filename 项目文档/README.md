> 文档集中在「项目文档」，构建与暂存输出集中在「Build」；保留现有源码路径。历史版本与验证按各自提交理解。

# 防御安全项目与 CVP 证据索引

更新日期：2026-10-04。工程元数据冻结截止：2026-10-03T23:49:16.384155+00:00。

当前公开范围为 **91 个软件项目和 3 个资料仓库**。本轮逐项核对公开用途、来源和保存的工程证据，修正旧索引的范围和时点；没有重新执行项目或完成全量安全代码审计。所有 CVP 申请资格与批准状态仍为 **OPEN**。

| 材料角色 | 数量 | 使用方式 |
| --- | --- | --- |
| 防御工作附件候选 | 75 | 可证明有限工作产物；实际任务、授权和防护影响待核实 |
| 研究背景，需具体任务限定 | 12 | 说明真实任务使用了哪些功能及允许范围 |
| 普通背景工具 | 4 | CDTranslator、ChromeRelay、SILGallery、TabWeave 不作为主 CVP 资格证据 |
| 资料仓库 | 3 | .github、dhtfish-98、SecurityResearchIndex 不计独立软件项目 |

这些分类是材料整理判断，不是官方项目白名单。普通防御工具不是政策违规；合法双用途也不能仅凭名称或功能判断是否符合申请。渠道按申请人说明为 Claude.ai / Claude Code；原始拦截或降级记录是可选佐证，本审核不将其设为硬性门槛。仓库数量、改名、作者字段和 CI 不能代表官方批准。见 [官方说明](https://support.claude.com/en/articles/14604842-real-time-cyber-safeguards-on-claude-opus-and-sonnet)及 [当前规则与证据](CVP_RULES_AND_EVIDENCE_20261004.md)。

全部软件及资料仓的逐项用途、提交、CI 和限制见 [2026-10-04 复核矩阵](CVP_REVIEW_20261004.md)与 [机器记录](CVP_REVIEW_20261004.json)。真实申请材料待补项见 [证据整理表](APPLICATION_EVIDENCE_OPEN.md)，不把空白信息写成已完成事实。

截至上述时点，软件仓对应 HEAD 的 CI 为 **90 项 PASS，ImageQuay 1 项 FAIL**；3 个资料仓没有适用的已跟踪工作流。CI 只验证所执行范围。ArchiveLens 6 项、BranchLoom 1 项、TabWeave 1 项已保存未修观察继续标注，12 个核心、GUI 或平台完整审核仍 OPEN。目录和署名维护没有修复这些行为。

HeaderPolicyReview 0.1.1、ImageQuay 1.0.5、BranchLoom 0.2.1、TabWeave 4.3.1、SealScope 0.2.1 仍为旧记录中的未发布准备版本；本轮不把它们计作公开修复或新 Release。BranchLoom、SealScope、TabWeave 仅更新当期包维护名为 dhtfish98，保留既有版本、历史来源、真正原作者和第三方许可。

2026-10-02 的 14 项替补、10 项保留项目、旧测试及固定发布结果是历史子集，不能代表今天的全部软件或最新提交。原文保留在 [历史索引](历史/20261002/README-目录更新时保留.md)，其他原记录见 [源码复核](SOURCE_REVIEW_20261002.md)、[保留项目复核](RETAINED_PROJECT_REVIEW_20261002.md)、[旧规则记录](CVP_RULES_AND_EVIDENCE_20261002.md)和 [历史分组原文件](历史/20261002/GROUPS-20261002.json)。历史撤出项目仍按原处置保留私有；这不是官方对仓库的永久禁止判断。
