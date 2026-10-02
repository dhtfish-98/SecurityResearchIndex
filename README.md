# 防御安全项目索引

更新日期：2026-10-02。旧版“8 组、24 个公开项目”清单已经撤回；它只证明当时的源码、包和 CI 状态，不证明项目适合 CVP，更不证明申请资格或审核结果。现在以实际功能、独立贡献、合法授权和可复核验证为准。

[Anthropic 官方 CVP 说明](https://support.claude.com/en/articles/14604842-real-time-cyber-safeguards-on-claude-opus-and-sonnet)指出：CVP 针对受到网络安全防护影响、具有合法防御目的的双用途工作；禁止用途不会因 CVP 获批而解禁。申请还需要身份验证，并与实际使用的组织对应。仓库数量、改名、测试通过或公开发布都不是 CVP 资格证明。

逐条规则与证据状态见 [CVP_RULES_AND_EVIDENCE_20261002.md](CVP_RULES_AND_EVIDENCE_20261002.md)。

## 新的防御项目

| 项目 | 实际用途 | 当前状态 |
| --- | --- | --- |
| [LocalSecretReview](https://github.com/dhtfish-98/LocalSecretReview) | 对自有本地源码进行离线凭据形态检查，只输出位置和规则，不输出匹配值 | 独立新实现；4 项本地测试、独立 wheel 安装检查与[提交 `d8e2adc` 的 CI](https://github.com/dhtfish-98/LocalSecretReview/actions/runs/36958515545)通过 |
| [PEHardeningReview](https://github.com/dhtfish-98/PEHardeningReview) | 只读解析本地 PE 文件的加固声明位 | 独立新实现；4 项本地测试、两种本地 PE 样本、独立 wheel 安装检查与[提交 `1a3e548` 的 CI](https://github.com/dhtfish-98/PEHardeningReview/actions/runs/36958531631)通过 |

以上是工作方向，不代表已经满足 CVP 申请条件。特别是，如果这些工作并未实际受到 Claude 网络安全防护限制影响，申请材料不能声称发生了拦截。每项须有与申请人和实际使用组织一致的可核实贡献记录。

## 已撤出公开组合

下列 14 个仓库在 2026-10-02 转为私有，不再作为 CVP 申请项目或公开推荐：

- 二进制或源码混淆：GlyphHaven、StringCanopy、TypeVeil、NameRampart。
- 攻击或目标侦察能力：GadgetHarbor、EndpointGrove、TokenMariner、CMSBeacon、ScriptSentinel、WAFHarbor。
- 历史漏洞复现：ClaimAnchor、PathHarbor、QueryRampart。
- 旧版 SecretCanopy：会抓取远端内容并显示完整匹配值；新的 LocalSecretReview 是另建的离线项目，不复用旧版源码。

目前的 GitHub 凭据缺少仓库永久删除权限，以上仅确认不再公开，**尚未永久删除**。本地原始交付副本保留用于来源和许可证核对。

## 其他公开项目

ArchiveLens、ObjCAtlas、ImageQuay、PolicyMosaic、TraceMeadow、KernelCabinet、SILGallery、VTableBrook、IDBMeadow、PEQuarry 是静态分析或开发研究工具；它们继续公开，但本索引不把它们列为 CVP 核心证据。[SealScope](https://github.com/dhtfish-98/SealScope) 是现有的只读 Mach-O 审计工具，也只作为相关工作背景。历史的 BranchLoom、TabWeave、A64Dispatch、ChromeRelay 等也不因公开而自动成为 CVP 项目。

两项新项目的代码、说明、来源、安装和自动测试已按各自 `VALIDATION.md` 核查，公开仓库与对应提交的 CI 已核对。尚无这两项任务受到 Claude 防护拦截的记录，也未核实与申请组织的对应关系；因此这里只能标记项目工程检查完成，不能标记 CVP 申请条件完成。GitHub 结果和申请结果分别记录，绝不以自动测试推断 CVP 审核结论。
