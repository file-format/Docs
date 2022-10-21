{
  "date" : "2021-08-10",
  "keywords" :[ ".ovf 文件", "文件格式", "什么是 .ovf 文件", "文件", "文件扩展名"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
   "toc" : true,
  "description" :"了解什么是 .ovf 文件格式以及可以创建和打开 OVF 文件的 API。",
  "title" :"OVF 文件格式 - 打开虚拟化文件",
  "linktitle" : "OVF",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2022-01-03"
}

## 什么是一 .ovf 文件？

OVF 文件是一个文本文件，其中包含有关在虚拟机上运行的软件的打包和分发信息。它按照 [Open Virtualization Standard Specifications](https://www.dmtf.org/standards/ovf) 进行格式化，描述了在虚拟机上运行应用程序的所有要求（例如安全性、可移植性、效率和可扩展性）。国际标准化组织 (ISO) 已采用 OVF 作为 ISO 17203 标准。

## OVF 文件格式简史

OVF 文件格式由创建开放管理标准的 DMTF（分布式管理任务组）引入。它独立于任何特定的管理程序或指令集架构。 OVF 包包含一个或多个虚拟系统，每个虚拟系统都可以部署到虚拟机上。

## OVF 文件格式 - 更多信息

OVF 包由放置在单个目录中的多个文件组成。其中，仅包含一个 OVF 描述符（扩展名为 .ovf）文件，该文件以 [XML](/zh/web/xml/) 文件格式存储。它描述了 OVF 包的打包虚拟机信息和元数据信息，例如：

* 姓名
* 硬件要求
* 对 OVF 包中其他文件的引用，以及
*人类可读的描述

可以在 OVF 包中找到的其他文件包括一个或多个磁盘映像以及可选的证书文件和其他辅助文件。

## 参考

* [开放虚拟化格式 - DMTF](https://www.dmtf.org/standards/ovf)
* [OVF 文件格式规范](https://www.dmtf.org/sites/default/files/standards/documents/DSP0243_1.1.0.pdf)

