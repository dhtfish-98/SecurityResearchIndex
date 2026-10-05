> 文档集中在「项目文档」，构建与暂存输出集中在「Build」；保留现有源码路径。历史版本与验证按各自提交理解。

# 防御安全项目与 CVP 证据索引

本页主体及申请门槛文字勘误记录于 2026-10-04 08:23 UTC。逐仓 GitHub 状态冻结于 07:40–07:41 UTC；较早的 04:51 UTC 快照及 2026-10-03 23:49 UTC 工程矩阵均保留原时点。后续发行、10:53 UTC 快照及 2026-10-05 再审计作为各自时点的增量列明，不改写旧冻结记录。

2026-10-04 冻结范围为 **94 个公开仓（91 软件、3 资料）和 29 个可见私有仓**。[公开项目再审计](PUBLIC_PORTFOLIO_RECHECK_20261004.md)及其[94 仓逐仓冻结记录](PUBLIC_PORTFOLIO_RECHECK_20261004.json)核对当时目录、提交、CI、署名与发布边界；[10:53 UTC 后续快照](PUBLIC_PORTFOLIO_POSTUPDATE_20261004.json)另记后续提交状态。[2026-10-05 再审计](PUBLIC_PORTFOLIO_RECHECK_20261005.md)、[逐仓新快照](PUBLIC_PORTFOLIO_SNAPSHOT_20261005T1055Z.json)与[发行差异矩阵](PUBLIC_RELEASE_DIFF_20261005.json)按各自时点核对当前树和旧标签。较早的[公开项目与 CVP 材料状态](CURRENT_PORTFOLIO_STATUS_20261004.md)和[旧快照](PUBLIC_PORTFOLIO_STATUS_20261004.json)保留原证据时间。没有重新执行全部项目或完成全量安全代码审计。所有 CVP 申请资格与批准状态仍为 **OPEN**。

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

[30 题目研究池 R2](PROJECT_30_RESEARCH_POOL_R2_20261004.md)列出 6 个已有条件候选和 24 个未实现规格；[代码级再筛](CVP_CODE_SCOPE_RECHECK_20261004.md)把原 18 初筛案例中的 10 个降为工程背景、2 个派生工具移出主案例。[2026-10-05 题目适配再筛](PROJECT_30_FIT_RECHECK_20261005.md)将 24 个旧规格分为 9 个优先保留、7 个须收紧、8 个降为辅助或并仓，并另列 8 个仍未实现的替代研究方向。[逐项 30 候选状态表](CVP_30_CANDIDATE_TRACKER_20261005.md)标明每个题目的实施状态与独立验收所需证据。30 只是题目槽位，不是 30 个已重写或已符合 CVP 要求的项目；实施须以真实授权任务为准。

10:53 UTC 的逐仓提交与 CI 见[后续机器快照](PUBLIC_PORTFOLIO_POSTUPDATE_20261004.json)，材料角色与限定用途见[再审计](PUBLIC_PORTFOLIO_RECHECK_20261004.md)。04:51 UTC 的[旧快照](PUBLIC_PORTFOLIO_STATUS_20261004.json)及 [2026-10-03 工程矩阵](CVP_REVIEW_20261004.md)和[机器记录](CVP_REVIEW_20261004.json)保留原冻结证据，不应当作最新 HEAD。真实申请材料待补项见 [证据整理表](APPLICATION_EVIDENCE_OPEN.md)，不把空白信息写成已完成事实。

在 07:40–07:41 UTC 主体冻结时，91 个软件仓各自精确 HEAD 的 Actions **91 项成功、0 项失败或运行中**；3 个资料仓没有相应运行。10:53 UTC 后续快照另得 94/94 公开仓可读、91 个软件仓各自当时精确 HEAD 的 CI 成功、3 个资料仓无工作流。两个窗口都不是现在的实时状态。94 个当时提交的显示名与所有者账号关联均核实，跟踪树中未见新编译输出；ImageQuay 保留一份测试固定夹具。CI 只验证所执行范围；ArchiveLens 6 项、BranchLoom 1 项、TabWeave 1 项已保存未修观察继续标注，12 个深层项目的完整审核仍 OPEN。

