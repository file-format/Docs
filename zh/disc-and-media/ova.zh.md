{
  "date" : "2021-08-10",
  "keywords" :[".ova 文件","文件格式","什么是 .ova 文件","文件","文件扩展名"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
   "toc" : true,
  "description" :"了解什么是 .ova 文件格式以及可以创建和打开 ova 文件的 API。",
  "title" :"OVA 文件格式 - 打开虚拟设备文件",
  "linktitle" : "OVA",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2022-01-03"
}

## 什么是 .ova 文件？

OVA（开放式虚拟设备）文件是使用 .tar 归档格式保存为归档的 OVF 目录。它是一个虚拟设备包文件，其中包含用于分发在虚拟机上运行的软件的文件。一个 OVA 包包含一个 [.ovf](/zh/disc-and-media/ovf/) 描述符文件、证书文件、一个可选的 [.mf](/zh/programming/mf/) 文件以及其他相关文件。 OVA 文件的媒体类型为 application/ovf。

## OVA 文件格式

如前所述，OVA 文件是使用 OVF 目录以 TAR 文件格式创建的存档文件。文件本身保存为二进制文件。大多数虚拟化平台，例如 VMware、Microsoft、Oracle 和 Citrix，都可以从 OVF 文件安装虚拟设备，该文件是一个描述符文件，其中包含要在虚拟机中加载的映像的详细信息。

## OVA 文件的优点

* OVA 文件经过压缩，可加快下载速度。
* vSphere Client 在导入 OVA 文件之前对其进行验证，并确保它与预期的目标服务器兼容。如果设备与所选主机不兼容，则无法导入并显示错误消息。
* OVA 可以封装多层应用程序和多个虚拟机。

## 参考

* [OVA 文件格式和模板](https://docs.vmware.com/en/VMware-vSphere/7.0/com.vmware.vsphere.vm_admin.doc/GUID-AE61948B-C2EE-436E-BAFB-3C7209088552.html )
* [OVF 文件格式规范](https://products.conholdate.app/viewer/view/3XKCLQbwAw/open-virtualization-format-specification-dsp0243_1-1-0.pdf)

