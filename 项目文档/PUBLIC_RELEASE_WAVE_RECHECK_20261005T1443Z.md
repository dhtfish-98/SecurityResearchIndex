# 公开仓发行与目录复核（2026-10-05 14:43–14:44 UTC）

本页绑定 14:43:34–14:44:09 UTC 的非原子逐仓读取。[逐仓机器快照](PUBLIC_RELEASE_WAVE_SNAPSHOT_20261005T1443Z.json)保留每仓所读 HEAD、最新 Release、目录和检查状态；早期快照均保留其自身时点。

- 账号可见公开仓 94、私有仓 29；91 个软件仓均有正式 Release，**91 个最新标签与所读主分支同提交**。3 个资料仓没有 Release。旧撤出组 14/14 仍为私有。
- 所读 94/94 仓均有「项目文档」，且 `Build` 根目录只跟踪 `.gitignore`；91/91 软件 HEAD 的提交作者和提交者显示名为 `dhtfish98`。继承的第三方版权和许可证继续保留。
- 91/91 软件 HEAD 有有效成功的精确提交 CI。ChromeRelay、MachOInspect 的 GraphQL 汇总仍保留较早同提交取消运行的失败状态，较新的完整 push 工作流成功；快照保存两种状态供复核。

从 [14:13 UTC 快照](PUBLIC_RELEASE_WAVE_RECHECK_20261005T1413Z.md)之后，[ArchiveLens v1.0.6](https://github.com/dhtfish-98/ArchiveLens/releases/tag/v1.0.6)修复五个在旧版复现的输入边界问题，[ObjCAtlas v1.0.1](https://github.com/dhtfish-98/ObjCAtlas/releases/tag/v1.0.1)同步现行源码目录并纠正两处过时说明。这两版的精确提交 CI、源码归档、发行附件及权利文件核对分别见[ArchiveLens 收据](ARCHIVELENS_V1_0_6_RELEASE_20261005.json)和[ObjCAtlas 收据](OBJCATLAS_V1_0_1_RELEASE_20261005.json)。ObjCAtlas 没有新增 Objective-C/C 运行源码修改，也没有上传新二进制。

这次关闭的是最新 Release 标签与所读 HEAD 的**发行同步**，不等于 91 个仓的语义安全深审已完成。ObjCAtlas 的完整 Xcode/Pods/CoreData/dSYM、设备运行和先前被中断的深审继续 OPEN；ArchiveLens 五项以外的真实 GUI/设备场景也未由这次回归覆盖。PEQuarry 旧阶段 3 的私有来源与公开范围冲突仍待独立解决。[第三批 30 项新候选](NEW_30_RESEARCH_CANDIDATES_20261005.md)不是这 91 个现有 Release 的一部分，真实授权任务与 CVP 审批仍须另行核对。
