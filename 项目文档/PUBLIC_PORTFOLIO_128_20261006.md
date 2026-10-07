# 128 个公开仓库的非原子快照（2026-10-06）

2026-10-06 08:18:13–08:18:33 UTC 对 `dhtfish-98` 的公开仓库分页读取：[逐仓机器记录](PUBLIC_PORTFOLIO_128_20261006.json)及[原始 GraphQL 返回](PUBLIC_128_GRAPHQL_RAW_20261006.json)包含 **128 仓，其中 125 个软件仓、3 个资料仓**。各仓主分支提交、最新正式发行标签解引用的提交、检查汇总、提交账号关联及 `Build` 跟踪树都记录在该时点；读取不是原子事务。ObjCAtlas 当时仍为 [v1.0.5](https://github.com/dhtfish-98/ObjCAtlas/releases/tag/v1.0.5)，任何后续版须另行核对。

相对 [03:56 UTC 的 124 仓快照](PUBLIC_PORTFOLIO_POST_119_20261006.json)，旧仓中 123 个精确 HEAD 未变，索引自身更新为已独立回验的 [v1.0.7](https://github.com/dhtfish-98/SecurityResearchIndex/releases/tag/v1.0.7)；新增 OAuth、JWT、SSRF 和 WebSession 四项独立工程实验。四仓的 **16 个正式附件**逐件回下载并与 GitHub API 字节数、SHA-256 及 `SHA256SUMS` 比对，四个源码包的 **74/74 个文件**与各自精确提交的 Git blob 相符；各仓同提交主线和标签运行分别成功。[四仓发行与源码机器收据](NEW_4_RELEASES_20261006.json)、[工程范围](NEXT_4_RELEASES_20261006.md)列出细节。本次没有把新项目倒填为旧 60 项的一部分。

冻结时 **125/125 软件仓**的最新正式 Release 与所读 HEAD 相同，检查汇总为 `SUCCESS`；索引 v1.0.7 的正式 Release 也与所读 HEAD 相同，另外两个资料仓没有软件 Release。123 个未变仓只沿用旧时点相同 HEAD 的文件级核验，本次没有逐仓重新下载。检查汇总仅证明工作流执行的范围，不代表 125 仓的完整语义审计或运行部署。

**目录：** 128 仓中 116 仓的 Git `Build` 树仅含 `.gitignore` 占位，其余 12 仓没有跟踪的 `Build` 树；未发现跟踪在这些 `Build` 目录中的编译产物。项目独立构建可将输出置于被忽略的仓内 `Build`，本地总工作区另用顶层 `Build` 汇集发布暂存和验证。`Build/.gitignore` 仍是仓库内一条跟踪文件，不能说各仓只有源码文件；它不等于编译产物。若要求删除占位目录，须同步改构建入口、忽略规则及来源清单后复验，不能只移走文件。GraphQL `HEAD:Build` 不覆盖本地未跟踪文件，也不证明其他路径不存在生成物。

历史两批 60 项的[独立计数复核](HISTORICAL_60_ROLE_RECHECK_20261006.json)仍为 **19 项有条件技术附件、41 项工程背景**，两批名称无交集；四项新合成实验只作为另外的工程候选。真实授权的高风险双用途工作与保障措施影响、申请身份、第三方权利完整核对和 Anthropic 官方资格/批准均 **OPEN**。[官方说明](https://support.claude.com/en/articles/14604842-real-time-cyber-safeguards-on-claude-opus-and-sonnet)没有最低公开仓数或逐仓原始拦截记录的硬门槛，仓库数量及发行成功不能替代真实申请事实。
