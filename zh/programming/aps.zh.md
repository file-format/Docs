{
  "date" : "2021-04-22",
  "keywords": [ "aps file", "visual studio aps file", "extension", "format","aps file visual studio","aps file extension","how to open aps file","APS file format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"APS - Visual C++ 资源文件",
  "description":"通过 APS 示例和可以创建和打开 APS 文件的 API 了解 APS 文件格式。",
  "linktitle" : "APS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-22"
}

## 什么是 APS 文件格式？
APS 文件由 Microsoft 的软件开发应用程序 Visual C++ 创建。它保存与项目合并的资源的二进制表示，并允许应用程序更快地加载资源。您可以轻松找到这些带有 .aps 文件扩展名的文件。事实上，资源编辑器并不直接读取 resource.h 文件，这就是资源编译器将它们编译为资源编辑器使用的 .aps 文件的原因。

## APS 文件格式
APS 文件格式只是一个编译步骤，只存储符号数据。在编译过程中会丢弃注释等非符号信息。例如，当您保存时，资源编辑器会覆盖资源脚本文件和 resource.h 文件。对资源本身的任何更改都保留在资源脚本文件中，但是一旦资源脚本文件被覆盖，注释将始终丢失。


## 参考

* [资源文件 (C++)](https://learn.microsoft.com/en-us/cpp/windows/resource-files-visual-studio?view=msvc-160)
 


