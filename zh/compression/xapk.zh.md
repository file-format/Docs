{
  "date" : "2021-04-11",
  "keywords" :["xapk 文件","xapk 文件格式","什么是 xapk 文件","文件","xapk 示例","xapk 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XAPK - 元包文件格式",
  "description":"了解 XAPK 文件格式和可以创建和打开 XAPK 文件的 API。",
  "linktitle" : "XAPK",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-11"
}

## 什么是一 .xapk 文件？

扩展名为 .xapk 的文件是一个压缩包文件，用于在移动设备上安装 Android 应用程序。它是一种容器文件格式，其中包含安装所需的 APK 和其他相关文件。另一个关联文件是 OBB 文件，其中存储了保持应用程序运行所需的其他文件，例如图形、媒体文件和应用程序数据。 XAPK 文件不受 Google Play 支持，仅用于在第三方 Android 应用下载网站上分发。这些可以使用 XAPK Installer 安装到 Android 设备上。

## XAPK 文件格式

XAPK 文件使用标准 [ZIP](/zh/compression/zip/) 文件格式压缩。这些可以使用标准压缩/解压缩软件（例如 WinZIP）提取。将 XAPK 文件解压缩到光盘后，文件夹中包含以下文件。

* APK - 用于在 Android 设备上安装应用程序的标准安装文件
* OBB - 包含相关资源文件的附加文件

## 参考

* [Android 包文件](https://en.wikipedia.org/wiki/Android_application_package)

