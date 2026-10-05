# 115 个公开仓续审：ImageQuay 源码版发行后

**非原子读取窗口：2026-10-05 22:54:41–22:54:53 UTC。**[新逐仓矩阵](PUBLIC_115_POST_IMAGEQUAY_METADATA_20261006.json)重新读取全部 115 个公开仓的 HEAD、账号关联、检查汇总和最新发行。与[上一轮 115 仓冻结矩阵](PUBLIC_115_CURRENT_METADATA_20261006.json)相比，只有 ImageQuay 和本索引仓的 HEAD／最新发行改变；其余 113 仓的精确提交未变，沿用上一轮树、标签和工作流核查。两处变更另查公开树、注释标签和发行证据。发布本索引新版本会再次移动索引仓 HEAD，因此本报告只代表上述读取窗口。

| 核对项 | 冻结结果 |
| --- | --- |
| 公开仓 | 115：112 软件、3 资料或索引 |
| 当前 HEAD 作者／提交者账号关联 | 115/115 为 `dhtfish-98`；这只证明当前提交元数据，不证明历史与全部实际创作者 |
| 软件最新正式 Release 与所读 HEAD | 112/112 同提交 |
| 软件 HEAD 工作流 | 112/112 主线成功；90 仓另有同提交标签成功，22 仓仅配置主线触发 |
| 文档与 Build 跟踪树 | 115/115 有「项目文档」；114 仓的 `Build` 只跟踪 `.gitignore`，PgPoolPrincipalIsolation 在构建时创建忽略的 Build |
| 已识别当前跟踪编译路径 | 路径及已知夹具清单复核为 0；无扩展名文件的全字节识别仍 OPEN |
| 第三批固定 30 项 | 21/30 有正式发行；9 项未发行，和历史另一个 30 项分别计数 |

[ImageQuay v1.0.9](https://github.com/dhtfish-98/ImageQuay/releases/tag/v1.0.9) 对应提交 `a1089c4f2b1b360dc7f017121dc8c6aef667b536`。此前跟踪的 `checks/bins/testbin1`、`testbin1.fat`、`testbin1.signed`、`testlib1.dylib` 四个编译夹具已从当前树移除；新的源码、wheel 与 sdist 均未包含编译夹具。保留注明来源的上游测试源码，生成物只落在忽略的 Build。GitHub 使用 Xcode 27.0 编译后得到不同字节，明确记录差异，并从固定的旧公开提交取出四个原测试输入；每份均经既有整文件 SHA-256 核验后才放入 Build。这是测试资料的历史回退，不代表跨机器逐字节可重现编译。[主线 CI](https://github.com/dhtfish-98/ImageQuay/actions/runs/37384397862)和[标签 CI](https://github.com/dhtfish-98/ImageQuay/actions/runs/37384712494)均在该 SHA 成功，记录 387 项测试、822 次上游对照、安装后消费和六项 CLI 流程。四个正式附件回下载与本地准备品逐字节相同，见[发行收据](IMAGEQUAY_V1_0_9_RELEASE_20261006.json)。1.0.8 只有失败的标签检查，没有正式 Release；保留该历史事实，不把它当作已交付版本。

本索引仓的 [v1.0.0](https://github.com/dhtfish-98/SecurityResearchIndex/releases/tag/v1.0.0) 也已按提交 `a9b781a52e95b2356a1aec8bfd56659ff81db311` 正式发行；它是资料仓，无 CI，附件回下载与源码文件核查见[自身发行收据](SECURITY_RESEARCH_INDEX_V1_0_0_RELEASE_20261006.json)。旧 115 矩阵读到的是索引发行前的 HEAD，历史记录保留原样。

**发现一处公开材料矛盾，待负责对话更新：**FederatedConnectorIdentityGate 的 [v0.1.0](https://github.com/dhtfish-98/FederatedConnectorIdentityGate/releases/tag/v0.1.0)、主线和标签 CI 已在同一提交成功，但该提交的 README、DESIGN 与 VALIDATION 仍把公开仓、CI 或正式发行写为 OPEN。此处只需按已证实的状态修文档，不能把本轮未做的附件回下载或 CVP 资格写成已通过。该仓由另一个仍在处理它的对话负责，本轮不并行改动；精确链接与范围见[申请材料只读分层复核](PUBLIC_115_CVP_CLAIM_TRIAGE_20261006.md)。

这是公开目录、身份、版本及检查状态的复核，并补充了 ImageQuay 的独立验证；**不是**其余 111 个软件仓的逐函数深审或全部历史权利鉴定。已有针对性修复不能替代整仓审计。派生项目继续保留真正上游作者、版权与许可证，新写部分由 `dhtfish98` 署名；改名或当前提交账号关联不产生原始权利。申请方面，官方[现行 CVP 说明](https://support.claude.com/en/articles/14604842-real-time-cyber-safeguards-on-claude-opus-and-sonnet)没有“30 仓”或逐仓拒绝日志硬门槛。实际授权工作、申请人账号和组织、相关保障措施影响及最终批准均 **OPEN**；21 个正式版本只是工程交付计数，不是 21 个官方合格案例。
