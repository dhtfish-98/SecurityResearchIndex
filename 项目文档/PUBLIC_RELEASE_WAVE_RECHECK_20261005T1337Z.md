# 公开仓发行与目录复核（2026-10-05 13:37 UTC）

本页对应 13:37:28–13:38:02 UTC 的逐仓非原子 GitHub 读取；[机器快照](PUBLIC_RELEASE_WAVE_SNAPSHOT_20261005T1337Z.json)保留每仓当时的主分支提交、最新正式发行、目录树和检查状态。此前 10:55、12:10、13:06 UTC 的快照各有自己的时间边界，均未倒改。

- 账号可见公开仓 94、私有仓 29；其中 91 个软件仓全部有 Release，3 个资料仓没有 Release。91 个软件仓中 90 个最新 Release 标签与所读主分支是同一提交；唯一差异是 ObjCAtlas（`main` 为 `329fc1ab…`，最新 v1.0.0 标签较早）。
- 94/94 个仓有「项目文档」与 `Build`；所读 `Build` 根目录仅跟踪 `.gitignore`。91 个软件仓当前 HEAD 的提交作者、提交者显示名均为 `dhtfish98`。这不改变旧贡献者的版权或第三方许可证。
- 91/91 个软件仓的当前 HEAD 均有有效成功的精确提交自动检查。ChromeRelay、MachOInspect 的汇总还保留较早同提交取消运行的 FAILURE，较新的完整 push 工作流成功，快照单列了例外运行。此前撤出的 14 个仓在本次查询中仍为私有，0 个公开。

这次关闭三个先前发行滞后项：[SealScope v0.2.2](https://github.com/dhtfish-98/SealScope/releases/tag/v0.2.2)、[GoCryptoPolicyReview v0.1.3](https://github.com/dhtfish-98/GoCryptoPolicyReview/releases/tag/v0.1.3) 和 [VTableBrook v1.0.2](https://github.com/dhtfish-98/VTableBrook/releases/tag/v1.0.2)。[DOMSinkReview v0.1.5](https://github.com/dhtfish-98/DOMSinkReview/releases/tag/v0.1.5) 另修复包内 NOTICE 的旧版本号；其运行源码和 Acorn 原版权/许可未改。逐仓主线/标签检查与包/源码回下载范围见[发行增量](PUBLIC_RELEASE_INCREMENT_20261005_AFTER_SNAPSHOT.md)。

ObjCAtlas 的大文本清单已独立补扫，但先前中断的完整深审仍未恢复，不能把发行标签落后当成已核清的发布候选。旧 PEQuarry 阶段 3 的私有范围/来源冲突和自动公开发布拒绝同样未解除。上述目录、版本、作者显示名和自动检查是工程状态，不证明完整安全代码审计、实际环境效果或 CVP 审批。[30 项队列](CVP_30_CANDIDATE_TRACKER_20261005.md)仍区分已实现条件案例与未实现方向；官方[CVP 说明](https://support.claude.com/en/articles/14604842-real-time-cyber-safeguards-on-claude-opus-and-sonnet)未规定 30 仓或逐仓拦截记录为硬性申请附件。
