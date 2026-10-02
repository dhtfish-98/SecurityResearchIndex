# 保留的 10 项公开工具：能力与来源复核（2026-10-02）

## 当前结果

本轮逐项核对当前入口、文件写出、联网或进程执行能力及来源许可。五个 Python 项目的 96 个已跟踪运行时文件完成语法解析，人工检查聚焦于实际输入、输出、执行和联网路径。该范围不是对每条上游算法或所有输入的形式化证明。

3 项发现的具体问题已修正并发布：

- KernelCabinet 重写文件读取、Mach-O/记录/地址边界和输出流程，禁止输入名称决定写出路径或覆盖已有文件；138 个合成进程检查在 ASan/UBSan 下通过，验证输入保留和原始输出字节。
- SILGallery 重写为固定编译模式、私有文件通信和进程限额；新版构建成功，96 种选项组合与 36 组编译器输出比较通过，并验证大输入、双流、超时、无效字节及启动错误。
- ArchiveLens 移除外部助手的无限制执行参数和自动 Bash 授权，配置只读或无工具运行，使用每次独立的私有临时文件；2 个 GUI 安全边界检查通过。没有实际向外部助手发送请求。

另外 7 项完成能力与来源复核及说明更新。本轮没有把其全部上游算法重写为独立实现，也没有把历史等价测试当作全面安全证明。所有 10 个最新公开提交均已核对相符的成功 CI。

IDBMeadow、PEQuarry 第一次说明更新的 CI 因文件摘要清单未同步而失败，后续已同步已知修改的说明/打包文件，并增加新说明的安装包身份检查；运行时代码的既有摘要均未改变，修正后的提交通过。

## 逐项证据

