# CITrustBoundaryReview v0.1.4 独立发行后只读验收

复核时间：2026-10-06（Asia/Tokyo）。范围为公开仓库、公开 GitHub Actions、公开 Release 四附件的重新下载字节、下载包内代码与权利文件，以及从下载 wheel 独立运行的惰性合成工作流。没有修改公开仓库、Release、项目树或目标工作流。

## 结论

**PASS：发行绑定、CI、附件完整性和本次直接 `run` secret 漏报回归。** 公开 `main`、注释标签 `v0.1.4` 的目标、Release manifest 均指向提交 [`5a18be56c75d4814e321010f2f3def090b50615a`](https://github.com/dhtfish-98/CITrustBoundaryReview/commit/5a18be56c75d4814e321010f2f3def090b50615a)。[Release](https://github.com/dhtfish-98/CITrustBoundaryReview/releases/tag/v0.1.4) 已正式发布，非草稿/预发行；标签对象 `4dc4c25877f4e7ef53be3b382acdb578359e586f` 指向该提交。主线和标签两条 CI 分别为 [37392093765](https://github.com/dhtfish-98/CITrustBoundaryReview/actions/runs/37392093765) 与 [37392549828](https://github.com/dhtfish-98/CITrustBoundaryReview/actions/runs/37392549828)，head SHA 都是上述提交，Python 3.11、3.14 四个 job 均 `completed/success`。每个 job 的日志有两次 `Ran 42 tests`，分别对应源码和新装 wheel 消费者。CI 没有运行 sdist 安装消费者；Release 中 sdist 42/42 的依据是同提交本地回执，不能把它归入托管 CI 结论。

四附件从 GitHub Release 重新下载，字节大小及 SHA-256 均与 GitHub API 的 `digest` 相同；`SHA256SUMS.txt` 的三项与下载字节相同，manifest 的两项包摘要、提交及标签对象也相同：

| 附件 | 字节 | SHA-256 |
| --- | ---: | --- |
| wheel | 49,256 | `75b953f29baa47ebe4a27a6d6fa608503b223d2d18907fee385e819033560c36` |
| sdist | 68,649 | `3f13282a29ee3e5c92e63e55d3e7f77986f29d62a3f0c0818ac81372b7607d21` |
| `RELEASE_MANIFEST.json` | 1,347 | `eb25b358a234b3812b1b468ced5fdb3916d6def66efa815197569c7e0e7ea7bb` |
| `SHA256SUMS.txt` | 306 | `aa592bfae414da181f358fcaa75b288c55f6c4be615834f4190555f51c0045f8` |

下载 wheel、sdist 和公开提交的八个 Python 运行模块逐字节一致。wheel 的 `ORIGIN.md`、`NOTICE`、`LICENSE` 与公开提交文档逐字节一致。包元数据为 0.1.4，Author/Maintainer 都是 `dhtfish98`。固定 zizmor 上游 `56941012a98a93ccb3846dc625f64ee1d97f623e` 的原 MIT LICENSE 前 1109 字节在包 LICENSE 中逐字保留；原 William Woodruff 版权、PyYAML 独立依赖、维护者代码归属在 ORIGIN/NOTICE 中分列。作者字段仅是包署名，不能单独证明实际个人贡献。

下载 wheel 的 `review.py` 由 wheel 压缩包直接导入，再运行六个独立构造的惰性输入。`pull_request` 默认 checkout 后 `./inert.sh "${{ secrets.GITHUB_TOKEN }}"` 得到 `FAIL / privileged_workspace_execution`、零 OPEN；同 secret 经 step `env` 传入也得到相同结果。仅 `echo` 数据和无 secret 脚本均 `PASS`。`pull_request_target` 默认 checkout 的相同直接 secret 没有该 finding，因未提供 workspace 程序体为 `OPEN`。`github.token` 变体为 `OPEN`（未解析表达式），没有被误报为 PASS。输入未执行、没有提供实际令牌；逐项 SHA、状态及模块路径见 [内含 `independent-replay.json` 的 v1.0.4 独立证据包](https://github.com/dhtfish-98/SecurityResearchIndex/releases/download/v1.0.4/CITRUST_V0_1_4_INDEPENDENT_EVIDENCE_20261006.tar.gz)。

## 边界与残留

在上述有限回归中未发现新的关键 false PASS。项目声明的是九条有限静态规则；未知动作、shell、token 实际可用性、具体权限、脚本行为和可利用性仍为 **OPEN**。`github.token` 的敏感度目前没有被确定为 FAIL，实测以 OPEN 关闭；这是一个可继续覆盖的语义空白，但没有足够证据将它当成当前 0.1.4 已承诺规则的违反。公开 Release 的“合成演示、无真实 token/脚本执行、CVP 未验证”表述与证据一致。不能据本次 PASS 宣称真实攻击链、保护效果、申请人身份或 CVP 合格/录取。

精确可复核材料保存在本索引 v1.0.4 的[独立验收证据包](https://github.com/dhtfish-98/SecurityResearchIndex/releases/download/v1.0.4/CITRUST_V0_1_4_INDEPENDENT_EVIDENCE_20261006.tar.gz)：`public-api-claims.json`、`verify_public.py`、`independent-replay.json`、`verify_release.py`、`main-ci.log`、`tag-ci.log` 以及 `downloads/` 中四个原始附件。`public-api-claims.json` 记录查询时的公开 main 与 run 状态；后续 main 如有推进，需要重新绑定时间点，不能复用此快照。
