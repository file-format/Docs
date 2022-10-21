



{
  "date" : "2021-08-11",
  "keywords" :["wim 文件","wim 文件格式","什么是 wim 文件","文件","wim 示例","wim 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"了解 WIM 文件格式和可创建和打开 WIM 文件的 API。",
  "title" :"WIM - Windows 映像格式文件",
  "linktitle" : "WIM",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-11"
}

## 什么是一 .wim 文件？
带有 .wim 扩展名的文件首次出现在 Windows Vista 中。 WIM 属于基于文件的映像格式，通常在 Microsoft Windows Vista 中引入。它使单个磁盘映像能够部署到各种计算机平台。 WIM 文件用于管理更新、驱动程序和组件等文件，而无需重新启动操作系统映像。 AQ WIM 文件包含一组文件和相关的元数据，与其他磁盘文件格式非常相似。

## WIM 文件格式
WIM 文件格式不像 VHD 或 IS 等基于扇区的格式，实际上它是基于文件的，这意味着 WIM 中信息的基本单位是文件。基于文件的基本好处是文件系统树中多次引用的文件的单实例存储和硬件独立性。它减少了单独打开和关闭各种文件的开销，因为文件存储在单个 WIM 中文件。 WIM 文件可以存储多个磁盘映像，这些映像通过其唯一名称或数字索引来引用。
### 支持压缩算法
WIM 在降速和升速方面支持以下压缩算法系列：
- 快报
- LZX
- LZMS
- 固体压缩。
前三个系列基于 LZ77，而 Solid-compression 与 LZMS 一起在 WIMGAPI Windows 8 和 DISM Windows 8.1 中引入。
### WIM 文件格式工具
以下工具通常支持 WIM 文件格式：

- **ImageX**：用于编辑、创建和部署 Windows 映像格式的 Windows 磁盘映像的命令行工具。它与相关的 WIMGAPI 一起作为免费的 Windows 自动安装工具包的一部分分发。从 Windows Vista 开始，Windows 安装程序使用 WAIK API 来安装 Windows。
- **DISM**：Windows 7 和 Windows Server 2008 R2 中引入的一种工具，可以在 Windows 安装映像上执行服务相关任务，无论是文件夹或 WIM 文件中的联机映像或脱机映像。该工具能够挂载和卸载映像，将设备驱动程序添加到脱机映像，并在脱机映像中查询已安装的设备驱动程序。
 




## 参考


* [Windows 图像格式 - 维基百科提供](https://en.wikipedia.org/wiki/Windows_Imaging_Format)


