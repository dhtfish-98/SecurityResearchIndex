# 保留的 10 项公开工具：能力与来源复核（2026-10-02）

## 当前结果

本轮逐项核对当前入口、文件写出、联网或进程执行能力及来源许可。前一复核阶段中，五个 Python 项目的 96 个已跟踪运行时文件完成语法解析，人工检查聚焦于实际输入、输出、执行和联网路径。该范围不是对每条上游算法或所有输入的形式化证明。

9 项已有具体运行时或入口改写并发布；完整项目重写仍逐项迭代：

- KernelCabinet 重写文件读取、Mach-O/记录/地址边界和输出流程，禁止输入名称决定写出路径或覆盖已有文件；138 个合成进程检查在 ASan/UBSan 下通过，验证输入保留和原始输出字节。
- SILGallery 重写为固定编译模式、私有文件通信和进程限额；新版构建成功，96 种选项组合与 36 组编译器输出比较通过，并验证大输入、双流、超时、无效字节及启动错误。
- ArchiveLens 移除外部助手的无限制执行参数和自动 Bash 授权，配置只读或无工具运行，使用每次独立的私有临时文件；2 个 GUI 安全边界检查通过。没有实际向外部助手发送请求。

- VTableBrook 四个运行时 C 文件及共享头全部改为有界图像上下文和静态模式解释；普通文件读取、命令/节/地址/13 项元数据及输出限额均检查。182 次正常对照、230 项 ASan/UBSan 与边界检查、13 项独立汇编操作数及安装后运行检查通过。保留的有限模式分析输出为候选值；RET 后扫描的旧行为单独登记为修正。

- ImageQuay 1.0.3：新增 record/plist、绑定/链式重定位和两阶段加载实改；291 项测试、822 项观察（416 相等、402 项独立位字段修正、4 项严格图像修正）及安装消费者通过。ARM64_32 的 Apple 工具对照只对固定样本的 2 个名称差异作独立操作码验证；对应源码行为解释为推断，工具二进制的精确源码身份仍 OPEN。
- PolicyMosaic 1.0.4：策略解码、隔离模拟及 NFA 正则语言归约实改；466 项测试、956 项观察（927 相等、29 项精确修正）、21,024 项独立语言检查、8 个普通 SBPL/C 报告和安装消费者通过。真实固件路径、操作决策图及完整报告继续迭代。
- TraceMeadow 1.0.3：v2/v3 输入、元数据/代码目录、分组/路径聚合及栈索引重写；459 项测试、1,233 项观察（1,173 相等、60 项精确畸形输入修正）及安装消费者通过。栈映像归属仍是最近前驱启发式，事件处理器和其他格式核心继续 OPEN。
- PEQuarry 1.0.2：新增重定位、动态重定位、函数覆盖及异常遍历实改；211 项项目测试、366 项来源控制和 366 项维护版检查通过；373 项 PE、149 项目录、1,204 项签名观察相等。历史 23 项结果仍是双方各 10 PASS、13 来源样本失败。资源、版本和其余目录继续迭代。

- IDBMeadow 1.0.2：稳定有限输入、容器/节、标志/名称页与 TIL 桶实改；本地完整测试 1,767 PASS、1 项严格预期失败，进程正常退出。CI 默认套件另为 1,608 PASS、160 项慢测试明确跳过；116 项自有边界测试和独立安装消费者通过。149 项来源及页观察中 127 相等、22 项精确修正。B-tree/游标、语义/类型语言及脚本接口等仍需后续重写。

ObjCAtlas 当前发布阶段仍只有能力与来源复核，没有全部运行时重写。其他已改写项目也明确保留尚继承的核心算法、设备/真实数据路径和未验证边界。表中 10 个固定公开提交均已核对相符的成功 CI；三个子任务与主任务正在进行的后续修改尚未混入这些已发布证据。

历史上 IDBMeadow、PEQuarry 第一次说明更新的 CI 因文件摘要清单未同步而失败，后续已同步已知修改的说明/打包文件，并增加新说明的安装包身份检查；当时运行时代码的既有摘要均未改变，修正后的提交通过；此后 IDBMeadow、PEQuarry 的运行时实改另列当前阶段证据。

## 逐项证据

