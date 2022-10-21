{
  "date" : "2019-10-11",
  "keywords" :["tgs 文件","tgs 文件格式","什么是 tgs 文件","文件","tgs 示例","tgs 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TGS - 电报动画贴纸文件格式",
  "description":"了解 TGS 文件格式和可以创建和打开 TGS 文件的 API。",
  "linktitle" : "TGS",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-02"
}

## 什么是一 .tgs 文件？

扩展名为 .tgs 的文件是由跨平台消息服务 [Telegram](https://core.telegram.org/animated_stickers) 引入的动画贴纸文件。消息应用程序用户使用动画贴纸在消息中发送更多增强和生动的内容，这与静态图像的静态图形不同。 Telegram 最初使用 [WEBP](/zh/image/webp/) 文件格式用于静态图像贴纸。与静态 WEBP 贴纸相比，TGS 文件格式可以以更高分辨率和更小的文件大小存储动画数据。可以使用 Telegram、7-zip、Apple Archive Utility 和 Corel WinZip 等应用程序打开 TGS 文件。

## TGS 文件格式

Telegram 早在 2019 年 7 月就引入了基于 Lottie 库的 TGS 文件格式。 TGS 文件包含从 Adobe After Effects 中的动画导出的 [JSON](/zh/web/json/) 文本。导出的 JSON 文本使用 gzip 压缩来压缩，从而减小文件大小。文本文件的 JSON 信息存储在文本文件中，成为高压缩率的基础。

### TGS 贴纸规格

TGS 文件格式对 TGS 动画贴纸的创建施加了某些限制。 TGS 动画文件：

* 贴纸/画布尺寸必须为 512х512 像素。
* 贴纸对象不得离开画布。
* 动画长度不得超过 3 秒。
* 所有动画必须循环播放。
* 在 Bodymovin 中渲染后，贴纸大小不得超过 64 KB。
* 所有动画必须以每秒 60 帧的速度运行。

### 示例 TGS JSON 文本

示例动画贴纸在解压缩后包含以下 JSON 文本内容。
```
$ head -c 200 animated-sticker
{"tgs":1,"v":"5.5.2","fr":60,"ip":0,"op":180,"w":512,"h":512,"nm":"C-07","ddd":0,"assets":[],"comps":[],"layers":[{"ddd":0,"ind":1,"ty":3,"nm":"master","sr":1,"ks":{"o":{"a":0,"k":0},"r":{"a":0,"k":0}
```
## 参考 ＃＃

* [TGS](https://core.telegram.org/animated_stickers)
* [gzip - 维基百科](https://en.wikipedia.org/wiki/Gzip)

