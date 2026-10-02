# 保留的 10 项公开工具：能力与来源复核（2026-10-02）

## 当前结果

本轮逐项核对当前入口、文件写出、联网或进程执行能力及来源许可。前一复核阶段中，五个 Python 项目的 96 个已跟踪运行时文件完成语法解析，人工检查聚焦于实际输入、输出、执行和联网路径。该范围不是对每条上游算法或所有输入的形式化证明。

8 项已有具体运行时或入口改写并发布；完整项目重写仍逐项迭代：

- KernelCabinet 重写文件读取、Mach-O/记录/地址边界和输出流程，禁止输入名称决定写出路径或覆盖已有文件；138 个合成进程检查在 ASan/UBSan 下通过，验证输入保留和原始输出字节。
- SILGallery 重写为固定编译模式、私有文件通信和进程限额；新版构建成功，96 种选项组合与 36 组编译器输出比较通过，并验证大输入、双流、超时、无效字节及启动错误。
- ArchiveLens 移除外部助手的无限制执行参数和自动 Bash 授权，配置只读或无工具运行，使用每次独立的私有临时文件；2 个 GUI 安全边界检查通过。没有实际向外部助手发送请求。

- VTableBrook 四个运行时 C 文件及共享头全部改为有界图像上下文和静态模式解释；普通文件读取、命令/节/地址/13 项元数据及输出限额均检查。182 次正常对照、230 项 ASan/UBSan 与边界检查、13 项独立汇编操作数及安装后运行检查通过。保留的有限模式分析输出为候选值；RET 后扫描的旧行为单独登记为修正。

- ImageQuay 1.0.2：容器输入/签名/导出/VM 与显式文件输出、更新入口实改；162 项本地测试、822 项观察（818 相等、4 项精确修正）及安装后编辑/组合/提取检查通过。Apple 工具的 4 项本地独立对照在 Linux CI 明确跳过。
- PolicyMosaic 1.0.2：策略/字符串/正则解码和受限辅助进程实改，输出为有限本地分析报告；150 项测试、956 项观察（927 相等、29 项精确修正）、普通 SBPL/C 报告及安装检查通过。ARM64 输入由独立进程中的原生 Unicorn 库模拟；当前主机沙盒出现 SIGILL，普通授权主机探针通过，不证明真实固件结果。
- TraceMeadow 1.0.3：v2/v3 输入、元数据/代码目录、分组/路径聚合及栈索引重写；459 项测试、1,233 项观察（1,173 相等、60 项精确畸形输入修正）及安装消费者通过。栈映像归属仍是最近前驱启发式，事件处理器和其他格式核心继续 OPEN。
- PEQuarry 1.0.1：PE 输入/映射/编辑/序列化及签名数据库实改；127 项项目测试、366 项来源控制和 366 项维护版检查通过；373 项 PE、1,204 项签名观察相等。历史 23 项结果严格相同，均为 10 PASS、13 来源样本失败，不能记为全通过。

ObjCAtlas 和 IDBMeadow 当前发布阶段仍只有能力与来源复核，没有全部运行时重写。其他已改写项目也明确保留尚继承的核心算法、设备/真实数据路径和未验证边界。表中 10 个固定公开提交均已核对相符的成功 CI；三个子任务与主任务正在进行的后续修改尚未混入这些已发布证据。

历史上 IDBMeadow、PEQuarry 第一次说明更新的 CI 因文件摘要清单未同步而失败，后续已同步已知修改的说明/打包文件，并增加新说明的安装包身份检查；当时运行时代码的既有摘要均未改变，修正后的提交通过；此后 PEQuarry 的运行时实改另列当前阶段证据。

## 逐项证据

