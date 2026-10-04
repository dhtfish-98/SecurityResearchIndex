# 原30题目工作池复核（6 条件候选 + 10 背景 + 2 移出 + 12 待实施）

固定资料时间：2026-10-04 05:17 UTC；已有仓的 HEAD/Actions 状态来源于 04:56 UTC 的账号冻结。此清单用于保留原 30 题目的审查轨迹，**不是 30 个已达到 CVP 申请门槛的项目**。代码级再筛将原 18 个“条件案例”收紧为 6 个条件候选、10 个背景备用及 2 个移出独立重写主池；详见[逐仓代码证据](CVP_CODE_SCOPE_RECHECK_20261004.md)。

依据 [Anthropic 官方 CVP 说明](https://support.claude.com/en/articles/14604842-real-time-cyber-safeguards-on-claude-opus-and-sonnet)，合法防御的高风险双用途任务须实际受网络安全防护影响；Claude.ai / Claude Code 由有权限管理员走 Verification Portal。官方公开说明没有规定 30 仓数量，也没有列每仓拦截截图为必附。申请人身份、组织、目标授权、任务与决定未核实，下面全部 CVP 资格为 **OPEN**。

## 已有公开实现：6 个条件候选、10 个背景备用、2 个移出主池

下表保留 04:56 UTC 的原始 HEAD 锚点，分类按后续代码级再筛修正；公开、CI 成功不证明运行时安全。

| 项目 | 04:56 UTC 冻结提交 | CVP 状态 |
|---|---|---|
| [WheelNamespaceReview](https://github.com/dhtfish-98/WheelNamespaceReview) | [`f337a3a49dfe`](https://github.com/dhtfish-98/WheelNamespaceReview/tree/f337a3a49dfe2836606c28b7aef4e14e940b2b10) | 条件候选；CVP OPEN |
| [CITrustBoundaryReview](https://github.com/dhtfish-98/CITrustBoundaryReview) | [`40ed13a4fddc`](https://github.com/dhtfish-98/CITrustBoundaryReview/tree/40ed13a4fddcc616e460472e0abcf59af4808391) | 条件候选；CVP OPEN |
| [DeserializeCallReview](https://github.com/dhtfish-98/DeserializeCallReview) | [`81354b9e6746`](https://github.com/dhtfish-98/DeserializeCallReview/tree/81354b9e67468bec04c7f1b00d09d26ba11901ef) | 条件候选；CVP OPEN |
| [GoCryptoPolicyReview](https://github.com/dhtfish-98/GoCryptoPolicyReview) | [`aed3cca5fd9f`](https://github.com/dhtfish-98/GoCryptoPolicyReview/tree/aed3cca5fd9f95288c476bb37f28f1a8093d3461) | 背景备用；CVP OPEN |
| [DOMSinkReview](https://github.com/dhtfish-98/DOMSinkReview) | [`e74f1ac7c704`](https://github.com/dhtfish-98/DOMSinkReview/tree/e74f1ac7c704ae6994fe529163a3c4aa7ff48343) | 条件候选；CVP OPEN |
| [LifecyclePolicyReview](https://github.com/dhtfish-98/LifecyclePolicyReview) | [`745f8227e174`](https://github.com/dhtfish-98/LifecyclePolicyReview/tree/745f8227e174ad5dbf34ce5acb636b8fa2cb90b7) | 背景备用；CVP OPEN |
| [YaraRuleDraftReview](https://github.com/dhtfish-98/YaraRuleDraftReview) | [`aa37ffc76394`](https://github.com/dhtfish-98/YaraRuleDraftReview/tree/aa37ffc763946e4c41fa94a469bd9ce75d96dc51) | 条件候选；CVP OPEN |
| [NginxConfigGuard](https://github.com/dhtfish-98/NginxConfigGuard) | [`a850a60d33b4`](https://github.com/dhtfish-98/NginxConfigGuard/tree/a850a60d33b499c9c7c2dcd821d3c80a4c9073e1) | 背景备用；CVP OPEN |
| [CSPPolicyLens](https://github.com/dhtfish-98/CSPPolicyLens) | [`4414f49a3e0b`](https://github.com/dhtfish-98/CSPPolicyLens/tree/4414f49a3e0b69255a53c8ed2c683d424fb3798a) | 背景备用；CVP OPEN |
| [ZoneGraphGuard](https://github.com/dhtfish-98/ZoneGraphGuard) | [`919bdeff1b70`](https://github.com/dhtfish-98/ZoneGraphGuard/tree/919bdeff1b70377fad718b271005158e663e8741) | 背景备用；CVP OPEN |
| [DjangoSessionGuard](https://github.com/dhtfish-98/DjangoSessionGuard) | [`04de12f8699b`](https://github.com/dhtfish-98/DjangoSessionGuard/tree/04de12f8699bedd5b86b7f85b6542f1a8d150b7e) | 背景备用；CVP OPEN |
| [ModelOpcodeReview](https://github.com/dhtfish-98/ModelOpcodeReview) | [`542d79772e94`](https://github.com/dhtfish-98/ModelOpcodeReview/tree/542d79772e94a761dd98cca08a3222b038e5abbf) | 条件候选；CVP OPEN |
| [SudoScopeAudit](https://github.com/dhtfish-98/SudoScopeAudit) | [`c6779b7e1a50`](https://github.com/dhtfish-98/SudoScopeAudit/tree/c6779b7e1a507193c3da69dcc403fd268d1282e9) | 背景备用；CVP OPEN |
| [AuditRuleCoverage](https://github.com/dhtfish-98/AuditRuleCoverage) | [`6c522e46e501`](https://github.com/dhtfish-98/AuditRuleCoverage/tree/6c522e46e50115e7434b185f7ac0b10e6b9d7f1b) | 背景备用；CVP OPEN |
| [NftIngressAudit](https://github.com/dhtfish-98/NftIngressAudit) | [`031b9d053b85`](https://github.com/dhtfish-98/NftIngressAudit/tree/031b9d053b85f29ead285a85cbd506f794a4f817) | 背景备用；CVP OPEN |
| [NetworkPolicyReachabilityReview](https://github.com/dhtfish-98/NetworkPolicyReachabilityReview) | [`10072426a975`](https://github.com/dhtfish-98/NetworkPolicyReachabilityReview/tree/10072426a97570863a488b22675d855216c62007) | 背景备用；CVP OPEN |
| [ImageQuay](https://github.com/dhtfish-98/ImageQuay) | [`30619167cac8`](https://github.com/dhtfish-98/ImageQuay/tree/30619167cac87c6520f97b68f4401fd4316d105a) | 移出独立重写主池；CVP OPEN |
| [KernelCabinet](https://github.com/dhtfish-98/KernelCabinet) | [`7cd05089810b`](https://github.com/dhtfish-98/KernelCabinet/tree/7cd05089810b2c3ad35e48a4989c56e9c0648a85) | 移出独立重写主池；CVP OPEN |

## 新增待实施：12 个独立题目

以下仅完成范围与最小验证规格；**没有建仓、源码重写、构建、发布或 CVP 审批**。参考上游只用于固定技术背景；实际复用代码/数据时需保留适用许可证、作者与通知。不能把薄包装称为完整上游重写。

| 题目 | 优先级 | 一手参考 | 工程状态 |
|---|---|---|---|
| APIContractStateReview | P1 | [固定源码](https://github.com/schemathesis/schemathesis/tree/7d799f38a542b62395595ff55da1e2769e11aec7) | 研究规格；未实现、未发布；CVP OPEN |
| WebSessionDastReview | P1 | [固定源码](https://github.com/zaproxy/zaproxy/tree/c75375055d78f8cf89762e009cc9d4d35d0e9f54) | 研究规格；未实现、未发布；CVP OPEN |
| IAMPrivilegeGraphReview | P1 | [固定源码](https://github.com/nccgroup/PMapper/tree/91d2e60102bdadf346d77b60d90ddaa4a678f037) | 研究规格；未实现、未发布；CVP OPEN |
| ParserCrashBoundaryReview | P1 | [固定源码](https://github.com/llvm/llvm-project/tree/4d807b161f802800617703cdf885ef8f5707a912) | 研究规格；未实现、未发布；CVP OPEN |
| NetworkIDSReplayReview | P2 | [固定源码](https://github.com/OISF/suricata/tree/819c61265d9e3c74516c45e88c4645b4d055bb74) | 研究规格；未实现、未发布；CVP OPEN |
| ContainerRuntimeRuleReview | P2 | [固定源码](https://github.com/falcosecurity/falco/tree/b608d820c8a380f6a098d8946359070addb7243f) | 研究规格；未实现、未发布；CVP OPEN |
| SymbolicPathBoundaryReview | P2 | [固定源码](https://github.com/angr/angr/tree/0c9553751f7dad862daa966862d4960ff86a8c86) | 研究规格；未实现、未发布；CVP OPEN |
| RuntimeFlowTraceReview | P2 | [固定源码](https://github.com/DynamoRIO/dynamorio/tree/2ef1f41e0b74893c699ba7ccdbf4c8c890025bba) | 研究规格；未实现、未发布；CVP OPEN |
| PackageBehaviorSandboxReview | P3 | [固定源码](https://github.com/ossf/package-analysis/tree/c5c45008da694036d701ba76fe9567fc8a5b9675) | 研究规格；未实现、未发布；CVP OPEN |
| KubeProcessLineageReview | P3 | [固定源码](https://github.com/cilium/tetragon/tree/2b865d019d48905ca4f14a38d2671706abee3c6f) | 研究规格；未实现、未发布；CVP OPEN |
| MobileRuntimeEvidenceReview | P3 | [固定源码](https://github.com/frida/frida-core/tree/ea9efa1e2459e62acf8463b6ad2b178c01f3c64f) | 研究规格；未实现、未发布；CVP OPEN |
| LinuxMemoryCaptureReview | P3 | [固定源码](https://github.com/microsoft/avml/tree/4f385320cddd1876280f44f891eb988567372d06) | 研究规格；未实现、未发布；CVP OPEN |

优先题目包括受控本地 API 契约与会话隔离测试、离线 IAM 权限图、授权解析器崩溃回归；高成本的内核 fuzz 和 JavaScript 引擎语料方向暂缓。只有真实防御任务需要、目标获授权且功能不重复，才逐项实施。用户所用 Claude 组织与适用模型、实际任务是否受 cyber safeguards 影响仍待核对。

公共项目总状态见 [现行组合](CURRENT_PORTFOLIO_STATUS_20261004.md)、[94 仓固定快照](PUBLIC_PORTFOLIO_STATUS_20261004.json)；后续提交请以各仓当期 HEAD 为准。
