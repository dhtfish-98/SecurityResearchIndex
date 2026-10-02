# CVP 官方规则与项目证据核对（2026-10-02）

依据：[Anthropic CVP 帮助页](https://support.claude.com/en/articles/14604842-real-time-cyber-safeguards-on-claude-opus-and-sonnet)、[Anthropic 使用政策](https://www.anthropic.com/legal/aup)。规则可能更新，正式提交前须再次核对申请页面和实际账号。

| 官方要求或边界 | 当前可核实事实 | 状态 |
| --- | --- | --- |
| 有合法防御目的，且实际工作受到网络安全防护对双用途任务的限制 | 两个新项目均为本地、只读或脱敏防御工具；目前没有与它们对应的 Claude 拦截记录 | 用途 PASS；受限事实 OPEN |
| CVP 只调整合规双用途任务的限制，禁止用途不因此获准 | 当前源码不抓取远端目标、不验证凭据、不执行 PE 输入，也不提供攻击流程 | 当前代码 PASS；具体使用仍须逐次符合政策 |
| 申请需要身份验证，第一方入口由有权限的组织管理员操作 | 仓库和 CI 只能证明代码状态，不能证明申请人身份或管理员权限 | OPEN |
| 授权与申请绑定到实际组织 | 仓库所属 GitHub 用户不等同于 Claude Organization ID | OPEN |
| Zero Data Retention 组织目前不符合 CVP 自助参与条件 | 未在这里检查实际 Claude 组织设置 | OPEN |
| 申请决定由 Anthropic 作出 | 远端提交和 CI 成功仅是工程证据；没有本轮申请决定 | OPEN |

## 项目逐项检查

| 项目 | 代码与来源 | 功能检查 | 远端检查 | 仍需的申请证据 |
| --- | --- | --- | --- | --- |
| [LocalSecretReview](https://github.com/dhtfish-98/LocalSecretReview) | 12 个提交文件，独立新实现；`ORIGIN.md` 说明旧版 SecretCanopy 的关系 | 4 项测试通过；独立 wheel 安装及合成值脱敏检查通过；具体边界见仓库 `VALIDATION.md` | 公开 `main`=`d8e2adc8b291b0b95165e13fdbe38b1723019f08`；[对应 CI 成功](https://github.com/dhtfish-98/LocalSecretReview/actions/runs/36958515545) | 同一申请人/组织的真实受限任务记录 |
| [PEHardeningReview](https://github.com/dhtfish-98/PEHardeningReview) | 12 个提交文件，独立新实现；参考微软 PE 格式规范，未复制 PEQuarry 源码 | 4 项测试通过；独立 wheel 安装和本地 PE32/PE32+ 样本只读检查通过；具体边界见仓库 `VALIDATION.md` | 公开 `main`=`1a3e548587ac4a6de9132dc77195cf5f4855f004`；[对应 CI 成功](https://github.com/dhtfish-98/PEHardeningReview/actions/runs/36958531631) | 同一申请人/组织的真实受限任务记录 |

两项工具都不证明凭据有效、PE 运行时保护生效或漏洞存在。测试样本不涉及真实第三方目标。GitHub 项目历史、他人账号的拦截、旧的申请草稿或第三方成功案例不能代替本次账号与组织的事实记录。

## 旧项目处置

原 24 项清单中的 14 项已撤出公开组合并转为私有，详见 [项目索引](CVP_PROJECT_INDEX.md)。当前 GitHub 命令行凭据缺少 `delete_repo` 权限，因此仓库还未永久删除；本地保留原始交付副本供来源、许可证和历史核对。
