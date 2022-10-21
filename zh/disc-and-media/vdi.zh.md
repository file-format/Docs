{
  "date" : "2021-08-11",
  "keywords" :["vdi 文件","vdi 文件格式","什么是 vdi 文件","文件","vdi 示例","vdi 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"了解 VDI 文件格式和可以创建和打开 VDI 文件的 API。",
  "title" :"VDI - VirtualBox 虚拟磁盘映像文件",
  "linktitle" : "VDI",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-11"
}

## 什么是一 .vdi 文件？
带有 .vdi 扩展名的文件是虚拟磁盘映像；特定于 Oracle 的开源桌面虚拟化程序 VirtualBox。 VDI 文件用于启动 VirtualBox 虚拟机。 VM 允许用户在单台计算机上运行其他操作系统或程序。因此，VDI 文件的好处是用户可以将这些磁盘映像文件保存在他们的硬盘上，并且可以在需要时使用模拟器运行这些文件。

## VDI 文件格式
虚拟磁盘映像 (VDI) 是积极开发的开源 Oracle VM（称为 VirtualBox）的主要磁盘文件格式，VirtualBox 是一种企业级虚拟化产品。 VDI 文件格式旨在制作可使用其他虚拟化程序轻松运行的便携式光盘映像。它支持动态分配和固定大小的存储。它允许您在创建图像文件后展开它，即使它已经包含数据。

### 磁盘虚拟化
系统以 VDI 磁盘映像格式模拟硬盘。 VirtualBox VM 可以使用在 Microsoft Virtual PC 或 VMware 中创建的早期磁盘，以及它自己的本机格式。 VirtualBox 还能够连接到 iSCSI 目标和主机上的原始分区，将两者用作虚拟硬盘。 VirtualBox 模拟 IDE（PIIX4 和 ICH6 控制器）、SATA（ICH8M 控制器）、可连接硬盘的 SAS 控制器和 SCSI。

自 VirtualBox 2.2.0 版起，该支持可用于开放虚拟化格式 (OVF)。主机连接的物理设备和 ISO 映像都可以安装为 CD 或 DVD 驱动器。
默认情况下，VirtualBox 通过兼容 VESA 的自定义虚拟显卡支持图形。

### 对以太网的虚拟化支持
VirtualBox 为以太网网络适配器虚拟化以下网络接口卡：
- AMD PCnet PCI II (Am79C970A)
- AMD PCnet-Fast III (Am79C973)
- 英特尔 Pro/1000 MT 台式机 (82540EM)
- 英特尔 Pro/1000 MT 服务器 (82545EM)
- 英特尔 Pro/1000 T 服务器 (82543GC)
- 半虚拟化网络适配器（virtio-net）

模拟网卡使客户操作系统无需搜索和安装网络硬件驱动程序即可运行，因为它们作为客户操作系统的一部分提供。特殊的半虚拟化网络适配器通过减少匹配特定硬件接口的需要来提高网络性能。因此，它需要客户机中的特殊驱动程序支持。


## 参考

* [VirtualBox - 维基百科提供](https://en.wikipedia.org/wiki/VirtualBox#VirtualBox_Disk_Image)


