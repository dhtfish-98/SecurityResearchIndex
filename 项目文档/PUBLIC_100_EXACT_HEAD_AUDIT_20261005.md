# 100 个公开仓库的精确提交目录与署名复核（2026-10-05）

这次以 16:30:08–16:30:43 UTC 的[非原子 GitHub 快照](PUBLIC_100_METADATA_20261005.json)为冻结基准，对 100 个公开仓的同一提交做跟踪树、路径和文本关键词复核。[逐仓脱敏矩阵](PUBLIC_100_EXACT_HEAD_TEXT_PATH_AUDIT_20261005.json)合并 95 个本地精确结账与 5 个单独抓取的缺口仓，覆盖 4,041 条跟踪文件路径。此后新增的 AcmeChallengeAuthorization、RelationAccessDecision 不倒填进 100 仓冻结数。

冻结时 97 个软件仓均有最新 Release 与所读 HEAD 同提交，精确 HEAD 的最新有效 CI 均成功；100/100 仓把文档放在「项目文档」，Git 跟踪的 `Build` 路径仅 `.gitignore`。97/97 个软件仓的精确提交树均有许可证或权利文件；三个资料/索引仓没有单独权利文件，不能从缺省文件推断其内容可任意再许可。该窗口软件仓 HEAD 的提交作者/提交者显示名均为 `dhtfish98`。

本次已读文本的 AI/Codex/Claude 等命中均经上下文分类：官方 CVP 说明、实际功能名称、上游文件路径或历史证据；未确认将 AI/Codex 记作代码作者。一个 PEHardeningReview 规则候选是官方说明句的误报。真实继承或捆绑的第三方版权和许可证仍应保留，维护者显示名与原始权利归属分别记录。ImageQuay 的 `checks/bins/testlib1.dylib` 是有文档和测试引用的解析夹具；本轮没有反编译其字节，不能将它等同于一般构建输出。

发现 ArchiveLens、ObjCAtlas 的 `项目文档/ORIGIN.md` 各混入其他项目的模板权利句，现已分别在 [ArchiveLens v1.0.7](https://github.com/dhtfish-98/ArchiveLens/releases/tag/v1.0.7) 和 [ObjCAtlas v1.0.2](https://github.com/dhtfish-98/ObjCAtlas/releases/tag/v1.0.2) 更正。两版的运行源码未改，主线和标签检查成功，源码附件回下载与提交包一致；[发行收据](ORIGIN_DOC_CORRECTIONS_PUBLIC_RELEASES_20261005.json)逐项列出提交、版本、检查和 SHA-256。JRBusiness/REipa、nygard/class-dump 与实际第三方权利记录保留。

这项检查只证明冻结提交的跟踪路径、可读文本模式、浅层发行元数据和两处文档修正。二进制内容、历史对象、全部运行分支、设备/真实部署及此前被系统中断的深层代码审计仍未由此关闭。仓库数量和 CI 通过也不证明 CVP 资格；真实授权任务、受保障措施影响、申请人身份与官方审查结果仍须单独如实核对。
