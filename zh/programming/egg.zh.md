{
  "date" : "2022-03-15",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EGG 文件格式 - Python 分发文件",
  "description":"了解 EGG 文件格式和可以创建和打开 EGG 文件的 API。",
  "linktitle" : "EGG",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-03-15"
}

## 什么是一 .egg 文件？

EGG 文件，也称为 Python 鸡蛋，是一种较旧的分布格式 Python 发行版。它是一个带有 .egg 扩展名的 [ZIP](/zh/compression/zip/) 压缩存档，包含 Python 应用程序的源文件以及有关分发的元信息。 EGG 文件是 Windows Executable [EXE](/zh/executable/exe/) 文件的替代品，但它是跨平台的。在 2010 年初，这种用于 Python 发行版的旧格式已被更新的 Wheel (WHL) 文件格式所取代。

## 蛋文件格式

EGG 文件保存为压缩的 ZIP 档案。这意味着如果您将 .egg 扩展名替换为 .zip，您将能够使用 Corel WinZIP、Microsoft Explorer 或 RARLAB WinRAR 等标准解压缩实用程序打开它。

可以使用 Python 提供的 **distutils** 包创建 EGG 文件。另一个可以创建和打开 EGG 文件的工具是 **SetupTools**。可以使用 **easy_install** 将 EGG 文件安装为一个包。

`注意 - EGG 文件格式已经过时，取而代之的是新的车轮 WHL 文件格式。

## 参考 ＃＃

* [Python EGG](https://python101.pythonlibrary.org/chapter38_eggs.html)

