# 115 个公开仓的 CVP 申请材料只读分层复核

复核截止：2026-10-05 22:58 UTC。只读核对；未改源码、仓库或 GitHub，未重跑测试。本页是申请材料真实性与有限代码/测试抽样，不是 115 仓完整代码审计或官方资格判断。

## 基准与覆盖

- 基准索引：[旧基准报告](PUBLIC_115_CURRENT_STATUS_20261006.md)，SHA-256 `5d11bdf8fe7e5918cae2c4b5a6774704bbdbfccb0ebfd69f5940da285f2cf231`；读取窗口 2026-10-05 22:23:29–22:24:14 UTC，非原子。
- 115 行矩阵：`PUBLIC_115_CURRENT_METADATA_20261006.json`，SHA-256 `303ca5de2a79e0823ebfa60e79321617c1061e63f482306318e133ff12ba488c`。矩阵报告 112 软件、3 资料/索引；第三批固定 30 项中 21 项正式发行、9 项待定。复核期间单独从 GitHub 读取第三批 21 个已发行仓 `main`，21/21 仍等于矩阵中的精确 HEAD。矩阵不是 22:55 UTC 的全账号新快照：ImageQuay 此后已有新发行，见下文。
- 独立读取 21 个已发行仓在该 HEAD 的常见公开材料文件（README、DESIGN、VALIDATION、RELEASE_NOTES、CVP_STATUS、ORIGIN、THIRD_PARTY，存在时），并读其当前提交信息及最新 Release 正文；没有发现声称获 CVP 批准的明确语句，也没有发现 Codex/OpenAI/AI 代码作者署名。该词项抽样不覆盖全部源码、Git 历史、二进制字节、非抽样文档或实际创作过程。
- 对 PgPoolPrincipalIsolation、QuicEarlyDataPolicy、FederatedConnectorIdentityGate、DexInvokeEvidence、CapabilityRuleEval、ObfuscatedStringRecovery 的代表性测试文件，计算本地 Git blob SHA-1 并与其公开精确提交的 GitHub blob SHA-1 比较，6/6 相同；阅读了断言与实验范围。没有重新运行服务、编译器、CI 或正式附件。

## P1：公开 FederatedConnectorIdentityGate 发行状态与自身文档矛盾

