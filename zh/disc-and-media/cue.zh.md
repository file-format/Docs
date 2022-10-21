{
  "date" : "2021-06-09",
  "keywords" :["cue","文件","扩展名","格式","什么是 cue 文件","音乐","cue 文件格式","cue 文件格式规范","cue sheet","CDRWIN" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"了解 CUE 文件格式和可以创建、转换和打开 CUE 文件的 API。",
  "title" :"CUE - 提示表文件",
  "linktitle" : "CUE",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-07-01"
}

## 什么是一 .cue 文件？

扩展名为 .cue 的文件，也称为提示表文件，是一种元数据文件，其中包含有关 CD 或 DVD 上轨道布局的信息。这些由媒体播放器和光盘创作应用程序支持。存储在 CD 上的主要音频数据由 cue 文件引用，以及轨道长度、光盘标题和表演者的规范。因此，如果单个音频文件包含多个音轨，则可以使用 cue 文件将音频分成多个文件或引用多个音轨。

## 提示文件格式

CUE 或提示表文件以人类可读的纯文本格式存储。提示文件中的信息是带有一个或多个参数的命令。这些命令要么适用于整个文件，要么适用于单个轨道，具体取决于特定的命令和上下文。 CDRWIN 用户指南描述了提示表语法和语义的规范。

## CUE 表基本命令

|命令|描述|
---|---|
|文件|指包含数据及其格式的文件，例如[MP3]（/audio/mp3/）、[WAV]（/audio/wav/）或普通二进制光盘映像）|
|跟踪| | 定义轨道上下文信息，例如其编号和类型或模式。
|索引|将位置表示为 FILE 中的索引。格式为 mm:ss:ff（分-秒-帧）。|
|PREGAP 和 POSTGAP|这表示轨道的前间隙或后间隙，它不存储在任何数据文件中。长度以与 INDEX 相同的分秒帧格式指定。|

### CUE 表示例

```
REM GENRE Electronica
REM DATE 1998
PERFORMER "Faithless"
TITLE "Live in Berlin"
FILE "Faithless - Live in Berlin.mp3" MP3
  TRACK 01 AUDIO
    TITLE "Reverence"
    PERFORMER "Faithless"
    INDEX 01 00:00:00
  TRACK 02 AUDIO
    TITLE "She's My Baby"
    PERFORMER "Faithless"
    INDEX 01 06:42:00
  TRACK 03 AUDIO
    TITLE "Take the Long Way Home"
    PERFORMER "Faithless"
    INDEX 01 10:54:00
  TRACK 04 AUDIO
    TITLE "Insomnia"
    PERFORMER "Faithless"
    INDEX 01 17:04:00
  TRACK 05 AUDIO
    TITLE "Bring the Family Back"
    PERFORMER "Faithless"
    INDEX 01 25:44:00
  TRACK 06 AUDIO
    TITLE "Salva Mea"
    PERFORMER "Faithless"
    INDEX 01 30:50:00
  TRACK 07 AUDIO
    TITLE "Dirty Old Man"
    PERFORMER "Faithless"
    INDEX 01 38:24:00
  TRACK 08 AUDIO
    TITLE "God Is a DJ"
    PERFORMER "Faithless"
    INDEX 01 42:35:00
```
## 参考

* [.cda 文件 - 维基百科提供](https://en.wikipedia.org/wiki/.cda_file)

