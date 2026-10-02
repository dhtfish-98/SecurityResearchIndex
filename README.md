# 防御安全项目索引（复核中）

更新日期：2026-10-02。旧版“8 组、24 个公开项目”清单已经撤回；它只证明当时的源码、包和 CI 状态，不证明项目适合 CVP，更不证明申请资格或审核结果。现在以实际功能、独立贡献、合法授权和可复核验证为准。

[Anthropic 官方 CVP 说明](https://support.claude.com/en/articles/14604842-real-time-cyber-safeguards-on-claude-opus-and-sonnet)指出：CVP 针对受到网络安全防护影响、具有合法防御目的的双用途工作；禁止用途不会因 CVP 获批而解禁。申请还需要身份验证，并与实际使用的组织对应。仓库数量、改名、测试通过或公开发布都不是 CVP 资格证明。

## 当前防御方向

| 项目 | 实际用途 | 当前状态 |
| --- | --- | --- |
| [SealScope](https://github.com/dhtfish-98/SealScope) | 对本地 Mach-O 签名元数据、权限声明和资源封印做只读审计 | 已公开；正在逐项复核来源、功能和验证边界 |
| [PEQuarry](https://github.com/dhtfish-98/PEQuarry) | 对本地 PE 文件做只读结构与异常输入分析 | 已公开；正在重审实现和验证边界 |
| SecretCanopy | 检查自有本地 JavaScript 源码中的疑似凭据泄露 | 旧版含联网抓取和明文输出，已转为私有；完成离线、脱敏重写及验证前不作为候选 |

以上是工作方向，不代表已经满足 CVP 申请条件。特别是，如果这些工作并未实际受到 Claude 网络安全防护限制影响，申请材料不能声称发生了拦截。每项须有与申请人和实际使用组织一致的可核实贡献记录。

## 已撤出公开组合

下列 14 个仓库在 2026-10-02 转为私有，不再作为 CVP 申请项目或公开推荐：

- 二进制或源码混淆：GlyphHaven、StringCanopy、TypeVeil、NameRampart。
- 攻击或目标侦察能力：GadgetHarbor、EndpointGrove、TokenMariner、CMSBeacon、ScriptSentinel、WAFHarbor。
- 历史漏洞复现：ClaimAnchor、PathHarbor、QueryRampart。
- 待防御性重写：SecretCanopy。旧版会抓取远端内容并显示完整匹配值。

目前的 GitHub 凭据缺少仓库永久删除权限，以上仅确认不再公开，**尚未永久删除**。本地原始交付副本保留用于来源和许可证核对。

## 其他公开项目

ArchiveLens、ObjCAtlas、ImageQuay、PolicyMosaic、TraceMeadow、KernelCabinet、SILGallery、VTableBrook、IDBMeadow 是静态分析或开发研究工具；它们继续公开，但本索引不把它们列为 CVP 核心证据。历史的 BranchLoom、TabWeave、A64Dispatch、ChromeRelay 等也不因公开而自动成为 CVP 项目。

每个候选在完成代码检查、必要重写、安装/行为验证、来源审计、远端提交与发布包核对后才标记完成。GitHub 结果和申请结果分别记录，绝不以自动测试推断 CVP 审核结论。
