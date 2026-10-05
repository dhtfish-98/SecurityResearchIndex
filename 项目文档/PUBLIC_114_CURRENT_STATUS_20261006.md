# 114 个公开仓当前元数据与申请材料续审

**读取窗口：2026-10-05 21:58:44–22:04:29 UTC；非原子快照。**逐仓记录见 [114 仓机器矩阵](PUBLIC_114_CURRENT_METADATA_20261006.json)。本记录接在 [113 仓旧冻结报告](PUBLIC_113_CORRECTED_STATUS_20261005.md)之后；旧报告是其当时事实，不倒改成当前结论。索引仓发布本记录后自身 HEAD 会变化，因此此处的索引 HEAD 仍以读取窗口为准。

| 当前公开状态 | 读取结果 | 范围 |
| --- | ---: | --- |
| 公开仓库 | 114 | 111 个软件、3 个资料或索引；旧 113 仓仍在，新增 DexInvokeEvidence |
| 当前 HEAD 作者和提交者关联 `dhtfish-98` | 114/114 | GitHub 账号映射，不代表历史提交或第三方代码归属 |
| 软件仓当前 HEAD 检查汇总成功 | 111/111 | GitHub 当前提交的检查汇总；不代替逐平台、逐功能或安装验证 |
| 当前 HEAD 的全部源码主线工作流成功 | 111/111 | 独立逐工作流复核共 113 个工作流；旧 cancelled 运行另记 |
| 同 HEAD 标签检查成功／工作流仅触发主线 | 89／22 | 22 仓的当前工作流不配置标签触发，不能要求不存在的标签运行 |
| 软件仓最新正式 Release 标签指向所读 HEAD | 111/111 | 同时复核 GitHub Release 和标签引用；不代表全部历史附件已逐字节回下载 |
| 最新正式发行的注释标签 tagger 为本账号邮箱 | 73/73 | 其余 38 个为轻量标签，没有 tagger 字段 |
| 含「项目文档」且跟踪的 `Build` 仅 `.gitignore` | 114/114 | 只说明所读 Git 跟踪树；本地历史归档另查 |
| 第三批固定 30 候选已有正式 Release | 20/30 | 16 个 A 级研究题目、4 个 B 级题目；其余 10 个未计入 |

上次 [113 仓账号关联审计](PUBLIC_113_CORRECTED_STATUS_20261005.md)指出的 13 个当前 HEAD 错误映射已通过各自**新提交及新版本**纠正：ArchiveLens v1.0.8、GraphQLQueryCostGate v0.1.2、JupyterKernelOriginGate v0.1.1、NatsSubjectTenantGate v0.1.1、ObjCAtlas v1.0.5、PluginHandshakeTrustGate v0.1.1、ProxyIdentityHeaderTrust v0.1.1、QuicEarlyDataPolicy v0.1.1、RecoveryCodeAccountBinding v0.1.1、RedirectCredentialBoundary v0.1.2、SftpHandlePermissionGate v0.1.1、WebSocketUpgradeOriginGate v0.1.2、XmlEntityResourceBoundary v0.1.1。旧版本与旧标签中的错误关联继续作为历史事实保留。新提交的显示名是 `dhtfish98`，其作者和提交者映射到所有者账号 `dhtfish-98`；这只证明提交元数据关联，真实来源和第三方权利继续按各仓证据表述。

第三批的 16 个 A 级题目现均有正式版本；B 级中 CapabilityRuleEval、DexInvokeEvidence、FederatedConnectorIdentityGate、ObfuscatedStringRecovery 有正式版本。**尚未发行的 10 项**为 BuildSecretMountLifetimeGate、ContainerCapabilityDropGate、CsiSecretNamespaceGate、HeadscaleEnrollmentGate、LandlockFilesystemGate、PgPoolPrincipalIsolation、RemoteDesktopTransferGate、RootlessIdMapBoundary、WireGuardPeerPrefixBinding、XlmFormulaTrace。PgPoolPrincipalIsolation 已有本地真实 PostgreSQL/PgCat 实验候选，但尚未完成独立审核与公开发行；不能提前计数。此前接管的另一个历史 30 项名单与这批 30 项无同名交集；前者仍按 [历史 30 项接管再筛](HISTORICAL_30_CVP_HANDOVER_RECHECK_20261005.md)的旧六项条件技术附件和 24 项工程背景分组，不应合并为 50 个“符合 CVP 项目”。

**目录遗漏：**所读 4,338 个跟踪文件中，ImageQuay 的 `checks/bins/testbin1`、`testbin1.fat`、`testbin1.signed`、`testlib1.dylib` 为供测试读取的二进制夹具，其中仅 `.dylib` 被本轮扩展名初筛标记。它们虽不是发行编译输出，但仍是项目源码树中的已编译文件，故“每个项目目录仅留源码”尚未完全达成。需要保留测试意义，在 `Build` 生成或归档夹具并修改测试引用，完成版本化修订后再关闭这一项。其他无扩展名二进制的全字节识别未在本轮完成。

本轮检查只读取公开 GitHub 元数据、精确 HEAD 的跟踪目录、工作流和最新标签指向；没有重新执行 111 个软件项目，没有逐文件复核全部作者文本、所有第三方权利、全部发行附件，也没有完成 12 个旧大型项目的全量语义与平台审核。ChromeRelay、MachOInspect 各有一次同提交较早取消的运行，之后的对应主线运行成功；不能误报成当前失败。早期记录的八项具体程序观察已分别通过 [ArchiveLens v1.0.4 的管道修复、v1.0.6 的五项边界修复](PUBLIC_RELEASE_INCREMENT_20261005_AFTER_SNAPSHOT.md)及 [BranchLoom v0.2.1、TabWeave v4.3.1](MAINTENANCE_RELEASES_20261004T1545Z.json)的定向测试与发行处理；这些限定修复仍不能替代各仓完整深审和真实平台验证。发行仍需按各仓独立的构建、测试、回下载回执判定；旧的编译、上传或旧 SHA 成功不替代新提交。

[Anthropic 官方 CVP 说明](https://support.claude.com/en/articles/14604842-real-time-cyber-safeguards-on-claude-opus-and-sonnet)针对真实合法的高风险双用途防御工作及所受防护影响；Claude.ai / Claude Code 走第一方门户。公开说明没有把 30 个仓库或逐仓拒绝日志列为申请硬门槛。20 个版本是工程交付计数，**不是 20 个已获官方认定的申请案例**。申请人的实际授权任务、影响、账号/组织和批准结果仍为 **OPEN**，见 [申请证据待补表](APPLICATION_EVIDENCE_OPEN.md)。
