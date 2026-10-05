# 第三批 30 项研究候选的实施进度

本页记录 2026-10-05 15:20 UTC 的增量，不改写 [14:03 UTC 冻结的筛选表](NEW_30_RESEARCH_CANDIDATES_20261005.md)。筛选表中的 30 是题目，不是 30 个已实现、已发布或已获 CVP 认定的项目。

|题目|当前状态|可核查范围|开放事项|
|---|---|---|---|
|RedirectCredentialBoundary|独立重写、本地验证并公开发布 `v0.1.0`|[仓库](https://github.com/dhtfish-98/RedirectCredentialBoundary)、[正式 Release](https://github.com/dhtfish-98/RedirectCredentialBoundary/releases/tag/v0.1.0)；提交 `4dd80a3f326e7b39cfcd1f738a5f002c0fd51e7d` 的[主线 CI](https://github.com/dhtfish-98/RedirectCredentialBoundary/actions/runs/37330921996)和[标签 CI](https://github.com/dhtfish-98/RedirectCredentialBoundary/actions/runs/37331626805)均在 Python 3.11/3.14 成功。本地源码及独立安装的 wheel 各 22 项测试，两个本地 HTTP 来源的对照实验通过；回下载 wheel 与源码包分别与本地资产 SHA-256 一致：`5e55903bb6bcc5119a0c48ba627f5bd07a0e989552afb4fcffbc64bd479d5460`、`50856c80960a5efb1675ed8547154a74353453f6560f02eee177bcf77b4c39eb`。|HTTPS 证书链、代理、IPv6、DNS 重绑定、实际部署及 CVP 资格未验证。上游 urllib3 固定 SHA 是源码研究快照，并非本实验缺陷的修复提交。|
|WebSocketUpgradeOriginGate|本地重写与修订版验证完成，尚未发布|本地原始握手、两来源 Chrome 页面、源码与安装版测试均已通过；独立复审发现的事件错位、未验证头值落日志、预握手超时和文档来源引用已在本地修订并重新验证。|仍需独立复核修订版、公开提交与发行；TLS/WSS、代理和生产会话仍未验证。|
|GraphQLQueryCostGate|本地原型完成；独立复审发现发布阻断，正在修复|合成 GraphQL 查询的成本/解析器调用对照已有本地收据。|大变量导致响应体放大的边界及完整验证脚本哈希尚需修复、重验；未发布。|
|XmlEntityResourceBoundary、PluginHandshakeTrustGate|独立目录内实施中|当前不计完成或验证。|待实现、独立复审与发布门槛。|

新写代码作者字段为 `dhtfish98`；参考上游源码、第三方依赖与许可证按真实关系记载，不把其他作者材料改署为本项目作者。合成弱化基线只用于自有实验，不能证明上游漏洞、申请人真实任务受模型防护影响或官方审批通过。第三批项目目录彼此隔离，不改动另外两个对话所用的旧批次目录。
