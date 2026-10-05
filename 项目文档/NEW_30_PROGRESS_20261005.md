# 第三批 30 项研究候选的实施进度

本页记录 2026-10-05 15:20 UTC 的增量，不改写 [14:03 UTC 冻结的筛选表](NEW_30_RESEARCH_CANDIDATES_20261005.md)。筛选表中的 30 是题目，不是 30 个已实现、已发布或已获 CVP 认定的项目。

|题目|当前状态|可核查范围|开放事项|
|---|---|---|---|
|RedirectCredentialBoundary|独立重写、本地验证并公开发布 `v0.1.0`|[仓库](https://github.com/dhtfish-98/RedirectCredentialBoundary)、[正式 Release](https://github.com/dhtfish-98/RedirectCredentialBoundary/releases/tag/v0.1.0)；提交 `4dd80a3f326e7b39cfcd1f738a5f002c0fd51e7d` 的[主线 CI](https://github.com/dhtfish-98/RedirectCredentialBoundary/actions/runs/37330921996)和[标签 CI](https://github.com/dhtfish-98/RedirectCredentialBoundary/actions/runs/37331626805)均在 Python 3.11/3.14 成功。本地源码及独立安装的 wheel 各 22 项测试，两个本地 HTTP 来源的对照实验通过；回下载 wheel 与源码包分别与本地资产 SHA-256 一致：`5e55903bb6bcc5119a0c48ba627f5bd07a0e989552afb4fcffbc64bd479d5460`、`50856c80960a5efb1675ed8547154a74353453f6560f02eee177bcf77b4c39eb`。|HTTPS 证书链、代理、IPv6、DNS 重绑定、实际部署及 CVP 资格未验证。上游 urllib3 固定 SHA 是源码研究快照，并非本实验缺陷的修复提交。|
|WebSocketUpgradeOriginGate|本地重写与修订版验证完成，尚未发布|本地原始握手、两来源 Chrome 页面、源码与安装版测试均已通过；独立复审发现的事件错位、未验证头值落日志、预握手超时和文档来源引用已在本地修订并重新验证。|仍需独立复核修订版、公开提交与发行；TLS/WSS、代理和生产会话仍未验证。|
|GraphQLQueryCostGate|本地原型完成；独立复审发现发布阻断，正在修复|合成 GraphQL 查询的成本/解析器调用对照已有本地收据。|大变量导致响应体放大的边界及完整验证脚本哈希尚需修复、重验；未发布。|
|XmlEntityResourceBoundary、PluginHandshakeTrustGate|独立目录内实施中|当前不计完成或验证。|待实现、独立复审与发布门槛。|

新写代码作者字段为 `dhtfish98`；参考上游源码、第三方依赖与许可证按真实关系记载，不把其他作者材料改署为本项目作者。合成弱化基线只用于自有实验，不能证明上游漏洞、申请人真实任务受模型防护影响或官方审批通过。第三批项目目录彼此隔离，不改动另外两个对话所用的旧批次目录。

## 15:46 UTC 发行增量

上述 15:20 UTC 表格保留原时点。此后又有两项从本地验收进入正式 GitHub Release：

|项目|版本与精确提交|核对结果|仍未证明|
|---|---|---|---|
|[WebSocketUpgradeOriginGate](https://github.com/dhtfish-98/WebSocketUpgradeOriginGate)|[v0.1.0](https://github.com/dhtfish-98/WebSocketUpgradeOriginGate/releases/tag/v0.1.0)，`9840fb8832fa7ad4e401a67b6853f79e37bcd326`|[主线 CI](https://github.com/dhtfish-98/WebSocketUpgradeOriginGate/actions/runs/37333512683)、[标签 CI](https://github.com/dhtfish-98/WebSocketUpgradeOriginGate/actions/runs/37334555749)均在 macOS/Python 3.11、3.14 成功，包含真 Chrome 两来源实验；本地源码/安装版各 13 项测试。回下载 wheel 和源码包 SHA-256 分别为 `6ad319d9c5ec87d38913b01d9da6edce62958eef65aae2b017ab0b187c9b8966`、`de806554c52ec18f3f8584787dd0dc8d2755cdda4bf6c233d87fb645393d2000`，与准备包一致。|WSS、代理、并发上限、生产会话和 CVP 资格。|
|[GraphQLQueryCostGate](https://github.com/dhtfish-98/GraphQLQueryCostGate)|[v0.1.0](https://github.com/dhtfish-98/GraphQLQueryCostGate/releases/tag/v0.1.0)，`98395957ff8407e991a07c79fcc6b5c05f57780c`|[主线 CI](https://github.com/dhtfish-98/GraphQLQueryCostGate/actions/runs/37334817059)、[标签 CI](https://github.com/dhtfish-98/GraphQLQueryCostGate/actions/runs/37335120728)均在 Node 22、24 成功；本地 15 项测试、四组成对 HTTP 对照及两项资源限额回归，独立安装消费者通过。原 28 KB 变量放大请求现在在 0 次解析器调用前拒绝；回下载源码包 SHA-256 `ab6503f299815b2092ccd8ef3abfc6d1b23f417bf7af7b817291ef418e58f08d` 与本地一致，GraphQL-JS 原 MIT 权利随包保留。|响应大小限制在执行后生效，不能当峰值内存上限；真实部署、通用 schema 和 CVP 资格仍 OPEN。|

截至这次增量，第三批 30 个题目中**3 项正式发布、2 项本地实现但有待修复/复核、1 项在独立目录实施、24 项尚未实施**；并非 30 项均符合 CVP。该账号公开仓库数现为 97，其中旧 94 仓快照仍只覆盖其原读取时点。XmlEntityResourceBoundary 的参数实体/重复声明预算和 PluginHandshakeTrustGate 的包内构建及插件端准入边界仍在修订，尚未发布。

## 16:06 UTC 目录补丁、版本对齐和全公开仓复核

前三项新仓库已各自发布 `v0.1.1`：本次只补齐 GitHub 跟踪树中的 `Build/.gitignore`，并将包、测试和文档版本对齐；防御运行逻辑未变。每项 `main`、标签、最新 Release 均指向同一提交，精确提交的主线与标签 CI 均成功，正式附件回下载与构建包及 GitHub 资产摘要一致。逐项机器收据见 [三仓补丁发行](THREE_PUBLIC_PATCH_RELEASES_20261005.json)。

|项目|当前版本、提交与 CI|正式附件 SHA-256|
|---|---|---|
|[RedirectCredentialBoundary](https://github.com/dhtfish-98/RedirectCredentialBoundary)|[v0.1.1](https://github.com/dhtfish-98/RedirectCredentialBoundary/releases/tag/v0.1.1)，`7802a8dc27c9eaf1718127815f14d0c2946490fd`；[主线](https://github.com/dhtfish-98/RedirectCredentialBoundary/actions/runs/37337268661)、[标签](https://github.com/dhtfish-98/RedirectCredentialBoundary/actions/runs/37337306331)|wheel `e25a37047faef195f4ed5eaea2eddc42263894aab4832b0c025c11de8d6019d2`；sdist `c263c31bdf42ebc1814bd71de3b75937a34f7cd3d39eaa9e61fde3987d704cde`|
|[WebSocketUpgradeOriginGate](https://github.com/dhtfish-98/WebSocketUpgradeOriginGate)|[v0.1.1](https://github.com/dhtfish-98/WebSocketUpgradeOriginGate/releases/tag/v0.1.1)，`0f666f636cf0d33e9cbcccf5f3c2c54f917349b2`；[主线](https://github.com/dhtfish-98/WebSocketUpgradeOriginGate/actions/runs/37337268749)、[标签](https://github.com/dhtfish-98/WebSocketUpgradeOriginGate/actions/runs/37337307354)|wheel `759aa33ac1bfab9a23fa71bf4095aa761155893470146711d81ef0b897213d58`；sdist `0f8d24461e8c45c09168a38f416327b041d0e8fec53c5cfb6f65f0f49269c4fb`|
|[GraphQLQueryCostGate](https://github.com/dhtfish-98/GraphQLQueryCostGate)|[v0.1.1](https://github.com/dhtfish-98/GraphQLQueryCostGate/releases/tag/v0.1.1)，`27d57114d032f4a04bd06fb99620045fa0e856a8`；[主线](https://github.com/dhtfish-98/GraphQLQueryCostGate/actions/runs/37337268977)、[标签](https://github.com/dhtfish-98/GraphQLQueryCostGate/actions/runs/37337307612)|npm 源码包 `e3bde415c0a56f259c2749965cee38e40e77e17203676e5acb37835b53d50b2e`|

[97 个公开仓库的非原子元数据快照](PUBLIC_97_METADATA_20261005.json)读取于 16:05–16:06 UTC：97/97 有「项目文档」目录，97/97 的 `Build` 跟踪树仅有 `.gitignore`；94 个软件仓各有 Release，94/94 最新标签与各自所读主分支 HEAD 同提交，94/94 精确 HEAD 的最新有效工作流成功。另 3 个资料仓无 Release。ChromeRelay 与 MachOInspect 的较早取消/失败记录仍使 GraphQL 聚合状态显示失败，逐工作流同 SHA 最新成功运行另有记录；不能抹除旧历史。旧撤出组 14/14 仍 private。该快照只读取仓库元数据及根目录布局，不是 94 个软件的全量语义、版权或构建产物深审。

XmlEntityResourceBoundary、PluginHandshakeTrustGate、ProxyIdentityHeaderTrust 已各自完成本地修复与独立技术复核，正在准备独立公开仓验收；尚无 GitHub Release。第三批 30 题目当前仍为 **3 项正式发布、3 项本地通过、24 项未实施**，不是 30 个符合 CVP 申请要求的证明。申请人的真实授权工作、组织身份及官方审批继续 OPEN。

## 16:30 UTC 第二组三项正式发行

XmlEntityResourceBoundary、ProxyIdentityHeaderTrust、PluginHandshakeTrustGate 均在本地修复、独立复审、仓内验收后各自建立公开仓并正式发布 `v0.1.0`。这三个仓的防御实现、测试及文档分别留在原有源码路径和「项目文档」，GitHub 跟踪树中的 `Build` 仅有 `.gitignore`。提交作者与包作者为 `dhtfish98`；上游真实权利和来源不改署为新项目作者。

|项目|精确提交与公开验证|附件回下载 SHA-256|
|---|---|---|
|[XmlEntityResourceBoundary](https://github.com/dhtfish-98/XmlEntityResourceBoundary)|[v0.1.0](https://github.com/dhtfish-98/XmlEntityResourceBoundary/releases/tag/v0.1.0)，`ee05d37a617e6b989eff10f53cc69fccd4f47afa`；[主线](https://github.com/dhtfish-98/XmlEntityResourceBoundary/actions/runs/37339560041)、[标签](https://github.com/dhtfish-98/XmlEntityResourceBoundary/actions/runs/37339746184) Python 3.11/3.14 成功；31 项源码和 31 项安装版测试、合成外部实体/膨胀对照通过。|wheel `808c7f0db01f4bdd82b0965f75f2782ed546a151666f86bd91ef656ef2225638`；sdist `5e96d75aa2ac4e59d84f8b20717ab31a652d9c27c7a4f1dd91aa194ce30dc6f7`，详见[双仓发行收据](XML_PROXY_PUBLIC_RELEASES_20261005.json)。|
|[ProxyIdentityHeaderTrust](https://github.com/dhtfish-98/ProxyIdentityHeaderTrust)|[v0.1.0](https://github.com/dhtfish-98/ProxyIdentityHeaderTrust/releases/tag/v0.1.0)，`8c3866dae7aa5ea2f3e9b94c9fd606d62e60ef3e`；[主线](https://github.com/dhtfish-98/ProxyIdentityHeaderTrust/actions/runs/37339668484)、[标签](https://github.com/dhtfish-98/ProxyIdentityHeaderTrust/actions/runs/37339966693) Python 3.11/3.14 成功；20 项源码和 20 项安装版测试、四类真实本机请求及非 ASCII 输入回归通过。|wheel `3baaa455e09b46afcf3bd86857c535e631fed9f1f0b7a18441437a8c95cd781e`；sdist `25001c20cdd1540904fe75d6d53c80a31195dc42e1b51ac130be5ac10b0964d0`，详见[双仓发行收据](XML_PROXY_PUBLIC_RELEASES_20261005.json)。|
|[PluginHandshakeTrustGate](https://github.com/dhtfish-98/PluginHandshakeTrustGate)|[v0.1.0](https://github.com/dhtfish-98/PluginHandshakeTrustGate/releases/tag/v0.1.0)，`83f085a446a6378f75d03c4d907e0d7deb0e2557`；[主线](https://github.com/dhtfish-98/PluginHandshakeTrustGate/actions/runs/37340440335)、[标签](https://github.com/dhtfish-98/PluginHandshakeTrustGate/actions/runs/37340983240) Go 1.24/1.26 成功；11 组真实子进程/客户端对照及解包重跑通过。|源码包 `0e12e7924e66c6244542de2a01b266d6e5d04aac75b311100033a8cd7abda1a3`，见[插件发行收据](PLUGIN_PUBLIC_RELEASE_20261005.json)。|

[100 个公开仓的非原子元数据快照](PUBLIC_100_METADATA_20261005.json)读取于 16:30 UTC：100/100 有「项目文档」，`Build` 跟踪树仅 `.gitignore`；97 个软件仓 97/97 有 Release、最新标签与各自所读 HEAD 同提交、精确 HEAD 最新有效工作流成功，HEAD 作者及提交者显示名均为 `dhtfish98`。另 3 个资料仓无 Release；旧撤出组 14/14 保持 private。ChromeRelay/MachOInspect 较早失败/取消聚合记录仍保留；本快照不等于逐仓语义、运行、权利深审。

第三批 30 题目现为 **6 项已正式发布，3 项在隔离目录实施，21 项尚未实施**。公开实验不证明参考上游存在漏洞，也不能证明 CVP 申请人真实用途、所受保障措施影响或官方审批。

## 17:20 UTC 两项新发行与 100 仓文本/路径复核

[AcmeChallengeAuthorization v0.1.0](https://github.com/dhtfish-98/AcmeChallengeAuthorization/releases/tag/v0.1.0) 在提交 `9b3661613b9a40c5b104f71532c49d462491b3de` 的主线和标签 CI 均成功；正式 wheel/sdist 回下载 SHA-256 分别为 `75dabb70ac5bdba4c540b1a85cd156815673fe9e20447d9f4fdc0b080bea8f59`、`6f8199675249926425b657c1adb6888f1d9b596e26407ab02aee75d7bd5039cf`。两实例并发挑战仅消费一次，签名期间过期不入库，独立 X.509 链、SAN 和序列号核验通过。账户 ID 由可信测试调用方传入，未实现 JWS/会话身份认证。

[RelationAccessDecision v0.1.0](https://github.com/dhtfish-98/RelationAccessDecision/releases/tag/v0.1.0) 在提交 `f6b1b67f365a791fc20f988da5c64b7634c07e1c` 的主线和标签 CI 均成功；正式 wheel/sdist 回下载 SHA-256 分别为 `d9bf9994b241fde41d3aa64653246f35d75400b7d969953a90f7590a58394c52`、`30e10497f7238cbb4431079d62bd05c17c861824cc931d2ff87dcdac82a25a58`。源码与安装版各 61 条 HTTP 决策事件相同，正式 wheel 无故意弱缓存。外部调用方仍可自带其他 store，实验不能证明任意应用安全。

两仓的[公开发行收据](NEW_30_RELEASES_7_9_20261005.json)记录精确 CI 和资产摘要。第三批现为 **8/30 已正式发行**，RefreshTokenReuseRevocation 与 SshCertIssuanceGate 本地验收后仍在独立终审，其余 20 项未实施。此时账号公开仓数为 102；此前 [100 仓冻结复核](PUBLIC_100_EXACT_HEAD_AUDIT_20261005.md)不含新两仓。所有新项目仍是自有合成实验，不证明上游漏洞、真实部署或 CVP 获批。

## 18:21 UTC 刷新令牌与 SSH 用户证书两项正式发行

[RefreshTokenReuseRevocation v0.1.0](https://github.com/dhtfish-98/RefreshTokenReuseRevocation/releases/tag/v0.1.0) 发布于提交 `9e7267507d91e85059297984935b0fe1fa60384a`；[主线](https://github.com/dhtfish-98/RefreshTokenReuseRevocation/actions/runs/37349978138)及[标签 CI](https://github.com/dhtfish-98/RefreshTokenReuseRevocation/actions/runs/37350259469)均精确提交成功。源码、解包 sdist、隔离 wheel 各 11 项测试及各 9 项本机 HTTP/SQLite 实验通过；正式 wheel 无故意弱基线。wheel/sdist 回下载 SHA-256 为 `a0860269b2cbb110ee1ec4d48446830913a3f4daed8898ba86a4683c32748a17`、`d7dc71d309dbe1e0c3a3caa33fe1a20a334fd330d1df84a29bf06be4a286ab4f`。真实 OAuth 身份、TLS、生产部署均不在本实验范围。

[SshCertIssuanceGate v0.1.0](https://github.com/dhtfish-98/SshCertIssuanceGate/releases/tag/v0.1.0) 发布于提交 `454993dee1c3eb90dcd829428fa2ebfdfbd4fda5`；[主线](https://github.com/dhtfish-98/SshCertIssuanceGate/actions/runs/37350176592)及[标签 CI](https://github.com/dhtfish-98/SshCertIssuanceGate/actions/runs/37354655181)的 Python 3.11/3.14 作业均成功。源码、解包 sdist、隔离 wheel 各 16 项测试和 16 项签发/独立验签对照通过；wheel 无弱基线与私钥。wheel/sdist 回下载 SHA-256 为 `b5379fa79b854f0573ef6211fb826d3f9883e724e614959eca87cc80c8da5c07`、`8e20c3a98b1e3a249b2552bcbcb20dfb7b7c612b08ebf673d29e9e330a854a49`。真实 `sshd` 登录、外部身份与持钥证明仍 OPEN。

两仓均是独立新写的自有实验，固定上游仅为范围参考，原第三方版权与许可归原权利人；逐项[脱敏发行收据](NEW_30_RELEASES_8_10_20261005.json)保留精确 CI 与资产摘要。账号此时为 **104 个公开仓，第三批 10/30 已发行**。18:20–18:21 UTC 的[104 仓非原子元数据快照](PUBLIC_104_METADATA_20261005.json)显示 101 个软件仓的最新 Release 与各自所读 HEAD 同提交、有效精确 CI 成功，104/104 仓有「项目文档」且 Build 跟踪树仅 `.gitignore`；另外 3 个资料仓无 Release。早期取消/失败运行及快照后可能的新提交仍按各自时间解释。RecoveryCodeAccountBinding 与 SftpHandlePermissionGate 正在独立实施，其余 18 项未实施。CVP 资格和真实受影响任务仍 OPEN。

## 19:00 UTC 三项新发行与 107 仓续审

[SftpHandlePermissionGate v0.1.0](https://github.com/dhtfish-98/SftpHandlePermissionGate/releases/tag/v0.1.0)、[RecoveryCodeAccountBinding v0.1.0](https://github.com/dhtfish-98/RecoveryCodeAccountBinding/releases/tag/v0.1.0)、[JupyterKernelOriginGate v0.1.0](https://github.com/dhtfish-98/JupyterKernelOriginGate/releases/tag/v0.1.0)已分别从自有源码完成正式发行。三项各自的主分支、注释标签和最新 Release 均对应同一精确提交，主分支与标签 CI 均成功；正式附件回下载与本地构建结果、GitHub 摘要一致。提交及包作者为 `dhtfish98`，第三方来源与权利按真实关系记载。逐项提交、CI、资产摘要和实验限制见[三项发行收据](NEW_30_RELEASES_11_13_20261005.json)。

SFTP 实验以真实回环 SFTP v3 服务验证句柄授权，不代表外部服务器。恢复码实验包含自有账户绑定实现，以及单独运行的固定 Kratos 上游参考实验；该包未集成到 Kratos，真实身份与邮箱所有权未验证。Jupyter 实验以真实内核和 REST/WebSocket 请求验证单用户无浏览器场景的 Origin 限制；Origin 不是原生客户端身份凭据。三项都不证明上游存在漏洞、生产部署安全或 CVP 获批。

第三批至此 **13/30 已正式发行**，其余 17 项仍在候选、实施或审查阶段。[107 个公开仓的非原子元数据快照](PUBLIC_107_METADATA_20261005.json)读取于 18:58–18:59 UTC：104 个软件仓的最新 Release 均与各自所读 HEAD 同提交，104/104 精确 HEAD 的有效 CI 成功；107/107 有「项目文档」，`Build` 跟踪树仅 `.gitignore`。旧撤出组 14/14 仍为私有。角色整理见[107 仓 CVP 材料矩阵](PUBLIC_107_CVP_MATERIAL_RECHECK_20261005.json)：13 个新增实验与 6 个旧条件技术案例均仅为有条件材料，实际资格、授权任务与官方决定仍 OPEN。元数据和材料角色核对不能替代 107 仓逐文件语义深审。

[ObjCAtlas v1.0.3](https://github.com/dhtfish-98/ObjCAtlas/releases/tag/v1.0.3)同期完成有界 Mach-O 游标、段与链接编辑范围修复，源码归档、主线/标签 CI、39 项原有与 39 项维护测试、9 个合成畸形样例均按[定向修复收据](OBJCATLAS_V1_0_3_RELEASE_20261005.json)核对。它是保留真实上游权利的派生工具，不计为独立新写 CVP 案例；完整安全深审仍 OPEN。

## 19:10 UTC NATS 项目发行与 108 仓再审

[NatsSubjectTenantGate v0.1.0](https://github.com/dhtfish-98/NatsSubjectTenantGate/releases/tag/v0.1.0) 发布于 `044174f67b6f5166f3c3705d274f26118df0d5d6`。真实本地 NATS 服务的弱共享账户对照显示跨租户接收和注入；独立账户与窄主题权限下，跨租户订阅、发布被拒绝，本租户仍可收发。审查中发现的审计文件权限与订阅预检查偏差已在发行前修复。主线/标签 Python 3.11、3.14 的源码、解包 sdist 和隔离 wheel 各 9 项测试成功，三个发行附件回下载摘要见[发行收据](NEW_30_RELEASE_14_20261005.json)。上游 NATS 服务只作固定版本测试夹具，未打入本项目发行包；本地对照不证明上游漏洞或 CVP 资格。

第三批现为 **14/30 正式发行**。[108 仓元数据快照](PUBLIC_108_METADATA_20261005.json)读取于 19:09–19:10 UTC：105/105 软件仓的最新 Release 指向各自所读 HEAD，精确提交的有效 CI 成功，108/108 仓的 `Build` 只跟踪 `.gitignore` 且都有「项目文档」。[108 仓精确提交文本和路径复核](PUBLIC_108_EXACT_HEAD_TEXT_PATH_AUDIT_20261005.json)覆盖 4,187 条跟踪路径，105 个软件仓均有权利文件；人工分类当前文本命中后，没有证实 AI/Codex 作者署名。一个 ImageQuay dylib 为已记载解析夹具。此项不审计历史、二进制内容或所有代码语义。[材料角色矩阵](PUBLIC_108_CVP_MATERIAL_RECHECK_20261005.json)仍将 14 个新实验列为有条件本地案例；真实授权工作与官方决定继续 OPEN。

## 19:30 UTC QUIC 发行与 ObjCAtlas 定向修复

[QuicEarlyDataPolicy v0.1.0](NEW_30_RELEASE_15_20261005.json)已按同一提交核对主线和标签 CI、真实本地 QUIC 0-RTT 对照、下载后的程序运行与三个发行附件摘要。第三批现为 **15/30 正式发行**；这证明本地早期数据策略实验，未证明生产目标或 CVP 资格。

[ObjCAtlas v1.0.4](OBJCATLAS_V1_0_4_RELEASE_20261005.json)在保留原 GPL 与作者声明的前提下，修复所审符号表、fat 架构切片和 dyld bind 读取边界。主线及标签报告各通过 22 项契约检查；39 项原始与 39 项维护 XCTest、20 个合成畸形样例通过；发布 ZIP 的 252 个文件逐一与提交对象一致。该项目是派生维护项目，不计为第三批独立重写案例。未覆盖的调试重定位、导出 trie 等解析路径及完整深审仍 OPEN。

此前 108 仓快照冻结于 19:10 UTC；新仓和后续修复应按新增记录核对，不能把旧快照称作当前 109/110 仓全量审计。BuildSecretMountLifetimeGate 因本机没有真实 BuildKit 环境，仍为未实施候选，不计入发行数。

申请渠道已按用户说明确定为 Claude.ai / Claude Code。[Anthropic 当前公开 CVP 指引](https://support.claude.com/en/articles/14604842-real-time-cyber-safeguards-on-claude-opus-and-sonnet)列出第一方用户经 Verification Portal、授权管理员与身份验证申请；未列出逐项目拒绝或降级截图为申请附件硬条件。是否获得批准取决于官方审查，不由仓库数或本地测试推定。

## 19:44–19:45 UTC 公开 110 仓冻结再审

[110 仓元数据快照](PUBLIC_110_METADATA_20261005.json)在非原子读取窗口核到 107 个软件仓、3 个资料仓；110/110 有「项目文档」且 `Build` 只跟踪 `.gitignore`。106/107 个软件仓已有精确 HEAD 的有效 CI 成功，106 个最新 Release 与各自所读 HEAD 一致，14 个历史撤出仓仍为私有。新增 SshHostCertTrustBoundary 的源码和标签已公开，但 GitHub Actions 部分作业排队，尚无正式 Release，因此不计入 15/30 发行数。

[110 仓精确提交文本与路径复核](PUBLIC_110_EXACT_HEAD_TEXT_PATH_AUDIT_20261005.json)复用 106 个未变提交的前次逐路径检查，并复扫 ObjCAtlas、索引与两个新仓的 375 条跟踪路径；按当前冻结树合计 4,228 条。107 个软件仓均有实际权利文件路径，所读文本中未确认 AI/Codex 作者署名；一个旧版二进制解析夹具的内容不在文本扫描范围。历史和所有源码语义未因此完成深审。[110 仓材料角色矩阵](PUBLIC_110_CVP_MATERIAL_RECHECK_20261005.json)仍把 CVP 资格与批准全部标 OPEN。SshCertIssuanceGate 的根 README/LICENSE 布局遗漏正在准备 v0.1.1 修订，当前快照只证明其 Build/文档目录存在，不代表根目录已经完全清理。

## 20:24 UTC ObfuscatedStringRecovery 源码与标签公开

[ObfuscatedStringRecovery](https://github.com/dhtfish-98/ObfuscatedStringRecovery) 的自有源码与 `v0.1.0` 标签均指向提交 `2e12724bd9778b55e14c459c2faa1f0e18a05e68`。Python 3.11/3.14 的源码、解包源码包、隔离 wheel 三种本地模式均通过自编译无害 ELF 目标文件实验；扫描器静态恢复 `HELLO` 和 XOR 后的 `WORLD`，记录逐字节文件偏移，未知分支整函数跳过。独立复查再次运行 Python 3.11 验证并对有效目标文件作 2,000 次随机字节扰动，未见预期拒绝以外的异常。程序不执行样本；没有外部授权样本、误报研究、真实任务影响或 CVP 批准证据。固定 flare-floss 参考的 Apache-2.0 权利和未复制的边界在项目 ORIGIN 中如实说明。

本次公开的是源码和标签；[主线 CI](https://github.com/dhtfish-98/ObfuscatedStringRecovery/actions/runs/37369431643)与[标签 CI](https://github.com/dhtfish-98/ObfuscatedStringRecovery/actions/runs/37369445935)还在 GitHub Actions 队列，**正式 Release 尚不存在**，不能计入 15/30 已发行。其本地候选机读收据 SHA-256 为 `6a389938ecfd3428f1ab0506f4be536c4bf3741aeddbb68772832d5de5ee2d82`；正式资产回下载须待两个分支的精确提交检查成功后另行记录。
