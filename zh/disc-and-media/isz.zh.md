{
  "date" : "2023-01-25",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" :"了解 ISZ 文件格式以及可以创建和打开 ISZ 文件的 API。",
  "title" :"ISZ 文件格式 - 压缩 ISO 磁盘映像",
  "linktitle" : "ISZ",
  "menu" : {
    "docs" : {
      "identifier":"disc-and-media-isz",
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2023-01-25"
}

## 什么是 .isz 文件？

ISZ 是一种用于存储磁盘映像的文件格式，类似于 ISO 或 NRG。 ISZ 格式是 ISO 格式的压缩版本，它可以减小图像的文件大小，同时仍保留原始图像的确切内容。 ISZ 文件可用于创建 CD、DVD 或其他光学介质的备份，或存储和分发软件和其他类型的数据。

可以使用 UltraISO、Alcohol 120% 或 ISOBuster 等程序打开 ISZ 文件并将其安装为虚拟驱动器。这些程序允许用户访问 ISZ 文件的内容，就像它们位于物理磁盘上一样。 ISZ文件中的文件也可以直接解压使用。

值得注意的是，ISZ 并不是一种广泛使用的格式，并且并非所有工具都可以打开它。此外，根据您尝试打开的图像类型，还有其他更流行的图像格式，例如 ISO、BIN/CUE 和 NRG，它们得到了更广泛的支持。

## ISZ 和 ISO 的区别

ISZ 和 ISO 都是用于存储和分发数字媒体的文件格式。

ISO 文件是一种映像文件，包含 CD、DVD 或其他光盘上数据的完整副本。它通常用于分发软件和游戏，以及创建光学介质的备份。 ISO 文件可以像物理光盘一样打开和使用，并且可以刻录到 CD 或 DVD。

另一方面，ISZ 文件是一种类似于 ISO 文件的压缩图像文件，但使用称为“zisofs”的不同压缩方法。此方法旨在压缩光盘上的数据，使生成的 ISZ 文件小于等效的 ISO 文件。 ISZ文件也可以像物理光盘一样使用，但需要先解压缩才能使用。

所以ISZ文件是ISO的压缩版本，但不能直接使用，需要解压后再使用。

## 如何打开 ISZ 文件？

要打开 ISZ 文件，您需要一个能够解压缩该文件并将其安装为虚拟光盘的程序。

其中一个程序是 UltraISO，它是一款专门为处理 ISO 和 ISZ 文件而设计的商业软件。它允许您打开、编辑和提取 ISZ 文件的内容。它还可以将 ISZ 文件转换为 ISO 或其他光盘映像格式。

另一个可以打开 ISZ 文件的程序是 MagicISO。这也是一个商业软件，它还允许您打开、编辑和提取 ISZ 文件的内容，并将其转换为其他光盘映像格式。

还有一些免费的替代品，例如 Daemon Tools Lite、Gizmo Drive 和 Virtual CloneDrive。这些程序允许您将 ISZ 文件安装为虚拟光盘，从而使您可以像访问物理光盘一样访问其内容。

您还可以使用命令行工具“zisofs-tools”将 ISZ 文件解压缩为 ISO。

## 参考
* [UltraISO](https://www.ultraiso.com/)

