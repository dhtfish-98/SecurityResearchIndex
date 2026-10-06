# 119 个公开仓续审：Container 发行与 Rootless 环境实验

**冻结点：2026-10-06 约 01:09 UTC，非原子读取。** [119 仓逐仓矩阵](PUBLIC_119_POST_CONTAINER_METADATA_20261006.json)读取公开仓的当前 HEAD、最新 Release 和检查汇总；原始 GraphQL 快照作为本索引 v1.0.5 的发行附件保留，SHA-256 `3b8f187c7fb28f339dcb682ab618fa312c22399a603ee8bd61a8033880882e10`。以前次 117 仓矩阵的精确提交证据为基准比较：此前 117 仓仅索引自身由 v1.0.3 前进到 v1.0.4，其余 HEAD 和最新版本未变；新增 ContainerCapabilityDropGate、RootlessIdMapBoundary。沿用旧提交的源码路径、标签与 CI 记录是增量复核，**不是 116 个软件仓的全量语义深审**。

| 冻结范围 | 结果 |
| --- | --- |
| 公开仓 | 119：116 软件、3 资料或索引 |
| 当前 HEAD 作者和提交者账号关联 | 119/119 为 `dhtfish-98`；当前元数据不能代替历史版权或自然人贡献鉴定 |
| 软件最新正式 Release 与所读 HEAD | 115/116；Rootless 当前无 Release |
| 软件所读 HEAD 的主线 CI 成功 | 115/116；Rootless 当前真实内核作业失败 |
| 软件同提交标签 CI 成功 | 93/116；其中 23 个没有成功标签运行，含只配置主线的 22 仓和未发行的 Rootless |
| 文档和构建目录 | 119/119 有「项目文档」；116 仓的 `Build` 仅跟踪 `.gitignore`，另 3 软件仓在运行时创建 Build |
| 已识别跟踪编译产物路径 | 0；无扩展名文件的全量逐字节识别仍 OPEN |
| 第三批固定 30 题 | **24 项正式发行、6 项待完成**；项目数不等于 CVP 获批数 |

[ContainerCapabilityDropGate v0.1.0](https://github.com/dhtfish-98/ContainerCapabilityDropGate/releases/tag/v0.1.0) 绑定提交 `c2a49435bdf40ca7892c064151cad8a8dd41fa46`。同提交[主线](https://github.com/dhtfish-98/ContainerCapabilityDropGate/actions/runs/37396568344)与[标签](https://github.com/dhtfish-98/ContainerCapabilityDropGate/actions/runs/37396721905)各五项检查成功；真实 Linux/runc 的受限 `run-exec`、越权拒绝和直接 runc 合成对照均有原始日志。四个正式附件回下载摘要、19 个源码包文件、同提交本地 ARM64 VM 和独立复核见[发行收据](CONTAINER_V0_1_0_RELEASE_20261006.json)。其输入限于已审查的可信自有 OCI bundle；hooks、mounts 和 `root.path` 不审查，创建记录与实际运行容器的生产绑定、远端分支/标签保护及 CVP 资格仍 OPEN。上游 runc Apache-2.0 许可与原 NOTICE 均保留，不能因为自有门禁代码重写而删除上游权利。

[RootlessIdMapBoundary](https://github.com/dhtfish-98/RootlessIdMapBoundary) 在此冻结点的公开 HEAD `e13d308611935bc48b230aa7ba173588cfa65f43` 只完成源码公开与本地 Linux VM 复核。[首次公开运行](https://github.com/dhtfish-98/RootlessIdMapBoundary/actions/runs/37395533872)在用户命名空间映射预检失败；[修订后运行](https://github.com/dhtfish-98/RootlessIdMapBoundary/actions/runs/37397219635)已证明临时 AppArmor profile 加载和附着、`0:1000:1` 映射预检通过，但真实文件权限探针在执行阶段失败，最终回执为 FAIL。后续诊断版[运行 37398156021](https://github.com/dhtfish-98/RootlessIdMapBoundary/actions/runs/37398156021)明确发现测试身份无法遍历 `/home/runner`，仍未完成正式探针；**不计入 24 项正式发行**，未创建标签或 Release。

历史接管的另外 30 项仍按[再筛结果](HISTORICAL_30_CVP_HANDOVER_RECHECK_20261005.md)分为 6 项有条件技术附件和 24 项工程背景；六项定向深审和 CITrustBoundaryReview v0.1.4 修复在此前记录中，不把工程背景硬凑为申请合格案例。申请渠道为 Claude.ai / Claude Code。[Anthropic 官方 CVP 指引](https://support.claude.com/en/articles/14604842-real-time-cyber-safeguards-on-claude-opus-and-sonnet)列出第一方 Verification Portal、授权管理员与身份验证路径，没有规定 30 个 GitHub 仓或每个项目的拒绝/降级日志为硬门槛。合法防御用途、申请主体及官方审核结果仍 OPEN；源码、作者字段、测试和发行各只证明其限定的工程事实。
