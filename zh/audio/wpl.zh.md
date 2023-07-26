{
  "date" : "2021-06-11",
  "keywords" :["wpl","wpl 文件","扩展名","格式","什么是 wpl 文件","音乐","wpl 文件格式"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"了解 WPL 文件格式和可以创建、转换和打开 WPL 文件的 API。",
  "title" :"WPL - Windows Media Player 播放列表文件",
  "linktitle" : "WPL",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-06-11"
}

## 什么是一 .wpl 文件？
扩展名为 .wpl 的文件包含要在 Microsoft Windows Media Player 上运行的歌曲的播放列表。这些文件通常由用户为其视频和音频收藏创建。 WPL 文件中写入的内容，只是 .wpl 文件的创建者选择的多媒体文件的目录路径或位置，因此媒体播放器应用程序可以迅速从其目录位置找到并播放多媒体内容。

## WPL 文件格式
WPL（Windows Media Player 播放列表）是 Microsoft Windows Media Player 9 或更高版本中使用的专有文件格式。它是一种存储多媒体播放列表的计算机文件格式。默认情况下，播放列表以 .wpl（Windows Media Player 播放列表）扩展名保存。如果您想在不支持此扩展名的设备上播放数据光盘，您可以改用 [.m3u](/zh/audio/m3u/) 扩展名。 WPL 文件的元素以 XML 格式表示。顶级元素“smil"指定文件的元素遵循同步多媒体集成语言 (SMIL) 结构。该文件以 .wpl 扩展名创建并保存，其 MIME 类型为 application/vnd.ms-wpl。

### WPL 示例
这是一个 wpl 文件的示例：
```
<?wpl version="1.0"?>
<smil>
    <head>
        <meta name="Generator" content="Microsoft Windows Media Player -- 11.0.5721.5145"/>
        <meta name="AverageRating" content="33"/>
        <meta name="TotalDuration" content="1102"/>
        <meta name="ItemCount" content="3"/>
        <author/>
        <title>Bach Organ Works</title>
    </head>
    <body>
        <seq>
            <media src="\\server\vol\music\Classical\Bach\OrganWorks\cd03\audio01.mp3"/>
            <media src="\\server\vol\music\Classical\Bach\OrganWorks\cd03\audio02.mp3"/>
            <media src="SR15.mp3" tid="{35B39D45-94D8-40E1-8FC2-9F6714191E47}"/>
        </seq>
    </body>
</smil>
```




## 参考 ＃＃

* [MPEG-1 Audio Layer II - 维基百科](https://en.wikipedia.org/wiki/MPEG-1_Audio_Layer_II)


