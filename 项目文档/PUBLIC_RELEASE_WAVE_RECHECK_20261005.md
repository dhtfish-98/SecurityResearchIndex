# 公开仓发行波次后再读取（2026-10-05 13:06 UTC）

本页是 13:06:15–13:06:49 UTC 对 GitHub 的逐仓只读、非原子读取；[机器记录](PUBLIC_RELEASE_WAVE_SNAPSHOT_20261005T1306Z.json)绑定每仓读取时的 HEAD、最新 Release 和目录树。它不倒填 10:55 或 12:10 UTC 的冻结快照，也不代替完整源码安全审计、实际部署或 CVP 审批。

- 公开仓 94 个、账号可见私有仓 29 个；91 个软件仓全部已有正式 Release，3 个资料/索引仓没有 Release。
- 91 个软件仓中，87 个最新 Release 标签指向逐仓读取时的 HEAD；4 个落后，分别是 GoCryptoPolicyReview、ObjCAtlas、SealScope、VTableBrook。前两项中的 GoCryptoPolicyReview 与 VTableBrook 涉及新构建暂存/CI 路径，尚需单独版本核对；SealScope 此次比较仅有安全说明链接文字，ObjCAtlas 完整深审此前被系统中断。
- 94/94 个仓有「项目文档」和 `Build`，所读 `Build` 根目录只跟踪 `.gitignore`；91 个软件仓的 HEAD 提交作者/提交者显示名均为 `dhtfish98`。这不证明历史版权均属同一人，也不证明树中每个二进制都是构建产物。
- 91/91 个软件仓的精确 HEAD 有最近成功的工作流。ChromeRelay 与 MachOInspect 的原始汇总仍显示 FAILURE，是较早同 SHA 取消运行保留在汇总中；后来的完整 push 工作流成功，详细运行在机器记录中单列。
- 此前撤出的 14 个仓逐个查询仍为 private（14/14，0 public）；公开机器记录只列统计与审计源摘要，不列私有名称。

35 个因文档集中而改变分发输入的 Python 仓已经分成[第一组 12 仓](MANIFEST12_RELEASES_20261005.json)、[第二组 12 仓](LAG12_RELEASES_20261005.json)及[第三组 11 仓](MANIFEST11C_RELEASES_20261005.json)逐仓重建、安装验证并补发。第三组 11 个 Release 的 `main`/标签同提交，主线及标签 CI 全作业成功；隔离安装测试 296 项、44 个资产回下载逐字节匹配。TufTopLevelReview 与 WebAuthnAssertionReview 的真正上游许可原字节移入「项目文档」并保持构建恢复。20 个优先仓的 10 个后端变化项和 9 个包元数据变化项也已单独补发；ObjCAtlas 保持 OPEN。各批精确范围见[发行增量](PUBLIC_RELEASE_INCREMENT_20261005_AFTER_SNAPSHOT.md)。

[30 个题目槽位](CVP_30_CANDIDATE_TRACKER_20261005.md)仍是 6 个已实现的有条件技术案例和 24 个未实施方向，不能把上述版本维护计作新案例。申请人真实合法防御任务及授权、相关防护影响、身份/组织条件和 Anthropic 决定均未由仓库工程证据确立；CVP 资格与批准仍为 OPEN。
