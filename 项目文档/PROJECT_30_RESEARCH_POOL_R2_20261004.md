# 30 个防御研究题目候选池（6 已有条件案例 + 24 未实现规格）

更新：2026-10-04 06:14 UTC。这是对[原30题目初筛](PROJECT_30_TOPIC_POOL_20261004.md)的代码级更正与新增选题；**不是 30 个已重写、已发布或已符合 CVP 要求的项目**。现有仓库中仅 6 个暂列条件候选，另 24 个只是独立范围与验收设计，尚未建仓、实现、测试或发布。30/30 的实际 CVP 资格及审批均 OPEN。

依据 [Anthropic CVP 官方说明](https://support.claude.com/en/articles/14604842-real-time-cyber-safeguards-on-claude-opus-and-sonnet)，申请针对申请人真实、获授权且确实受网络安全防护影响的高风险双用途防御任务。公开说明未规定 30 仓数量或逐仓拦截截图必附；这也不代表无需真实任务、组织和身份核实。选题只在相符的自有或明确授权环境实施。

## 已有实现：6 个条件候选

| 项目 | 冻结源码 | 实际能力边界 |
|---|---|---|
| [WheelNamespaceReview](https://github.com/dhtfish-98/WheelNamespaceReview) | [`f337a3a49d`](https://github.com/dhtfish-98/WheelNamespaceReview/tree/f337a3a49dfe2836606c28b7aef4e14e940b2b10) | 离线解析 wheel 路径、RECORD 与安装映射，可联系恶意软件包/安装链审查；不会安装目标 wheel。 |
| [CITrustBoundaryReview](https://github.com/dhtfish-98/CITrustBoundaryReview) | [`40ed13a4fd`](https://github.com/dhtfish-98/CITrustBoundaryReview/tree/40ed13a4fddcc616e460472e0abcf59af4808391) | 解析 GitHub Actions YAML，追踪事件字段到 run 的模板注入路径；shell 子集不执行。 |
| [DeserializeCallReview](https://github.com/dhtfish-98/DeserializeCallReview) | [`81354b9e67`](https://github.com/dhtfish-98/DeserializeCallReview/tree/81354b9e67468bec04c7f1b00d09d26ba11901ef) | 静态解析 Python 反序列化调用和绑定，测试证明目标源码不会被导入/执行。 |
| [DOMSinkReview](https://github.com/dhtfish-98/DOMSinkReview) | [`e74f1ac7c7`](https://github.com/dhtfish-98/DOMSinkReview/tree/e74f1ac7c704ae6994fe529163a3c4aa7ff48343) | Acorn AST 检查 DOM HTML sink 的值与静态 sanitizer 绑定，不运行浏览器目标代码。 |
| [YaraRuleDraftReview](https://github.com/dhtfish-98/YaraRuleDraftReview) | [`aa37ffc763`](https://github.com/dhtfish-98/YaraRuleDraftReview/tree/aa37ffc763946e4c41fa94a469bd9ce75d96dc51) | 从目标/良性/留出样本字节生成 YARA 草稿并编译、扫描验证；恶意性与泛化性在报告中明示 OPEN。 |
| [ModelOpcodeReview](https://github.com/dhtfish-98/ModelOpcodeReview) | [`542d79772e`](https://github.com/dhtfish-98/ModelOpcodeReview/tree/542d79772e94a761dd98cca08a3222b038e5abbf) | 离线读取 pickle/npy/zip 结构和危险引用；object dtype 与无法证明的行为维持 OPEN，不反序列化目标。 |

这些候选经[代码与代表性测试锚点复核](CVP_CODE_SCOPE_RECHECK_20261004.md)，但实际任务、目标授权、safeguards 影响及批准均 OPEN。原初筛的 10 个普通离线检查已降为工程背景，ImageQuay 与 KernelCabinet 属有明确派生来源的通用二进制工具，已移出独立重写主案例。

## 待实现：先前12项最小规格

| 题目 | 优先级 | 固定研究来源 | 最小独立交付 |
|---|---|---|---|
| APIContractStateReview | P1 | [上游固定提交](https://github.com/schemathesis/schemathesis/tree/7d799f38a542b62395595ff55da1e2769e11aec7)、[许可](https://github.com/schemathesis/schemathesis/blob/7d799f38a542b62395595ff55da1e2769e11aec7/LICENSE) | OpenAPI 限定路径/方法/参数与响应断言的独立状态检查器；只请求自有环回服务、预置测试令牌、可回滚接口。 |
| WebSessionDastReview | P1 | [上游固定提交](https://github.com/zaproxy/zaproxy/tree/c75375055d78f8cf89762e009cc9d4d35d0e9f54)、[许可](https://github.com/zaproxy/zaproxy/blob/c75375055d78f8cf89762e009cc9d4d35d0e9f54/LICENSE) | 独立会话隔离检查状态机，限定环回地址、两个一次性测试账号、固定请求预算；只比较授权测试应用的会话行为。 |
| IAMPrivilegeGraphReview | P1 | [上游固定提交](https://github.com/nccgroup/PMapper/tree/91d2e60102bdadf346d77b60d90ddaa4a678f037)、[许可](https://github.com/nccgroup/PMapper/blob/91d2e60102bdadf346d77b60d90ddaa4a678f037/LICENSE) | 离线 IAM 主体、角色信任、资源策略的限定语义图；独立计算声明权限路径，未知条件给 OPEN。无凭据和云端写调用。 |
| ParserCrashBoundaryReview | P1 | [上游固定提交](https://github.com/llvm/llvm-project/tree/4d807b161f802800617703cdf885ef8f5707a912)、[许可](https://github.com/llvm/llvm-project/blob/4d807b161f802800617703cdf885ef8f5707a912/LICENSE.TXT) | 自有小型解析器的有限语料、sanitizer 输出归并及修复回归证据核心；libFuzzer 只作参考/外部测试引擎。 |
| NetworkIDSReplayReview | P2 | [上游固定提交](https://github.com/OISF/suricata/tree/819c61265d9e3c74516c45e88c4645b4d055bb74)、[许可](https://github.com/OISF/suricata/blob/819c61265d9e3c74516c45e88c4645b4d055bb74/LICENSE) | 独立实现离线 PCAP 的有限流重组与只读规则匹配子集，输出告警位置/规则版本；不监听、不发流量。 |
| ContainerRuntimeRuleReview | P2 | [上游固定提交](https://github.com/falcosecurity/falco/tree/b608d820c8a380f6a098d8946359070addb7243f)、[许可](https://github.com/falcosecurity/falco/blob/b608d820c8a380f6a098d8946359070addb7243f/LICENSE) | 独立的容器事件归一化与规则判定器；在自有可销毁容器环境取得只读事件，不做自动封禁。 |
| SymbolicPathBoundaryReview | P2 | [上游固定提交](https://github.com/angr/angr/tree/0c9553751f7dad862daa966862d4960ff86a8c86)、[许可](https://github.com/angr/angr/blob/0c9553751f7dad862daa966862d4960ff86a8c86/LICENSE) | 仅对自有小函数/中间表示的限定指令集做输入约束与分支到达性分析；求解器可作第三方依赖，未知指令/预算为 OPEN。 |
| RuntimeFlowTraceReview | P2 | [上游固定提交](https://github.com/DynamoRIO/dynamorio/tree/2ef1f41e0b74893c699ba7ccdbf4c8c890025bba)、[许可](https://github.com/DynamoRIO/dynamorio/blob/2ef1f41e0b74893c699ba7ccdbf4c8c890025bba/License.txt) | 自有测试进程的分支事件采集和修复路径对照；限定固定二进制/进程，插桩框架只作依赖，独立实现证据归并。 |
| PackageBehaviorSandboxReview | P3 | [上游固定提交](https://github.com/ossf/package-analysis/tree/c5c45008da694036d701ba76fe9567fc8a5b9675)、[许可](https://github.com/ossf/package-analysis/blob/c5c45008da694036d701ba76fe9567fc8a5b9675/LICENSE) | 一次性隔离 VM 中的包安装/导入行为元数据采集与归并；首版只跑自写合成包，不执行未知第三方包。 |
| KubeProcessLineageReview | P3 | [上游固定提交](https://github.com/cilium/tetragon/tree/2b865d019d48905ca4f14a38d2671706abee3c6f)、[许可](https://github.com/cilium/tetragon/blob/2b865d019d48905ca4f14a38d2671706abee3c6f/LICENSE) | 自有测试集群单 namespace 的进程/网络事件父子图与缺事件账本；只读收集，无阻断动作。 |
| MobileRuntimeEvidenceReview | P3 | [上游固定提交](https://github.com/frida/frida-core/tree/ea9efa1e2459e62acf8463b6ad2b178c01f3c64f)、[许可](https://github.com/frida/frida-core/blob/ea9efa1e2459e62acf8463b6ad2b178c01f3c64f/COPYING) | 本人编写的模拟器 App 中固定安全函数调用次数/顺序记录；限定签名和进程 ID，不读内存内容、不附着他人应用。 |
| LinuxMemoryCaptureReview | P3 | [上游固定提交](https://github.com/microsoft/avml/tree/4f385320cddd1876280f44f891eb988567372d06)、[许可](https://github.com/microsoft/avml/blob/4f385320cddd1876280f44f891eb988567372d06/LICENSE) | 只在自建一次性 Linux VM 中实现明确限制的易失内存采集与完整性记录；超范围内核/权限失败受控，不上传内容。 |

## 待实现：新增12项最小规格

| 题目 | 优先级 | 固定研究来源与许可 | 最小独立交付 |
|---|---|---|---|
| HttpDesyncBoundaryReview | P1 | [源码](https://github.com/defparam/smuggler/tree/2be871e6151ce85167a277fab21c74c851d8b20b)、[许可](https://github.com/defparam/smuggler/blob/2be871e6151ce85167a277fab21c74c851d8b20b/LICENSE)：MIT; Evan Custodio | owned two-hop HTTP/1.1 framing differential state recorder |
| JwtVerifierConfusionReview | P1 | [源码](https://github.com/jpadilla/pyjwt/tree/b5bd6fe6d7ac0370ba90557c7a1e3d50a9414572)、[许可](https://github.com/jpadilla/pyjwt/blob/b5bd6fe6d7ac0370ba90557c7a1e3d50a9414572/LICENSE)：MIT; José Padilla | trusted algorithm/key binding and claims policy state machine; use vetted crypto dependency |
| OAuthCodePkceReplayReview | P1 | [源码](https://github.com/oauthlib/oauthlib/tree/16801a6f98e4bcbf4d38ae8ebd75e01b1b525cbc)、[许可](https://github.com/oauthlib/oauthlib/blob/16801a6f98e4bcbf4d38ae8ebd75e01b1b525cbc/LICENSE)：BSD-3-Clause; OAuthlib Community | owned two-client authorization-code state, redirect and PKCE binding recorder |
| SamlSignatureWrappingReview | P2 | [源码](https://github.com/SAML-Toolkits/python3-saml/tree/52d2ac8da3f35262755f6e1c32ba7c62a6011fe1)、[许可](https://github.com/SAML-Toolkits/python3-saml/blob/52d2ac8da3f35262755f6e1c32ba7c62a6011fe1/LICENSE)：MIT; OneLogin and IAM Digital Services | trusted signed XML reference-to-consumed-assertion binding, with external XML signature library |
| ADCSIssuanceAbuseReview | P3 | [源码](https://github.com/ly4k/Certipy/tree/3ae34426c58d266a1979ff9607514c3d7fe1aa21)、[许可](https://github.com/ly4k/Certipy/blob/3ae34426c58d266a1979ff9607514c3d7fe1aa21/LICENSE)：MIT; ly4k | owned AD CS lab request-template-issuance-identity evidence reconciler |
| SMBRelaySigningBoundaryReview | P2 | [源码](https://github.com/fortra/impacket/tree/1875828d0f2e987cd89c1bcb45f843708981a199)、[许可](https://github.com/fortra/impacket/blob/1875828d0f2e987cd89c1bcb45f843708981a199/LICENSE)：modified Apache Software License 1.1 with file-specific third-party terms; GitHub NOASSERTION; no code reuse planned | offline SMB signing and channel-binding precondition model, no relay engine |
| DNSResolverPoisonReplayReview | P2 | [源码](https://github.com/miekg/dns/tree/2e4905fb030255032d4343cb83bc2f8c3cfcb82a)、[许可](https://github.com/miekg/dns/blob/2e4905fb030255032d4343cb83bc2f8c3cfcb82a/LICENSE)：BSD-3-Clause; Go Authors, Miek Gieben and other COPYRIGHT notice holders | isolated DNS transaction/source/question association and cache adoption state machine |
| UpdateRollbackClientReview | P2 | [源码](https://github.com/theupdateframework/python-tuf/tree/1db152642ec023448a9dde7f199ddd63e920a108)、[许可](https://github.com/theupdateframework/python-tuf/blob/1db152642ec023448a9dde7f199ddd63e920a108/LICENSE)：Apache-2.0 | local signed-update persistent-state and version replay validator; no package execution |
| WASIPreopenBoundaryReview | P3 | [源码](https://github.com/bytecodealliance/wasmtime/tree/56f25ee84245686d62922824efa0406a9669af43)、[许可](https://github.com/bytecodealliance/wasmtime/blob/56f25ee84245686d62922824efa0406a9669af43/LICENSE)：Apache-2.0 WITH LLVM-exception per pinned root Cargo.toml; component rights still require review | two-preopen file capability transition model with controlled guest/host comparison |
| WindowsIoctlDispatchReview | P3 | [源码](https://github.com/microsoft/Windows-driver-samples/tree/2dc3fd3a0cc84a2933f2194e7ec0871584979071)、[许可](https://github.com/microsoft/Windows-driver-samples/blob/2dc3fd3a0cc84a2933f2194e7ec0871584979071/LICENSE)：MS-PL; Microsoft | self-written disposable VM test driver and IOCTL access/length dispatch harness |
| KubeAdmissionWebhookBypassReview | P2 | [源码](https://github.com/kubernetes/kubernetes/tree/e7967bb9b76d43a6388abb7a4e90d2f899ef97ff)、[许可](https://github.com/kubernetes/kubernetes/blob/e7967bb9b76d43a6388abb7a4e90d2f899ef97ff/LICENSE)：Apache-2.0 | owned validating/mutating webhook and dynamic admission decision evidence in disposable namespace |
| TLSHandshakeDowngradeReview | P2 | [源码](https://github.com/openssl/openssl/tree/4d25710dbfeacbb36d055592a3bc6811172248b1)、[许可](https://github.com/openssl/openssl/blob/4d25710dbfeacbb36d055592a3bc6811172248b1/LICENSE.txt)：Apache-2.0 | local client/server handshake matrix and transcript invariant checker |

每项新增规格的正负测试、资源限制、来源文件 Git blob 与重叠边界已在本地研究档中冻结；这里只公开选题和有限交付边界。固定上游是研究对照，实际复用任何代码、样例或测试须逐文件复核并保留适用原作者/许可证。尤其 Impacket 含修改版 Apache 1.1 及多项原作者条款，不能将其直接写成 Apache-2.0 或删去通知。

如果真实防御任务不需要其中某题，应合并或撤去，不为凑数拆仓。未来完成代码、构建、CI 和 GitHub 发布仍只证明相应工程范围；CVP 申请事实与官方决定另需独立核对。
