# 116 个公开仓续审：Landlock 正式发行后

**冻结点：2026-10-05 23:18:57 UTC，非原子读取。**[逐仓矩阵](PUBLIC_116_POST_LANDLOCK_METADATA_20261006.json)重新读取账号下全部公开仓的 HEAD 和最新 Release；与前一轮 115 仓矩阵相比，新增 LandlockFilesystemGate，索引仓自身从 v1.0.0 前进到 v1.0.1，其余 114 仓的 HEAD 与最新版本未变。未变仓沿用其原提交的树、标签、CI 明细；这不是 113 个软件仓的全量代码语义重审。

| 项目 | 冻结结果 |
| --- | --- |
| 公开仓 | 116：113 软件、3 资料或索引 |
| 当前 HEAD 作者／提交者账号关联 | 116/116 为 `dhtfish-98`；只核对当前提交，不代替历史权利鉴定 |
| 软件最新正式 Release 与所读 HEAD | 113/113 同提交 |
| 软件当前 HEAD 的主线 CI | 113/113 成功；91 仓另有同提交标签 CI，22 仓只配置主线触发 |
| 文档与构建目录 | 116/116 有「项目文档」；114 仓的 `Build` 仅跟踪 `.gitignore`，LandlockFilesystemGate 和 PgPoolPrincipalIsolation 由忽略规则／构建配置在运行时创建 Build |
| 当前跟踪树的已识别编译路径 | 0；对所有无扩展名文件的逐字节识别仍 OPEN |
| 第三批固定 30 题 | **22/30 正式发行，8 项待完成**；这不是官方 CVP 合格项目数 |

[LandlockFilesystemGate v0.1.0](https://github.com/dhtfish-98/LandlockFilesystemGate/releases/tag/v0.1.0) 对应 `348621ed20c22fdb0792f8cedf9fe521e1ea6ea0`。真实 Linux 内核上的[主线 CI](https://github.com/dhtfish-98/LandlockFilesystemGate/actions/runs/37387227822)及[标签 CI](https://github.com/dhtfish-98/LandlockFilesystemGate/actions/runs/37387342144)都对源码检出和解包源码返回 PASS，报告 Landlock ABI 7、静态 ELF、允许与拒绝操作、子进程继承限制和拒绝区文件未变。本地 macOS/Alpine VM 另有独立实验。正式附件回下载后，源码包 SHA-256 为 `7d9e0234d8ff4e5ba681c4b18e63e17ec0aea193c51d8f910a130518f5f669c1`；包内 20 个文件与 Git 提交及中央源码／文档逐字节一致，详见[发行回执](LANDLOCK_V0_1_0_RELEASE_20261006.json)。最初两次主线 CI 失败仍保留：第二次揭示 `open(O_CREAT)` 缺创建模式，修复后才发行。它是自有进程的防御实验，不声称上游 rust-landlock 漏洞；原作者及双许可证保留。

本索引仓 [v1.0.1](https://github.com/dhtfish-98/SecurityResearchIndex/releases/tag/v1.0.1) 的公开主线、注释标签与六个附件也已核验，其发行发生在上一轮 115 仓读取之后。它是资料仓，没有程序 CI。本报告写入后索引仓 HEAD 还会随自身下一次发行前进，故上表的索引行只代表读取时的 v1.0.1。

此前九项待发行候选的冻结复核保留 21/30 时点；Landlock 发行后这九项中仍有八项未发行。HeadscaleEnrollmentGate 有本地修复与独立复核，尚待公开主线、CI 和版本；另七项按各自真实环境门槛继续推进。另一活跃对话负责的 FederatedConnectorIdentityGate 与 PEQuarry 不属于这八项，本轮未并行改动。Federated 的公开文档状态矛盾仍待其负责对话修正。

申请渠道按用户说明为 Claude.ai / Claude Code。当前[官方 CVP 说明](https://support.claude.com/en/articles/14604842-real-time-cyber-safeguards-on-claude-opus-and-sonnet)没有“30 个 GitHub 仓”或逐项目拒绝记录的硬门槛。真实合法任务、保障措施影响、申请账号与组织条件及官方批准仍 **OPEN**；仓库数量、作者字段、CI 和 Release 只证明各自限定的工程事实。真实第三方版权和许可证不能因本项目重写而删除。
