# 防御项目源码复核记录（2026-10-02）

本轮复核覆盖 14 个替补项目的分析器、读取入口、命令行、测试、依赖、工作流、来源说明和使用边界。此前的绿色测试未覆盖下面这些输入，不能作为完整复核的证明；本轮已经补上对应行为和回归测试。

| 项目或范围 | 复核发现 | 当前行为 |
| --- | --- | --- |
| IAMScopeReview | 错误类型的 Action 可返回空结果；Allow 的补集字段未充分提示 | 校验字段类型和互斥关系；NotAction、NotResource、NotPrincipal 给出范围复核提示 |
| WorkflowPermissionReview | 非字符串触发器导致未捕获异常；重复 YAML 键可覆盖先前值 | 拒绝无效触发器、权限值和重复键；按工作流或作业的显式权限处理继承 |
| KubePodReview | 字符串形式的 privileged 可被当作安全；未检查初始化与临时容器 | 验证声明类型，检查常规、初始化、临时容器，并检查 UID 0、显式添加能力和主机命名空间 |
| SBOMFieldReview | 嵌套组件不参与组件字段及引用集合 | 收集元数据根组件和嵌套组件，复核字段与依赖引用 |
| ContainerfileReview | USER 0:组名会漏检；阶段继承和 heredoc 内容可能误读 | 识别 UID 0、已知阶段 USER 继承、有效摘要、逃逸指令和常见 heredoc；不执行构建 |
| HeaderPolicyReview | 空 CSP 可返回空结果；重复响应头被覆盖 | 复核空 CSP、重复安全响应头、HSTS 声明及 HAR 的 HTML MIME 信息 |
| DependencyPinReview | ==1.* 被当作精确锁定 | 使用 packaging 解析直接依赖；通配符、非精确版本、无效语法和未解析来源给出提示 |
| EntitlementFlagReview | 安全 entitlement 的字符串值可返回空结果 | 布尔字段类型必须正确；重复 plist 键及损坏 XML/二进制输入明确报错 |
| SSHPolicyReview | 引号包裹的 yes 漏检；Include/Match 检查不完整时仍可能显示空结果 | 解析引号和等号；Include 明确标为未解析，Match 声明提供复核提示，不推断实际匹配结果 |
| AuthLogReview | 极端时区转换可能抛出未捕获异常；隐藏身份后的分组不便定位 | 无效时间和空身份字段明确报错；失败频次提示输出原文件行号，不输出身份字段 |
| FileModeReview | .env.production 等常见变体未纳入敏感文件名检查 | 纳入 .env.*；说明仅报告权限位，目录读取错误仍然报错 |
| 13 个读取文件内容的项目 | 先检查大小再整文件读取，无法保证实际读取上限 | 在同一常规文件描述符上检查类型并按字节上限读取；特殊文件和直接符号链接被拒绝 |
| LocalSecretReview | 不可读取或跳过文件仍可能用退出码 0 表示结束；JSON 引号键覆盖不足 | 检查不完整时退出码为 2；保留发现元数据并继续脱敏，补充 JSON 键和常见凭据形态 |
| PEHardeningReview | 文件读取上限需要在读取时生效 | 描述符读取与头部解析两处都限制输入大小；输出仍仅表示加固位声明 |
| 6 个 JSON 分析器 | 重复对象键及非标准数字可造成解释歧义 | 拒绝重复键、NaN/Infinity，限制容器嵌套为 128 层 |

本地 Python 3.14.6 的当前测试共 101 项通过，各仓库的 VALIDATION.md 记录各自范围。LocalSecretReview 和 PEHardeningReview 的 1.0.1 wheel 还在独立 Python 3.12 环境中安装并运行；包内五个源码文件与当前源码逐字节一致。凭据样本全部为合成值，PE32/PE32+ 样本只读未执行。每个公开提交与相应 GitHub 工作流的结果在项目索引中记录。

本轮代码和文档由 Codex 按仓库所有者的指示辅助编写与修改，个人贡献仍须由实际申请人核实。

本轮检查确认这些实现用于本地防御复核，没有加入攻击目标访问、凭据验证、漏洞利用或攻击载荷生成。它们仍有明确的静态检查边界，测试通过不能证明生产系统安全。

[Anthropic 官方 CVP 规则](https://support.claude.com/en/articles/14604842-real-time-cyber-safeguards-on-claude-opus-and-sonnet)要求合法防御用途确实受到网络安全防护影响，并与实际申请人和组织相符。当前未收到与申请人和组织一致的实际受限任务记录，因此 CVP 申请条件仍为 OPEN。源码改写、仓库数量和自动测试不能替代这一事实，也不能保证模型永远不触发防护。