当前公开 `main` 与 `v0.1.0` 标签均指向 `7c589130ec3bc8216f61738a3c6c8b5d23cd28dc`。正式 [Release](https://github.com/dhtfish-98/FederatedConnectorIdentityGate/releases/tag/v0.1.0) 于 2026-10-05 21:32:37 UTC 发布；同一 SHA 的 [main CI](https://github.com/dhtfish-98/FederatedConnectorIdentityGate/actions/runs/37373188926) 与 [标签 CI](https://github.com/dhtfish-98/FederatedConnectorIdentityGate/actions/runs/37373188944) 均成功。GitHub API 当前列出源码包摘要 `sha256:62a95409f59bfd002e698af60dc9384af60c00deebb1660b0b2bb5e1bfcb180d`、`SHA256SUMS` 摘要 `sha256:057e30349799b7ac7d2d273986c6d2be365eea07deb39a97b2675ef329fca146`。本轮没有自行回下载附件核对字节。

但该精确公开提交的 [`项目文档/README.md:3`](https://github.com/dhtfish-98/FederatedConnectorIdentityGate/blob/7c589130ec3bc8216f61738a3c6c8b5d23cd28dc/%E9%A1%B9%E7%9B%AE%E6%96%87%E6%A1%A3/README.md#L3) 仍称远端发布 OPEN；[`DESIGN.md:3`](https://github.com/dhtfish-98/FederatedConnectorIdentityGate/blob/7c589130ec3bc8216f61738a3c6c8b5d23cd28dc/%E9%A1%B9%E7%9B%AE%E6%96%87%E6%A1%A3/DESIGN.md#L3) 称 public CI OPEN 且没有公开仓；[`VALIDATION.md:9`](https://github.com/dhtfish-98/FederatedConnectorIdentityGate/blob/7c589130ec3bc8216f61738a3c6c8b5d23cd28dc/%E9%A1%B9%E7%9B%AE%E6%96%87%E6%A1%A3/VALIDATION.md#L9) 把精确 CI、正式发行及附件核验继续列为 OPEN。应由该仓负责对话以新版本或明确勘误同步这三处事实，保留本地实验范围和 CVP 资格 OPEN；不要把本轮未做的附件回下载写成独立复核通过。

供负责对话使用的事实修正文案：`v0.1.0 was published on 2026-10-05 at commit 7c589130ec3bc8216f61738a3c6c8b5d23cd28dc. The main and v0.1.0 tag workflows for that commit succeeded. GitHub lists the source archive and SHA256SUMS with published SHA-256 digests. Local live validation passed in its recorded environment. Production use, a real authorized defensive task, safeguard impact, CVP eligibility and provider approval remain OPEN.` 若要写“附件回下载一致”，须引用并独立核对对应发行收据，不能由本次 GitHub 元数据读取推出。

并行冲突：Codex 对话 `筛选并重写30个CVP防御项目`（`01a0fb46-6335-7683-9644-1f8eaccb4fa3`）仍 active，现行 turn 包含 FederatedConnectorIdentityGate 的源码、CI、标签和发布工作。因此本复核没有创建该仓修改候选。

## P1：申请事实与代码归属仍待单独证明

官方[当前 CVP 说明](https://support.claude.com/en/articles/14604842-real-time-cyber-safeguards-on-claude-opus-and-sonnet)要求合法高风险双用途防御用途受到相关保障措施影响；第一方 Claude.ai/Claude Code 经 Verification Portal，需身份核验，入口只对授权管理员可见。其当前模型范围还特别排除 Opus 5.5 和 Sonnet 5.5，计划以后扩展。仓库数量、CI、公开 Release、提交账号映射均不能替代实际授权任务、受影响情况、组织/身份和批准决定。`APPLICATION_EVIDENCE_OPEN.md` 对这些事实逐项仍标 OPEN。第三批 21 个 Release 应称工程交付或有条件技术附件，不能称 21 个官方合格案例。

115 矩阵的 `115/115` 当前 HEAD 作者/提交者 GitHub 账号关联只核对提交元数据，不证明全部实际创作者或历史权利。此前 113 仓报告记录过 13 个当时 HEAD 的错误账号关联，后续新提交修正了当前映射；旧提交和旧标签仍保留历史事实。若申请文本声称“全部源码完全自主重写”或“所有历史提交均由 dhtfish98 创作”，证据不足。已有 12 个研究/派生背景仓须明确保留上游归属，例如 ImageQuay 来源 ktool、KernelCabinet 来源 kextract、ArchiveLens 来源 REipa、ObjCAtlas 来源 class-dump；这些仓的 ORIGIN 文档明确承认派生关系与 MIT/GPL 权利。应逐仓将新写模块、继承算法、分发的第三方内容分开，不能凭改名或当前提交元数据重归属。

## P2：工程证据强度与剩余边界

- PgPoolPrincipalIsolation 的公开测试文件确实启动 PostgreSQL/PgCat，断言自造弱池泄露合成标记、门禁拒绝错配连接及真实服务身份；README 明确弱池不是 PgCat 漏洞。QuicEarlyDataPolicy 的测试要求观察 QUIC 0-RTT 包、弱基线重复状态变更和受控策略拒绝；文档明确不声称字节相同的 UDP 密文重放。FederatedConnectorIdentityGate 的 live test 要求固定 Dex 可执行文件，缺少时会失败，测试真实签名令牌和跨身份拒绝。这三项有可核对的真实本地服务/协议断言，但生产部署、真实授权任务和 CVP 影响仍 OPEN。
- DexInvokeEvidence 使用自写 Java 样本与 JDK/Android SDK 工具比较静态调用点；CapabilityRuleEval 仅编译无害对象文件并作文件级特征规则判断；ObfuscatedStringRecovery 用自写 ELF 对象恢复有限的堆栈字符串。它们文档均限定为合成或文件级证据，不证明真实外部样本中的漏洞、执行可达性、检测率或 CVP 资格。其余 15 个已发行项目本轮仅核材料与元数据，没有逐函数或独立重跑。
- 第三批剩余 9 个题目（BuildSecretMountLifetimeGate、ContainerCapabilityDropGate、CsiSecretNamespaceGate、HeadscaleEnrollmentGate、LandlockFilesystemGate、RemoteDesktopTransferGate、RootlessIdMapBoundary、WireGuardPeerPrefixBinding、XlmFormulaTrace）在冻结矩阵中均无正式版；不得与另一历史 30 项相加为官方合格项目数。Headscale/Landlock 的候选由其他对话处理，本轮未触碰。
- 22:23–22:24 UTC 的 115 仓旧基准中，ImageQuay 跟踪了 `checks/bins/testbin1`、`testbin1.fat`、`testbin1.signed`、`testlib1.dylib` 四个已编译测试夹具。随后 [ImageQuay v1.0.9](https://github.com/dhtfish-98/ImageQuay/releases/tag/v1.0.9) 于 22:50:36 UTC 正式发行，当前 `main` 为 `a1089c4f2b1b360dc7f017121dc8c6aef667b536`。[ImageQuay 发行收据](IMAGEQUAY_V1_0_9_RELEASE_20261006.json) 记录该提交的主线/标签 CI 成功、四个正式附件回下载相同、97 个跟踪文件和当前包内均无上述编译夹具；本轮从 GitHub 重新核对了 `main` 与最新 Release。旧基准问题已在新版本关闭，历史发行附件可仍含这些夹具。无扩展名文件的全账号字节级识别及 12 个较大派生仓的完整代码/权利深审仍 OPEN。

## 建议的申请材料口径

只从与申请人真实授权工作相符的少数仓选精确版本、功能边界和可复现实验作为技术附件。把自造弱基线明确标为实验对照，把第三方源码与依赖按原许可证和版权归属陈述，把公开版本与实际申请事实分开。没有证据时写 OPEN；不要补造上游漏洞、生产影响、保障措施拦截或审批结果。
