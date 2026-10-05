# 当前 104 个已发行软件仓的版本与附件元数据续审

从[修正的 111 仓快照](PUBLIC_111_METADATA_20261005.json)选出当时主分支精确提交 CI 已成功、最新正式 Release 与该提交一致的 104 个软件仓，分别再读 GitHub 最新 Release。结果见[逐仓 104 行、275 附件元数据](PUBLIC_104_CURRENT_RELEASE_ASSETS_METADATA_20261005.json)。104/104 标签仍与冻结快照一致，均为正式、非草稿、非预发行版本。

其中 85 仓上传了共 275 个附件；这 275 个附件的 GitHub 元数据均给出 SHA-256，报告大小均大于零。另 **19 仓未上传独立附件**，只能按其正式标签和 [GitHub 自动生成的源码归档](https://docs.github.com/en/repositories/releasing-projects-on-github/about-releases)理解，不能说这些仓发布了 wheel、二进制或自定义源码包。84 个有附件仓的至少一个主要附件名称包含本版版本号；ObjCAtlas 的主附件名固定为 `ObjCAtlas-source.zip`，该 v1.0.4 源码 ZIP 此前已逐文件比对提交对象，见[定向回执](OBJCATLAS_V1_0_4_RELEASE_20261005.json)。

未上传独立附件的 19 仓：A64Dispatch、ArtifactDigestReview、AuthLogReview、CDTranslator、ChromeRelay、ContainerfileReview、DependencyPinReview、EntitlementFlagReview、FileModeReview、HeaderPolicyReview、IAMScopeReview、KubePodReview、LocalSecretReview、MachOInspect、PEHardeningReview、SBOMFieldReview、SealScope、SSHPolicyReview、WorkflowPermissionReview。这是发行形式差异；本次不据此断言程序缺陷或 CVP 不合格。

本轮 104 仓读取的是发行元数据，**未回下载 275 个附件，也未逐包检查内部版本或执行程序**。另行回下载核对的六个主材料候选、17 个附件见[历史 30 项接管复核](HISTORICAL_30_CVP_HANDOVER_RECHECK_20261005.md)。CapabilityRuleEval、PEQuarry、SshCertIssuanceGate、SshHostCertTrustBoundary 在 111 仓快照中属于待发布链路，未混入 104 项；它们的正式发行需按后续同提交 CI 和资产结果另记。所有项目的 CVP 资格和官方决定仍为 OPEN。

本报告机器记录 SHA-256：`3c82b57ed20c88aff7740c0a0e036747cd4b37c5ef224c797e6888fad83b1f96`。各仓读取非原子完成，后续更新须另建时点记录。
