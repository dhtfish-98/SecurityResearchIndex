# 安全研究项目索引

这里列出本次新增并公开发布的 **24 个项目**，按用户指定的 **8 组、每组 3 项**整理。前 7 组是保留来源、许可证和行为验证的重写项目；第 8 组是独立编写的、只研究已公开 CVE 的本地实验项目。另有早期的 SealScope、BranchLoom、TabWeave，未计入这 24 项。

这些“申请账号”是本地资料分组标签，不代表已创建 8 个 CVP 账号、已提交申请或已获批。官方 [Claude Verified Program 说明](https://support.claude.com/en/articles/14604842-real-time-cyber-safeguards-on-claude-opus-and-sonnet) 涉及专业防御用途、资格及核验；项目数量或换名本身不构成资格。每个项目的 `ORIGIN.md`、`VALIDATION.md`、许可证与发布包记录给出来源和验证边界。

保留 `README.md`、`pyproject.toml`、工作流等工具要求的固定文件名；可自主命名的项目文件、模块和自有符号按映射重写。无法把相同算法的重写等同于逐场景功能完全一致，因此各仓库明确记录已测向量与未测范围。

## 申请账号1：Mach-O / Swift 符号与字符串研究

| 项目 | 来源或公告 | 发布版本 | 验证 |
| --- | --- | --- | --- |
| [GlyphHaven](https://github.com/dhtfish-98/GlyphHaven) | [MachObfuscator](https://github.com/kam800/MachObfuscator.git) | [v1.0.0](https://github.com/dhtfish-98/GlyphHaven/releases/tag/v1.0.0) | 远端源码、发布包与自动测试均通过 |
| [StringCanopy](https://github.com/dhtfish-98/StringCanopy) | [Obfuscator](https://github.com/thexande/Obfuscator.git) | [v1.0.0](https://github.com/dhtfish-98/StringCanopy/releases/tag/v1.0.0) | 远端源码、发布包与自动测试均通过 |
| [TypeVeil](https://github.com/dhtfish-98/TypeVeil) | [swiftshield](https://github.com/rockbruno/swiftshield.git) | [v1.0.0](https://github.com/dhtfish-98/TypeVeil/releases/tag/v1.0.0) | 远端源码、发布包与自动测试均通过 |

## 申请账号2：IPA / Objective-C 静态分析

| 项目 | 来源或公告 | 发布版本 | 验证 |
| --- | --- | --- | --- |
| [ArchiveLens](https://github.com/dhtfish-98/ArchiveLens) | [REipa](https://github.com/JRBusiness/REipa.git) | [v1.0.1](https://github.com/dhtfish-98/ArchiveLens/releases/tag/v1.0.1) | 远端源码、发布包与自动测试均通过 |
| [NameRampart](https://github.com/dhtfish-98/NameRampart) | [ios-class-guard](https://github.com/Polidea/ios-class-guard.git) | [v1.0.0](https://github.com/dhtfish-98/NameRampart/releases/tag/v1.0.0) | 远端源码、发布包与自动测试均通过 |
| [ObjCAtlas](https://github.com/dhtfish-98/ObjCAtlas) | [class-dump](https://github.com/nygard/class-dump.git) | [v1.0.0](https://github.com/dhtfish-98/ObjCAtlas/releases/tag/v1.0.0) | 远端源码、发布包与自动测试均通过 |

## 申请账号3：Darwin 镜像、调用与策略分析

| 项目 | 来源或公告 | 发布版本 | 验证 |
| --- | --- | --- | --- |
| [ImageQuay](https://github.com/dhtfish-98/ImageQuay) | [ktool](https://github.com/0cyn/ktool.git) | [v1.0.1](https://github.com/dhtfish-98/ImageQuay/releases/tag/v1.0.1) | 远端源码、发布包与自动测试均通过 |
| [PolicyMosaic](https://github.com/dhtfish-98/PolicyMosaic) | [sandblaster_26](https://github.com/chensokolovsky/sandblaster_26.git) | [v1.0.1](https://github.com/dhtfish-98/PolicyMosaic/releases/tag/v1.0.1) | 远端源码、发布包与自动测试均通过 |
| [TraceMeadow](https://github.com/dhtfish-98/TraceMeadow) | [pykdebugparser](https://github.com/matan1008/pykdebugparser.git) | [v1.0.1](https://github.com/dhtfish-98/TraceMeadow/releases/tag/v1.0.1) | 远端源码、发布包与自动测试均通过 |

## 申请账号4：内核与编译器机制研究

| 项目 | 来源或公告 | 发布版本 | 验证 |
| --- | --- | --- | --- |
| [KernelCabinet](https://github.com/dhtfish-98/KernelCabinet) | [kextract](https://github.com/0x7ff/kextract.git) | [v1.0.0](https://github.com/dhtfish-98/KernelCabinet/releases/tag/v1.0.0) | 远端源码、发布包与自动测试均通过 |
| [SILGallery](https://github.com/dhtfish-98/SILGallery) | [SILInspector](https://github.com/alblue/SILInspector.git) | [v1.0.0](https://github.com/dhtfish-98/SILGallery/releases/tag/v1.0.0) | 远端源码、发布包与自动测试均通过 |
| [VTableBrook](https://github.com/dhtfish-98/VTableBrook) | [vtable](https://github.com/0x7ff/vtable.git) | [v1.0.0](https://github.com/dhtfish-98/VTableBrook/releases/tag/v1.0.0) | 远端源码、发布包与自动测试均通过 |

## 申请账号5：原生二进制、PE 与 IDB 解析

| 项目 | 来源或公告 | 发布版本 | 验证 |
| --- | --- | --- | --- |
| [GadgetHarbor](https://github.com/dhtfish-98/GadgetHarbor) | [ROPgadget](https://github.com/JonathanSalwan/ROPgadget.git) | [v1.0.0](https://github.com/dhtfish-98/GadgetHarbor/releases/tag/v1.0.0) | 远端源码、发布包与自动测试均通过 |
| [IDBMeadow](https://github.com/dhtfish-98/IDBMeadow) | [python-idb](https://github.com/williballenthin/python-idb.git) | [v1.0.1](https://github.com/dhtfish-98/IDBMeadow/releases/tag/v1.0.1) | 远端源码、发布包与自动测试均通过 |
| [PEQuarry](https://github.com/dhtfish-98/PEQuarry) | [pefile](https://github.com/erocarrera/pefile.git) | [v1.0.0](https://github.com/dhtfish-98/PEQuarry/releases/tag/v1.0.0) | 远端源码、发布包与自动测试均通过 |

## 申请账号6：应用入口、密钥与令牌防御研究

| 项目 | 来源或公告 | 发布版本 | 验证 |
| --- | --- | --- | --- |
| [EndpointGrove](https://github.com/dhtfish-98/EndpointGrove) | [LinkFinder](https://github.com/GerbenJavado/LinkFinder.git) | [v1.0.4](https://github.com/dhtfish-98/EndpointGrove/releases/tag/v1.0.4) | 远端源码、发布包与自动测试均通过 |
| [SecretCanopy](https://github.com/dhtfish-98/SecretCanopy) | [SecretFinder](https://github.com/m4ll0k/SecretFinder.git) | [v1.0.4](https://github.com/dhtfish-98/SecretCanopy/releases/tag/v1.0.4) | 远端源码、发布包与自动测试均通过 |
| [TokenMariner](https://github.com/dhtfish-98/TokenMariner) | [jwt_tool](https://github.com/ticarpi/jwt_tool.git) | [v1.0.2](https://github.com/dhtfish-98/TokenMariner/releases/tag/v1.0.2) | 远端源码、发布包与自动测试均通过 |

## 申请账号7：Web / CMS / WAF / 脚本研究

| 项目 | 来源或公告 | 发布版本 | 验证 |
| --- | --- | --- | --- |
| [CMSBeacon](https://github.com/dhtfish-98/CMSBeacon) | [droopescan](https://github.com/SamJoan/droopescan.git) | [v1.0.0](https://github.com/dhtfish-98/CMSBeacon/releases/tag/v1.0.0) | 远端源码、发布包与自动测试均通过 |
| [ScriptSentinel](https://github.com/dhtfish-98/ScriptSentinel) | [XSStrike](https://github.com/s0md3v/XSStrike.git) | [v1.0.0](https://github.com/dhtfish-98/ScriptSentinel/releases/tag/v1.0.0) | 远端源码、发布包与自动测试均通过 |
| [WAFHarbor](https://github.com/dhtfish-98/WAFHarbor) | [wafw00f](https://github.com/EnableSecurity/wafw00f.git) | [v1.0.0](https://github.com/dhtfish-98/WAFHarbor/releases/tag/v1.0.0) | 远端源码、发布包与自动测试均通过 |

## 申请账号8：已公开 CVE 的历史版本复现与回归

| 项目 | 来源或公告 | 发布版本 | 验证 |
| --- | --- | --- | --- |
| [ClaimAnchor](https://github.com/dhtfish-98/ClaimAnchor) | [CVE-2022-29217](https://github.com/jpadilla/pyjwt/security/advisories/GHSA-ffqj-6fqr-9h24) · PyJWT | [v1.0.0](https://github.com/dhtfish-98/ClaimAnchor/releases/tag/v1.0.0) | 远端源码、发布包与自动测试均通过 |
| [PathHarbor](https://github.com/dhtfish-98/PathHarbor) | [CVE-2024-23334](https://github.com/aio-libs/aiohttp/security/advisories/GHSA-5h86-8mv2-jq9f) · aiohttp | [v1.0.0](https://github.com/dhtfish-98/PathHarbor/releases/tag/v1.0.0) | 远端源码、发布包与自动测试均通过 |
| [QueryRampart](https://github.com/dhtfish-98/QueryRampart) | [CVE-2024-4340](https://github.com/andialbrecht/sqlparse/security/advisories/GHSA-2m57-hf25-phgg) · sqlparse | [v1.0.1](https://github.com/dhtfish-98/QueryRampart/releases/tag/v1.0.1) | 远端源码、发布包与自动测试均通过 |

第 8 组的漏洞编号均已由原项目或安全公告公开；原发现者在各仓库 `ORIGIN.md` 中署名。此处没有新 CVE 发现、分配或披露的主张。历史受影响版本只在一次性隔离环境、合成输入及自有临时文件／localhost 上测试。

本索引的“通过”指记录中的当前 Git 提交、发布标签、逐文件哈希、发布资产哈希和该提交对应的 GitHub Actions 状态已核对。它不证明真实设备、真实服务或 CVP 申请结果。