| 项目 | 本轮复核/修改 | 当前公开提交与成功检查 | 具体范围 |
| --- | --- | --- | --- |
| [ArchiveLens](https://github.com/dhtfish-98/ArchiveLens) | 本地 IPA/Mach-O 静态分析；助手权限与临时文件已修复 | [`ea9e4af7`](https://github.com/dhtfish-98/ArchiveLens/commit/ea9e4af7e4f800d7cc0ead414a4fc3b9a7c20702)；[ArchiveLens contracts](https://github.com/dhtfish-98/ArchiveLens/actions/runs/36966314824)；[ArchiveLens workspace tests](https://github.com/dhtfish-98/ArchiveLens/actions/runs/36965598266)；[ArchiveLens contracts](https://github.com/dhtfish-98/ArchiveLens/actions/runs/36965598175) | [DEFENSIVE_SCOPE.md](https://github.com/dhtfish-98/ArchiveLens/blob/ea9e4af7e4f800d7cc0ead414a4fc3b9a7c20702/DEFENSIVE_SCOPE.md) |
| [ObjCAtlas](https://github.com/dhtfish-98/ObjCAtlas) | 本地 Objective-C 元数据；保护段解码/写出辅助入口明确登记 | [`c28c9e05`](https://github.com/dhtfish-98/ObjCAtlas/commit/c28c9e05b73a1b0ad12e77ce34bcae4bc29963c5)；[ObjCAtlas contracts](https://github.com/dhtfish-98/ObjCAtlas/actions/runs/36965601375) | [DEFENSIVE_SCOPE.md](https://github.com/dhtfish-98/ObjCAtlas/blob/c28c9e05b73a1b0ad12e77ce34bcae4bc29963c5/DEFENSIVE_SCOPE.md) |
| [ImageQuay](https://github.com/dhtfish-98/ImageQuay) | Mach-O/签名信息；编辑、组合和更新检查能力明确登记 | [`7ebb7d6d`](https://github.com/dhtfish-98/ImageQuay/commit/7ebb7d6d6dacfb6c8b98d03ef0fdd70bc0da322a)；[Verify](https://github.com/dhtfish-98/ImageQuay/actions/runs/36965604211) | [DEFENSIVE_SCOPE.md](https://github.com/dhtfish-98/ImageQuay/blob/7ebb7d6d6dacfb6c8b98d03ef0fdd70bc0da322a/DEFENSIVE_SCOPE.md) |
| [PolicyMosaic](https://github.com/dhtfish-98/PolicyMosaic) | sandbox 策略解释；下载、模拟与编译辅助入口明确登记 | [`d9fc883f`](https://github.com/dhtfish-98/PolicyMosaic/commit/d9fc883f30081f079d5670b4ab4d3ef4dd0392da)；[Verify](https://github.com/dhtfish-98/PolicyMosaic/actions/runs/36965607325) | [DEFENSIVE_SCOPE.md](https://github.com/dhtfish-98/PolicyMosaic/blob/d9fc883f30081f079d5670b4ab4d3ef4dd0392da/DEFENSIVE_SCOPE.md) |
| [TraceMeadow](https://github.com/dhtfish-98/TraceMeadow) | 本地 Darwin 轨迹解释；日志敏感信息与版本范围明确登记 | [`1e887aac`](https://github.com/dhtfish-98/TraceMeadow/commit/1e887aacfea40c593d94b3e0356c4e3717faafb3)；[Verify](https://github.com/dhtfish-98/TraceMeadow/actions/runs/36965609784) | [DEFENSIVE_SCOPE.md](https://github.com/dhtfish-98/TraceMeadow/blob/1e887aacfea40c593d94b3e0356c4e3717faafb3/DEFENSIVE_SCOPE.md) |
| [KernelCabinet](https://github.com/dhtfish-98/KernelCabinet) | 兼容内核扩展定位；有界只读输入和独占原始段输出已重写 | [`a303a0ee`](https://github.com/dhtfish-98/KernelCabinet/commit/a303a0ee1bd994e7bb085eaa80e8c94f9c8687d0)；[CI](https://github.com/dhtfish-98/KernelCabinet/actions/runs/36965612917) | [DEFENSIVE_SCOPE.md](https://github.com/dhtfish-98/KernelCabinet/blob/a303a0ee1bd994e7bb085eaa80e8c94f9c8687d0/DEFENSIVE_SCOPE.md) |
| [SILGallery](https://github.com/dhtfish-98/SILGallery) | 固定 Swift 编译视图；通信、输入/输出及超时流程已重写 | [`e6c2050e`](https://github.com/dhtfish-98/SILGallery/commit/e6c2050e35e6a1e934be3c08ce732265ccd848b6)；[CI](https://github.com/dhtfish-98/SILGallery/actions/runs/36965615556) | [DEFENSIVE_SCOPE.md](https://github.com/dhtfish-98/SILGallery/blob/e6c2050e35e6a1e934be3c08ce732265ccd848b6/DEFENSIVE_SCOPE.md) |
| [VTableBrook](https://github.com/dhtfish-98/VTableBrook) | 兼容内核类/vtable 静态解释；继承解析器的边界未完成全面加固 | [`53c929f9`](https://github.com/dhtfish-98/VTableBrook/commit/53c929f988f6db5557ed1d2b69c6d222eca8e0f5)；[CI](https://github.com/dhtfish-98/VTableBrook/actions/runs/36965618901) | [DEFENSIVE_SCOPE.md](https://github.com/dhtfish-98/VTableBrook/blob/53c929f988f6db5557ed1d2b69c6d222eca8e0f5/DEFENSIVE_SCOPE.md) |
| [IDBMeadow](https://github.com/dhtfish-98/IDBMeadow) | 离线 IDB/I64；脚本执行与个人元数据导出入口明确登记 | [`9a05c578`](https://github.com/dhtfish-98/IDBMeadow/commit/9a05c57809ff7b28835ba37e504e7d2d79750a80)；[Frozen static analysis verification](https://github.com/dhtfish-98/IDBMeadow/actions/runs/36965999994) | [DEFENSIVE_SCOPE.md](https://github.com/dhtfish-98/IDBMeadow/blob/9a05c57809ff7b28835ba37e504e7d2d79750a80/DEFENSIVE_SCOPE.md) |
| [PEQuarry](https://github.com/dhtfish-98/PEQuarry) | PE 静态结构；显式写 API 与签名数据库下载回退明确登记 | [`0f193a73`](https://github.com/dhtfish-98/PEQuarry/commit/0f193a739df3c06fc8df019088388d7256463953)；[Frozen static analysis verification](https://github.com/dhtfish-98/PEQuarry/actions/runs/36966002539) | [DEFENSIVE_SCOPE.md](https://github.com/dhtfish-98/PEQuarry/blob/0f193a739df3c06fc8df019088388d7256463953/DEFENSIVE_SCOPE.md) |

## 当前源码发布

这些发布提供与当前提交一致的源码。旧二进制包未被替换成新版本，也没有被当作本轮修复后的运行证据；旧发布保留原内容并附历史说明。

| 项目 | 当前源码发布 | 源码包 SHA-256 |
| --- | --- | --- |
| ArchiveLens | [v1.0.2](https://github.com/dhtfish-98/ArchiveLens/releases/tag/v1.0.2) | `40aaf1483b1e70e0b5acd9c414bbbbfec17c8556a254f6027067b7167c2fa8bb` |
| KernelCabinet | [v1.0.1](https://github.com/dhtfish-98/KernelCabinet/releases/tag/v1.0.1) | `48af56345f3ae5dbf84983a04c1faa2963d5d7918180e3181a7efe5699d5944d` |
| SILGallery | [v1.0.1](https://github.com/dhtfish-98/SILGallery/releases/tag/v1.0.1) | `86aebd6e7ee675fa1ee62b0811af9c927c19eb188e2c07db792e9478c180cb1f` |

## 来源与申请边界

保留全部原作者和许可证：ArchiveLens/ImageQuay/TraceMeadow/SILGallery/PEQuarry 为 MIT 衍生维护，ObjCAtlas 为 GPL-2.0-or-later，KernelCabinet/VTableBrook 为 GPL-3.0，PolicyMosaic 为 BSD-3-Clause，IDBMeadow 为 Apache-2.0。固定来源提交和不同样本的归属以各仓库 ORIGIN.md 与许可证为准。本轮 Codex 辅助修改不证明申请人独立编写了上游算法。

当前组合是 14 项新防御工具加 10 项保留研究工具，共 24 项公开仓库；另 14 个撤出的旧仓库均存在且保持私有。合法防御使用仍须与实际授权、受限任务、产品渠道、身份和组织对应。CVP 的适用性和申请结果均为 OPEN，任何构建、来源说明或 CI 都不能替代这些事实。
