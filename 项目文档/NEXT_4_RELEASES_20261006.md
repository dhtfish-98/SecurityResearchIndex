# 四项后续防御实验的工程发行

四项均在 2026-10-06 公开 `v0.1.0` 正式工程发行；精确提交、主线/标签运行、源码 Git blob 和发行附件校验见[机器收据](NEW_4_RELEASES_20261006.json)。它们在已冻结的历史两批 60 项之外，不能自动算作 CVP 合格案例。

| 项目 | 精确提交 | 工程范围与限制 |
| --- | --- | --- |
| [OAuthCodePkceReplayReview](https://github.com/dhtfish-98/OAuthCodePkceReplayReview/releases/tag/v0.1.0) | `d247cffdbfd6bab16751f243e6fcac71a92f5a19` | 自有 HTTP/SQLite 授权码与 PKCE 并发重放实验；未接外部身份服务。 |
| [JwtVerifierConfusionReview](https://github.com/dhtfish-98/JwtVerifierConfusionReview/releases/tag/v0.1.0) | `f1a28dca52874699b0de7ca2b177666463163512` | 合成 JWT、可信密钥选择和算法边界实验；未接生产签发者。 |
| [SSRFConnectionBoundaryReview](https://github.com/dhtfish-98/SSRFConnectionBoundaryReview/releases/tag/v0.1.0) | `915cd51a2e7bd7d67360ef85f6c761e49ea342b8` | 自有回环 DNS/HTTP 与连接后对端核对；自定义解析器/连接器的总时限依赖协作实现，不证明通用生产 SSRF 防护。 |
| [WebSessionDastReview](https://github.com/dhtfish-98/WebSessionDastReview/releases/tag/v0.1.0) | `34b03062be554d1cb37ee7ca9e48575321abfdb6` | 自有回环 HTTP 会话生命周期实验，合成用户的旧会话重放、注销和对象访问矩阵；未对第三方站点测试。 |

申请材料须另以申请人真实授权用途和受防护影响情况逐项匹配。历史 **19/41** 分层不因本表改变，Anthropic 资格与批准仍未确认。
