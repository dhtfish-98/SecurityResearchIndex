# 公开防御项目再审计（2026-10-04）

本报告以[逐仓冻结记录](PUBLIC_PORTFOLIO_RECHECK_20261004.json)的观察窗口和各仓精确提交为准。它核对公开 GitHub 的默认分支、完整跟踪文件树、当前提交署名、该提交的工作流及最新正式 Release；它不是全部项目的运行时安全审计，也不是 CVP 批准结果。后续推送须另按新提交复核。

| 项目用途 | 数量 | 申请材料处理 |
| --- | ---: | --- |
| 已实现的条件技术案例 | 6 | 只在能对应本人真实、获授权且受网络安全防护影响的防御任务时使用；资格仍 OPEN。 |
| 技术研究暂缓 | 8 | 已记录的问题、审计或发布边界未闭合，暂不作主案例。 |
| 防御工程背景 | 71 | 可证明工程经历，不把普通静态检查器等同高风险双用途任务。 |
| 有明确派生来源的通用工具 | 2 | ImageQuay、KernelCabinet 不作“独立重写”主案例，保留上游权利。 |
| 通用浏览器自动化背景 | 2 | 不作主 CVP 资格证据。 |
| 非网络安全背景 | 2 | CDTranslator、SILGallery 不作主 CVP 资格证据。 |
| 资料仓 | 3 | 不计作独立软件项目。 |

[30 题目研究池 R2](PROJECT_30_RESEARCH_POOL_R2_20261004.md)由上述 **6 个已有条件案例**和 **24 个未实现的研究规格**组成。24 个规格还没有独立代码、测试、仓库或正式发行；30 不是官方仓库数门槛，也不等于 30 个已符合申请要求的项目。原 18 个初筛案例经[代码级再筛](CVP_CODE_SCOPE_RECHECK_20261004.md)收紧：10 个归工程背景，2 个有派生来源的工具退出独立重写主池。本轮再次按六仓当前源码入口、固定来源和精确提交 CI 核对，维持“有条件案例”分类；实际防护影响与申请资格仍待本人和官方核实。

冻结记录中，94 个公开仓均可完整读取且无截断树；91 个软件仓在各自**当前精确提交**的 GitHub Actions 均成功，3 个资料仓无工作流。94 个当前提交的 Git 显示名均为 `dhtfish98`，GitHub 作者及提交者账号均关联仓库所有者 `dhtfish-98`。这只说明当前提交元数据，不会改写历史作者或改变真实第三方权利。仓内跟踪的 ImageQuay `checks/bins/testlib1.dylib` 是被测试引用的固定夹具，并非新编译输出。PEQuarry 的三份根目录历史报告因公开发布边界仍未迁移；其源码 1.0.3 与最新正式 Release v1.0.2 不一致，继续 OPEN。

77 个仓有正式 Release。其中 72 个可独立读取标签内产品版本的仓，其标签内源码版本均与 Release 版本一致；另 5 个缺少可直接提取的独立产品版本字段，保持版本验证边界。ArchiveLens 的 [v1.0.3 源码发行](https://github.com/dhtfish-98/ArchiveLens/releases/tag/v1.0.3)和 SILGallery 的 [v1.0.4 源码发行](https://github.com/dhtfish-98/SILGallery/releases/tag/v1.0.4)均有标签、源码资产与构建范围证据。SILGallery v1.0.3 曾遗漏无效 UTF-8 解码扩张造成的二次分配预算问题，已在旧发行说明标为被 v1.0.4 取代；v1.0.4 从公开基线补上解码前的可见 UTF-8 预算检查与 11 MiB 反例，并让默认 Xcode 测试进入 [精确提交 CI](https://github.com/dhtfish-98/SILGallery/actions/runs/37192047491)，[发行说明](https://github.com/dhtfish-98/SILGallery/releases/tag/v1.0.4)列出验证范围。该工具仍属一般开发辅助背景，手工 GUI 验收保持 OPEN。其历史 v1.0.2 标签提交曾被 GitHub 关联到另一个名为 `dhtfish98` 的账号，发行说明已勘误，旧标签和资产未改。PEQuarry 的 v1.0.3 未正式发行，不能把 main 的版本字符串当成发布。

来源清单已按当前提交再核：ObjCAtlas 的完整文件清单已重建；DOMSinkReview、GoCryptoPolicyReview 的旧路径和 UnicodeSourceReview 的行数元数据已修正。A64Dispatch、ChromeRelay、MachOInspect 的旧本地清单保留原字节，现行说明明确它们是历史交付快照、不能证明当前 HEAD。上述六个仓库各自新提交的工作流均成功。另八份现行正式源码清单的已列文件哈希准确，但未列非运行源码的 `Build/.gitignore`，因此不能将它们解释成完整 Git 跟踪文件清单。

本轮已识别的第三方版权、许可证和来源继续随项目保存；潜在未识别权利仍需逐文件核查。只对确属当前自有维护内容的显示名使用 `dhtfish98`。构建、打包、CI、GitHub 发布、合法授权任务、实际防护影响和 Anthropic 审核属于不同证据层级。按[Anthropic 当前 CVP 说明](https://support.claude.com/en/articles/14604842-real-time-cyber-safeguards-on-claude-opus-and-sonnet)，Claude.ai / Claude Code 可走第一方验证门户，但仅授权管理员可见申请入口，提交需要身份验证；ZDR 组织当前不符合参与资格。真实防御用途、适用组织、模型和官方决定仍须申请人实际核对。该说明当前还明确**不适用于 Opus 5.5 与 Sonnet 5.5**，未来扩展不能当作已生效；没有逐仓拦截截图不构成本报告所设的硬性门槛，也不能虚构“已受影响”。

ArchiveLens 的六项、BranchLoom 的一项、TabWeave 的一项旧程序观察，以及 12 个较大项目被中断的完整深审继续 OPEN。普通 CI 成功并未关闭这些事项。
