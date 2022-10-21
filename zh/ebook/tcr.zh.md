{
  "date" : "2021-03-09",
  "keywords" :["TCR","Psion","扩展","格式","电子书"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"了解 Psion 3 系列的 TCR 文件格式以及可以创建和打开 tcr 文件的 API。",
  "title" :"TCR - Psion 系列 3 电子书文件",
  "linktitle" : "TCR",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-03-09"
}

## 什么是一 .tcr 文件？

在 90 年代初期，TCR 文件格式被引入用于古老的 **Psion Series 3** 掌上设备。该公司使用其特定于平台的压缩，这种格式对文本格式的支持非常有限。它是一种基于 ZVR 的文件格式，提供比 PalmDOC 更好的压缩率。它也适用于 FontMachine。尽管 TCR 文件格式属于已停产的设备，但仍可以使用某些电子阅读器读取此文件格式。这种文件格式也可以在桌面上使用 Sumatra PDF 以及 Windows 和 Linux 中的 Calibre 应用程序进行查看。

## 技术细节

由于 TCR 文件格式基于 ZVR 压缩器，它能够将许多文件减少大约 50% 的原始大小。 over 使用的压缩方案有点老了。压缩文件以包含可能显示在压缩文件中的 256 个可能符号的字典开头。字典包含每个这些符号的固定替代字符串。即使在 OPL 中，解压缩也变得非常快，并且可以从压缩文件中的任何位置开始。

## 打开 TCR 文件的问题##

如果您无法打开和运行 TCR 文件；这并不意味着您的设备上没有安装合适的软件。可能还有一些其他问题会阻止文件正常工作。可能的问题可能是以下之一：

- TCR 文件损坏。
- 错误链接到注册表项中的 TCR 文件。
- 从 Windows 注册表中删除了 TCR 的描述
- 支持 TCR 格式的应用程序安装损坏
- 带有不良恶意软件的受感染 TCR 文件。
- 计算机没有足够的硬件资源来操作 TCR 文件。
- 计算机用于打开 TCR 文件的驱动程序已过时。




## 参考

* [TCR - 通过 MobileRead](https://wiki.mobileread.com/wiki/TCR)
* [ZVR 压缩文本文件阅读器](https://iay.org.uk/zvr/)

