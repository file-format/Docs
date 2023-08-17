{
  "date" : "2021-03-12",
  "keywords" :["VP9","文件","扩展名","文件格式","视频格式","TrueMotion Video","VPX","On2 Technologies"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VP9 - TrueMotion 视频文件",
  "description":"了解 VP9 文件格式和可以创建和打开 VP9 文件的 API。",
  "linktitle" : "VP9",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-03-27"
}

## 什么是 VP9 文件？

Google 开发了 VP9 编解码器，作为 VP8 的继任者，作为免版税、开源的视频编码标准。它最初旨在压缩 YouTube 上的超高清内容，因为它扩展并增强了其前身的编码效率。如果说最初的 VPX 编解码器，它们来自于 2010 年被谷歌同化的 On2 Technologies。谷歌后来开源了该编解码器。 VP8 和 VP9 两种格式都可在免费的 BSD 许可下使用，该许可允许运营商在专有软件和开源软件中组织编码或解码能力，而无需透露其源代码。

## VP9的技术特点

* VP9 提供高达 120 fps 和多个色彩空间的最大分辨率 8192x4352，包括 Rec 601、Rec 709、Rec 2020、SMPTE-170、SMPTE-240 和 sRGB
* 这种格式完全支持从低比特率压缩到高质量超高清的所有网络和移动用例，此外还支持 10/12 位编码和 HDR
* 与其他产品相比，它可以将视频比特率降低多达 50%
* 它支持自适应流媒体，并被 YouTube 和其他知名网络视频提供商使用
* Chrome、Opera、Edge、Firefox、Android 设备，以及数百万台智能电视，支持解码此编解码器
* 大于1080p的视频分辨率通过VP9修改，允许无损压缩
* 不同的色彩空间，如 Rec。 601，建议。 709，建议。 VP9 支持 2020、SMPTE-170、SMPTE-240 和 sRGB
* VP9 也可以支持使用混合对数伽玛和感知量化器的 HDR 视频


## 历史简介

* VP9 视频编解码器开发于 2011 年开始，其解码器已于 2012 年 12 月添加到 Chromium 网络浏览器中
* 其首个谷歌Chrome浏览器版本于2013年2月发布，当时发布解码
* Google 于 2013 年 8 月发布了 Chrome 29.0.1547，最终支持 VP9
* 2013 年 10 月，本能的 VP9 解码器被添加到 FFmpeg
* Mozilla 于 2013 年 12 月在 2014 年 3 月 18 日发布的版本 2 中为 Firefox 添加了 VP9 支持
 

## VP9的工作

通常，4K 视频通过缩小特定像素来提高图像质量，VP9 编解码器和 HEVC 使它们变大以缩小比特率和文件大小。虽然这似乎是矛盾的，但编码引擎会采用较大的像素并将它们更改为更好的分辨率生产力。包含视频帧的源视频被编码或压缩以形成压缩视频比特流。每个单独的帧首先被分成像素块。然后仔细检查这些块以进行 3D 消除，并评估帧之间的顺序连接以利用无法更改的区域。这些是通过运动矢量编码的，以确保下一帧上给定块的质量。使用有效的二进制压缩对残差信息进行编码。

## 参考

* [VP9 维基百科](https://en.wikipedia.org/wiki/VP9)
* [MDN 网络文档](https://developer.mozilla.org/en-US/docs/Web/Media/Formats/Video_codecs#vp9)
* [椰子](https://www.coconut.co/)

