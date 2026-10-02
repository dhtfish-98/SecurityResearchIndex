# CVP 官方规则与项目证据核对（2026-10-02）

依据：[Anthropic CVP 帮助页](https://support.claude.com/en/articles/14604842-real-time-cyber-safeguards-on-claude-opus-and-sonnet)、[Anthropic 使用政策](https://www.anthropic.com/legal/aup)。规则可能更新，正式提交前须再次核对申请页面和实际账号。

| 官方要求或边界 | 当前可核实事实 | 状态 |
| --- | --- | --- |
| 当前适用的 Claude 产品与访问渠道须按官方页面核对 | 官方页面目前说明适用于 Opus/Sonnet 类模型，但尚不适用于 Opus 5.5/Sonnet 5.5；第三方平台还需由平台确认 CVP 可用性 | 实际申请渠道 OPEN |
| 有合法防御目的，且实际工作受到网络安全防护对双用途任务的限制 | 14 项替补项目均为本地、只读或脱敏防御工具；目前没有与它们对应的 Claude 拦截记录 | 用途 PASS；受限事实 OPEN |
| CVP 只调整合规双用途任务的限制，禁止用途不因此获准 | 当前替补项目不抓取远端目标、不验证凭据、不执行 PE 输入，也不提供攻击流程 | 当前代码 PASS；具体使用仍须逐次符合政策 |
| 申请需要身份验证，第一方入口由有权限的组织管理员操作 | 仓库和 CI 只能证明代码状态，不能证明申请人身份或管理员权限 | OPEN |
| 授权与申请绑定到实际组织 | 仓库所属 GitHub 用户不等同于 Claude Organization ID | OPEN |
| Zero Data Retention 组织目前不符合 CVP 自助参与条件 | 未在这里检查实际 Claude 组织设置 | OPEN |
| 申请决定由 Anthropic 作出 | 远端提交和 CI 成功仅是工程证据；没有本轮申请决定 | OPEN |

## 项目逐项检查

| 项目 | 代码与来源 | 功能检查 | 远端检查 | 仍需的申请证据 |
| --- | --- | --- | --- | --- |
| [LocalSecretReview](https://github.com/dhtfish-98/LocalSecretReview) | 独立新实现；`ORIGIN.md` 说明来源与边界 | 4 项测试、独立 wheel 安装与合成值脱敏检查；详细限制见 `VALIDATION.md` | 公开 `main`=`d8e2adc8b291b0b95165e13fdbe38b1723019f08`；[对应 CI 成功](https://github.com/dhtfish-98/LocalSecretReview/actions/runs/36958515545) | 同一申请人/组织的真实受限任务记录 |
| [PEHardeningReview](https://github.com/dhtfish-98/PEHardeningReview) | 独立新实现；`ORIGIN.md` 说明来源与边界 | 4 项测试、独立 wheel 安装与 PE32/PE32+ 样本检查；详细限制见 `VALIDATION.md` | 公开 `main`=`1a3e548587ac4a6de9132dc77195cf5f4855f004`；[对应 CI 成功](https://github.com/dhtfish-98/PEHardeningReview/actions/runs/36958531631) | 同一申请人/组织的真实受限任务记录 |
| [IAMScopeReview](https://github.com/dhtfish-98/IAMScopeReview) | 独立新实现；`ORIGIN.md` 说明来源与边界 | 4 项本地测试、命令行合成输入检查；详细限制见 `VALIDATION.md` | 公开 `main`=`e9b33a528dab2f11bc63ea67fdb4e6f9a4c694ca`；[对应 CI 成功](https://github.com/dhtfish-98/IAMScopeReview/actions/runs/36959756905) | 同一申请人/组织的真实受限任务记录 |
| [ContainerfileReview](https://github.com/dhtfish-98/ContainerfileReview) | 独立新实现；`ORIGIN.md` 说明来源与边界 | 4 项本地测试、命令行合成输入检查；详细限制见 `VALIDATION.md` | 公开 `main`=`a827c69e0e0157c659eace10f7c1a382664e343a`；[对应 CI 成功](https://github.com/dhtfish-98/ContainerfileReview/actions/runs/36959784288) | 同一申请人/组织的真实受限任务记录 |
| [WorkflowPermissionReview](https://github.com/dhtfish-98/WorkflowPermissionReview) | 独立新实现；`ORIGIN.md` 说明来源与边界 | 4 项本地测试、命令行合成输入检查；详细限制见 `VALIDATION.md` | 公开 `main`=`76f19240cc994fd49aef351bf848fbbdb896ea78`；[对应 CI 成功](https://github.com/dhtfish-98/WorkflowPermissionReview/actions/runs/36959791948) | 同一申请人/组织的真实受限任务记录 |
| [HeaderPolicyReview](https://github.com/dhtfish-98/HeaderPolicyReview) | 独立新实现；`ORIGIN.md` 说明来源与边界 | 4 项本地测试、命令行合成输入检查；详细限制见 `VALIDATION.md` | 公开 `main`=`6862447d57c19a97cc61bf0ed6ce6479567c15c9`；[对应 CI 成功](https://github.com/dhtfish-98/HeaderPolicyReview/actions/runs/36959971283) | 同一申请人/组织的真实受限任务记录 |
| [SBOMFieldReview](https://github.com/dhtfish-98/SBOMFieldReview) | 独立新实现；`ORIGIN.md` 说明来源与边界 | 5 项本地测试、命令行合成输入检查；详细限制见 `VALIDATION.md` | 公开 `main`=`daecd73b81808bde944b19898708054f8b5b29a3`；[对应 CI 成功](https://github.com/dhtfish-98/SBOMFieldReview/actions/runs/36959973426) | 同一申请人/组织的真实受限任务记录 |
| [DependencyPinReview](https://github.com/dhtfish-98/DependencyPinReview) | 独立新实现；`ORIGIN.md` 说明来源与边界 | 4 项本地测试、命令行合成输入检查；详细限制见 `VALIDATION.md` | 公开 `main`=`1f19613d6f261520f61fd78cadbd2d859a69bca8`；[对应 CI 成功](https://github.com/dhtfish-98/DependencyPinReview/actions/runs/36959968772) | 同一申请人/组织的真实受限任务记录 |
| [EntitlementFlagReview](https://github.com/dhtfish-98/EntitlementFlagReview) | 独立新实现；`ORIGIN.md` 说明来源与边界 | 4 项本地测试、XML/二进制 plist 与命令行检查；详细限制见 `VALIDATION.md` | 公开 `main`=`bbbfa77c7b0f058506b606ade52429debdc1e14e`；[对应 CI 成功](https://github.com/dhtfish-98/EntitlementFlagReview/actions/runs/36959825321) | 同一申请人/组织的真实受限任务记录 |
| [SSHPolicyReview](https://github.com/dhtfish-98/SSHPolicyReview) | 独立新实现；`ORIGIN.md` 说明来源与边界 | 4 项本地测试、命令行合成输入检查；详细限制见 `VALIDATION.md` | 公开 `main`=`9ab591c4bda93325033cdae2e522bd79b4ff1e00`；[对应 CI 成功](https://github.com/dhtfish-98/SSHPolicyReview/actions/runs/36959832514) | 同一申请人/组织的真实受限任务记录 |
| [KubePodReview](https://github.com/dhtfish-98/KubePodReview) | 独立新实现；`ORIGIN.md` 说明来源与边界 | 4 项本地测试、命令行合成输入检查；详细限制见 `VALIDATION.md` | 公开 `main`=`c3b6f9f814dd134ce2bbd38ea20af0c9546c1bc1`；[对应 CI 成功](https://github.com/dhtfish-98/KubePodReview/actions/runs/36959842924) | 同一申请人/组织的真实受限任务记录 |
| [ArtifactDigestReview](https://github.com/dhtfish-98/ArtifactDigestReview) | 独立新实现；`ORIGIN.md` 说明来源与边界 | 4 项本地测试、命令行合成文件检查；详细限制见 `VALIDATION.md` | 公开 `main`=`678f0304c91ea2767b39c972354165a168f6da7f`；[对应 CI 成功](https://github.com/dhtfish-98/ArtifactDigestReview/actions/runs/36959852089) | 同一申请人/组织的真实受限任务记录 |
| [AuthLogReview](https://github.com/dhtfish-98/AuthLogReview) | 独立新实现；`ORIGIN.md` 说明来源与边界 | 4 项本地测试、命令行合成日志检查；详细限制见 `VALIDATION.md` | 公开 `main`=`c0277d919eae5315f9f3d45f5c5d453e9931a457`；[对应 CI 成功](https://github.com/dhtfish-98/AuthLogReview/actions/runs/36959860264) | 同一申请人/组织的真实受限任务记录 |
| [FileModeReview](https://github.com/dhtfish-98/FileModeReview) | 独立新实现；`ORIGIN.md` 说明来源与边界 | 4 项本地测试、命令行合成目录检查；详细限制见 `VALIDATION.md` | 公开 `main`=`bebb1ec79472ca36694ccf8c66926b2fc2cc52e3`；[对应 CI 成功](https://github.com/dhtfish-98/FileModeReview/actions/runs/36959870958) | 同一申请人/组织的真实受限任务记录 |

以上测试均使用合成或本地输入，不涉及真实第三方目标。GitHub 项目历史、他人账号的拦截、旧的申请草稿或第三方成功案例不能代替本次账号与组织的事实记录。申请前还需复核所用 Claude 产品是否处在官方当前支持范围；仓库数量本身不是 CVP 标准。

## 旧项目处置

原 24 项清单中的 14 项已撤出公开组合并转为私有，详见 [项目索引](README.md)。按用户当前决定，这些仓库不永久删除；本地也保留原始交付副本供来源、许可证和历史核对。
