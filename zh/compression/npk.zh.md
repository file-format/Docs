{
  "date" : "2022-06-21",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"NPK 文件格式",
  "description":"了解 NPK 文件格式和可以创建和打开 NPK 文件的 API。",
  "linktitle" : "NPK",
  "menu" : {
    "docs" : {
      "identifier":"compression-npk",
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-21"
}

## 什么是一 .npk 文件？

NPK文件是**MikroTik**路由器用于升级路由器操作系统的软件升级包文件。它以压缩二进制存档的形式出现，加载到路由器中以安装软件更新。 NPK 文件中包含的信息包括网络信息，例如 IP 地址和 IP 服务、连接器信息（以太网接口和串行端口）、电子邮件设置、网桥配置和本地用户管理。

## 氮磷钾文件格式

NPK 文件存储为压缩的二进制存档。它是一种封闭的文件格式，仅供 MikroTik 自己使用。它不打算通过第 3 方创建 RouterOS 附加组件。 NPK 文件由 MikroTik 自己维护，可以从 [MikroTik](https://mikrotik.com/download) 网站的下载部分下载相同的升级版本。

当 NPK 文件上传到路由器时，路由器操作系统不会生效，除非重新启动。因此，需要重新启动才能升级路由器操作系统。

## 参考

* [MikroTik - 升级路由器操作系统](https://mikrotik.com/download)
* [如何创建 NPK 文件](https://forum.mikrotik.com/viewtopic.php?t=87126)

