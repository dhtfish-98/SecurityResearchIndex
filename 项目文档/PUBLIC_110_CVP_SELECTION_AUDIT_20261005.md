# 公开 110 仓 CVP 材料适配再审（2026-10-05 19:44–19:47 UTC 冻结）

按 [Anthropic 当前 CVP 官方说明](https://support.claude.com/en/articles/14604842-real-time-cyber-safeguards-on-claude-opus-and-sonnet)，这项申请针对**真实合法防御工作与高风险双用途防护相交、且受相关防护影响**的用途。Claude.ai / Claude Code 属第一方入口；公开说明列出 Verification Portal、授权管理员和身份验证，未列出逐仓原始拒绝日志、30 仓数量或仓库白名单。没有看到申请人的实际账号、任务与官方决定，因此下列所有仓的个人资格和批准状态均为 **OPEN**。

本轮把先前的工程审计、110 仓 GitHub 快照、精确提交文本/路径扫描和逐仓材料角色核到同一冻结表；这是**全量材料角色复核**，不是 110 仓逐函数语义安全审计。详见 [逐仓 110 行机器矩阵](PUBLIC_110_CVP_MATERIAL_RECHECK_20261005.json)、[远端元数据](PUBLIC_110_METADATA_20261005.json)、[文本与路径复核](PUBLIC_110_EXACT_HEAD_TEXT_PATH_AUDIT_20261005.json)。GitHub 读取分批完成，非原子快照；此页随之后的新提交不会自动更新。

| 当前材料角色 | 仓数 | 处置 |
| --- | ---: | --- |
| 已发行的本地技术实验 | 15 | 可作为有限功能附件；申请用途与受防护影响须另由真实事实支持。 |
| 旧批次条件技术案例 | 6 | 仅在功能与申请人的真实授权任务相符时使用；代码级再筛不是官方认定。 |
| 本地通过但未正式发行 | 1 | 不得计入已发行数；等同一提交的必需 CI 与正式附件回验。 |
| 普通防御工程附件 | 69 | 保留作工程能力背景；单凭仓库不能当作独立 CVP 用例。 |
| 研究或派生维护背景 | 12 | 核实具体来源和权利；不当作完全独立重写的主案例。 |
| 非主申请方向 | 4 | 移出主案例计数，可继续正常维护。 |
| 资料及账号仓 | 3 | 不计入软件项目数。 |

**当前可列入技术附件候选的是 15 项新本地实验及 6 项旧条件案例；它们均未由仓库证明 CVP 申请资格。** 一项 SSH 主机证书实验已公开源码但正式发行仍待 GitHub Actions，因此不计入已发行。其余 88 仓在当前材料中不作主案例：69 项工程附件、12 项研究/派生背景、4 项普通工具、3 项资料仓。代码或名称不能把这些自动改成合格用途；只有真实授权任务和功能证据相符时才重评。

## 已发行的本地技术实验（15）

可作为有限功能附件；申请用途与受防护影响须另由真实事实支持。

[AcmeChallengeAuthorization](https://github.com/dhtfish-98/AcmeChallengeAuthorization)、[GraphQLQueryCostGate](https://github.com/dhtfish-98/GraphQLQueryCostGate)、[JupyterKernelOriginGate](https://github.com/dhtfish-98/JupyterKernelOriginGate)、[NatsSubjectTenantGate](https://github.com/dhtfish-98/NatsSubjectTenantGate)、[PluginHandshakeTrustGate](https://github.com/dhtfish-98/PluginHandshakeTrustGate)、[ProxyIdentityHeaderTrust](https://github.com/dhtfish-98/ProxyIdentityHeaderTrust)。
[QuicEarlyDataPolicy](https://github.com/dhtfish-98/QuicEarlyDataPolicy)、[RecoveryCodeAccountBinding](https://github.com/dhtfish-98/RecoveryCodeAccountBinding)、[RedirectCredentialBoundary](https://github.com/dhtfish-98/RedirectCredentialBoundary)、[RefreshTokenReuseRevocation](https://github.com/dhtfish-98/RefreshTokenReuseRevocation)、[RelationAccessDecision](https://github.com/dhtfish-98/RelationAccessDecision)、[SftpHandlePermissionGate](https://github.com/dhtfish-98/SftpHandlePermissionGate)。
[SshCertIssuanceGate](https://github.com/dhtfish-98/SshCertIssuanceGate)、[WebSocketUpgradeOriginGate](https://github.com/dhtfish-98/WebSocketUpgradeOriginGate)、[XmlEntityResourceBoundary](https://github.com/dhtfish-98/XmlEntityResourceBoundary)。

## 旧批次条件技术案例（6）

仅在功能与申请人的真实授权任务相符时使用；代码级再筛不是官方认定。

[CITrustBoundaryReview](https://github.com/dhtfish-98/CITrustBoundaryReview)、[DeserializeCallReview](https://github.com/dhtfish-98/DeserializeCallReview)、[DOMSinkReview](https://github.com/dhtfish-98/DOMSinkReview)、[ModelOpcodeReview](https://github.com/dhtfish-98/ModelOpcodeReview)、[WheelNamespaceReview](https://github.com/dhtfish-98/WheelNamespaceReview)、[YaraRuleDraftReview](https://github.com/dhtfish-98/YaraRuleDraftReview)。

## 本地通过但未正式发行（1）

不得计入已发行数；等同一提交的必需 CI 与正式附件回验。

[SshHostCertTrustBoundary](https://github.com/dhtfish-98/SshHostCertTrustBoundary)。

## 普通防御工程附件（69）

保留作工程能力背景；单凭仓库不能当作独立 CVP 用例。

[AdvisoryOfflineReview](https://github.com/dhtfish-98/AdvisoryOfflineReview)、[AliasRecordReview](https://github.com/dhtfish-98/AliasRecordReview)、[AptSourceTrustAudit](https://github.com/dhtfish-98/AptSourceTrustAudit)、[ArtifactDigestReview](https://github.com/dhtfish-98/ArtifactDigestReview)、[AuditEventReview](https://github.com/dhtfish-98/AuditEventReview)、[AuditRuleCoverage](https://github.com/dhtfish-98/AuditRuleCoverage)。
[AuthLogReview](https://github.com/dhtfish-98/AuthLogReview)、[BodyfileTimelineReview](https://github.com/dhtfish-98/BodyfileTimelineReview)、[CertificateNamePolicy](https://github.com/dhtfish-98/CertificateNamePolicy)、[CompoundDocumentReview](https://github.com/dhtfish-98/CompoundDocumentReview)、[ContainerfileReview](https://github.com/dhtfish-98/ContainerfileReview)、[CrlRevocationReview](https://github.com/dhtfish-98/CrlRevocationReview)。
[CryptoRegressionBench](https://github.com/dhtfish-98/CryptoRegressionBench)、[CSPPolicyLens](https://github.com/dhtfish-98/CSPPolicyLens)、[DependencyPinReview](https://github.com/dhtfish-98/DependencyPinReview)、[DfxmlExtentReview](https://github.com/dhtfish-98/DfxmlExtentReview)、[DjangoSessionGuard](https://github.com/dhtfish-98/DjangoSessionGuard)、[DsseEnvelopeReview](https://github.com/dhtfish-98/DsseEnvelopeReview)。
[EntitlementFlagReview](https://github.com/dhtfish-98/EntitlementFlagReview)、[EvtxRecordReview](https://github.com/dhtfish-98/EvtxRecordReview)、[EvtxRecoveryReview](https://github.com/dhtfish-98/EvtxRecoveryReview)、[FileModeReview](https://github.com/dhtfish-98/FileModeReview)、[FinderStoreReview](https://github.com/dhtfish-98/FinderStoreReview)、[FirewalldZoneAudit](https://github.com/dhtfish-98/FirewalldZoneAudit)。
[GoCryptoPolicyReview](https://github.com/dhtfish-98/GoCryptoPolicyReview)、[HandshakeEvidenceReview](https://github.com/dhtfish-98/HandshakeEvidenceReview)、[HeaderPolicyReview](https://github.com/dhtfish-98/HeaderPolicyReview)、[IAMScopeReview](https://github.com/dhtfish-98/IAMScopeReview)、[JksTrustStoreReview](https://github.com/dhtfish-98/JksTrustStoreReview)、[JwkSetReview](https://github.com/dhtfish-98/JwkSetReview)。
[KubePodReview](https://github.com/dhtfish-98/KubePodReview)、[LifecyclePolicyReview](https://github.com/dhtfish-98/LifecyclePolicyReview)、[LnkEvidenceReview](https://github.com/dhtfish-98/LnkEvidenceReview)、[LocalSecretReview](https://github.com/dhtfish-98/LocalSecretReview)、[MachOInspect](https://github.com/dhtfish-98/MachOInspect)、[MailEvidenceReview](https://github.com/dhtfish-98/MailEvidenceReview)。
[MinisignFileReview](https://github.com/dhtfish-98/MinisignFileReview)、[ModprobePolicyAudit](https://github.com/dhtfish-98/ModprobePolicyAudit)、[NetworkPolicyReachabilityReview](https://github.com/dhtfish-98/NetworkPolicyReachabilityReview)、[NftIngressAudit](https://github.com/dhtfish-98/NftIngressAudit)、[NginxConfigGuard](https://github.com/dhtfish-98/NginxConfigGuard)、[OcspStapleReview](https://github.com/dhtfish-98/OcspStapleReview)。
[PackageOriginReview](https://github.com/dhtfish-98/PackageOriginReview)、[PamStackAudit](https://github.com/dhtfish-98/PamStackAudit)、[PDFActionReview](https://github.com/dhtfish-98/PDFActionReview)、[PEHardeningReview](https://github.com/dhtfish-98/PEHardeningReview)、[PngStreamReview](https://github.com/dhtfish-98/PngStreamReview)、[PrefetchEvidenceReview](https://github.com/dhtfish-98/PrefetchEvidenceReview)。
[RecycleRecordReview](https://github.com/dhtfish-98/RecycleRecordReview)、[RegistryHiveReview](https://github.com/dhtfish-98/RegistryHiveReview)、[SamlMetadataReview](https://github.com/dhtfish-98/SamlMetadataReview)、[SarifLinkReview](https://github.com/dhtfish-98/SarifLinkReview)、[SBOMFieldReview](https://github.com/dhtfish-98/SBOMFieldReview)、[SourceReleaseReview](https://github.com/dhtfish-98/SourceReleaseReview)。
[SSHPolicyReview](https://github.com/dhtfish-98/SSHPolicyReview)、[SudoScopeAudit](https://github.com/dhtfish-98/SudoScopeAudit)、[SysctlSnapshotAudit](https://github.com/dhtfish-98/SysctlSnapshotAudit)、[TLSProfileForge](https://github.com/dhtfish-98/TLSProfileForge)、[TransparencyProofCheck](https://github.com/dhtfish-98/TransparencyProofCheck)、[TufTopLevelReview](https://github.com/dhtfish-98/TufTopLevelReview)。
[UnicodeSourceReview](https://github.com/dhtfish-98/UnicodeSourceReview)、[UnitSandboxAudit](https://github.com/dhtfish-98/UnitSandboxAudit)、[UsnRecordReview](https://github.com/dhtfish-98/UsnRecordReview)、[WalFrameReview](https://github.com/dhtfish-98/WalFrameReview)、[WebAuthnAssertionReview](https://github.com/dhtfish-98/WebAuthnAssertionReview)、[WindowsBaselineSnapshot](https://github.com/dhtfish-98/WindowsBaselineSnapshot)。
[WorkflowPermissionReview](https://github.com/dhtfish-98/WorkflowPermissionReview)、[YaraCompileReview](https://github.com/dhtfish-98/YaraCompileReview)、[ZoneGraphGuard](https://github.com/dhtfish-98/ZoneGraphGuard)。

## 研究或派生维护背景（12）

核实具体来源和权利；不当作完全独立重写的主案例。

[A64Dispatch](https://github.com/dhtfish-98/A64Dispatch)、[ArchiveLens](https://github.com/dhtfish-98/ArchiveLens)、[BranchLoom](https://github.com/dhtfish-98/BranchLoom)、[IDBMeadow](https://github.com/dhtfish-98/IDBMeadow)、[ImageQuay](https://github.com/dhtfish-98/ImageQuay)、[KernelCabinet](https://github.com/dhtfish-98/KernelCabinet)。
[ObjCAtlas](https://github.com/dhtfish-98/ObjCAtlas)、[PEQuarry](https://github.com/dhtfish-98/PEQuarry)、[PolicyMosaic](https://github.com/dhtfish-98/PolicyMosaic)、[SealScope](https://github.com/dhtfish-98/SealScope)、[TraceMeadow](https://github.com/dhtfish-98/TraceMeadow)、[VTableBrook](https://github.com/dhtfish-98/VTableBrook)。

## 非主申请方向（4）

移出主案例计数，可继续正常维护。

[CDTranslator](https://github.com/dhtfish-98/CDTranslator)、[ChromeRelay](https://github.com/dhtfish-98/ChromeRelay)、[SILGallery](https://github.com/dhtfish-98/SILGallery)、[TabWeave](https://github.com/dhtfish-98/TabWeave)。

## 资料及账号仓（3）

不计入软件项目数。

[.github](https://github.com/dhtfish-98/.github)、[dhtfish-98](https://github.com/dhtfish-98/dhtfish-98)、[SecurityResearchIndex](https://github.com/dhtfish-98/SecurityResearchIndex)。

## 本次纠正及开放事项

- 已将“原始拦截/降级记录”与“真实用途及所受防护影响”分开：日志可选，不能把真实任务本身视为可选。已同步修正 [申请证据整理表](APPLICATION_EVIDENCE_OPEN.md) 与 [当前规则说明](CVP_RULES_AND_EVIDENCE_20261004.md)。
- 110/110 仓在冻结时都有「项目文档」，`Build` 跟踪树仅 `.gitignore`；107 个软件仓有实际权利文件。新增和未变 HEAD 的 4,228 条跟踪路径及可读文本未确认 AI/Codex 作者署名，但 Git 历史、二进制内容和源码语义不在该结论内。
- 冻结时 106/107 软件仓的精确 HEAD 有有效 CI 成功；106 个最新正式 Release 与各自读取的 HEAD 一致。SshHostCertTrustBoundary 的 GitHub Actions 当时因 hosted runner 排队，正式 Release 未创建；SshCertIssuanceGate v0.1.1 根文档整理随后推送，仍待对应 CI/Release，不能倒填进这次快照。
- 第三批 30 题目截至本窗口为 15 项正式发行、1 项主分支/标签已公开待发行，其余尚未达到发行门槛。另两个对话的 30 项交付与本批不重复计数；历史撤出 14 仓仍为 private。
- 继承或分发的第三方源码、依赖及材料必须保留真实版权、许可证与来源；新写代码可署 dhtfish98。仅改名、清掉真实第三方权利或增加仓库数不能满足申请要求。
- 真正提交申请前，须按实际 Claude.ai / Claude Code 账号核实渠道、管理员入口、身份、授权任务和具体受影响情况；模型范围及 ZDR 状态以官方当时页面为准。官方公开页面没有逐项目拒绝截图硬条件；是否批准仅由 Anthropic 决定。

证据文件 SHA-256：材料矩阵 `cd5ca5b22ddc686acaac42e3bff774a890fb4cfad707fb9c3b7d14f3dfc85ecb`；远端元数据 `6eaf0f0174698041275b688fb78ef02f18299173b7bb677ec1bf749c81986d5d`；文本/路径复核 `9a658989c99701fdb4cadb40ce9720850167783bf89d64e89cee6c394b2f27e8`。
