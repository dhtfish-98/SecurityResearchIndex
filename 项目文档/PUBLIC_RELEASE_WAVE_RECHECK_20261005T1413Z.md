# 公开仓发行与目录复核（2026-10-05 14:13–14:14 UTC）

本页对应 14:13:53–14:14:34 UTC 的逐仓非原子 GitHub 读取；[机器快照](PUBLIC_RELEASE_WAVE_SNAPSHOT_20261005T1413Z.json)保存各仓所读主分支、最新正式发行、浅层目录和自动检查。早先的 13:37 UTC 等快照各保留原时间边界。

- 可见公开仓 94、私有仓 29；91 个软件仓都有 Release，其中 90 个最新标签与所读主分支同提交。唯一差异是 ObjCAtlas，旧深层审计仍未完成，不能以发行标签差异推断代码安全结论。
- 94/94 个仓有所读「项目文档」目录，`Build` 根目录只跟踪 `.gitignore`；91/91 软件仓当前 HEAD 的作者和提交者显示名是 `dhtfish98`。真实第三方版权与许可证继续保留。
- 91/91 软件仓的精确 HEAD 有有效成功检查。ChromeRelay 和 MachOInspect 较早同提交取消运行仍在 GraphQL 汇总中，较新的完整 push 工作流成功，快照保留例外证据。旧撤出组 14/14 仍为私有。

这次读取已包含 [ImageQuay v1.0.7](https://github.com/dhtfish-98/ImageQuay/releases/tag/v1.0.7) 的源码目录版本回退修复，以及 PackageOriginReview、JwkSetReview、LnkEvidenceReview、MailEvidenceReview、MinisignFileReview、NetworkPolicyReachabilityReview、OcspStapleReview、PDFActionReview 的八项版本文档同步发行。具体提交、CI 和资产验收见[发行增量](PUBLIC_RELEASE_INCREMENT_20261005_AFTER_SNAPSHOT.md)。

[第三批 30 项研究候选](NEW_30_RESEARCH_CANDIDATES_20261005.md)另外列出，全部在本次读取时仍是候选，不能计入这 91 个已发布软件仓或 CVP 获批项目。官方[CVP 说明](https://support.claude.com/en/articles/14604842-real-time-cyber-safeguards-on-claude-opus-and-sonnet)没有把 30 仓或逐仓拦截截图列为硬性附件。真实合法授权任务、账号与组织条件、实际受防护影响情况及官方批准仍须分别核对。目录、版本、作者显示名和 CI 检查不等于全量安全代码审计。
