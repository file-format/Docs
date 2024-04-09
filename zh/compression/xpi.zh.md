{
  "date" : "2022-06-07",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XPI - 跨平台安装程序包文件",
  "description":"了解 XPI 文件格式和可以创建和打开 XPI 文件的 API。",
  "linktitle" : "XPI",
  "menu" : {
    "docs" : {
      "identifier": "compression-xpi",
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-07"
}

## 什么是一 .xpi 文件？

XPI 文件是经过压缩以减小文件大小的安装存档。 Mozilla 应用程序使用它来安装插件和附加文件。它在文件的根目录中包含安装脚本或清单以及许多数据文件。 XPI 文件可能包含主题、工具包或 Firefox 插件，用户可以安装这些插件以成为 Firefox 浏览器、Thunderbird 或 SeaMonkey 的一部分。

## XPI 文件格式 - 更多信息

XPI 文件以 [ZIP](/zh/compression/zip/) 档案形式保存到光盘，将多个文件组合成一个压缩文件。 XPI 文件中的文件可能包括安装脚本文件如 JS 和 web 文件如 [CSS](/zh/web/css/)、[HTML](/zh/web/html/) 和 [JSON](/zh/web/json/)。有时，它还可能包含 [PNG](/zh/image/png/) 图像文件，供插件用作图标。

### 如何查看 XPI 文件的内容？

XPI 文件实际上是一个 ZIP 存档，可以使用以下步骤查看其内容。

* 将文件扩展名从 XPI 更改为 ZIP
* 使用任何标准解压缩实用程序提取文件的内容，例如 WinZip (Windows, Mac)、7-Zip (Windows) 或 Apple Archive Utility (Mac)。

### 在 Firefox Android 上安装 XPI 文件

大多数人都很想知道 XPI 文件是否可以安装在 Android 设备上的 Firefox 中。在 Android 上，您可以从 XPI 文件中安装插件，方法是找到该文件并使用 Firefox 打开它。

## 参考

* [XPInstall - 维基百科](https://en.wikipedia.org/wiki/XPInstall)
* [如何打开 XPI 文件扩展名？](https://support.mozilla.org/en-US/questions/1009049)

