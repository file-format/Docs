{
  "date" : "2021-08-13",
  "keywords" :["sdi 文件","sdi 文件格式","什么是 sdi 文件","文件","sdi 示例","sdi 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"了解 SDI 文件格式和可创建和打开 SDI 文件的 API。",
  "title" :"SDI - Windows 系统部署映像文件",
  "linktitle" : "SDI",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-13"
}

## 什么是一 .sdi 文件？
扩展名为 .sdi 的文件包含加载 blob、引导 blob 和部分 blob； Windows Embedded Studio 常用来创建用于加载和安装 Windows 的 RAM 磁盘或引导磁盘。 SDI 是系统部署映像的缩写。 Windows Embedded Studio 是用于为 Windows 创建磁盘映像的程序。实际上这个程序包含SDI文件管理程序和一个名为**sdimgr.exe**的命令行工具，两者都可以用来部署、创建和编辑SDI图像。

## SDI 文件格式
SDI 文件格式广泛用于启用使用虚拟磁盘来引导系统。某些版本的 Microsoft Windows 启用了 **RAM 引导**，这对于将 SDI 文件加载到内存中然后从中引导非常重要。 SDI 文件格式还可以使用 PXE（预引导执行环境）进行网络引导。它也被用于硬盘映像。
### SDI 文件部分
SDI 文件本身可以细分为以下部分：
- **Boot BLOB**：这包含实际的引导程序 STARTROM.COM。这类似于硬盘的引导扇区。
- **加载 BLOB**：这通常包含 NTLDR 并由引导 BLOB 启动。
- **Part BLOB**：这包含实际的启动运行时；还包括 boot.ini 和 ntdetect.com 文件，它们应该位于运行时的根目录中。
- **磁盘 BLOB**：这是以 MBR 开头的平面 HDD 映像。它用于硬盘驱动器映像而不是引导。此外，只有磁盘 BLOB 可以使用 Microsoft 的实用程序挂载。


## 参考

* [系统部署图像 - 维基百科提供](https://en.wikipedia.org/wiki/System_Deployment_Image)