| 项目 | 本轮复核/修改 | 当前公开提交与成功检查 | 具体范围 |
| --- | --- | --- | --- |
| [ArchiveLens](https://github.com/dhtfish-98/ArchiveLens) | 本地 IPA/Mach-O 静态分析；助手权限与临时文件已修复 | [`ea9e4af7`](https://github.com/dhtfish-98/ArchiveLens/commit/ea9e4af7e4f800d7cc0ead414a4fc3b9a7c20702)；[ArchiveLens contracts](https://github.com/dhtfish-98/ArchiveLens/actions/runs/36966314824)；[ArchiveLens workspace tests](https://github.com/dhtfish-98/ArchiveLens/actions/runs/36965598266)；[ArchiveLens contracts](https://github.com/dhtfish-98/ArchiveLens/actions/runs/36965598175) | [DEFENSIVE_SCOPE.md](https://github.com/dhtfish-98/ArchiveLens/blob/ea9e4af7e4f800d7cc0ead414a4fc3b9a7c20702/DEFENSIVE_SCOPE.md) |
| [ObjCAtlas](https://github.com/dhtfish-98/ObjCAtlas) | 本地 Objective-C 元数据；保护段解码/写出辅助入口明确登记 | [`c28c9e05`](https://github.com/dhtfish-98/ObjCAtlas/commit/c28c9e05b73a1b0ad12e77ce34bcae4bc29963c5)；[ObjCAtlas contracts](https://github.com/dhtfish-98/ObjCAtlas/actions/runs/36965601375) | [DEFENSIVE_SCOPE.md](https://github.com/dhtfish-98/ObjCAtlas/blob/c28c9e05b73a1b0ad12e77ce34bcae4bc29963c5/DEFENSIVE_SCOPE.md) |
| [ImageQuay](https://github.com/dhtfish-98/ImageQuay) | 有限输入快照、Mach-O/FAT/签名/导出/VM/显式编辑写出和更新入口实改；ObjC/Swift、GUI、plist/record 与绑定完整核心仍待后续阶段。 | [`86c884f5`](https://github.com/dhtfish-98/ImageQuay/commit/86c884f5daec4dca2015824fa52c1129eca8ee93)；[对应 CI](https://github.com/dhtfish-98/ImageQuay/actions/runs/36975795025) | [DEFENSIVE_SCOPE.md](https://github.com/dhtfish-98/ImageQuay/blob/86c884f5daec4dca2015824fa52c1129eca8ee93/DEFENSIVE_SCOPE.md) |
| [PolicyMosaic](https://github.com/dhtfish-98/PolicyMosaic) | 策略 profile/string/regex 有限解码、图上下文预算、受限进程与模拟辅助路径实改；完整图归约语义和真实固件全路径仍 OPEN。 | [`13cb5a49`](https://github.com/dhtfish-98/PolicyMosaic/commit/13cb5a496d57ecf6384b0257bcf632ebcf7dc763)；[对应 CI](https://github.com/dhtfish-98/PolicyMosaic/actions/runs/36979363086) | [DEFENSIVE_SCOPE.md](https://github.com/dhtfish-98/PolicyMosaic/blob/13cb5a496d57ecf6384b0257bcf632ebcf7dc763/DEFENSIVE_SCOPE.md) |
| [TraceMeadow](https://github.com/dhtfish-98/TraceMeadow) | v2/v3 二进制输入、元数据、代码目录、分组/路径聚合及栈索引实改；事件处理器、其他筛选/格式及通用状态限额仍 OPEN。 | [`5fa339ca`](https://github.com/dhtfish-98/TraceMeadow/commit/5fa339ca3200f454b554cd0ced0c899cd16959ac)；[对应 CI](https://github.com/dhtfish-98/TraceMeadow/actions/runs/36975320669) | [DEFENSIVE_SCOPE.md](https://github.com/dhtfish-98/TraceMeadow/blob/5fa339ca3200f454b554cd0ced0c899cd16959ac/DEFENSIVE_SCOPE.md) |
| [KernelCabinet](https://github.com/dhtfish-98/KernelCabinet) | 兼容内核扩展定位；有界只读输入和独占原始段输出已重写 | [`a303a0ee`](https://github.com/dhtfish-98/KernelCabinet/commit/a303a0ee1bd994e7bb085eaa80e8c94f9c8687d0)；[CI](https://github.com/dhtfish-98/KernelCabinet/actions/runs/36965612917) | [DEFENSIVE_SCOPE.md](https://github.com/dhtfish-98/KernelCabinet/blob/a303a0ee1bd994e7bb085eaa80e8c94f9c8687d0/DEFENSIVE_SCOPE.md) |
| [SILGallery](https://github.com/dhtfish-98/SILGallery) | 固定 Swift 编译视图；通信、输入/输出及超时流程已重写 | [`e6c2050e`](https://github.com/dhtfish-98/SILGallery/commit/e6c2050e35e6a1e934be3c08ce732265ccd848b6)；[CI](https://github.com/dhtfish-98/SILGallery/actions/runs/36965615556) | [DEFENSIVE_SCOPE.md](https://github.com/dhtfish-98/SILGallery/blob/e6c2050e35e6a1e934be3c08ce732265ccd848b6/DEFENSIVE_SCOPE.md) |
| [VTableBrook](https://github.com/dhtfish-98/VTableBrook) | 兼容内核类/vtable 候选静态解释；全部运行时 C 文件及共享头有界重写 | [`652ff6ff`](https://github.com/dhtfish-98/VTableBrook/commit/652ff6ff00cd77e4e75420d335a49ae895e559b2)；[CI](https://github.com/dhtfish-98/VTableBrook/actions/runs/36969063766) | [DEFENSIVE_SCOPE.md](https://github.com/dhtfish-98/VTableBrook/blob/652ff6ff00cd77e4e75420d335a49ae895e559b2/DEFENSIVE_SCOPE.md) |
| [IDBMeadow](https://github.com/dhtfish-98/IDBMeadow) | 离线 IDB/I64；脚本执行与个人元数据导出入口明确登记 | [`9a05c578`](https://github.com/dhtfish-98/IDBMeadow/commit/9a05c57809ff7b28835ba37e504e7d2d79750a80)；[Frozen static analysis verification](https://github.com/dhtfish-98/IDBMeadow/actions/runs/36965999994) | [DEFENSIVE_SCOPE.md](https://github.com/dhtfish-98/IDBMeadow/blob/9a05c57809ff7b28835ba37e504e7d2d79750a80/DEFENSIVE_SCOPE.md) |
| [PEQuarry](https://github.com/dhtfish-98/PEQuarry) | PE 有限稳定输入、映射/序列化/编辑及签名数据库实改；目录/资源/重定位/异常/别名/格式算法完整重写仍 OPEN。 | [`1e74c7d3`](https://github.com/dhtfish-98/PEQuarry/commit/1e74c7d330f7714c696226640eb08774a4ef4cc1)；[对应 CI](https://github.com/dhtfish-98/PEQuarry/actions/runs/36979246175) | [DEFENSIVE_SCOPE.md](https://github.com/dhtfish-98/PEQuarry/blob/1e74c7d330f7714c696226640eb08774a4ef4cc1/DEFENSIVE_SCOPE.md) |

## 当前源码发布

以下是本次核对的固定提交发布。原 4 个发布只提供源码；新增 4 个 Python 发布同时提供源码包及经过独立安装检查的 wheel，全部摘要见 GROUPS.json。历史资产保留原内容，旧包不作为当前修复的运行证据。后续迭代以各项目新发布另行核对。

| 项目 | 当前源码发布 | 源码包 SHA-256 |
| --- | --- | --- |
| ArchiveLens | [v1.0.2](https://github.com/dhtfish-98/ArchiveLens/releases/tag/v1.0.2) | `40aaf1483b1e70e0b5acd9c414bbbbfec17c8556a254f6027067b7167c2fa8bb` |
| KernelCabinet | [v1.0.1](https://github.com/dhtfish-98/KernelCabinet/releases/tag/v1.0.1) | `48af56345f3ae5dbf84983a04c1faa2963d5d7918180e3181a7efe5699d5944d` |
| SILGallery | [v1.0.1](https://github.com/dhtfish-98/SILGallery/releases/tag/v1.0.1) | `86aebd6e7ee675fa1ee62b0811af9c927c19eb188e2c07db792e9478c180cb1f` |
| VTableBrook | [v1.0.1](https://github.com/dhtfish-98/VTableBrook/releases/tag/v1.0.1) | `677f5bc0030356a5f7dce810f2129031fd9f0292351dc52bd9bd4aacc6c97368` |
| ImageQuay | [v1.0.2](https://github.com/dhtfish-98/ImageQuay/releases/tag/v1.0.2) | `191a80413e99c4fd1f0f51d2ad6767675aad61ebfa5e5448afdc346e00647735` |
| PolicyMosaic | [v1.0.2](https://github.com/dhtfish-98/PolicyMosaic/releases/tag/v1.0.2) | `d0221d72abc31310495d2161aa667e2546428aaa742249b96908a4cf4ae23a37` |
| TraceMeadow | [v1.0.3](https://github.com/dhtfish-98/TraceMeadow/releases/tag/v1.0.3) | `6d69308ce8105903a0712d9dfbe327ac04c20d1a5c7f2e3ed0eda7d8d130688c` |
| PEQuarry | [v1.0.1](https://github.com/dhtfish-98/PEQuarry/releases/tag/v1.0.1) | `a095555fb6a0273620f954e3b8e0669e883680b2982dc2e61533355139842b37` |

## 来源与申请边界

保留全部原作者和许可证：ArchiveLens/ImageQuay/TraceMeadow/SILGallery/PEQuarry 为 MIT 衍生维护，ObjCAtlas 为 GPL-2.0-or-later，KernelCabinet/VTableBrook 为 GPL-3.0，PolicyMosaic 为 BSD-3-Clause，IDBMeadow 为 Apache-2.0。固定来源提交和不同样本的归属以各仓库 ORIGIN.md 与许可证为准。本轮 Codex 辅助修改不证明申请人独立编写了上游算法。

当前组合是 14 项新防御工具加 10 项保留研究工具，共 24 项公开仓库；另 14 个撤出的旧仓库均存在且保持私有。合法防御使用仍须与实际授权、受限任务、产品渠道、身份和组织对应。CVP 的适用性和申请结果均为 OPEN，任何构建、来源说明或 CI 都不能替代这些事实。
