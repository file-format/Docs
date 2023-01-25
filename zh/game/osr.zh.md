{
  "date" : "2021-09-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"了解 OSR 文件格式和可以创建和打开 OSR 文件的 API。”,
  "title" :"OSR 文件 - osu! 重播文件格式",
  "linktitle" : "OSR",
  "menu" : {
    "docs" : {
      "identifier":"game-osr",
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## 什么是 .osr 文件？

OSR 文件是由 [osu!游戏](https://osu.ppy.sh/home)。大须！是一种节奏游戏，用户可以在其中将鼠标点击与音乐相匹配。用户播放的歌曲、点击率和未命中率、播放时间和日期以及总排名都记录在 OSR 文件中。然后可以与其他人共享此 OSR 文件以进行重播。 OSR 文件要求 beatmap 文件存在于“Songs”文件夹中。

**OSR 文件格式的 MIME 类型：** x-osu-replay

## OSR 文件格式

OSR 文件保存为具有固定和可变长度数据字段的二进制文件。

|数据类型|格式|
---|---|
|字节 |回放的游戏模式（0 = osu! 标准，1 = 太鼓，2 = 赶节奏，3 = osu!mania）|
|整数 |创建回放时的游戏版本（例如 20131216）|
|字符串 |osu!谱面 MD5 散列 |
|字符串|选手姓名|
|字符串|奥苏！重播 MD5 哈希（包括重播的某些属性）|
|短| 300个数|
|短|标准100s，太鼓150s，CTB 100s，mania 100s|
|短|标准50s数，CTB小果数，mania 50s|
|短|标准中的 Gekis 数量，狂热中的 Max 300s|
|短|标准卡图数量，疯狂200s|
|短|未命中数|
|整数|成绩单上显示的总分|
|短|成绩单上显示的最佳连击|
|字节|完美/完整组合（1 = 没有遗漏，没有滑块断裂，也没有提前完成的滑块）|
|整数|使用的模组。请参阅下面的 mod 值列表。|
|字符串|生命条形图：逗号分隔的 u/v 对，其中 u 是歌曲开始的时间（以毫秒为单位），v 是 0 - 1 之间的浮点值，表示您在给定时间的生命量（0 = 生命条是空，1=生命条已满）|
|长|时间戳（Windows 刻度）|
|整数|压缩重放数据的字节长度|
|字节|数组压缩回放数据|
|长|在线分数编号|
|双|附加模组信息。仅在启用 Target Practice 时出现。|

## 参考

* [俄勒冈州立大学！节奏游戏](https://osu.ppy.sh/home)
* [OSR 文件格式](https://osu.ppy.sh/wiki/en/Client/File_formats/Osr_%28file_format%29#data-types)

