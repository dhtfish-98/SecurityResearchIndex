# 公开仓发行后再读取（2026-10-05 12:10 UTC）

[逐仓机器快照](PUBLIC_POSTRELEASE_SNAPSHOT_20261005T1210Z.json)在 12:10:23–12:10:58 UTC 逐仓读取，不是原子快照。它复核 GitHub 可见性、目录、当前主分支、最新正式 Release 与对应提交的检查状态；没有重跑所有源码功能测试或完整安全深审。旧 10:55 UTC [文本扫描](PUBLIC_PORTFOLIO_RECHECK_20261005.md)覆盖 3,813 个文本文件、跳过 93 个二进制/超大文件；本次没有重复该文本扫描。

- 仍为 94 个公开仓、29 个可见私有仓；91 个软件仓全部已有正式 Release，3 个资料/索引仓没有 Release。旧撤出的 14 个仓逐个复核，**14/14 仍为 private，0 public**；公开记录仅保留数量，不列其名称。
- 94/94 仓有「项目文档」和 `Build`，所查 `Build` 根目录只跟踪 `.gitignore`。这不把 ImageQuay 等测试用二进制夹具误认作新编译输出，也不证明运行时安装或完整源码布局无其他问题。
- 对应每仓读取时 HEAD，40 个软件仓最新 Release 标签指向同提交，51 个标签落后；历史 Release 仍是原标签的有效快照，但不能声称覆盖后来 HEAD。今日补发的项目应以各自独立发行收据为准，不能倒改 10:55 UTC 的 9/68 和 14 无 Release 计数。余下 51 个差异还需按文档、打包、验证与运行源码逐类判断，不能仅因标签落后就判定程序未发布。
- 91 个软件仓的当前提交均有成功的后续完整工作流。GitHub GraphQL 汇总中 ChromeRelay 和 MachOInspect 两仓显示 `FAILURE`，因为同一提交保留了较早 `cancelled` 的重复运行；两仓较新的完整运行分别为 [ChromeRelay 37306426521](https://github.com/dhtfish-98/ChromeRelay/actions/runs/37306426521) 与 [MachOInspect 37306354420](https://github.com/dhtfish-98/MachOInspect/actions/runs/37306354420)，均为 `success`。所以不能把原始 rollup 简写为 91/91 全绿，也不能把旧取消当成新测试失败。
- 相比 10:55 UTC 快照，33 个仓的 HEAD 有变动，逐项落在本轮已知维护范围；没有发现其他意外变动。此项只表示对比时点的仓库列表，不说明历史私有来源适合公开，也不说明任何项目获得 CVP 资格。

[30 项候选状态](CVP_30_CANDIDATE_TRACKER_20261005.md)仍为 6 个已实现的条件案例加 24 个未实施方向。工程发行、作者显示、仓库公开数量及 CI 成功都不能代替申请人的真实授权任务、身份/组织条件或 Anthropic 的审批。

## 12:19–12:20 UTC 的剩余差异逐仓分类

[独立的 39 仓只读比较](REMAINING39_RELEASE_TRIAGE_20261005.json)在各仓当时 HEAD/旧 Release 未变的窗口下完成。35 个 Python 项目虽然主要运行源码路径未变，但 `pyproject.toml` 和 `MANIFEST.in` 因文档集中而改变了分发输入；其旧 Release 仍代表旧标签，**新 HEAD 的包版本同步须逐仓重建、验证后再发布**。另 4 仓 GoCryptoPolicyReview、VTableBrook、HeaderPolicyReview、SealScope 的所查差异起初属文档/构建包装或自有署名文本，其中 HeaderPolicyReview 的旧 Release 未包含当前自有版权显示名，已另发 [v0.1.4 源码版](HEADERPOLICY_V0_1_4_RELEASE_20261005.json)。其余三个旧标签仍是历史有效发行，不能声称与后来 HEAD 完全相同。39 仓比较不包括另外 20 个验证/构建差异优先仓及 12:10 快照后新发行的提交；不把 35 个待补版本写为已完成。

此前 94 仓内容扫描跳过 93 个二进制或超大文件，其中只有 ObjCAtlas 的 `RENAME_MAP.json` 是超大文本，其余 92 个是图片、归档、IDB/i64 或其他二进制夹具。[该 JSON 的补充读取](OBJCATLAS_OVERSIZE_TEXT_SCAN_20261005.json)绑定当时远端 `main` 提交 `329fc1ab2c3518bd506b0040616943ba278c9950`，可完整解析，作者/版权/许可与 AI、Codex、Claude、OpenAI 等所查字样均无命中。这只补齐该文本遗漏；不等同于对二进制内容、旧历史对象或 ObjCAtlas 完整代码深审的结论。

后续 35 个打包输入差异仓分三组完成版本同步；[13:06 UTC 独立再读取](PUBLIC_RELEASE_WAVE_RECHECK_20261005.md)显示 91 个软件仓中 87 个最新标签等于所读 HEAD、4 个仍落后。该后续窗口与本页 12:10 UTC 计数分别保留，不改写旧结果。
