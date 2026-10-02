# 防御安全项目索引

更新日期：2026-10-02。旧版“8 组、24 个公开项目”清单已经撤回；它只证明当时的源码、包和 CI 状态，不证明项目适合 CVP，更不证明申请资格或审核结果。现在以实际功能、独立贡献、合法授权和可复核验证为准。

[Anthropic 官方 CVP 说明](https://support.claude.com/en/articles/14604842-real-time-cyber-safeguards-on-claude-opus-and-sonnet)指出：CVP 针对受到网络安全防护影响、具有合法防御目的的双用途工作；禁止用途不会因 CVP 获批而解禁。申请还需要身份验证，并与实际使用的组织对应。仓库数量、改名、测试通过或公开发布都不是 CVP 资格证明。

逐条规则与证据状态见 [CVP_RULES_AND_EVIDENCE_20261002.md](CVP_RULES_AND_EVIDENCE_20261002.md)。

## 14 项替补防御项目

原公开组合撤出的 14 个仓库均保留私有；下表 14 项是另建的防御项目。本轮完整源码复核修正了已确认的输入处理和漏检问题，当前共 101 项本地测试通过，14 个公开最新提交均有对应的成功 CI。具体问题、修正及边界见 [源码复核记录](SOURCE_REVIEW_20261002.md)。

| 项目 | 实际用途 | 当前工程证据 |
| --- | --- | --- |
| [LocalSecretReview](https://github.com/dhtfish-98/LocalSecretReview) | 本地源码凭据形态检查，仅报告位置；不完整检查明确报错 | 7 项本地测试及 CLI 检查；1.0.1 wheel 独立安装检查；[`31c20173` 对应 CI 成功](https://github.com/dhtfish-98/LocalSecretReview/actions/runs/36962272270) |
| [PEHardeningReview](https://github.com/dhtfish-98/PEHardeningReview) | 本地 PE 文件加固声明位和受限读取检查 | 6 项本地测试及 CLI 检查；1.0.1 wheel 独立安装检查；[`b6bdac35` 对应 CI 成功](https://github.com/dhtfish-98/PEHardeningReview/actions/runs/36962275907) |
| [IAMScopeReview](https://github.com/dhtfish-98/IAMScopeReview) | 本地 IAM 宽权限、补集声明及选定字段检查 | 8 项本地测试及 CLI 检查；[`9bd850f3` 对应 CI 成功](https://github.com/dhtfish-98/IAMScopeReview/actions/runs/36962279586) |
| [ContainerfileReview](https://github.com/dhtfish-98/ContainerfileReview) | 本地 Dockerfile 镜像摘要、阶段继承和最终用户检查 | 8 项本地测试及 CLI 检查；[`e3bdc360` 对应 CI 成功](https://github.com/dhtfish-98/ContainerfileReview/actions/runs/36962283218) |
| [WorkflowPermissionReview](https://github.com/dhtfish-98/WorkflowPermissionReview) | 本地 GitHub Actions 触发器、令牌权限及重复键检查 | 7 项本地测试及 CLI 检查；[`cb7f74f9` 对应 CI 成功](https://github.com/dhtfish-98/WorkflowPermissionReview/actions/runs/36962287101) |
| [HeaderPolicyReview](https://github.com/dhtfish-98/HeaderPolicyReview) | 本地 HAR 安全响应头、重复声明和 HTML MIME 检查 | 8 项本地测试及 CLI 检查；[`e66139f8` 对应 CI 成功](https://github.com/dhtfish-98/HeaderPolicyReview/actions/runs/36962290931) |
| [SBOMFieldReview](https://github.com/dhtfish-98/SBOMFieldReview) | 本地 CycloneDX 根组件、嵌套组件及依赖引用检查 | 8 项本地测试及 CLI 检查；[`dff819a6` 对应 CI 成功](https://github.com/dhtfish-98/SBOMFieldReview/actions/runs/36962294605) |
| [DependencyPinReview](https://github.com/dhtfish-98/DependencyPinReview) | 本地直接依赖规范、精确版本、通配符与来源提示 | 7 项本地测试及 CLI 检查；[`c06cc7f3` 对应 CI 成功](https://github.com/dhtfish-98/DependencyPinReview/actions/runs/36962298115) |
| [EntitlementFlagReview](https://github.com/dhtfish-98/EntitlementFlagReview) | 本地 Apple plist 安全字段类型、重复键和声明检查 | 6 项本地测试及 CLI 检查；[`f25d7ae0` 对应 CI 成功](https://github.com/dhtfish-98/EntitlementFlagReview/actions/runs/36962302027) |
| [SSHPolicyReview](https://github.com/dhtfish-98/SSHPolicyReview) | 本地 SSH 设置、引号及未解析 Include/Match 提示 | 7 项本地测试及 CLI 检查；[`0ad5c5fb` 对应 CI 成功](https://github.com/dhtfish-98/SSHPolicyReview/actions/runs/36962305980) |
| [KubePodReview](https://github.com/dhtfish-98/KubePodReview) | 本地工作负载全部三类容器的安全声明检查 | 9 项本地测试及 CLI 检查；[`80ec45af` 对应 CI 成功](https://github.com/dhtfish-98/KubePodReview/actions/runs/36962309222) |
| [ArtifactDigestReview](https://github.com/dhtfish-98/ArtifactDigestReview) | 本地清单与受限读取文件的 SHA-256 对照检查 | 7 项本地测试及 CLI 检查；[`df755ffe` 对应 CI 成功](https://github.com/dhtfish-98/ArtifactDigestReview/actions/runs/36962312258) |
| [AuthLogReview](https://github.com/dhtfish-98/AuthLogReview) | 本地认证失败频次检查，以原文件行号定位并隐藏身份 | 8 项本地测试及 CLI 检查；[`7ad0e361` 对应 CI 成功](https://github.com/dhtfish-98/AuthLogReview/actions/runs/36962315981) |
| [FileModeReview](https://github.com/dhtfish-98/FileModeReview) | 本地文件权限位和敏感名称检查，不读取文件内容 | 5 项本地测试及 CLI 检查；[`289a3cc1` 对应 CI 成功](https://github.com/dhtfish-98/FileModeReview/actions/runs/36962319942) |

这些结果仅证明已记录范围的工程行为。CVP 适用性仍需申请人真实、合法且受到防护影响的双用途任务，以及相符的身份和组织信息。静态检查工具、仓库数量及自动测试不能替代这些申请事实。

## 已撤出公开组合

下列 14 个仓库在 2026-10-02 转为私有，不再作为 CVP 申请项目或公开推荐：

- 二进制或源码混淆：GlyphHaven、StringCanopy、TypeVeil、NameRampart。
- 攻击或目标侦察能力：GadgetHarbor、EndpointGrove、TokenMariner、CMSBeacon、ScriptSentinel、WAFHarbor。
- 历史漏洞复现：ClaimAnchor、PathHarbor、QueryRampart。
- 旧版 SecretCanopy：会抓取远端内容并显示完整匹配值；新的 LocalSecretReview 是另建的离线项目，不复用旧版源码。

按用户当前决定，这 14 个仓库保留为私有，**不永久删除**。本地原始交付副本也保留用于来源和许可证核对。

## 其他公开项目

ArchiveLens、ObjCAtlas、ImageQuay、PolicyMosaic、TraceMeadow、KernelCabinet、SILGallery、VTableBrook、IDBMeadow、PEQuarry 继续公开。本轮已逐项核对实际能力、来源和许可证，已有 8 项发布具体运行时或入口改写，包含 VTableBrook 全部运行时 C 文件及共享头的有界重写，以及 ImageQuay、PolicyMosaic、TraceMeadow、PEQuarry 的有限解析和输出等实改；固定发布提交均有相符的成功 CI。尚继承的核心算法继续迭代，完整项目重写仍 OPEN。具体修改、历史软件包及仍未完成的边界见 [保留项目复核记录](RETAINED_PROJECT_REVIEW_20261002.md)。这些工具包含各自声明的输出、编辑、脚本或外部助手能力，不能统一描述为纯只读项目。[SealScope](https://github.com/dhtfish-98/SealScope) 是现有的只读 Mach-O 审计工具，也只作为相关工作背景。历史的 BranchLoom、TabWeave、A64Dispatch、ChromeRelay 等也不因公开而自动成为 CVP 项目。

14 项替补项目的代码、说明、来源和自动测试已按各自 `VALIDATION.md` 核查，公开仓库与对应提交的 CI 已核对。其中两项还完成了独立 wheel 安装检查。对本次申请，仍未核实与实际模型、渠道、申请人和组织一致的原始受限任务记录；因此这里只能标记项目工程检查完成，不能标记 CVP 申请条件完成。GitHub 结果和申请结果分别记录，绝不以自动测试推断 CVP 审核结论。
