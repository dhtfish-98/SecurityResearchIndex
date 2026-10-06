# 119 个公开仓续审：Rootless 正式发行

**冻结读取：2026-10-06 01:33:34–01:33:49 UTC，非原子。** [119 仓逐仓矩阵](PUBLIC_119_POST_ROOTLESS_METADATA_20261006.json)重新读取全部公开 HEAD、最新 Release 与检查汇总；原始 GraphQL 冻结件作为本索引 v1.0.5 的发行附件，SHA-256 `686d70778bca7fa601f4165de660c00d1065bff27d9699f71370172a7ff8a0da`。与[前次 119 仓冻结](PUBLIC_119_POST_CONTAINER_STATUS_20261006.md)逐仓比较，**只有 RootlessIdMapBoundary 的 HEAD 和最新版本变化**。其余 118 仓的先前精确树、标签和 CI 结果沿用；这是增量元数据复核，不是所有软件的全量语义深审。

| 冻结范围 | 结果 |
| --- | --- |
| 公开仓 | 119：116 软件、3 资料或索引 |
| 当前 HEAD 作者和提交者账号关联 | 119/119 为 `dhtfish-98`；这不证明历史或自然人创作 |
| 软件最新正式 Release 与所读 HEAD | 116/116 |
| 软件所读 HEAD 的主线 CI 成功 | 116/116 |
| 软件同提交标签 CI 成功 | 94/116；其余 22 仓只有主线成功运行 |
| 目录和跟踪编译产物 | 119/119 有「项目文档」；116 仓 `Build` 只跟踪 `.gitignore`，另外 3 软件仓运行时建立 Build；已识别跟踪编译产物路径为 0 |
| 第三批固定 30 题 | **25 项正式发行、5 项待完成**；发行数不是 CVP 合格或获批数 |

[RootlessIdMapBoundary v0.1.0](https://github.com/dhtfish-98/RootlessIdMapBoundary/releases/tag/v0.1.0) 的注解标签和 `main` 都指向 `708811e9ec24bd9b5fe28ed2e56efe5c2b7666e1`。[主线检查](https://github.com/dhtfish-98/RootlessIdMapBoundary/actions/runs/37398953021)与[标签检查](https://github.com/dhtfish-98/RootlessIdMapBoundary/actions/runs/37399263180)均有两项成功作业和实际 Ubuntu 内核的七模式 UID/GID、文件权限对照。临时 `/home/runner` ACL 的原始与恢复文件逐字节相同；AppArmor profile 实际附着，卸载命令成功，但卸载后内核状态缺独立快照。21 个源码包文件和 47 个证据包成员已核对；四个发行附件回下载摘要与 GitHub 摘要一致。完整限定与[发行收据](ROOTLESS_V0_1_0_RELEASE_20261006.json)对应。本实验只覆盖自建单映射，不证明完整 RootlessKit、容器生产隔离或上游缺陷。

其余五项为 BuildSecretMountLifetimeGate、CsiSecretNamespaceGate、RemoteDesktopTransferGate、WireGuardPeerPrefixBinding、XlmFormulaTrace。BuildSecret 正在本地独立审查，真实 BuildKit 合成对照未完成；XLM 仅有[本地严格 OOXML 候选](XLM_LOCAL_V0_2_0_STRICT_FINAL_20261006.json)，Excel 打开/执行和 BIFF 范围未验证；另外三项仍需可运行实验。未发行项目不计为已完成。历史接管的另外 30 项维持[六项有条件技术附件、24 项工程背景](HISTORICAL_30_CVP_HANDOVER_RECHECK_20261005.md)的审计分类。

申请渠道为 Claude.ai / Claude Code。[Anthropic 当前 CVP 说明](https://support.claude.com/en/articles/14604842-real-time-cyber-safeguards-on-claude-opus-and-sonnet)没有把 30 个仓或每项目拒绝日志列为硬性门槛；授权申请、身份验证、真实合法防御任务、保障机制影响及官方审核仍须由实际申请材料证明。自有重写文件使用 dhtfish98 归属；引用或依赖的第三方权利与许可证保持原样，不能因重写而删除真实上游声明。

**未关闭的全局审计边界：** 全部 116 个软件仓的完整源码语义深审、无扩展名文件的逐字节分类、第三方历史权利深查、远端分支/标签保护及官方 CVP 结论。
