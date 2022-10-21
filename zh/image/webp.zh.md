{
  "date" : "2019-10-11",
  "keywords" :["webp 文件","webp 文件格式","什么是 webp 文件","文件","webp 示例","webp 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"WEBP - 谷歌光栅图像文件格式",
  "description":"了解 WEBP 文件格式和可以创建和打开 WEBP 文件的 API。",
  "linktitle" : "WEBP",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## 什么是一 .WEBP 文件？

WebP 由 Google 推出，是一种基于无损和有损压缩的现代光栅 Web 图像文件格式。它提供相同的图像质量，同时大大减小了图像尺寸。由于大多数网页使用图像作为数据的有效表示，因此在网页中使用 WebP 图像会导致网页加载速度更快。根据 Google 的说法，WebP 无损图像的大小比 [PNG](/zh/image/png/) 小 26%，而 WebP 有损图像比可比较的 [JPEG](/zh/image/jpeg/) 图像小 25-34%。基于 WebP 和其他图像文件格式之间的结构相似性 (SSIM) 索引比较图像。 WebP 是 [WebM](https://en.wikipedia.org/wiki/WebM) 多媒体容器格式的姊妹项目。

## WebP 功能概述 ##

WebP 图像使用基于对其周围块的像素预测的压缩过程，从而导致在单个文件中多次使用像素。它支持动画图像，预计未来将支持更多功能。 Google 已提供其编码器和解码器的源代码 [在线](https://developers.google.com/speed/webp/download)，以便在需要时使用。 WebP 图像支持：

* **有损压缩：**有损压缩基于 [VP8](http://en.wikipedia.org/wiki/VP8) 关键帧编码。 VP8 是 On2 Technologies 创建的一种视频压缩格式，是 VP6 和 VP7 格式的继承者。
* **无损压缩：** 无损压缩格式由 WebP 团队开发。
* **透明度：** 8 位 Alpha 通道对图形图像很有用。 Alpha 通道可以与有损 RGB 一起使用，这是目前任何其他格式都没有的功能。
* **动画：**它支持真彩色动画图像。
* **元数据：** 它可能有 EXIF 和 XMP 元数据（例如，由相机使用）。
* **颜色配置文件：** 它可能具有嵌入的 ICC 配置文件。

有损 WebP 压缩使用预测编码对图像进行编码，与 VP8 视频编解码器用于压缩视频中的关键帧的方法相同。预测编码使用相邻像素块中的值来预测块中的值，然后仅对差异进行编码。

无损 WebP 压缩使用已经看到的图像片段来精确重建新像素。如果没有找到有趣的匹配，它也可以使用本地调色板。

## 文件格式 ＃＃

WebP 文件格式基于 RIFF（资源交换文件格式）文档格式。 WebP 容器提供对以上功能的支持，而不是仅包含编码为 VP8 关键帧的单个图像。 RIFF 文件的基本元素是一个块，它包括：


|字段|描述
---|---|
|块 FourCC：32 位|用于块识别的 ASCII 四字符代码
|Chunk Size: 32 bits (uint32)|不包括该字段、块标识符或填充的块大小
|块负载：块大小字节|数据负载。如果 Chunk Size 是奇数，则添加一个应该为 0 ~-~- 的填充字节 ~-~-
|ChunkHeader ('ABCD')|用于描述各个chunk的FourCC和Chunk Size header，其中'ABCD'是chunk的FourCC。该元素的大小为 8 个字节。

### WebP 标头###

WebP 文件头如下：

* RIFF Header - 代表 ASCII 字符 'R' 'I' 'F' 'F' 的 32 位
* 文件大小 - 32 位 (uint32) 表示从偏移量 8 开始的文件大小（以字节为单位）。该字段的最大值为 2^32 减去 10 字节，因此整个文件的大小最多为 4GiB 减去 2 字节.
* 'WEBP' - 32 位代表 ASCII 字符 'W' 'E' 'B' 'P'

### 有损文件格式###

如果图像基于有损编码并且不需要任何高级/扩展功能（例如透明度、动画、alpha 等），则 WebP 图像使用有损文件格式。有损图像更小，并且也受旧应用程序的支持。

在这种情况下，WebP 文件包括：

* 12 字节 WebP 文件头
* VP8 块

[VP8 数据格式和解码指南](https://tools.ietf.org/html/rfc6386) 说明了 VP8 比特流格式规范。

### 无损文件格式###

当图像基于无损编码并且不需要外部格式提供的高级功能时使用此布局。但是，较旧的应用程序可能无法读取此类文件。

在这种情况下，WebP 文件包括：

* 12 字节 WebP 文件头
* VP8L 块

## 参考 ＃＃

* [WebP 开发者参考 - 由 Google 提供](https://developers.google.com/speed/webp/)
* [WebP 文件格式 - 维基百科提供](https://en.wikipedia.org/wiki/WebP)

