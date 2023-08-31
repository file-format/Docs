{
  "date" : "2022-01-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LRC 文件格式 - 什么是 LRC 文件？",
  "description":"了解 LRC Lyric 文件和可以创建和打开 LRC 文件的 API。",
  "linktitle" : "LRC",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-26"
}

## 什么是一 .LRC 文件？

LRC 文件是基于文本的歌词文件，其中包含音频歌曲的歌词。当用电脑上的音乐播放器或音频播放软件播放音频歌曲时，LRC文件被并行读取并随时间显示。 LRC 文件包含用于在歌曲播放时显示歌词的提示点。通常，LRC 文件与对应的音频文件具有相同的名称，例如 audio.mp3 和 audio.lrc。 LRC 文件类似于 [SRT](/zh/video/srt/) 等字幕文件。

## LRC 文件格式 - 更多信息

LRC 歌词格式文件保存为纯文本文件，可以在文本文件中打开和编辑。 LRC 文件的内容包含用于显示歌词文本的颜色信息。

## LRC 格式

随着时间的推移，已经开发了多种格式的 LRC 文件。这些

### 简单的 LRC 格式

行时间标签的格式为 `[mm:ss.xx]`，其中 mm 是分钟，ss 是秒，xx 是百分之一秒。

```
[00:12.00]Line 1 lyrics
[00:17.20]Line 2 lyrics
[00:21.10]Line 3 lyrics
...
mm:ss.xxlast lyrics line
```

### 简单格式扩展

它包括通过使用 M：Male、F：Female、D：Duet 来更改和指定歌词性别的能力。

```
[00:12.00]Line 1 lyrics
[00:17.20]F: Line 2 lyrics
[00:21.10]M: Line 3 lyrics
[00:24.00]Line 4 lyrics
[00:28.25]D: Line 5 lyrics
[00:29.02]Line 6 lyrics
```
### 增强的 LRC 格式

增强型 LRC 格式是 Simple LRC 格式的扩展版本。它在格式中添加了一个字时间标签`<mm:ss.xx>`在上一个单词的末尾。

```
[ar: Jade Michael]
[al: Sarah Hi]
[au: Jade Michael]
[length: 2:58]
[by: lrc-maker]
[ti: Somebody to Love]

[00:00.00] <00:00.04> When <00:00.16> the <00:00.82> truth <00:01.29> is <00:01.63> found <00:03.09> to <00:03.37> be <00:05.92> lies
[00:06.47] <00:07.67> And <00:07.94> all <00:08.36> the <00:08.63> joy <00:10.28> within <00:10.53> you <00:13.09> dies
[00:13.34] <00:14.32> Don't <00:14.73> you <00:15.14> want <00:15.57> somebody <00:16.09> to <00:16.46> love
```

## 参考

* [LRC 歌词文件格式 - 维基百科](https://en.wikipedia.org/wiki/LRC_(file_format))

