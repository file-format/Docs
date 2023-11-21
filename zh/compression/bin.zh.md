{
"日期":"2023-07-20",
   "keywords":[
"垃圾桶",
"BIN 文件",
"文件",
"BIN 文件扩展名",
"扩大",
"文件"
],
   "author":{
"display_name":"沙基尔·法伊兹"
},
"draft": "false",
"toc": true,
"title":"BIN 文件格式 - MacBinary 编码文件",
   "description":"了解 BIN 格式以及可以创建和打开 BIN 文件的 API。",
"linktitle":"BIN",
   "menu":{
      "docs":{
         "identifier":"compression-bin",
"parent": "compression"
}
},
"lastmod": "2023-07-20"
}

## 什么是 .bin 文件？

在 Macintosh 计算机的上下文中，BIN 文件可以指以 MacBinary 格式保存的文件。 MacBinary 是一种文件格式，专门用于通过互联网、电子邮件、FTP 或便携式媒体传输 Macintosh 文件。 MacBinary 的目的是在单个文件中保留 Macintosh 文件的完整文件结构和属性，包括数据分支和资源分支。

MacBinary 格式通过将 Macintosh 分层文件系统 (HFS) 资源分支和数据分支封装到压缩文件中来实现此目的。它还包括一个查找器标头，其中包含有关文件的重要元数据。通过将所有这些组件合并到一个文件中，MacBinary 可确保该文件保持其完整性，并且可以轻松地在不同平台上传输和共享。

随着 Apple 文件系统和文件传输协议的进步，BIN 文件和 MacBinary 格式的使用已变得不那么常见。 ZIP 等文件格式的引入以及向 HFS+ 和 APFS 等更现代的文件系统的过渡减少了对 MacBinary 编码文件的需求。这些较新的文件系统提供了更有效的方法来处理文件属性、资源分叉和数据分叉，使得 MacBinary 格式在当今的计算环境中不再必要。

## BIN 文件格式 - 更多信息

在麦金塔计算机的早期，由于数据限制，文件被存储在两个单独的“叉子”中。 “资源叉”包含结构化数据，而“数据叉”包含非结构化数据。虽然经典 Mac 操作系统将这些分叉视为单个文件，但将文件传输到非 Mac 系统会导致数据丢失，因为它们无法将这些分叉识别为单个实体。为了解决这个问题，MacBinary 格式是由 Dennis Brothers、Harry Chesley 和 Yves Lempereur 等人创建的。 MacBinary 将这些分支压缩并组合成一个文件（称为 BIN 文件），以便传输到非 Mac 系统。返回 Mac 操作系统后，叉子将再次分离。随着 2000 年代基于分叉的 HFS 的转变，MacBinary 格式的使用显着下降。如今，很少会遇到 MacBinary 编码的 BIN 文件，除非您在非 Mac 系统上遇到旧文件或从 Internet 下载一个文件。

随着时间的推移，MacBinary 格式经历了多个版本，以适应 Macintosh 系统和文件处理的变化。以下是 MacBinary 格式的一些不同版本：

- **MacBinary I：** MacBinary 的初始版本，于 20 世纪 80 年代末推出。它将资源分支和数据分支合并到一个二进制文件中，从而允许 Macintosh 文件的跨平台传输。

- **MacBinary II：** 该版本于 20 世纪 90 年代初发布，通过向二进制文件的标头添加附加信息（例如文件类型和创建者代码）来改进原始 MacBinary 格式。这些代码有助于在传输过程中保持 Macintosh 文件的完整性和可识别性。

- **MacBinary III：** MacBinary III 格式于 20 世纪 90 年代中期推出，通过在二进制文件的标头中包含额外的元数据（例如文件名以及文件创建和修改日期），进一步增强了以前的版本。这样可以在传输过程中更全面地保留 Macintosh 文件属性。

- **MacBinary IV：** MacBinary IV 的开发是为了解决 2000 年代初新兴的 Mac OS X 操作系统的兼容性问题。它进行了更改以适应 Mac OS X 中引入的新文件系统结构和属性。

## 如何打开 .bin 文件？

MacBinary 编码的 BIN 文件可以使用各种压缩实用程序打开。对于 macOS 用户，**Apple Archive Utility** 是一个合适的选项。 Windows 用户可以利用 **Smith Micro StuffIt Deluxe** 等软件来提取 MacBinary 编码的 BIN 文件的内容。 macOS 用户的另一个选择是**The Unarchiver**，它是一款多功能工具，能够处理多种文件格式，包括 MacBinary。

需要注意的是，.bin 文件扩展名适用于多种文件格式，而不仅仅是 MacBinary。因此，如果您遇到无法使用上述实用程序打开的 BIN 文件，它可能会以不同的格式保存。在这种情况下，您可能需要识别特定的文件格式并使用专为该格式设计的适当软件或实用程序来访问文件内容。

## 其他BIN文件

以下是使用 **.bin** 文件扩展名的其他文件类型。

- [BIN - 二进制光盘映像文件](/zh/disc-and-media/bin/)
- [BIN - Unix 可执行文件](/zh/executable/bin/)
- [BIN - BlackBerry IT 策略文件](/zh/settings/bin/)
- [BIN - 世嘉创世游戏 ROM](/zh/game/bin/)
- [BIN - PSX PlayStation BIOS 映像](/zh/game/bin-pcsx/)

## 参考

* [MacBinary](https://en.wikipedia.org/wiki/MacBinary)

