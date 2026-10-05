# 115 个公开仓当前续审与第三批 21 项发行

**非原子读取窗口：2026-10-05 22:23:29–22:24:14 UTC。**[逐仓矩阵](PUBLIC_115_CURRENT_METADATA_20261006.json)先重新读取全部公开仓及其当前 HEAD、作者账号、检查汇总和最新 Release；[上一轮 114 仓的逐树审计](PUBLIC_114_CURRENT_STATUS_20261006.md)中全部 114 个 HEAD 与最新发行目标均未变化，因此其精确提交的目录、标签和工作流证据可以沿用。新增的 PgPoolPrincipalIsolation 另行核对精确树、注释标签、双分支检查和公开附件。发布本索引文档后，索引仓自身 HEAD 会前进；这里的索引 HEAD 属于上述冻结窗口。

| 项目 | 当前核对结果 |
| --- | --- |
| 公开范围 | **115 仓**：112 软件、3 资料或索引；比上一轮新增 PgPoolPrincipalIsolation 一仓 |
| 当前提交作者与提交者的 GitHub 账号关联 | **115/115** 均为 `dhtfish-98`；新建仓的显示名、邮箱及注释标签 tagger 同为正确所有者信息 |
| 软件仓最新正式版本与所读 HEAD | **112/112** 精确同提交；没有缺失或落后版本 |
| 软件仓当前 HEAD 检查 | **112/112** 检查汇总及所有源码主线工作流成功；90 仓另有同提交标签检查，22 仓的工作流仅配置主线触发 |
| 跟踪目录 | **115/115** 有「项目文档」；旧 114 仓的 `Build` 均只跟踪 `.gitignore`，新仓在构建时创建 `Build` 并把它列为忽略目录，没有跟踪编译产物 |
| 第三批固定 30 题目 | **21/30** 正式发行：16 个 A 级、5 个 B 级；9 个未发行 |

[PgPoolPrincipalIsolation v0.1.0](https://github.com/dhtfish-98/PgPoolPrincipalIsolation/releases/tag/v0.1.0)于提交 `06f415dff81e65e44a372a9855dfdf003e6141ac` 公开。其 [main](https://github.com/dhtfish-98/PgPoolPrincipalIsolation/actions/runs/37381169382)和[标签](https://github.com/dhtfish-98/PgPoolPrincipalIsolation/actions/runs/37381173663)工作流均为该 SHA 且成功；两份 GitHub Linux 回执各记录真实 PostgreSQL 17.6 和固定 PgCat 1.3.0 的 22 项通过。正式源码归档 16 个跟踪文件与 Git 对象逐文件相同，wheel、sdist、源码包和 SHA256SUMS 公开回下载与本地字节完全一致，详情见[脱敏发行收据](PGPOOL_V0_1_0_RELEASE_20261006.json)。它是原创的应用侧只读连接门禁，自造弱池仅作对照；没有声称 PgCat 上游漏洞或实际 CVP 资格。PgCat、PostgreSQL 与 Psycopg 的原权利和来源在项目文档中保留。

第三批余下 **9 项未发行**：BuildSecretMountLifetimeGate、ContainerCapabilityDropGate、CsiSecretNamespaceGate、HeadscaleEnrollmentGate、LandlockFilesystemGate、RemoteDesktopTransferGate、RootlessIdMapBoundary、WireGuardPeerPrefixBinding、XlmFormulaTrace。其中 Headscale 和 Landlock 的真实本地服务/内核实验正在形成候选，不能提前计入发行。此前接管的**另一个历史 30 项**与第三批名单无同名交集，按[历史接管再筛](HISTORICAL_30_CVP_HANDOVER_RECHECK_20261005.md)保留其原有条件技术附件／工程背景划分，不把两个名单相加当作已获 CVP 认定的项目数。

**仍需修正的目录例外：**ImageQuay 当前公开仓仍跟踪四个编译测试夹具：`checks/bins/testbin1`、`testbin1.fat`、`testbin1.signed`、`testlib1.dylib`。其精确来源、复建与测试迁移正在独立候选中审核；在新提交、测试和正式发行之前，不能写成“115 仓全部仅有源码”。本轮路径初筛只识别 `.dylib` 后缀，另外三个靠固定夹具清单识别；全部无扩展名文件的字节级扫描仍 OPEN。

本次是目录、身份、版本与 CI 的全账号复核，并对 PgPool 做了独立本地真实服务复跑；它没有逐函数重审其他 111 个软件仓、重新安装所有公开附件、鉴定全部历史权利或完成此前被中断的 12 个较大项目完整深审。早期八项具体程序观察已有[ArchiveLens v1.0.4/v1.0.6、BranchLoom v0.2.1 和 TabWeave v4.3.1 的限定修复记录](PUBLIC_114_CURRENT_STATUS_20261006.md)；这些定向结果不等于整仓无缺陷。

[Anthropic 当前公开 CVP 说明](https://support.claude.com/en/articles/14604842-real-time-cyber-safeguards-on-claude-opus-and-sonnet)关注真实合法的高风险双用途防御任务及所受防护影响。官方没有规定 30 个仓库或逐仓拒绝日志为硬门槛；Claude.ai / Claude Code 使用第一方申请路径。21 个版本是工程计数，**不是 21 个官方合格案例**。申请人的实际授权任务、账号/组织、相关防护影响与批准状态均为 **OPEN**，见[待补事实表](APPLICATION_EVIDENCE_OPEN.md)。
