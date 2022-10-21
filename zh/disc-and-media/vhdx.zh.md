{
  "date" : "2022-07-22",
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
   "toc" : true,
  "description" :"了解可创建和打开 VHDX 文件的 VHDX 文件格式和 API。",
  "title" :"VHDX 文件格式 - 什么是 VHDX 文件？",
  "linktitle" : "VHDX",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2022-07-22"
}

## 什么是一 .vhdx 文件？

VHDX 文件是虚拟硬盘 v2 文件格式的磁盘映像文件。它包含一个完整的操作系统，可以作为任何普通机器加载和使用，用于测试软件或运行需要特定操作系统的软件。尽管 VHDX 是一个完整的磁盘映像，但它存储在单个文件中。 Parallels Desktop、Windows Virtual Machine 和 Virtual Box 等虚拟机软件可以加载和打开磁盘映像。

VHDX 文件可以使用 Hyper-V 管理器转换为 [VHD](/zh/disc-and-media/vhd/)，或使用 VirtualBox 转换为 [VDI](/zh/disc-and-media/vdi/)。

## VHDX 文件格式 - 更多信息

VHDX 文件格式详细信息已完整记录并作为 [VHDX 文件格式规范]（https://docs.microsoft.com/en-us/openspecs/windows_protocols/ms-vhdx/83e061f8-f6e2-4de1-91bd-5d518a43d477）在线提供) 在 Microsoft 文档中。它是 VHD 格式的扩展，包括增强的功能。 VHDX 文件格式提供了在虚拟硬盘和虚拟硬盘文件层可用的附加功能。它更加优化，并为存储硬件配置和功能提供了更好的结果。可以打开 VHDX 文件

### 支持 VHDX 中的虚拟硬盘

它支持三种类型的虚拟硬盘。

1. **固定虚拟硬盘** - 分配了固定数据大小的虚拟硬盘。虚拟硬盘的大小不会随着数据的添加或删除而改变。

1. **动态虚拟硬盘** - 具有动态磁盘大小的虚拟硬盘。它的大小在任何时候都与写入它的实际数据和元数据一样大。它的文件大小随着数据的添加或删除而动态增加。

1. **区分虚拟硬盘** - 将当前虚拟硬盘表示为一组修改后的块，与父虚拟硬盘文件相比。

## 参考

* [VHDX 文件格式规范](https://docs.microsoft.com/en-us/openspecs/windows_protocols/ms-vhdx/83e061f8-f6e2-4de1-91bd-5d518a43d477)
* [VHD - 维基百科](https://en.wikipedia.org/wiki/VHD_(file_format))

