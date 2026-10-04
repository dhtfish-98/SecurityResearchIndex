> 文档集中在「项目文档」，构建与暂存输出集中在「Build」；保留现有源码路径。历史版本与验证按各自提交理解。

# 防御安全项目与 CVP 证据索引

本页主体及申请门槛文字勘误记录于 2026-10-04 08:23 UTC。逐仓 GitHub 状态冻结于 07:40–07:41 UTC；较早的 04:51 UTC 快照及 2026-10-03 23:49 UTC 工程矩阵均保留原时点。后续发行及 10:53 UTC 逐仓快照作为增量列明，不改写旧冻结记录。

当前范围为 **94 个公开仓（91 软件、3 资料）和 29 个私有仓**。[公开项目再审计](PUBLIC_PORTFOLIO_RECHECK_20261004.md)及其[94 仓逐仓冻结记录](PUBLIC_PORTFOLIO_RECHECK_20261004.json)核对当时目录、提交、CI、署名与发布边界；[10:53 UTC 后续快照](PUBLIC_PORTFOLIO_POSTUPDATE_20261004.json)另记后续提交状态。较早的[公开项目与 CVP 材料状态](CURRENT_PORTFOLIO_STATUS_20261004.md)和[旧快照](PUBLIC_PORTFOLIO_STATUS_20261004.json)保留原证据时间。没有重新执行全部项目或完成全量安全代码审计。所有 CVP 申请资格与批准状态仍为 **OPEN**。

| 材料角色 | 数量 | 使用方式 |
| --- | --- | --- |
| 条件技术案例 | 6 | 代码级再筛后保留的条件候选；仍需真实受影响任务 |
| 技术研究暂缓 | 8 | 已记录问题、审计或发布边界仍开放 |
| 防御工程背景 | 71 | 包含从原条件案例降级的 10 个离线检查工具 |
| 派生通用二进制工具 | 2 | ImageQuay、KernelCabinet；保留真实上游权利，移出独立重写主案例 |
| 通用浏览器自动化背景 | 2 | ChromeRelay、TabWeave 不作为主 CVP 资格证据 |
| 非网络安全背景 | 2 | CDTranslator、SILGallery 不作为主 CVP 资格证据 |
| 资料仓库 | 3 | .github、dhtfish-98、SecurityResearchIndex 不计独立软件项目 |

