# SCSPOurStreamData

棱镜拾光 · Prism Memories 的OurSTREAM 节目资源独立数据仓库。客户端 2.18.0，资源 20006100。

资源按不可变内容包存放在 Releases，仓库文件提供版本入口和阅读目录。推荐通过支持本版本的启动器下载；每个文件都按原始 SHA256 校验。

## 当前版本

[ourstream-61-v2](https://github.com/1498zl-coder/SCSPOurStreamData/releases/tag/ourstream-61-v2)：61 个独立包，约 5.53 GB。

- [完整版本入口](versions/current.json)
- [资源目录](CATALOG.md)
- [存储与索引格式](FORMAT.md)

Release 中的 `mirror.json` 给出包清单，`members.tsv.gz` 给出文件位置。基础和增量包使用同一格式；各版完整索引可以引用历史包，无需依次安装补丁。

GitHub 自动提供的 Source code ZIP/TAR 只包含仓库说明，不包含游戏或节目正文。玩家资料、认证信息、存档、照片与日志不属于此仓库。
