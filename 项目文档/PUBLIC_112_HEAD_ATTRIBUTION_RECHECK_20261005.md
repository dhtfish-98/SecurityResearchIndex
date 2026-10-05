# 112 个公开仓当前提交的 GitHub 账号署名复核

2026-10-05 20:26–20:27 UTC 冻结读取 112 个公开仓各自 `main` 的精确提交后，另以 GitHub GraphQL 读取该提交的**显示名**和**实际关联的 GitHub 账号**。[逐仓机读结果](PUBLIC_112_HEAD_ATTRIBUTION_AUDIT_20261005.json)显示：94 仓的作者和提交者均关联 `dhtfish-98`；**18 仓虽然显示名为 `dhtfish98`，实际关联到别的账号**。该问题不在先前的“文本中无 AI 作者署名”检查范围内，原结论不能代替账号关联核验。

15 仓的当前提交关联到 `ToolShedd`：ArchiveLens、CapabilityRuleEval、GraphQLQueryCostGate、JupyterKernelOriginGate、NatsSubjectTenantGate、ObjCAtlas、PluginHandshakeTrustGate、ProxyIdentityHeaderTrust、QuicEarlyDataPolicy、RecoveryCodeAccountBinding、RedirectCredentialBoundary、SftpHandlePermissionGate、SshHostCertTrustBoundary、WebSocketUpgradeOriginGate、XmlEntityResourceBoundary。另 3 仓关联到 `newstorn245`：ObfuscatedStringRecovery、SecurityResearchIndex、SshCertIssuanceGate。两个错误邮箱分别用了不属于 `dhtfish-98` 的数字前缀 `160427136` 和 `274931615`。GitHub API 当前返回的 `dhtfish-98` 用户 ID 为 `109978225`；GitHub 的[官方邮箱说明](https://docs.github.com/en/account-and-profile/reference/email-addresses-reference)规定 ID 型隐私邮箱为 `ID+USERNAME@users.noreply.github.com`，其[提交邮箱说明](https://docs.github.com/en/account-and-profile/how-tos/email-preferences/setting-your-commit-email-address)说明账号关联取决于提交邮箱。

这是**发布元数据的错误关联**，不能据此推定这些代码的实际创作者是上述账号，也不能把真实上游作者和许可改成新作者。已在未公开的 FederatedConnectorIdentityGate 本地候选使用正确 ID；其他待发行或已发行仓将按其发布链路分别修正，并重新核对 GitHub 实际账号关联。对已有正式 Release 的仓库，不以改写标签和历史来冒充旧资产仍有效；修订版须重新通过对应提交的 CI 与发行检查。旧 Git 对象仍会保留其历史字段，完整历史范围待另审。

本轮读取是非原子快照，后续修订会让这些提交号前进。它只检查各仓当时的当前提交，不是 112 仓全历史、第三方权利或源码语义审计，也不决定 CVP 资格。该机读记录 SHA-256：`aeac1487b3bba64fb0d668dcd750ae8f038f3b126d82116b46528c9ca81a9a93`。
