# 102 个公开仓的 CVP 材料角色续审（2026-10-05 17:27 UTC 冻结）

本页将当时的公开仓库逐项列入[102 仓矩阵](PUBLIC_102_CVP_MATERIAL_RECHECK_20261005.json)。分类是申请材料的保守用途判断，不是 Anthropic 的资格或批准决定，也不是 102 仓完整语义代码深审。逐仓简介和最新 Release 正文另有[文本补查](PUBLIC_102_METADATA_TEXT_AUDIT_20261005.json)：未检出 AI/Codex 作者标记或声称 CVP 已获批的措辞；SILGallery 的旧安装标识为兼容保留。

|材料角色|仓数|处理|
|---|---:|---|
|已有条件技术案例|6|可作为技术附件，但须对应申请人真实授权任务与实际防护影响|
|第三批本地实验条件案例|8|已完成限定的自有实验与发行；真实场景、部署和申请结果仍待独立证明|
|其他防御工作附件|69|保留为工程背景；仅凭工具功能或测试，不计作独立 CVP 合格案例|
|研究背景及派生工具|12|保留真实第三方来源和权利；不得把派生项目表述成完全独立重写|
|普通工程背景|4|不列作主要 CVP 案例|
|资料/账号仓|3|仅作索引或账号说明|

六个此前经代码级再筛的条件案例是 WheelNamespaceReview、CITrustBoundaryReview、DeserializeCallReview、DOMSinkReview、YaraRuleDraftReview、ModelOpcodeReview。第三批已发行的八个本地实验是 RedirectCredentialBoundary、WebSocketUpgradeOriginGate、GraphQLQueryCostGate、XmlEntityResourceBoundary、ProxyIdentityHeaderTrust、PluginHandshakeTrustGate、AcmeChallengeAuthorization、RelationAccessDecision。两组都没有由仓库本身证明 CVP 资格；其余项目也不是政策意义的“不合规项目”，只是目前不应当作申请主证据。

本轮更新办法是继续实现并独立审查[第三批 30 项研究候选](NEW_30_RESEARCH_CANDIDATES_20261005.md)，对发布缺陷做版本化修复，同时让低适配度项目留在对应的背景角色。不会通过删除真实第三方版权、把自建弱基线说成上游漏洞、制造拦截记录或堆仓库数量来提高材料等级。[Anthropic 官方说明](https://support.claude.com/en/articles/14604842-real-time-cyber-safeguards-on-claude-opus-and-sonnet)没有规定最低 30 仓或每仓拦截截图；申请人的真实合法高风险双用途工作、授权、组织/身份条件及审批仍是独立待核事项。

矩阵沿用 [2026-10-04 逐仓材料角色](CVP_REVIEW_20261004.json)与[六案例代码级复核](CVP_CODE_SCOPE_RECHECK_20261004.md)，结合第三批八项发行收据和 2026-10-05 的公开简介/最新 Release 数据。老项目的新版本、源码权利文件和目录另有[100 仓精确提交文本/路径检查](PUBLIC_100_EXACT_HEAD_AUDIT_20261005.md)；该检查截止于八个新实验中只有六个公开的时点。所有窗口均非原子读取，不覆盖历史 Release 正文、未解析二进制或真实部署。