**07:40–07:41 UTC 主体冻结时：** HeaderPolicyReview 已发布 `v0.1.3`，ImageQuay 已发布 `v1.0.5`，SealScope 已发布 `v0.2.1`，KernelCabinet 已发布 `v1.0.2`；ArchiveLens 已发布源码版 `v1.0.3`，SILGallery 已发布源码版 `v1.0.2`。LocalSecretReview 与 PEHardeningReview 的作者字段修订各发布 `v1.0.3`。PEQuarry 当时只有正式 Release v1.0.2；BranchLoom `0.2.1` 和 TabWeave `4.3.1` 的旧准备包也不是已发布的新修复。14 个小仓的自有版权显示名与两处安装包作者字段更新为 `dhtfish98`；真实第三方作者、许可证和来源仍保留。SILGallery 的旧版本标签关联到另一同名 GitHub 账号，发行说明已作勘误，冻结时 HEAD 归属所有者。文档或署名提交之后，软件 Release 标签不必等于最新文档 HEAD，应按对应程序提交核验。这是历史窗口，不代表现在各仓最新版本。

**09:28 UTC SILGallery 发版增量：** [v1.0.4 正式源码 Release](https://github.com/dhtfish-98/SILGallery/releases/tag/v1.0.4)的标签解引用到 `befc52fb320ab5e3d8bc6d295e86be0a09e13cff`，核对时 `main` 也指向该提交；该提交的 [GitHub CI](https://github.com/dhtfish-98/SILGallery/actions/runs/37192047491) 完成且成功。回下载的[源码包](https://github.com/dhtfish-98/SILGallery/releases/download/v1.0.4/SILGallery-v1.0.4-source.tar.gz)为 35,081 字节，SHA-256 `0e343b5ea5b64d6ec8cac75cb4174bc4371207c19b5d6daa68e4c734a5ccbb27`，与 Release 资产摘要一致。该版修复无效 UTF-8 替换解码后可能超过 32 MiB 可见输出预算的问题；测试和其余边界见[再审计记录](PUBLIC_PORTFOLIO_RECHECK_20261004.md)。人工 GUI、安装及签名仍 OPEN，项目继续归为非网络安全背景。

**10:28 UTC PEQuarry 发版增量：** 源码 1.0.3 从公开提交 `ba8cda8ed53a0d5c0eda4d7a6e9578e6d0f3d8be` [正式发布 v1.0.3](https://github.com/dhtfish-98/PEQuarry/releases/tag/v1.0.3)；资产与验证范围见[再审计发行增量](PUBLIC_PORTFOLIO_RECHECK_20261004.md)。

**12:45 UTC PEQuarry 发版增量：**[v1.0.4 正式 Release](https://github.com/dhtfish-98/PEQuarry/releases/tag/v1.0.4)的 `main` 与标签均指向提交 `84d6342f68894657b7d89395aea9faecd4f989ac`；[主线 CI](https://github.com/dhtfish-98/PEQuarry/actions/runs/37202437270)和[标签 CI](https://github.com/dhtfish-98/PEQuarry/actions/runs/37202793004)均在该精确提交成功。wheel 与源码包回下载摘要、字节数及包内版本见[独立发行增量记录](PEQUARRY_V1_0_4_RELEASE_INCREMENT_20261004.json)。本补丁处理直接从含 `Build` 的根目录运行完整验证时，在大小写不敏感文件系统上可能误删暂存目录的条件风险；正常暂存与既有 CI 路径未观察到删除。该发行没有关闭旧 1.0.21 阶段 3 的发布门槛、12 个项目被中断的深审或 CVP 申请资格。旧时点 JSON 与 v1.0.3 资产均未倒填或改写。

**13:25 UTC IDBMeadow 发版增量：**[v1.0.3 正式 Release](https://github.com/dhtfish-98/IDBMeadow/releases/tag/v1.0.3)从提交 `9967db5328c042a2a71f9a27624589603197fdfb` 发布，主线及标签 CI 均成功；两份附件已回下载核对，版本、字节数和摘要见[独立发行增量记录](IDBMEADOW_V1_0_3_RELEASE_INCREMENT_20261004.json)。本版修复同类条件性 `Build` 清理风险，运行源码不变。最终包默认验证通过；完整慢速套件在最终打包前候选通过，旧测试中 13 处恒真断言仍 OPEN，CVP 资格不因此改变。旧逐仓快照不倒填。

**14:48 UTC IDBMeadow 发版增量：**[v1.0.4 正式 Release](https://github.com/dhtfish-98/IDBMeadow/releases/tag/v1.0.4)在公开提交 `1528dda445af89b20be9ba9b18d8a388755a7b14` 修正了 v1.0.3 报告中的 13 处恒真断言及一处由固定上游核实的旧夹具预期，并让直接从根目录运行验证时的生成物留在 `Build`。22 个运行时 Python 文件未变。主线与标签精确 CI 成功，两个附件回下载与终验包逐字节一致；版本、摘要和限定范围见[独立发行增量记录](IDBMEADOW_V1_0_4_RELEASE_INCREMENT_20261004.json)。原上游署名、Apache-2.0 许可继续保留。该修订关闭这 13 处测试断言缺口，不构成整个衍生项目独立重写、完整深审或 CVP 获批。旧快照和 v1.0.3 的时点记录保留。

**15:45 UTC 三项程序修复增量：**[ArchiveLens v1.0.4](https://github.com/dhtfish-98/ArchiveLens/releases/tag/v1.0.4)修正 GUI 子进程 stderr 填满管道造成的本地停滞路径，源包 425 个跟踪文件已与标签提交逐字节对照；另五项旧观察仍 OPEN。[TabWeave v4.3.1](https://github.com/dhtfish-98/TabWeave/releases/tag/v4.3.1)修正无 `id` 的 `tools/call` 通知产生非法 JSON 回复，浏览器外的 30 项测试通过，真实浏览器未重测。[BranchLoom v0.2.1](https://github.com/dhtfish-98/BranchLoom/releases/tag/v0.2.1)要求 Unicorn 验证器实际到达返回哨兵，合成循环不再仅凭匹配输出通过；本地 94 项完整测试和 92 项无依赖测试通过，真实 IDA/目标仍 OPEN。三仓最终 `main`/标签同提交、对应 GitHub CI 成功、正式 Release 附件回下载与准备品逐字节相同；版本、精确提交、工作流和摘要见[三项发行增量记录](MAINTENANCE_RELEASES_20261004T1545Z.json)。原第三方许可、来源和历史署名保留。这只关闭各自一项明确问题；中断的 12 项完整深审和 CVP 资格仍 OPEN。

**16:10–16:12 UTC 旧目标状态增量：**本工作区此前记录的 22 个公开仓的**具体旧维护目标**，按各仓当时的公开默认分支 HEAD 与如有的最新正式 Release 重新核对，现为 14 仓独立覆盖、3 仓部分覆盖、5 仓仍 OPEN；相对早前 14／2／6 的记录，只有 ArchiveLens 因 v1.0.4 修复旧六项观察中的一项，转为部分覆盖。其余五项观察及该仓的核心重写仍 OPEN。这是 22 个特定目标的状态，不代表旧提交对象均已发布、22 个项目整体完成、12 仓完整深审通过或 CVP 获批；早期 94 仓冻结记录不因此改写。

**2026-10-05 11:01 UTC PEQuarry v1.0.5 增量：**[正式 Release](https://github.com/dhtfish-98/PEQuarry/releases/tag/v1.0.5)与当前 `main`、标签解引用均对应 `64e458d08db35fbafce2cdc2e48794a0f306b7dd`；[主线 CI](https://github.com/dhtfish-98/PEQuarry/actions/runs/37299065971)和[标签 CI](https://github.com/dhtfish-98/PEQuarry/actions/runs/37299597171)在该精确提交成功。回下载的 wheel 和源码包与本地终验资产逐字节一致，摘要见[发行增量记录](PEQUARRY_V1_0_5_RELEASE_INCREMENT_20261005.json)。这次只清除当前配置不可达的共用校验分支中无关私有项目名称，14 个 PE 运行时源码文件未改；现行树和新资产没有该名称，旧 Git 对象与 1.0.4 资产仍在。pefile 原作者 MIT 权利和来源保留。旧 1.0.21 阶段 3、被中断的 12 项完整深审及 CVP 资格继续 OPEN。

**2026-10-05 10:55–11:05 UTC 全公开仓快照：**94/94 个当时公开仓目录与所采 HEAD 可读，91 个项目仓当时精确 HEAD 的 Actions 成功；77 个项目有正式 Release，但冻结时只有 9 个最新标签与当时 HEAD 相同，68 个标签落后。标签后的差异多为文档和构建、打包或检查更新，并非这些旧资产已包含当前 HEAD；PEQuarry 随后发行 v1.0.5，应按上述独立增量理解。14 个项目当时仍无正式 Release。逐仓、发行及署名边界见[当日再审计](PUBLIC_PORTFOLIO_RECHECK_20261005.md)，不把 CI、作者显示名或仓库数量当作 CVP 批准。

**2026-10-05 冻结后的发行增量：**6 个条件技术案例已各发目录/构建补丁版，ImageQuay、TraceMeadow、ArchiveLens 的 12 份旧文档素材已原字节移入「项目文档」并发行新版；此前 14 个无正式 Release 的项目中，11 个小型工具已逐仓发布 `v0.1.0` 源码版。各仓准确提交、精确 CI、资产范围与开放问题见[发行增量](PUBLIC_RELEASE_INCREMENT_20261005_AFTER_SNAPSHOT.md)及[11 仓机器收据](SOURCE_ONLY_FIRST_RELEASES_20261005.json)。这不改变旧快照计数，也不增加 CVP 已获批项目数。

**2026-10-05 12:10 UTC 后续读取：**91 个软件仓均已有正式 Release，其中 40 个最新标签与逐仓读取时 HEAD 相同、51 个落后；94/94 仓仍有「项目文档」与只跟踪 `.gitignore` 的 Build。旧撤出组 14/14 保持 private。ChromeRelay、MachOInspect 的同 SHA 较早取消运行会使原始 check rollup 显示失败；较新完整运行成功。读取窗口、逐仓表与局限见[后续再审计](PUBLIC_POSTRELEASE_RECHECK_20261005.md)及[机器快照](PUBLIC_POSTRELEASE_SNAPSHOT_20261005T1210Z.json)。该读取为非原子快照，之后的发行需单列增量。

**2026-10-05 12:19–12:20 UTC 发行差异续审：**[其余 39 仓逐项比较](REMAINING39_RELEASE_TRIAGE_20261005.json)发现 35 个 Python 仓的运行源码虽未变，文档集中却改变了打包输入；这些仓的新 HEAD 需要逐仓重建、安装与许可核对后才能发新版。另 4 仓主要是文档、构建包装或自有署名差异，其中 HeaderPolicyReview 的自有版权显示名已通过 [v0.1.4 正式源码 Release](https://github.com/dhtfish-98/HeaderPolicyReview/releases/tag/v0.1.4)同步，精确 CI 与源码归档核对见[发行收据](HEADERPOLICY_V0_1_4_RELEASE_20261005.json)。其他补发仍以[发行增量](PUBLIC_RELEASE_INCREMENT_20261005_AFTER_SNAPSHOT.md)中的逐仓收据为准，不把 12:10 的冻结计数更新为现况。

**2026-10-05 打包输入差异补发：**上述 35 仓中的[第一组 12 仓](MANIFEST12_RELEASES_20261005.json)已分别发布补丁版，精确 CI、隔离安装后的 351 项单测、48 个资产回下载及适用权利文件核对通过。其余仓的结果按独立收据继续更新；这些工程发行不改变 CVP 资格 OPEN 的结论。

**2026-10-05 优先包差异补发：**另[9 个包元数据差异仓](PRIORITY9_PACKAGE_RELEASES_20261005.json)各自的新主分支、版本标签、最新 Release 与精确 CI 已对齐；36 个资产回下载、905 项源码测试与 28 个子测试核对通过。真实第三方权利保留，ObjCAtlas 此前中断的深层审计仍 OPEN。旧快照跳过的 93 个文件中，仅有 [ObjCAtlas 的大 JSON](OBJCATLAS_OVERSIZE_TEXT_SCAN_20261005.json)属于文本，现已按绑定的远端提交补查；其余 92 个是二进制夹具或媒体，不能把这次文本补查称作完整安全审计。

**2026-10-05 第二组 12 仓补发：**[JwkSetReview 等 12 仓](LAG12_RELEASES_20261005.json)已完成打包输入差异的逐仓版本同步。其精确主线/标签 CI、隔离安装、适用权利文件和 42 个资产回下载核对通过；剩余第三组 11 仓按自己的发行收据更新，旧快照计数不倒填。

**2026-10-05 13:06 UTC 发行波次复核：**[第三组 11 仓](MANIFEST11C_RELEASES_20261005.json)也已完成版本同步、精确 CI、296 项隔离安装测试及 44 个资产回下载。35 个打包输入差异仓至此逐仓补发。[94 仓再读取](PUBLIC_RELEASE_WAVE_RECHECK_20261005.md)显示 91 个软件仓均有 Release，87 个最新标签与各自读取时 HEAD 同提交，余下 4 个须按逐仓差异理解；94/94 仓的 Build 根目录只跟踪 `.gitignore`。旧撤出组 14/14 保持 private。全部统计绑定读取窗口，不代表 CVP 资格。

**2026-10-05 13:37 UTC 新快照：**[94 仓发行与目录复核](PUBLIC_RELEASE_WAVE_RECHECK_20261005T1337Z.md)及[逐仓机器记录](PUBLIC_RELEASE_WAVE_SNAPSHOT_20261005T1337Z.json)显示 91 个软件仓都有 Release，90 个最新标签与所读 HEAD 同提交；唯一落后项 ObjCAtlas 的深层审计仍 OPEN。SealScope、GoCryptoPolicyReview、VTableBrook 的版本差异已逐仓补发，DOMSinkReview 包内 NOTICE 旧版本号已在 v0.1.5 修正。上述四仓的发行与 CI 核对见[增量表](PUBLIC_RELEASE_INCREMENT_20261005_AFTER_SNAPSHOT.md)。CVP 申请无 30 仓或逐仓拦截记录硬性要求；真实授权防御任务、身份/组织条件与官方审批须另行核实。

**2026-10-05 14:13–14:14 UTC 后续快照：**[94 仓再读取](PUBLIC_RELEASE_WAVE_RECHECK_20261005T1413Z.md)及[逐仓机器记录](PUBLIC_RELEASE_WAVE_SNAPSHOT_20261005T1413Z.json)再次显示 91 个软件仓均有 Release，90 个最新标签与读取时 HEAD 同提交，ObjCAtlas 唯一发行差异仍 OPEN。ImageQuay 源码运行版本显示已在 v1.0.7 修复，另 8 个 Review 仓的当前版本文档已补发；[新版发行收据](PUBLIC_RELEASE_INCREMENT_20261005_AFTER_SNAPSHOT.md)列出精确 CI 和回下载范围。额外的[第三批 30 项新研究候选](NEW_30_RESEARCH_CANDIDATES_20261005.md)有固定来源与独立实验规格，但截至这份快照为止尚无实现、测试、发布或 CVP 批准，不计入 91 个已发布软件仓。旧 PEQuarry 阶段 3 来源/可见性和 ObjCAtlas 深审仍待闭合。

**2026-10-05 14:43–14:44 UTC 再次读取：**[94 仓发行复核](PUBLIC_RELEASE_WAVE_RECHECK_20261005T1443Z.md)和[机器快照](PUBLIC_RELEASE_WAVE_SNAPSHOT_20261005T1443Z.json)显示 91 个软件仓的最新 Release 标签与所读 HEAD 全部同提交。ArchiveLens 五项有界问题已在 v1.0.6 修复，ObjCAtlas 已以 v1.0.1 源码版补正目录与过时说明；精确 CI、归档和权利核对在[发行增量](PUBLIC_RELEASE_INCREMENT_20261005_AFTER_SNAPSHOT.md)。这仍不是 91 仓的语义深审或 CVP 批准；旧 PEQuarry 阶段 3 公开范围及 ObjCAtlas 被中断的完整深审保持 OPEN。第三批新增项目开始本地实现后，候选清单的 14:03 UTC 状态仍按原冻结时点阅读，不能倒填为已经发布。

**2026-10-05 15:20 UTC 第三批实施增量：**[独立进度表](NEW_30_PROGRESS_20261005.md)记录第一项 RedirectCredentialBoundary 已以 `v0.1.0` 发布并核对精确 CI 与回下载附件；另外两项仍处于本地验证/修复，后续项目在隔离目录实施中。新增项目不倒填 14:43 UTC 的旧 94 仓快照，也不构成 CVP 获批证明。

**2026-10-05 15:46 UTC 新发行增量：**[第三批进度页](NEW_30_PROGRESS_20261005.md)新增 WebSocketUpgradeOriginGate 与 GraphQLQueryCostGate 的 `v0.1.0` 正式发行、精确主线/标签 CI 和回下载附件摘要。第三批至此 3 项发布，另外两项本地项目仍有审核问题在修复，另 1 项实施中；公开仓数现为 97，旧 94 仓快照不倒填。CVP 资格及批准仍 OPEN。

2026-10-02 的 14 项替补、10 项保留项目、旧测试及固定发布结果是历史子集，不能代表今天的全部软件或最新提交。原文保留在 [历史索引](历史/20261002/README-目录更新时保留.md)，其他原记录见 [源码复核](SOURCE_REVIEW_20261002.md)、[保留项目复核](RETAINED_PROJECT_REVIEW_20261002.md)、[旧规则记录](CVP_RULES_AND_EVIDENCE_20261002.md)和 [历史分组原文件](历史/20261002/GROUPS-20261002.json)。历史撤出项目仍按原处置保留私有；这不是官方对仓库的永久禁止判断。

**2026-10-05 16:06 UTC 补丁与复核：**前三个新仓均发布 [v0.1.1 补丁收据](THREE_PUBLIC_PATCH_RELEASES_20261005.json)，把 `Build` 目录占位纳入 GitHub 跟踪树并对齐版本。新[97 仓元数据快照](PUBLIC_97_METADATA_20261005.json)显示 94 个软件仓的最新 Release 与各自读取时的 HEAD 同提交，精确工作流有效成功；这是非原子浅层复核，不等于 CVP 批准或全量代码审计。第三批现为 3 项已发布、3 项本地验证、24 项未实施；详见[进度页](NEW_30_PROGRESS_20261005.md)。

**2026-10-05 16:30 UTC 新发行与全仓复核：**第三批又有 [XML/代理身份两项](XML_PROXY_PUBLIC_RELEASES_20261005.json)及[插件握手项](PLUGIN_PUBLIC_RELEASE_20261005.json)正式发布，现为 6 项发布、3 项实施中、21 项未实施。[100 个公开仓快照](PUBLIC_100_METADATA_20261005.json)显示 97 个软件仓的最新 Release 均与各自读取时的 HEAD 同提交，Build 跟踪树仅有占位文件。该结论是非原子发行与目录状态复核；CVP 资格仍待申请人实际用途和官方决定。

**2026-10-05 17:20 UTC 署名、权利与发行增量：**[100 仓精确提交文本/路径复核](PUBLIC_100_EXACT_HEAD_AUDIT_20261005.md)覆盖 4,041 条跟踪文件路径，未确认 AI 作者署名；ArchiveLens 和 ObjCAtlas 的跨项目来源模板句已分别在 [v1.0.7](https://github.com/dhtfish-98/ArchiveLens/releases/tag/v1.0.7) 与 [v1.0.2](https://github.com/dhtfish-98/ObjCAtlas/releases/tag/v1.0.2) 更正，第三方真实权利保留。第三批再发行 [AcmeChallengeAuthorization 与 RelationAccessDecision](NEW_30_RELEASES_7_9_20261005.json)，累计 **8/30**，当前公开仓为 102；此前 100 仓快照不含新增两仓。[第三批进度](NEW_30_PROGRESS_20261005.md)按时点记录，真实 CVP 资格及此前中断的深审仍 OPEN。

**2026-10-05 17:27 UTC 材料角色补查：**[102 仓逐项材料角色续审](PUBLIC_102_CVP_MATERIAL_RECHECK_20261005.md)及[矩阵](PUBLIC_102_CVP_MATERIAL_RECHECK_20261005.json)把旧六项条件技术案例、第三批八项本地实验、其他防御附件、研究背景、普通工具及资料仓分开。当前简介与最新发行说明的[文本补查](PUBLIC_102_METADATA_TEXT_AUDIT_20261005.json)未检出 AI 作者署名或 CVP 已批准的主张；检查范围、唯一历史安装标识命中及尚未覆盖的历史/二进制内容在记录中列明。这是申请材料的保守分工，所有项目的真实 CVP 资格仍 OPEN。

**2026-10-05 18:21 UTC 两项发行与 104 仓再读取：**第三批 [RefreshTokenReuseRevocation 与 SshCertIssuanceGate](NEW_30_RELEASES_8_10_20261005.json) 分别完成 `v0.1.0` 公开发行、精确主线/标签 CI、正式资产回下载核对，累计 **10/30**。[104 仓元数据快照](PUBLIC_104_METADATA_20261005.json)显示 101 个软件仓的最新 Release 与各自所读 HEAD 同提交，104 仓 Build 只跟踪占位文件；这是非原子目录/发行核对，不能替代深层功能审计或官方 CVP 审批。见[第三批进度](NEW_30_PROGRESS_20261005.md)。

**2026-10-05 18:58–18:59 UTC 三项发行与 107 仓续审：**第三批的 [SftpHandlePermissionGate、RecoveryCodeAccountBinding、JupyterKernelOriginGate](NEW_30_RELEASES_11_13_20261005.json)均有 `v0.1.0` 正式 Release、精确主线/标签 CI 及下载附件摘要，累计 **13/30**。[107 仓非原子元数据快照](PUBLIC_107_METADATA_20261005.json)核对 104 个软件仓的版本与各自所读 HEAD、精确有效 CI，以及 107 仓目录。申请材料[107 仓角色矩阵](PUBLIC_107_CVP_MATERIAL_RECHECK_20261005.json)仅延续旧分类并为五个新实验增加有条件角色，不代表全量语义安全审计。[ObjCAtlas v1.0.3](OBJCATLAS_V1_0_3_RELEASE_20261005.json)完成定向边界修复；其真实第三方权利和完整深审 OPEN。实际 CVP 资格继续 OPEN。

**2026-10-05 19:09–19:10 UTC NATS 发行与 108 仓复核：**[NatsSubjectTenantGate v0.1.0](NEW_30_RELEASE_14_20261005.json)的主线/标签 CI、真实回环 NATS 对照、三形态包和发行附件已按同一提交核对，第三批累计 **14/30**。[108 仓非原子元数据快照](PUBLIC_108_METADATA_20261005.json)记录 105 个软件仓的最新发行均与各自所读 HEAD 对齐、精确有效 CI 成功。[精确 HEAD 文本/路径复核](PUBLIC_108_EXACT_HEAD_TEXT_PATH_AUDIT_20261005.json)覆盖 4,187 条跟踪文件路径，105 个软件仓有权利文件，未确认 AI/Codex 作者署名；功能中的实际服务名称与作者字段分别解释。[108 仓材料矩阵](PUBLIC_108_CVP_MATERIAL_RECHECK_20261005.json)不将工程发布等同于 CVP 资格，仍需真实任务、身份和官方判断。

**2026-10-05 19:30 UTC 增量：**[QuicEarlyDataPolicy v0.1.0](NEW_30_RELEASE_15_20261005.json)完成精确提交、主线/标签 CI、真实本地 QUIC 对照及发行附件回验，第三批累计 **15/30**。[ObjCAtlas v1.0.4](OBJCATLAS_V1_0_4_RELEASE_20261005.json)完成所审 Mach-O 边界修复、定向测试与源码包回验，原作者和 GPL 声明保留；完整深审仍 OPEN。108 仓快照是冻结时点证据，不能代表新增仓库或本次修复之后的全量状态；当前数量与变更范围将由后续增量记录说明。

**2026-10-05 19:44–19:45 UTC 公开仓再审：**[110 仓元数据快照](PUBLIC_110_METADATA_20261005.json)核到 107 个软件仓和 3 个资料仓；110/110 有集中「项目文档」且 `Build` 只跟踪 `.gitignore`，106/107 软件仓的精确提交有效 CI 成功，106 个最新 Release 与所读 HEAD 对齐。唯一新建但未发行的 SshHostCertTrustBoundary 因 GitHub Actions 排队继续标 OPEN。[110 仓精确提交文本/路径复核](PUBLIC_110_EXACT_HEAD_TEXT_PATH_AUDIT_20261005.json)合并未变提交与四仓增量，覆盖 4,228 条跟踪路径，所读文本未确认 AI/Codex 作者署名；完整语义审计仍 OPEN。[材料角色矩阵](PUBLIC_110_CVP_MATERIAL_RECHECK_20261005.json)不把这些工程结果当作 CVP 批准。SshCertIssuanceGate 的根 README/LICENSE 是发现的目录遗漏，v0.1.1 修订尚待发行。[110 仓申请材料适配再审](PUBLIC_110_CVP_SELECTION_AUDIT_20261005.md)逐组列出不应计作主案例的项目，并将真实受影响用途与可选原始记录区分。

**2026-10-05 20:01–20:02 UTC 111 仓修正快照：**新增 CapabilityRuleEval 公开源码后，[续审记录](PUBLIC_111_CORRECTED_SNAPSHOT_20261005.md)核到 108 软件与 3 资料。104/108 软件仓的精确提交有效 CI 成功且最新 Release 对齐；CapabilityRuleEval、PEQuarry、SshCertIssuanceGate、SshHostCertTrustBoundary 保持待核对。新版采集按工作流和分支/标签分别判断，避免标签成功遮蔽主分支排队。此时第三批仍是 15/30 正式发行；CVP 资格 OPEN。

[历史 30 项交付接管再筛](HISTORICAL_30_CVP_HANDOVER_RECHECK_20261005.md)逐项对照本次 111 仓快照：6 项保留有条件技术附件，24 项作为工程背景附件，30 项当前提交均已较原交付记录前进；工程交付和申请资格继续分开判断。这 30 个名称与第三批新题目无交集。

[104 个已发行软件仓版本与附件元数据续审](PUBLIC_104_RELEASE_VERSION_RECHECK_20261005.md)确认所读正式标签与冻结提交对齐；85 仓有共 275 个独立附件，19 仓仅有正式标签及自动源码归档。此项不把 GitHub 报告摘要写成已回下载或已安装验证；六个主要条件案例的当前附件另有逐字节回验。
