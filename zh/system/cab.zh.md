{
  "date" : "2021-06-29",
  "keywords" :["CAB","扩展","文件","格式","系统","Windows 文件柜文件","Microsoft","安装程序","SetUp","AdvPak"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CAB - Windows 内阁文件",
  "description":"了解 CAB 文件格式和可以创建和打开 CAB 文件的 API。",
  "linktitle" : "CAB",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-06-29"
}

## 什么是一 .cab 文件？ ##

带有 .cab 扩展名的文件属于属于系统文件类别的 windows cabinet 文件。它是在支持压缩数据算法的 Microsoft Windows 版本中以存档文件格式保存的文件，例如 [LZX](/zh/compression/lzx/)、Quantum 和 [ZIP](/zh/compression/zip/ ）。当用户或开发人员想要包含和共享软件安装数据和文件时，该文件非常有用。这些文件中包含的无损数据压缩和数字认证功能使该文件非常适合存储和共享此类文件。它支持不同的 Microsoft 安装程序，例如 Device Installer、SetUp API 和 AdvPak。

## 历史简介 ＃＃

CAB 文件是微软开发的一种数据压缩文件类型。它最初被称为“钻石"，但后来它被普遍称为 CAB 文件，是“内阁"一词的缩写

## 技术规格##

一个 CAB 文件通常最多可以包含 65535 个文件夹，而每个文件夹最多可以包含 65536 个文件。 CAB 文件存储机制节省时间和空间，因为它将每个文件夹保存为压缩块，而不是单独压缩和存储每个文件。空文件夹不能存储在 CAB 归档文件夹中。 CAB 文件最初由 Microsoft 开发，用于各种安装程序，例如格式略有不同的 InstallShield。 CAB 文件通常连接到自解压程序。 Microsoft CAB 文件易于识别，因为它们具有有助于识别格式的独特标记。所有 Microsoft CAB 文件的唯一标记是一个四字前缀 MSCF。看到此代码，用户可以轻松地将 Microsoft CAB 文件与其他文件区分开来，并在压缩器或版本中相应地使用它。可以使用更多软件安装数据压缩文件，或者可以使用正确的软件解压缩当前数据。


## 驾驶室示例##

以下示例说明了 CAB 文件结构中文件和文件夹之间的关系：

{{< figure src="../cab.png" alt="CAB 文件格式" >}}

## 参考 ＃＃

* [CAB - WIKIPEDIA](https://en.wikipedia.org/wiki/Cabinet_(file_format))
