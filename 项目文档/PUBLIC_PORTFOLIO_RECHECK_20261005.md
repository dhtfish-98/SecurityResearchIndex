# 公开项目目录、发布与署名复核（2026-10-05）

本轮在 10:55 UTC 左右读取 94 个公开仓库的当时默认分支树、最新正式 Release 与 Actions；最新标签的提交解引用与差异比较截至 11:05 UTC。逐仓结果见[冻结快照](PUBLIC_PORTFOLIO_SNAPSHOT_20261005T1055Z.json)和[发行差异矩阵](PUBLIC_RELEASE_DIFF_20261005.json)。两个读取窗口不是原子快照；后续更新须作为增量核对。

- 94/94 仓为公开、非 fork；其中 91 个项目仓、3 个资料仓。94/94 有「项目文档」和仅跟踪 `.gitignore` 的 `Build` 目录。91 个项目仓在读取时各有与当时 HEAD 对应的成功 Actions；资料仓无工作流。此项是目录、版本与自动检查元数据审计，没有重跑 91 个项目的功能测试或完整安全代码深审。
- 77 个项目仓有正式 Release，14 个没有 Release 或标签。77 个最新 Release 标签在冻结时仅 9 个与当时 HEAD 同提交，68 个落后 1–4 个提交。68 个差异未见 `src/` 等主要运行源码路径改动，但 24 个涉及测试、验证或构建后端代码，其余多数也有包装或构建配置变更；所以旧 Release 资产不能代表新 HEAD 的完整目录与构建状态。`PEQuarry` 是这 24 个之一，已在冻结后发布 [v1.0.5](PEQUARRY_V1_0_5_RELEASE_INCREMENT_20261005.json)，不能倒改冻结计数。
- 14 个当时无正式 Release 的项目：A64Dispatch、ArtifactDigestReview、AuthLogReview、ChromeRelay、ContainerfileReview、DependencyPinReview、EntitlementFlagReview、FileModeReview、IAMScopeReview、KubePodReview、MachOInspect、SBOMFieldReview、SSHPolicyReview、WorkflowPermissionReview。它们的 GitHub 主分支存在，不应写成“已发正式版本”。
- CDTranslator、HeaderPolicyReview、LocalSecretReview、PEHardeningReview、SealScope 的现有 Release 没有手工上传资产，但标签仍有 GitHub 自动源码归档；单凭零附件不能断言未发布。
- 94 个当时 HEAD 的 Git 提交作者与提交者显示为 `dhtfish98`。CDTranslator 当前许可文本的 `dhtfish988` 是同一 GitHub 数字账号的旧显示署名，宜在新提交更新；历史 Git 仍保持原样。BranchLoom、SILGallery 与其他有来源记录的第三方作者和许可证是真实权利，不能改称申请人独创。ArchiveLens 源码中的模型工具名称属于现有功能接口，不能误判为作者署名。
- IDBMeadow 的 IDB/i64 样本及 ImageQuay 的 dylib 样本可能是测试输入；是否迁出须按实际测试依赖验证，不能把它们直接当编译产物删除。

此轮没有证明 94 个项目均符合 CVP 要求。按[代码级申请材料再筛](CVP_CODE_SCOPE_RECHECK_20261004.md)，两批 60 个项目中仍只有 6 个有条件技术案例，其余 54 个为工程背景；另 24 个题目原本只是未实施规格，[今日适配再筛](PROJECT_30_FIT_RECHECK_20261005.md)又将其中 8 个降为辅助或并仓。身份、真实授权任务、受保障措施影响与官方批准均为 OPEN。