| 项目 | 本轮复核/修改 | 当前公开提交与成功检查 | 具体范围 |
| --- | --- | --- | --- |
| [ArchiveLens](https://github.com/dhtfish-98/ArchiveLens) | 本地 IPA/Mach-O 静态分析；助手权限与临时文件已修复 | [`ea9e4af7`](https://github.com/dhtfish-98/ArchiveLens/commit/ea9e4af7e4f800d7cc0ead414a4fc3b9a7c20702)；[ArchiveLens contracts](https://github.com/dhtfish-98/ArchiveLens/actions/runs/36966314824)；[ArchiveLens workspace tests](https://github.com/dhtfish-98/ArchiveLens/actions/runs/36965598266)；[ArchiveLens contracts](https://github.com/dhtfish-98/ArchiveLens/actions/runs/36965598175) | [DEFENSIVE_SCOPE.md](https://github.com/dhtfish-98/ArchiveLens/blob/ea9e4af7e4f800d7cc0ead414a4fc3b9a7c20702/DEFENSIVE_SCOPE.md) |
| [ObjCAtlas](https://github.com/dhtfish-98/ObjCAtlas) | 本地 Objective-C 元数据；保护段解码/写出辅助入口明确登记 | [`c28c9e05`](https://github.com/dhtfish-98/ObjCAtlas/commit/c28c9e05b73a1b0ad12e77ce34bcae4bc29963c5)；[ObjCAtlas contracts](https://github.com/dhtfish-98/ObjCAtlas/actions/runs/36965601375) | [DEFENSIVE_SCOPE.md](https://github.com/dhtfish-98/ObjCAtlas/blob/c28c9e05b73a1b0ad12e77ce34bcae4bc29963c5/DEFENSIVE_SCOPE.md) |
| [ImageQuay](https://github.com/dhtfish-98/ImageQuay) | 容器、record/plist、绑定/链式重定位及两阶段加载已实改；ObjC/Swift、头文件/GUI/内核解释等剩余核心继续 OPEN。 | [`9e791f67`](https://github.com/dhtfish-98/ImageQuay/commit/9e791f676a24fa788f349ca7b48768960efc963c)；[对应 CI](https://github.com/dhtfish-98/ImageQuay/actions/runs/36985769583) | [DEFENSIVE_SCOPE.md](https://github.com/dhtfish-98/ImageQuay/blob/9e791f676a24fa788f349ca7b48768960efc963c/DEFENSIVE_SCOPE.md) |
| [PolicyMosaic](https://github.com/dhtfish-98/PolicyMosaic) | 有限策略/字符串/字节码、隔离模拟及 NFA 正则语言归约实改；操作决策图、完整报告和真实固件路径继续 OPEN。 | [`081a6a0d`](https://github.com/dhtfish-98/PolicyMosaic/commit/081a6a0ddaa67c33d6f4a59328172a3949ce69f4)；[对应 CI](https://github.com/dhtfish-98/PolicyMosaic/actions/runs/36984676178) | [DEFENSIVE_SCOPE.md](https://github.com/dhtfish-98/PolicyMosaic/blob/081a6a0ddaa67c33d6f4a59328172a3949ce69f4/DEFENSIVE_SCOPE.md) |
| [TraceMeadow](https://github.com/dhtfish-98/TraceMeadow) | v2/v3 二进制输入、元数据、代码目录、分组/路径聚合及栈索引实改；事件处理器、其他筛选/格式及通用状态限额仍 OPEN。 | [`5fa339ca`](https://github.com/dhtfish-98/TraceMeadow/commit/5fa339ca3200f454b554cd0ced0c899cd16959ac)；[对应 CI](https://github.com/dhtfish-98/TraceMeadow/actions/runs/36975320669) | [DEFENSIVE_SCOPE.md](https://github.com/dhtfish-98/TraceMeadow/blob/5fa339ca3200f454b554cd0ced0c899cd16959ac/DEFENSIVE_SCOPE.md) |
| [KernelCabinet](https://github.com/dhtfish-98/KernelCabinet) | 兼容内核扩展定位；有界只读输入和独占原始段输出已重写 | [`a303a0ee`](https://github.com/dhtfish-98/KernelCabinet/commit/a303a0ee1bd994e7bb085eaa80e8c94f9c8687d0)；[CI](https://github.com/dhtfish-98/KernelCabinet/actions/runs/36965612917) | [DEFENSIVE_SCOPE.md](https://github.com/dhtfish-98/KernelCabinet/blob/a303a0ee1bd994e7bb085eaa80e8c94f9c8687d0/DEFENSIVE_SCOPE.md) |
| [SILGallery](https://github.com/dhtfish-98/SILGallery) | 固定 Swift 编译视图；通信、输入/输出及超时流程已重写 | [`e6c2050e`](https://github.com/dhtfish-98/SILGallery/commit/e6c2050e35e6a1e934be3c08ce732265ccd848b6)；[CI](https://github.com/dhtfish-98/SILGallery/actions/runs/36965615556) | [DEFENSIVE_SCOPE.md](https://github.com/dhtfish-98/SILGallery/blob/e6c2050e35e6a1e934be3c08ce732265ccd848b6/DEFENSIVE_SCOPE.md) |
| [VTableBrook](https://github.com/dhtfish-98/VTableBrook) | 兼容内核类/vtable 候选静态解释；全部运行时 C 文件及共享头有界重写 | [`652ff6ff`](https://github.com/dhtfish-98/VTableBrook/commit/652ff6ff00cd77e4e75420d335a49ae895e559b2)；[CI](https://github.com/dhtfish-98/VTableBrook/actions/runs/36969063766) | [DEFENSIVE_SCOPE.md](https://github.com/dhtfish-98/VTableBrook/blob/652ff6ff00cd77e4e75420d335a49ae895e559b2/DEFENSIVE_SCOPE.md) |
| [IDBMeadow](https://github.com/dhtfish-98/IDBMeadow) | 有限稳定输入、容器/节、标志/名称页及 TIL 桶实改；B-tree/游标、netnode/语义/类型语言和脚本接口等继续 OPEN。 | [`1060c033`](https://github.com/dhtfish-98/IDBMeadow/commit/1060c03345e94a4c09c7a96f2e6b8d99bbf515c2)；[对应 CI](https://github.com/dhtfish-98/IDBMeadow/actions/runs/36986903512) | [DEFENSIVE_SCOPE.md](https://github.com/dhtfish-98/IDBMeadow/blob/1060c03345e94a4c09c7a96f2e6b8d99bbf515c2/DEFENSIVE_SCOPE.md) |
| [PEQuarry](https://github.com/dhtfish-98/PEQuarry) | 输入/映射/编辑/签名、重定位与动态重定位/函数覆盖/异常遍历实改；资源、版本和其余目录算法继续 OPEN。 | [`f4b65ecf`](https://github.com/dhtfish-98/PEQuarry/commit/f4b65ecf119eb5b40d34b42130321b7c41a76c83)；[对应 CI](https://github.com/dhtfish-98/PEQuarry/actions/runs/36983578949) | [DEFENSIVE_SCOPE.md](https://github.com/dhtfish-98/PEQuarry/blob/f4b65ecf119eb5b40d34b42130321b7c41a76c83/DEFENSIVE_SCOPE.md) |

## 当前源码发布

以下是本次核对的固定提交发布。原 4 个发布只提供源码；5 个 Python 发布同时提供源码包及经过独立安装检查的 wheel，全部摘要见 GROUPS.json。历史资产保留原内容，旧包不作为当前修复的运行证据。后续迭代以各项目新发布另行核对。重新构建的压缩包可能因容器元数据产生不同摘要；源码、运行时、来源和许可文件逐字节核对，发布资产单独固定摘要。

| 项目 | 当前源码发布 | 源码包 SHA-256 |
| --- | --- | --- |
| ArchiveLens | [v1.0.2](https://github.com/dhtfish-98/ArchiveLens/releases/tag/v1.0.2) | `40aaf1483b1e70e0b5acd9c414bbbbfec17c8556a254f6027067b7167c2fa8bb` |
| KernelCabinet | [v1.0.1](https://github.com/dhtfish-98/KernelCabinet/releases/tag/v1.0.1) | `48af56345f3ae5dbf84983a04c1faa2963d5d7918180e3181a7efe5699d5944d` |
| SILGallery | [v1.0.1](https://github.com/dhtfish-98/SILGallery/releases/tag/v1.0.1) | `86aebd6e7ee675fa1ee62b0811af9c927c19eb188e2c07db792e9478c180cb1f` |
| VTableBrook | [v1.0.1](https://github.com/dhtfish-98/VTableBrook/releases/tag/v1.0.1) | `677f5bc0030356a5f7dce810f2129031fd9f0292351dc52bd9bd4aacc6c97368` |
| ImageQuay | [v1.0.3](https://github.com/dhtfish-98/ImageQuay/releases/tag/v1.0.3) | `11028ff69acbeca2c382167d719297e83b17420f5d189df89e9a2c051077c34e` |
| PolicyMosaic | [v1.0.4](https://github.com/dhtfish-98/PolicyMosaic/releases/tag/v1.0.4) | `e32dc41a8811c385ba638856682034e84b2f10a54f0d4cf6ca18035fff575fba` |
| TraceMeadow | [v1.0.3](https://github.com/dhtfish-98/TraceMeadow/releases/tag/v1.0.3) | `6d69308ce8105903a0712d9dfbe327ac04c20d1a5c7f2e3ed0eda7d8d130688c` |
| PEQuarry | [v1.0.2](https://github.com/dhtfish-98/PEQuarry/releases/tag/v1.0.2) | `06f838775c69ff6fca9558fff0e3b3712f0ad0f6555bf53437927ab10e523c2f` |
| IDBMeadow | [v1.0.2](https://github.com/dhtfish-98/IDBMeadow/releases/tag/v1.0.2) | `2dfccc347095dbb529c2ee1c6d2a68e7bcd00597dcb40023c2d9327b11f22720` |

## 来源与申请边界

保留全部原作者和许可证：ArchiveLens/ImageQuay/TraceMeadow/SILGallery/PEQuarry 为 MIT 衍生维护，ObjCAtlas 为 GPL-2.0-or-later，KernelCabinet/VTableBrook 为 GPL-3.0，PolicyMosaic 为 BSD-3-Clause，IDBMeadow 为 Apache-2.0。固定来源提交和不同样本的归属以各仓库 ORIGIN.md 与许可证为准。本轮 Codex 辅助修改不证明申请人独立编写了上游算法。

当前组合是 14 项新防御工具加 10 项保留研究工具，共 24 项公开仓库；另 14 个撤出的旧仓库均存在且保持私有。合法防御使用仍须与实际授权、受限任务、产品渠道、身份和组织对应。CVP 的适用性和申请结果均为 OPEN，任何构建、来源说明或 CI 都不能替代这些事实。
