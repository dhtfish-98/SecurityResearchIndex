# 历史 30 项中六个条件技术附件的复核

冻结于 2026-10-05 23:41 UTC。范围只有 WheelNamespaceReview、CITrustBoundaryReview、DeserializeCallReview、DOMSinkReview、YaraRuleDraftReview 和 ModelOpcodeReview，不能外推到历史 30 项全部源码。六仓的当前 HEAD、正式 Release 标签、作者账号及精确主线／标签 CI 均匹配；17 个正式附件摘要也与 GitHub 一致。这些是分发与运行字节证据，不是规则正确性或 CVP 资格证明。

选定行为复测中，五项通过各自边界样例；[CITrustBoundaryReview v0.1.3](https://github.com/dhtfish-98/CITrustBoundaryReview/releases/tag/v0.1.3) 有可复现漏报。对 `pull_request` 默认 checkout 后执行 `./script.sh "${{ secrets.GITHUB_TOKEN }}"`，源码和正式 wheel 均返回 `PASS`、零发现；将同一敏感值先放入步骤 `env` 后，则返回 `FAIL/privileged_workspace_execution`。固定提交的[敏感值识别](https://github.com/dhtfish-98/CITrustBoundaryReview/blob/8ed2862c414cdc2b9116a02aafa1a8c8a8c1574b/src/ci_trust_boundary_review/review.py#L172-L173)存在，但[工作区执行判断](https://github.com/dhtfish-98/CITrustBoundaryReview/blob/8ed2862c414cdc2b9116a02aafa1a8c8a8c1574b/src/ci_trust_boundary_review/review.py#L543-L573)未把 `run` 模板中的敏感流并入条件。真实令牌权限、CI 运行和可利用后果均未由该静态反例证明。v0.1.3 不应作为该规则正确性的申请附件；修复与新版验证另行记录。

WheelNamespaceReview v0.1.4 和 DeserializeCallReview v0.1.3 的发行说明曾把仓库的 `Build` 和 `项目文档` 布局说成整体包含在 wheel/sdist 内；实际包不含 `Build/`。两份 Release 文字已更正，附件、标签及提交不变，见[文字修正回执](HISTORICAL_RELEASE_TEXT_CORRECTIONS_20261006.json)。CITrustBoundaryReview v0.1.3 的同类说明应随其功能修复发行一并更正。

六项仅是**有条件技术附件**：真实获授权目标、申请账号的合法双用途任务、防护影响、历史来源权利和官方 CVP 批准仍 OPEN。新实现署名 `dhtfish98` 与真实上游参考、依赖作者和许可必须分别陈述。
