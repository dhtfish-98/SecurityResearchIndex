# 防御安全项目索引

更新日期：2026-10-02。旧版“8 组、24 个公开项目”清单已经撤回；它只证明当时的源码、包和 CI 状态，不证明项目适合 CVP，更不证明申请资格或审核结果。现在以实际功能、独立贡献、合法授权和可复核验证为准。

[Anthropic 官方 CVP 说明](https://support.claude.com/en/articles/14604842-real-time-cyber-safeguards-on-claude-opus-and-sonnet)指出：CVP 针对受到网络安全防护影响、具有合法防御目的的双用途工作；禁止用途不会因 CVP 获批而解禁。申请还需要身份验证，并与实际使用的组织对应。仓库数量、改名、测试通过或公开发布都不是 CVP 资格证明。

逐条规则与证据状态见 [CVP_RULES_AND_EVIDENCE_20261002.md](CVP_RULES_AND_EVIDENCE_20261002.md)。

## 14 项替补防御项目

原公开组合撤出的 14 个仓库均保留私有；下表 14 项是另建的防御项目，其中两项在本次补齐前已完成，另 12 项是本次新增。每项均有单独源码、来源说明、功能测试、边界说明和 GitHub 自动测试。

| 项目 | 实际用途 | 工程核查 |
| --- | --- | --- |
| [LocalSecretReview](https://github.com/dhtfish-98/LocalSecretReview) | 本地源码凭据形态检查，输出位置和规则，不输出匹配值 | 独立新实现；4 项测试、独立 wheel 安装与合成值脱敏检查；[`d8e2adc8` 对应 CI 成功](https://github.com/dhtfish-98/LocalSecretReview/actions/runs/36958515545) |
| [PEHardeningReview](https://github.com/dhtfish-98/PEHardeningReview) | 本地 PE 文件加固声明位只读检查 | 独立新实现；4 项测试、独立 wheel 安装与 PE32/PE32+ 样本检查；[`1a3e5485` 对应 CI 成功](https://github.com/dhtfish-98/PEHardeningReview/actions/runs/36958531631) |
| [IAMScopeReview](https://github.com/dhtfish-98/IAMScopeReview) | 本地 AWS IAM 策略的宽权限声明检查 | 独立新实现；4 项本地测试、命令行合成输入检查；[`e9b33a52` 对应 CI 成功](https://github.com/dhtfish-98/IAMScopeReview/actions/runs/36959756905) |
| [ContainerfileReview](https://github.com/dhtfish-98/ContainerfileReview) | 本地 Dockerfile 的基础镜像、远程 ADD 和最终用户检查 | 独立新实现；4 项本地测试、命令行合成输入检查；[`a827c69e` 对应 CI 成功](https://github.com/dhtfish-98/ContainerfileReview/actions/runs/36959784288) |
| [WorkflowPermissionReview](https://github.com/dhtfish-98/WorkflowPermissionReview) | 本地 GitHub Actions 工作流令牌权限与触发器检查 | 独立新实现；4 项本地测试、命令行合成输入检查；[`76f19240` 对应 CI 成功](https://github.com/dhtfish-98/WorkflowPermissionReview/actions/runs/36959791948) |
| [HeaderPolicyReview](https://github.com/dhtfish-98/HeaderPolicyReview) | 本地 HAR 中 HTTPS/HTML 安全响应头声明检查 | 独立新实现；4 项本地测试、命令行合成输入检查；[`6862447d` 对应 CI 成功](https://github.com/dhtfish-98/HeaderPolicyReview/actions/runs/36959971283) |
| [SBOMFieldReview](https://github.com/dhtfish-98/SBOMFieldReview) | 本地 CycloneDX JSON 的组件字段与依赖引用检查 | 独立新实现；5 项本地测试、命令行合成输入检查；[`daecd73b` 对应 CI 成功](https://github.com/dhtfish-98/SBOMFieldReview/actions/runs/36959973426) |
| [DependencyPinReview](https://github.com/dhtfish-98/DependencyPinReview) | 本地 pip requirements 的直接依赖锁定提示 | 独立新实现；4 项本地测试、命令行合成输入检查；[`1f19613d` 对应 CI 成功](https://github.com/dhtfish-98/DependencyPinReview/actions/runs/36959968772) |
| [EntitlementFlagReview](https://github.com/dhtfish-98/EntitlementFlagReview) | 本地 Apple entitlements plist 的安全敏感声明检查 | 独立新实现；4 项本地测试、XML/二进制 plist 与命令行检查；[`bbbfa77c` 对应 CI 成功](https://github.com/dhtfish-98/EntitlementFlagReview/actions/runs/36959825321) |
| [SSHPolicyReview](https://github.com/dhtfish-98/SSHPolicyReview) | 本地 sshd_config 中显式全局设置检查 | 独立新实现；4 项本地测试、命令行合成输入检查；[`9ab591c4` 对应 CI 成功](https://github.com/dhtfish-98/SSHPolicyReview/actions/runs/36959832514) |
| [KubePodReview](https://github.com/dhtfish-98/KubePodReview) | 本地 Kubernetes 工作负载 JSON 的容器安全声明检查 | 独立新实现；4 项本地测试、命令行合成输入检查；[`c3b6f9f8` 对应 CI 成功](https://github.com/dhtfish-98/KubePodReview/actions/runs/36959842924) |
| [ArtifactDigestReview](https://github.com/dhtfish-98/ArtifactDigestReview) | 本地清单与文件 SHA-256 对照检查 | 独立新实现；4 项本地测试、命令行合成文件检查；[`678f0304` 对应 CI 成功](https://github.com/dhtfish-98/ArtifactDigestReview/actions/runs/36959852089) |
| [AuthLogReview](https://github.com/dhtfish-98/AuthLogReview) | 本地规范化认证事件的失败频次检查，隐藏身份字段 | 独立新实现；4 项本地测试、命令行合成日志检查；[`c0277d91` 对应 CI 成功](https://github.com/dhtfish-98/AuthLogReview/actions/runs/36959860264) |
| [FileModeReview](https://github.com/dhtfish-98/FileModeReview) | 本地文件权限元数据检查，不读取文件内容 | 独立新实现；4 项本地测试、命令行合成目录检查；[`bebb1ec7` 对应 CI 成功](https://github.com/dhtfish-98/FileModeReview/actions/runs/36959870958) |

这些工具只处理本地、获授权的输入；检测结果是复核提示，不证明漏洞、凭据有效性或生产环境保护状态。14 项工程核查完成不等于 CVP 申请资格成立。如果没有与实际申请人和组织一致的、确实受到 Claude 网络安全防护影响的合法防御任务记录，就不能在申请中声称发生了拦截。

## 已撤出公开组合

下列 14 个仓库在 2026-10-02 转为私有，不再作为 CVP 申请项目或公开推荐：

- 二进制或源码混淆：GlyphHaven、StringCanopy、TypeVeil、NameRampart。
- 攻击或目标侦察能力：GadgetHarbor、EndpointGrove、TokenMariner、CMSBeacon、ScriptSentinel、WAFHarbor。
- 历史漏洞复现：ClaimAnchor、PathHarbor、QueryRampart。
- 旧版 SecretCanopy：会抓取远端内容并显示完整匹配值；新的 LocalSecretReview 是另建的离线项目，不复用旧版源码。

按用户当前决定，这 14 个仓库保留为私有，**不永久删除**。本地原始交付副本也保留用于来源和许可证核对。

## 其他公开项目

ArchiveLens、ObjCAtlas、ImageQuay、PolicyMosaic、TraceMeadow、KernelCabinet、SILGallery、VTableBrook、IDBMeadow、PEQuarry 是静态分析或开发研究工具；它们继续公开，但本索引不把它们列为 CVP 核心证据。[SealScope](https://github.com/dhtfish-98/SealScope) 是现有的只读 Mach-O 审计工具，也只作为相关工作背景。历史的 BranchLoom、TabWeave、A64Dispatch、ChromeRelay 等也不因公开而自动成为 CVP 项目。

14 项替补项目的代码、说明、来源和自动测试已按各自 `VALIDATION.md` 核查，公开仓库与对应提交的 CI 已核对。其中两项还完成了独立 wheel 安装检查。尚无这些任务受到 Claude 防护拦截的记录，也未核实与申请组织的对应关系；因此这里只能标记项目工程检查完成，不能标记 CVP 申请条件完成。GitHub 结果和申请结果分别记录，绝不以自动测试推断 CVP 审核结论。
