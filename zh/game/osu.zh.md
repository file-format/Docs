{
  "date" : "2023-01-18",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"了解可以创建和打开 OSU 文件的 OSU 文件格式和 API。”,
  "title" :"OSU 文件 - Osu! 脚本文件格式",
  "linktitle" : "OSU",
  "menu" : {
    "docs" : {
      "identifier":"game-osu",
      "parent" : "game"
}
},
  "lastmod" : "2023-01-18"
}

## 什么是 .OSU 文件？

OSU 文件是为 osu! 编写的游戏脚本。节奏游戏。它包含有关游戏中使用的节拍图的信息，例如难度级别、要播放的歌曲以及玩家必须与音乐同步的命中对象的时间。它让节奏游戏玩家可以开发自定义挑战并与游戏社区分享。

**MIME 类型的 OSR 文件格式：** x-osu-beatmap

## 俄勒冈州立大学文件格式

OSU 文件作为纯文本文件保存到光盘，其结构在 [OSU 文件格式](https://osu.ppy.sh/wiki/en/Client/File_formats/Osu_%28file_format%29) 中非常明确地定义为奥苏！

### OSU 文件中的部分

典型的 OSU 文件包含以下部分。

|章节 |描述 |内容类型|
---|---|---|
|[一般]|关于谱面的一般信息|键：值对|
|[编辑器]|谱面编辑器的保存设置|键：值对|
|[元数据] |用于识别谱面的信息|键：值对|
|[难度] |难度设置|键：值对|
|[活动]| Beatmap 和故事板图形事件|逗号分隔列表|
|[时间点]|时间与控制要点|逗号分隔列表|
|[颜色]|组合和肤色|键：值对|
|[命中对象]|打对象|逗号分隔列表|

## 参考

* [俄勒冈州立大学！节奏游戏](https://osu.ppy.sh/home)
* [OSU文件格式](https://osu.ppy.sh/wiki/en/Client/File_formats/Osu_%28file_format%29)

