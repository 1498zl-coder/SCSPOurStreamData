# 存储格式 2

`mirror.json` 是完整版本清单。`packs` 每项含固定 tag、附件名、大小、SHA256；媒体包另含 program_id 和原 manifest/index 身份。`members` 声明压缩索引的大小、SHA256、展开上限和条目数。

`members.tsv.gz` 为 ASCII TSV，每行八列：逻辑键、包号(从0开始)、ZIP成员数据offset、编码长度、原始长度、原始SHA256、方法(0=STORE/8=DEFLATE)、ZIP内成员名。游戏逻辑键为 D/XX/26位文件名，媒体键为四位节目编号/成员名。

首装可整包读取；少量补缺可严格 Range 读取完整成员并校验原SHA。包与版本索引不可原位替换。后续完整清单可固定引用历史tag，不使用latest地址。
