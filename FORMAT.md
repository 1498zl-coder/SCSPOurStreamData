# 存储格式2

mirror.json是完整版本清单；packs每项记录固定tag、附件名、大小、SHA256。节目包另含节目编号、原manifest和source.index摘要。members记录压缩索引摘要、展开上限和数量。

members.tsv.gz为ASCII TSV，八列依次为：逻辑键、包号(从0开始)、ZIP成员数据offset、编码长度、原始长度、原始SHA256、压缩方法(0=STORE/8=DEFLATE)、ZIP内成员名。游戏键为D/XX/26位文件名，媒体键为四位节目编号/成员名。

包名是pack-<完整包SHA256>.zip。首装可整包读取，少量补缺可严格Range取得成员；任何启用内容均验证原文件SHA。包和已发布索引不原位替换；版本索引可固定引用历史tag。

版本目录中的new_package_bytes仅统计当前tag新增包；package_bytes为完整目标引用的全部包。用户实际下载量由本地已验证内容决定，不能直接等同于新上传量或完整包体积。