这些分类是材料整理判断，不是官方项目白名单。普通防御工具不是政策违规；合法双用途也不能仅凭名称或功能判断是否符合申请。渠道按申请人说明为 Claude.ai / Claude Code；原始拦截或降级记录是可选佐证，本审核不将其设为硬性门槛。当前官方说明明确不适用于 Opus 5.5 和 Sonnet 5.5，ZDR 组织也暂不符合资格；第一方门户申请仅授权管理员可见，提交需身份验证。未来扩展不能当作已生效。仓库数量、改名、作者字段和 CI 不能代表官方批准。见 [官方说明](https://support.claude.com/en/articles/14604842-real-time-cyber-safeguards-on-claude-opus-and-sonnet)及 [当前规则与证据](CVP_RULES_AND_EVIDENCE_20261004.md)。

[现行30题目研究池 R2](PROJECT_30_RESEARCH_POOL_R2_20261004.md)列出 6 个已有条件候选和 24 个未实现规格；[代码级再筛](CVP_CODE_SCOPE_RECHECK_20261004.md)把原 18 初筛案例中的 10 个降为工程背景、2 个派生工具移出主案例。30 只是选题数量，不是 30 个已重写或已符合 CVP 要求的项目；实施须以真实授权任务为准。

10:53 UTC 的逐仓提交与 CI 见[后续机器快照](PUBLIC_PORTFOLIO_POSTUPDATE_20261004.json)，材料角色与限定用途见[再审计](PUBLIC_PORTFOLIO_RECHECK_20261004.md)。04:51 UTC 的[旧快照](PUBLIC_PORTFOLIO_STATUS_20261004.json)及 [2026-10-03 工程矩阵](CVP_REVIEW_20261004.md)和[机器记录](CVP_REVIEW_20261004.json)保留原冻结证据，不应当作最新 HEAD。真实申请材料待补项见 [证据整理表](APPLICATION_EVIDENCE_OPEN.md)，不把空白信息写成已完成事实。

在 07:40–07:41 UTC 主体冻结时，91 个软件仓各自精确 HEAD 的 Actions **91 项成功、0 项失败或运行中**；3 个资料仓没有相应运行。10:53 UTC 后续快照另得 94/94 公开仓可读、91 个软件仓各自当时精确 HEAD 的 CI 成功、3 个资料仓无工作流。两个窗口都不是现在的实时状态。94 个当时提交的显示名与所有者账号关联均核实，跟踪树中未见新编译输出；ImageQuay 保留一份测试固定夹具。CI 只验证所执行范围；ArchiveLens 6 项、BranchLoom 1 项、TabWeave 1 项已保存未修观察继续标注，12 个深层项目的完整审核仍 OPEN。

**07:40–07:41 UTC 主体冻结时：** HeaderPolicyReview 已发布 `v0.1.3`，ImageQuay 已发布 `v1.0.5`，SealScope 已发布 `v0.2.1`，KernelCabinet 已发布 `v1.0.2`；ArchiveLens 已发布源码版 `v1.0.3`，SILGallery 已发布源码版 `v1.0.2`。LocalSecretReview 与 PEHardeningReview 的作者字段修订各发布 `v1.0.3`。PEQuarry 当时只有正式 Release v1.0.2；BranchLoom `0.2.1` 和 TabWeave `4.3.1` 的旧准备包也不是已发布的新修复。14 个小仓的自有版权显示名与两处安装包作者字段更新为 `dhtfish98`；真实第三方作者、许可证和来源仍保留。SILGallery 的旧版本标签关联到另一同名 GitHub 账号，发行说明已作勘误，冻结时 HEAD 归属所有者。文档或署名提交之后，软件 Release 标签不必等于最新文档 HEAD，应按对应程序提交核验。这是历史窗口，不代表现在各仓最新版本。

**09:28 UTC SILGallery 发版增量：** [v1.0.4 正式源码 Release](https://github.com/dhtfish-98/SILGallery/releases/tag/v1.0.4)的标签解引用到 `befc52fb320ab5e3d8bc6d295e86be0a09e13cff`，核对时 `main` 也指向该提交；该提交的 [GitHub CI](https://github.com/dhtfish-98/SILGallery/actions/runs/37192047491) 完成且成功。回下载的[源码包](https://github.com/dhtfish-98/SILGallery/releases/download/v1.0.4/SILGallery-v1.0.4-source.tar.gz)为 35,081 字节，SHA-256 `0e343b5ea5b64d6ec8cac75cb4174bc4371207c19b5d6daa68e4c734a5ccbb27`，与 Release 资产摘要一致。该版修复无效 UTF-8 替换解码后可能超过 32 MiB 可见输出预算的问题；测试和其余边界见[再审计记录](PUBLIC_PORTFOLIO_RECHECK_20261004.md)。人工 GUI、安装及签名仍 OPEN，项目继续归为非网络安全背景。

**10:28 UTC PEQuarry 发版增量：** 源码 1.0.3 从公开提交 `ba8cda8ed53a0d5c0eda4d7a6e9578e6d0f3d8be` [正式发布 v1.0.3](https://github.com/dhtfish-98/PEQuarry/releases/tag/v1.0.3)；资产与验证范围见[再审计发行增量](PUBLIC_PORTFOLIO_RECHECK_20261004.md)。

**12:45 UTC PEQuarry 发版增量：**[v1.0.4 正式 Release](https://github.com/dhtfish-98/PEQuarry/releases/tag/v1.0.4)的 `main` 与标签均指向提交 `84d6342f68894657b7d89395aea9faecd4f989ac`；[主线 CI](https://github.com/dhtfish-98/PEQuarry/actions/runs/37202437270)和[标签 CI](https://github.com/dhtfish-98/PEQuarry/actions/runs/37202793004)均在该精确提交成功。wheel 与源码包回下载摘要、字节数及包内版本见[独立发行增量记录](PEQUARRY_V1_0_4_RELEASE_INCREMENT_20261004.json)。本补丁处理直接从含 `Build` 的根目录运行完整验证时，在大小写不敏感文件系统上可能误删暂存目录的条件风险；正常暂存与既有 CI 路径未观察到删除。该发行没有关闭旧 1.0.21 阶段 3 的发布门槛、12 个项目被中断的深审或 CVP 申请资格。旧时点 JSON 与 v1.0.3 资产均未倒填或改写。

**13:25 UTC IDBMeadow 发版增量：**[v1.0.3 正式 Release](https://github.com/dhtfish-98/IDBMeadow/releases/tag/v1.0.3)从提交 `9967db5328c042a2a71f9a27624589603197fdfb` 发布，主线及标签 CI 均成功；两份附件已回下载核对，版本、字节数和摘要见[独立发行增量记录](IDBMEADOW_V1_0_3_RELEASE_INCREMENT_20261004.json)。本版修复同类条件性 `Build` 清理风险，运行源码不变。最终包默认验证通过；完整慢速套件在最终打包前候选通过，旧测试中 13 处恒真断言仍 OPEN，CVP 资格不因此改变。旧逐仓快照不倒填。

**14:48 UTC IDBMeadow 发版增量：**[v1.0.4 正式 Release](https://github.com/dhtfish-98/IDBMeadow/releases/tag/v1.0.4)在公开提交 `1528dda445af89b20be9ba9b18d8a388755a7b14` 修正了 v1.0.3 报告中的 13 处恒真断言及一处由固定上游核实的旧夹具预期，并让直接从根目录运行验证时的生成物留在 `Build`。22 个运行时 Python 文件未变。主线与标签精确 CI 成功，两个附件回下载与终验包逐字节一致；版本、摘要和限定范围见[独立发行增量记录](IDBMEADOW_V1_0_4_RELEASE_INCREMENT_20261004.json)。原上游署名、Apache-2.0 许可继续保留。该修订关闭这 13 处测试断言缺口，不构成整个衍生项目独立重写、完整深审或 CVP 获批。旧快照和 v1.0.3 的时点记录保留。

**15:45 UTC 三项程序修复增量：**[ArchiveLens v1.0.4](https://github.com/dhtfish-98/ArchiveLens/releases/tag/v1.0.4)修正 GUI 子进程 stderr 填满管道造成的本地停滞路径，源包 425 个跟踪文件已与标签提交逐字节对照；另五项旧观察仍 OPEN。[TabWeave v4.3.1](https://github.com/dhtfish-98/TabWeave/releases/tag/v4.3.1)修正无 `id` 的 `tools/call` 通知产生非法 JSON 回复，浏览器外的 30 项测试通过，真实浏览器未重测。[BranchLoom v0.2.1](https://github.com/dhtfish-98/BranchLoom/releases/tag/v0.2.1)要求 Unicorn 验证器实际到达返回哨兵，合成循环不再仅凭匹配输出通过；本地 94 项完整测试和 92 项无依赖测试通过，真实 IDA/目标仍 OPEN。三仓最终 `main`/标签同提交、对应 GitHub CI 成功、正式 Release 附件回下载与准备品逐字节相同；版本、精确提交、工作流和摘要见[三项发行增量记录](MAINTENANCE_RELEASES_20261004T1545Z.json)。原第三方许可、来源和历史署名保留。这只关闭各自一项明确问题；中断的 12 项完整深审和 CVP 资格仍 OPEN。

2026-10-02 的 14 项替补、10 项保留项目、旧测试及固定发布结果是历史子集，不能代表今天的全部软件或最新提交。原文保留在 [历史索引](历史/20261002/README-目录更新时保留.md)，其他原记录见 [源码复核](SOURCE_REVIEW_20261002.md)、[保留项目复核](RETAINED_PROJECT_REVIEW_20261002.md)、[旧规则记录](CVP_RULES_AND_EVIDENCE_20261002.md)和 [历史分组原文件](历史/20261002/GROUPS-20261002.json)。历史撤出项目仍按原处置保留私有；这不是官方对仓库的永久禁止判断。
