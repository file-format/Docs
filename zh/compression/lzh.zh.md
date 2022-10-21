{
  "date" : "2021-06-16",
  "keywords" :["LZH","压缩","文件","扩展名","文件格式","Lempel-Ziv","Haruyasu","LHA"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LZH 文件格式",
  "description":"了解 LZH 文件格式和可以创建和打开 LZH 文件的 API。",
  "linktitle" : "LZH",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-06-16"
}

## 什么是一 .lzh 文件？ ##

带有 .lzh 和 .lha 扩展名的文件通常与存档压缩文件格式有关。这种文件格式与[ZIP](/zh/compression/zip/)、[RAR](/zh/compression/rar/)等其他文件压缩格式相同。这些文件格式的主要目的是减小文件大小格式以便于发送以及以压缩形式将它们保存在一起。 AS 与其他西方公司相比，LZH 文件在日本非常流行，通常用于压缩视频游戏数据。 Windows 7 的 LZH 加载项内置于日文版 Windows 7 中。Microsoft 首次发布了日文版 Windows XP 的 Microsoft 压缩 (LZH) 文件夹加载项。此文件格式通过 Lempel-Ziv 和 Haruyasu 算法使用的压缩规定和功能实现

## LZH 规格 ##

LZH 存档的压缩方法显示为一个五字节的文本字符串，例如 -lz1-。这些是压缩文件中的第三个到第七个字节。

|规格|说明|
---|---|
|扩展 | .lzh, .lha|
|媒体类型|应用程序/x-lzh-压缩|
|类型代码| “LHA_"（LHA-空间）|
|尿路感染| public.archive.lha|
|开发者|吉崎春康(Yoshi)|
|类型|压缩|
|扩展自|拉克|

## 打开 LZH 文件的问题##

以下是可能导致 LZH 文件格式工作不佳的几个问题：
  

* 文件可能已损坏。要解决此问题，请重新下载文件或要求发件人重新发送文件
* 第二个原因是被感染的文件在这种情况下正确扫描文件
* LZH 文件的链接不正确
* 删除 LZH 的描述
* 没有足够的硬件资源
* 设备驱动程序过时

## 参考 ＃＃

* [LZH - By Wikipedia](https://en.wikipedia.org/wiki/LHA_(file_format))
