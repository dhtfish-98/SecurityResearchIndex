# CVP 官方规则与项目证据核对（2026-10-02）

依据：[Anthropic CVP 帮助页](https://support.claude.com/en/articles/14604842-real-time-cyber-safeguards-on-claude-opus-and-sonnet)、[Anthropic 使用政策](https://www.anthropic.com/legal/aup)。规则可能更新，正式提交前须再次核对申请页面和实际账号。

| 官方要求或边界 | 当前可核实事实 | 状态 |
| --- | --- | --- |
| 当前适用的 Claude 产品与访问渠道须按官方页面核对 | 官方页面目前说明适用于 Opus/Sonnet 类模型，但尚不适用于 Opus 5.5/Sonnet 5.5；第三方平台还需由平台确认 CVP 可用性 | 实际申请渠道 OPEN |
| 有合法防御目的，且实际工作受到网络安全防护对双用途任务的限制 | 14 项替补项目均为本地防御工具；尚未核实与申请人和组织一致的原始受限任务记录，也未核实需要 CVP 调整的高风险双用途场景 | 用途 PASS；CVP 适用性 OPEN |
| CVP 只调整合规双用途任务的限制，禁止用途不因此获准 | 当前替补项目不抓取远端目标、不验证凭据、不执行 PE 输入，也不提供攻击流程 | 当前代码 PASS；具体使用仍须逐次符合政策 |
| 申请需要身份验证，第一方入口由有权限的组织管理员操作 | 仓库和 CI 只能证明代码状态，不能证明申请人身份或管理员权限 | OPEN |
| 授权与申请绑定到实际组织 | 仓库所属 GitHub 用户不等同于 Claude Organization ID | OPEN |
| Zero Data Retention 组织目前不符合 CVP 自助参与条件 | 未在这里检查实际 Claude 组织设置 | OPEN |
| 申请决定由 Anthropic 作出 | 远端提交和 CI 成功仅是工程证据；没有本轮申请决定 | OPEN |

## 项目逐项检查

本轮源码复核及 101 项测试的具体覆盖范围见 [SOURCE_REVIEW_20261002.md](SOURCE_REVIEW_20261002.md)，每个项目自身的限制见 VALIDATION.md。

| 项目 | 代码与来源 | 功能检查 | 远端检查 | 仍需的申请证据 |
| --- | --- | --- | --- | --- |
| [LocalSecretReview](https://github.com/dhtfish-98/LocalSecretReview) | 新实现并完成本轮源码复核；ORIGIN.md 说明来源 | 7 项当前本地测试、命令行检查；1.0.1 wheel 独立安装检查 | 公开 `main`=`31c20173852f24c538182371bb6fe7cff592342d`；[对应 CI 成功](https://github.com/dhtfish-98/LocalSecretReview/actions/runs/36962272270) | 与申请人/组织相符的实际受限合法任务及个人贡献记录 |
| [PEHardeningReview](https://github.com/dhtfish-98/PEHardeningReview) | 新实现并完成本轮源码复核；ORIGIN.md 说明来源 | 6 项当前本地测试、命令行检查；1.0.1 wheel 独立安装检查 | 公开 `main`=`b6bdac35074fd344dadc7a00f39e50bb2430de5b`；[对应 CI 成功](https://github.com/dhtfish-98/PEHardeningReview/actions/runs/36962275907) | 与申请人/组织相符的实际受限合法任务及个人贡献记录 |
| [IAMScopeReview](https://github.com/dhtfish-98/IAMScopeReview) | 新实现并完成本轮源码复核；ORIGIN.md 说明来源 | 8 项当前本地测试、命令行检查 | 公开 `main`=`9bd850f391ec8dfb9e1f435b2575ae23bf74d624`；[对应 CI 成功](https://github.com/dhtfish-98/IAMScopeReview/actions/runs/36962279586) | 与申请人/组织相符的实际受限合法任务及个人贡献记录 |
| [ContainerfileReview](https://github.com/dhtfish-98/ContainerfileReview) | 新实现并完成本轮源码复核；ORIGIN.md 说明来源 | 8 项当前本地测试、命令行检查 | 公开 `main`=`e3bdc360d901c4a87769132542bb8a329f7f8de1`；[对应 CI 成功](https://github.com/dhtfish-98/ContainerfileReview/actions/runs/36962283218) | 与申请人/组织相符的实际受限合法任务及个人贡献记录 |
| [WorkflowPermissionReview](https://github.com/dhtfish-98/WorkflowPermissionReview) | 新实现并完成本轮源码复核；ORIGIN.md 说明来源 | 7 项当前本地测试、命令行检查 | 公开 `main`=`cb7f74f924eb47b025d673b268db5bcf03542dfa`；[对应 CI 成功](https://github.com/dhtfish-98/WorkflowPermissionReview/actions/runs/36962287101) | 与申请人/组织相符的实际受限合法任务及个人贡献记录 |
| [HeaderPolicyReview](https://github.com/dhtfish-98/HeaderPolicyReview) | 新实现并完成本轮源码复核；ORIGIN.md 说明来源 | 8 项当前本地测试、命令行检查 | 公开 `main`=`e66139f8026359781fffae08cc5a644bb5b459dc`；[对应 CI 成功](https://github.com/dhtfish-98/HeaderPolicyReview/actions/runs/36962290931) | 与申请人/组织相符的实际受限合法任务及个人贡献记录 |
| [SBOMFieldReview](https://github.com/dhtfish-98/SBOMFieldReview) | 新实现并完成本轮源码复核；ORIGIN.md 说明来源 | 8 项当前本地测试、命令行检查 | 公开 `main`=`dff819a6802e4eccc3bb50cdfec738052a134acc`；[对应 CI 成功](https://github.com/dhtfish-98/SBOMFieldReview/actions/runs/36962294605) | 与申请人/组织相符的实际受限合法任务及个人贡献记录 |
| [DependencyPinReview](https://github.com/dhtfish-98/DependencyPinReview) | 新实现并完成本轮源码复核；ORIGIN.md 说明来源 | 7 项当前本地测试、命令行检查 | 公开 `main`=`c06cc7f35accaf244fda0eed98c1b2b2b0f2b994`；[对应 CI 成功](https://github.com/dhtfish-98/DependencyPinReview/actions/runs/36962298115) | 与申请人/组织相符的实际受限合法任务及个人贡献记录 |
| [EntitlementFlagReview](https://github.com/dhtfish-98/EntitlementFlagReview) | 新实现并完成本轮源码复核；ORIGIN.md 说明来源 | 6 项当前本地测试、命令行检查 | 公开 `main`=`f25d7ae06242d45f109384c05219f82a4421bc34`；[对应 CI 成功](https://github.com/dhtfish-98/EntitlementFlagReview/actions/runs/36962302027) | 与申请人/组织相符的实际受限合法任务及个人贡献记录 |
| [SSHPolicyReview](https://github.com/dhtfish-98/SSHPolicyReview) | 新实现并完成本轮源码复核；ORIGIN.md 说明来源 | 7 项当前本地测试、命令行检查 | 公开 `main`=`0ad5c5fb2db2b66acc756bc970e6c8683642f00c`；[对应 CI 成功](https://github.com/dhtfish-98/SSHPolicyReview/actions/runs/36962305980) | 与申请人/组织相符的实际受限合法任务及个人贡献记录 |
| [KubePodReview](https://github.com/dhtfish-98/KubePodReview) | 新实现并完成本轮源码复核；ORIGIN.md 说明来源 | 9 项当前本地测试、命令行检查 | 公开 `main`=`80ec45af828d3d5b23f54c1608cdeb5213fd24ac`；[对应 CI 成功](https://github.com/dhtfish-98/KubePodReview/actions/runs/36962309222) | 与申请人/组织相符的实际受限合法任务及个人贡献记录 |
| [ArtifactDigestReview](https://github.com/dhtfish-98/ArtifactDigestReview) | 新实现并完成本轮源码复核；ORIGIN.md 说明来源 | 7 项当前本地测试、命令行检查 | 公开 `main`=`df755ffe1caf9727d7058bf8e9c2c58933aee932`；[对应 CI 成功](https://github.com/dhtfish-98/ArtifactDigestReview/actions/runs/36962312258) | 与申请人/组织相符的实际受限合法任务及个人贡献记录 |
| [AuthLogReview](https://github.com/dhtfish-98/AuthLogReview) | 新实现并完成本轮源码复核；ORIGIN.md 说明来源 | 8 项当前本地测试、命令行检查 | 公开 `main`=`7ad0e361a28bf8453c9fdb08a58f4d23a32b28c5`；[对应 CI 成功](https://github.com/dhtfish-98/AuthLogReview/actions/runs/36962315981) | 与申请人/组织相符的实际受限合法任务及个人贡献记录 |
| [FileModeReview](https://github.com/dhtfish-98/FileModeReview) | 新实现并完成本轮源码复核；ORIGIN.md 说明来源 | 5 项当前本地测试、命令行检查 | 公开 `main`=`289a3cc1f8bb54f6ec914b216d3ab0d5a824ff21`；[对应 CI 成功](https://github.com/dhtfish-98/FileModeReview/actions/runs/36962319942) | 与申请人/组织相符的实际受限合法任务及个人贡献记录 |

测试使用合成或本地输入，不涉及真实第三方目标。CVP 以实际使用场景为依据，不要求制造每个仓库的拦截记录；禁止借用他人账号的拦截或将工程结果写成申请资格。申请产品、渠道、组织、身份和管理员权限仍须按官方当前规则核实。

## 旧项目处置

原 24 项清单中的 14 项已撤出公开组合并转为私有，详见 [项目索引](README.md)。按用户当前决定，这些仓库不永久删除；本地也保留原始交付副本供来源、许可证和历史核对。

## 保留项目能力复核

另 10 项公开研究工具的当前能力、9 项具体运行时或入口改写、来源许可及相符的成功 CI 见 [保留项目复核记录](RETAINED_PROJECT_REVIEW_20261002.md)。其静态解析、文件修改、脚本或辅助执行能力均按实际入口登记；尚继承的核心算法与完整项目重写继续迭代。有限验证不证明所有输入安全或本次申请具备 CVP 资格。
