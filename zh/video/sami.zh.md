{
"date": "2023-05-16",
  "keywords": [
"萨米文件",
"什么是 sami 文件",
"sami 文件示例",
"文件",
"sami 文件扩展名",
"扩大"
],
  "author": {
"display_name": "沙基尔·法伊兹"
},
"draft": "false",
"toc": true,
"title": "SAMI 文件格式 - 字幕和元数据交换文件",
  "description":"了解 SAMI 格式以及可以创建和打开 SAMI 文件的 API。",
"linktitle": "萨米",
  "menu": {
    "docs": {
      "identifier": "video-sami",
"parent": "video"
}
},
"lastmod": "2023-05-16"
}

## 什么是 .sami 文件？

扩展名为".sami"的文件通常指的是字幕和元数据交换 (SAMI) 文件。 SAMI 是一种字幕格式,用于在视频中显示字幕或隐藏式字幕。它最初是由 Microsoft 为其 Windows Media Player 开发的。

SAMI 文件包含字幕或隐藏式字幕的计时信息和文本内容,允许它们与视频播放同步。该格式支持基本的格式选项,例如字体样式,颜色和字幕在屏幕上的位置。

SAMI 文件通常是纯文本文件,可以使用文本编辑器打开和编辑。 SAMI 文件的内容通常包括提供有关文件信息的标头部分,后面是各个字幕条目及其各自的时间和文本。

以下是 SAMI 文件的示例：

```
<SAMI>
<HEAD>
<TITLE>Example Subtitles</TITLE>
</HEAD>
<BODY>
<SYNC Start=100><P Class=ENCC>Subtitle 1</P></SYNC>
<SYNC Start=500><P Class=ENCC>Subtitle 2</P></SYNC>
<SYNC Start=1000><P Class=ENCC>Subtitle 3</P></SYNC>
</BODY>
</SAMI>
```

SAMI 文件通常与支持字幕显示的视频播放器或媒体播放器（例如 Windows Media Player 或 VLC Media Player）结合使用。播放器读取SAMI文件并将字幕与视频内容同步,让观众在观看视频的同时阅读字幕。

## 支持的 HTML 标签

SAMI（字幕和元数据交换）文件支持一组有限的类似 HTML 的标签,用于格式化和样式化字幕。以下是 SAMI 支持的一些常用标签：

-``<SAMI> :`` 封装整个 SAMI 文件的根元素。
-``<HEAD> :`` 包含 SAMI 文件的标头信息。
<html>-``<TITLE> :`` 指定 SAMI 文件的标题。 </html>
-``<BODY> :`` 包含字幕条目及其时间信息。
-``<SYNC> :`` 表示字幕条目的同步点。它指定显示字幕的时间。
-``<P> :`` 包含字幕的实际文本内容。它通常用于<SYNC>堵塞。
<html>- `` <FONT>:`` 定义所包含文本的字体属性。颜色,外观,大小和样式等属性可用于修改字体外观。</font>
-``<BR> :`` 在副标题内插入换行符。
<html>- `` <B>:`` 以粗体显示所包含的文本。</b>
<html>- `` <I>:`` 以斜体显示包含的文本。</i>
<html>- `` <U>:`` 使所包含的文本带有下划线。</u>
-``<C> :`` 指定屏幕上字幕文本的位置或对齐方式。它支持 Center,Middle,Left,Right,Top,Bottom 及其组合等属性。
-``<LANG> :`` 指定字幕文本的语言代码。它有助于识别字幕的语言。

这些是 SAMI 文件支持的一些基本标签。值得注意的是,SAMI 不支持全部 HTML 标记和属性。支持的标签主要集中于字幕的样式和定位,而不是提供广泛的文档结构或交互性。

## 参考
* [萨米](https://en.wikipedia.org/wiki/SAMI)

