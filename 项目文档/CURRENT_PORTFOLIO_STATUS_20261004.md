# 2026-10-04 公开项目与 CVP 材料状态

GitHub 读取冻结于 2026-10-04T04:51:35.302600Z。当时账号共 123 仓：94 公开、29 私有；公开仓包括 91 软件和 3 资料仓。91 个软件仓各自冻结 HEAD 对应的 GitHub Actions 均成功，3 个资料仓没有相应精确 HEAD 工作流。逐仓提交和运行链接见[机器可读快照](PUBLIC_PORTFOLIO_STATUS_20261004.json)。这是一段时间内逐仓读取的快照，不是原子状态，也不代表完整安全代码审计、现场运行或 CVP 获批。

[Anthropic 官方 CVP 说明](https://support.claude.com/en/articles/14604842-real-time-cyber-safeguards-on-claude-opus-and-sonnet)说明申请针对合法防御目的且实际受到网络安全防护影响的高风险双用途任务；Claude.ai / Claude Code 使用第一方 Verification Portal，需按组织管理员、身份、模型和数据保留条件核对。禁止用途不因申请获批而解除。公开页面没有要求每个仓库附拦截截图；申请仍须如实说明真实任务、授权范围和受影响情况。

## 申请材料角色

以下按已记录的有限功能和公开证据分层，是材料编排判断，不是官方项目白名单。两批各 30 项的工程交付与另外 34 个公开仓合并后，当前只有 **18 个条件技术案例**适合在存在真实匹配任务时优先说明，距“30 个现成 CVP 技术案例”还差 12 个。全部 94 项的实际授权任务、组织身份、受防护影响和官方决定均未由仓库证明。

| 材料角色 | 数量 | 解释 |
| --- | ---: | --- |
| 条件技术案例 | 18 | 可联系真实授权双用途任务，仍需逐项核对相关性 |
| 技术研究暂缓 | 8 | 有相关能力，但既有反例、审计或发布边界尚未关闭 |
| 防御工程背景 | 61 | 有限定防御用途，单独不足以证明需调整高风险防护 |
| 通用浏览器自动化背景 | 2 | 浏览器控制能力不等于专属安全任务 |
| 非网络安全背景 | 2 | 翻译或开发辅助，不列入安全申请主案例 |
| 资料仓 | 3 | 导航和记录，不当作软件项目 |

条件技术案例（仅在实际任务匹配时使用）：

- [AuditRuleCoverage](https://github.com/dhtfish-98/AuditRuleCoverage)：Selected typed audit rule syntax and complete frozen literal baseline coverage。
- [CITrustBoundaryReview](https://github.com/dhtfish-98/CITrustBoundaryReview)：CI事件输入到脚本的信任边界。
- [CSPPolicyLens](https://github.com/dhtfish-98/CSPPolicyLens)：CSP指令、nonce/hash与严格策略。
- [DOMSinkReview](https://github.com/dhtfish-98/DOMSinkReview)：DOM HTML赋值与清洗证据。
- [DeserializeCallReview](https://github.com/dhtfish-98/DeserializeCallReview)：Python对象反序列化调用边界。
- [DjangoSessionGuard](https://github.com/dhtfish-98/DjangoSessionGuard)：会话/CSRF设置与中间件依赖检查。
- [GoCryptoPolicyReview](https://github.com/dhtfish-98/GoCryptoPolicyReview)：Go源码TLS/随机数/密钥参数误用。
- [ImageQuay](https://github.com/dhtfish-98/ImageQuay)：本地 Mach-O 解析及编辑、lipo、header/stub 生成等开发分析。
- [KernelCabinet](https://github.com/dhtfish-98/KernelCabinet)：授权兼容内核文件中的嵌入扩展元数据与原始 TEXT_EXEC 片段复制。
- [LifecyclePolicyReview](https://github.com/dhtfish-98/LifecyclePolicyReview)：依赖安装生命周期允许策略审查。
- [ModelOpcodeReview](https://github.com/dhtfish-98/ModelOpcodeReview)：模型序列化操作码与对象引用静态审查。
- [NetworkPolicyReachabilityReview](https://github.com/dhtfish-98/NetworkPolicyReachabilityReview)：Complete declared Kubernetes networking.k8s.io/v1 NetworkPolicy profile evaluated offline against a bounded topology and explicit directional connection questions。
- [NftIngressAudit](https://github.com/dhtfish-98/NftIngressAudit)：Offline nftables ingress policy structure audit。
- [NginxConfigGuard](https://github.com/dhtfish-98/NginxConfigGuard)：服务器配置继承、路径映射与代理变量。
- [SudoScopeAudit](https://github.com/dhtfish-98/SudoScopeAudit)：Snapshot sudoers include and alias scope audit。
- [WheelNamespaceReview](https://github.com/dhtfish-98/WheelNamespaceReview)：Python安装包命名空间与记录一致性。
- [YaraRuleDraftReview](https://github.com/dhtfish-98/YaraRuleDraftReview)：离线YARA检测规则草稿与良性对照。
- [ZoneGraphGuard](https://github.com/dhtfish-98/ZoneGraphGuard)：离线DNS区域、委派与别名图约束。

技术研究暂缓进入主材料：[A64Dispatch](https://github.com/dhtfish-98/A64Dispatch)、[ArchiveLens](https://github.com/dhtfish-98/ArchiveLens)、[BranchLoom](https://github.com/dhtfish-98/BranchLoom)、[IDBMeadow](https://github.com/dhtfish-98/IDBMeadow)、[ObjCAtlas](https://github.com/dhtfish-98/ObjCAtlas)、[PEQuarry](https://github.com/dhtfish-98/PEQuarry)、[PolicyMosaic](https://github.com/dhtfish-98/PolicyMosaic)、[VTableBrook](https://github.com/dhtfish-98/VTableBrook)。其完整代码深审或已记录程序问题仍需各自解决；普通 CI 成功不能代替关闭。CDTranslator、SILGallery 为非网络安全背景；ChromeRelay、TabWeave 为通用浏览器自动化背景。

## 本次工程更新与来源边界

- 14 个公开小仓的项目自有版权显示名已统一为 `dhtfish98`，其中 LocalSecretReview、PEHardeningReview 的安装包作者字段随 `v1.0.3` 更新；另外 12 仓仅有自有许可行和构建清单变动，软件版本未改变。
- A64Dispatch、ChromeRelay、MachOInspect、BranchLoom、SealScope 的安全报告入口链接与私密报告设置已校验。SealScope 的 `v0.2.1` 是程序标签，当前分支后续的安全说明提交属于文档更新。
- HeaderPolicyReview `v0.1.3`、ImageQuay `v1.0.5`、SealScope `v0.2.1`、KernelCabinet `v1.0.2` 以及上述两个 `v1.0.3` 各按对应程序或包提交与正式 Release 核对；较早的目录/项目表格只对应其原冻结时间。
- 衍生项目的真实上游作者、许可和来源通知继续保留。自有显示名更新不抹去第三方权利，也不证明独立原创。

适合申请的具体证据应从真实授权任务出发，选择与该任务直接相关的少数项目和精确提交。项目数、重命名、GitHub 发布和 CI 均不能替代申请人身份、组织权限及 Anthropic 的决定。
