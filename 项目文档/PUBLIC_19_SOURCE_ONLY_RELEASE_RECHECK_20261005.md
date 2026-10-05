# 19 个仅源码发行仓的归档回下载核对

以 [104 个已发行软件仓的冻结发行元数据](PUBLIC_104_RELEASE_VERSION_RECHECK_20261005.md)为范围，19 个未上传独立附件的正式 Release 均有 GitHub 自动提供的源码归档。本轮逐一从对应标签下载这 19 个归档，共 1,006,572 字节、665 个普通文件；归档 SHA-256、标签、文件数和逐仓结果见[机读记录](PUBLIC_19_SOURCE_ONLY_RELEASE_ARCHIVES_20261005.json)，本地记录 SHA-256 为 `6a66b5f076e67140cf2003d80eedf6931446ca6060d4897cfa7549d6f816ff9b`。

19/19 个归档均能读取；标签版本与各自 `pyproject.toml`、根 `CMakeLists.txt` 或「项目文档/README.md」的当前版本声明一致，均有「项目文档/LICENSE」。所读归档路径都有「项目文档」，`Build` 之下只含 `.gitignore`；未发现所筛的编译产物扩展名、越界路径或特殊归档成员。这补足了[先前仅看 GitHub 附件元数据的范围](PUBLIC_104_RELEASE_VERSION_RECHECK_20261005.md)。GitHub [正式 Release 的源码归档说明](https://docs.github.com/en/repositories/releasing-projects-on-github/about-releases)解释了为何这些仓库无自传附件仍可下载源码。

本项不等于对 665 个文件逐行语义审核、安装运行、检查历史提交，亦不证明 CVP 资格。归档路径与版本是本轮实证，源码功能和真实防御用途仍按各项目的有界证据及申请人的实际情况分别判断。
