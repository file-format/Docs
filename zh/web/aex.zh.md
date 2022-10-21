{
  "date" : "2019-10-11",
  "keywords" :["aex","aex 文件","文件格式","文件类型","什么是 aex 文件"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"AEX - Alpha 五编译全局函数文件",
  "description" :"了解什么是 AEX 文件以及可以创建和打开 AEX 文件的 API。",
  "linktitle" : "AEX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-12-07"
}

## 什么是一 .aex 文件？

AEX 文件（扩展名为 .aex）是编译后的 [Xbasic](https://documentation.alphasoftware.com/documentation/pages/Ref/Xbasic/index.xml) 文件，其中包含用于全局函数的编译程序代码。通过从服务器端 [.a5w](/zh/web/a5w/) 页面调用它们，可以在 Web 应用程序中使用它。通过分别从 A5W 文件调用 a5w_load_aex 和 a5w_unload_aex 函数来加载和卸载 AEX 文件。然而，在新的实现中，这些文件通过包含在 a5_application.5i 文件中被加载到内存中。 Alpha Anywhere 软件使用 Xbasic 编程语言来开发移动和 Web 应用程序。

## AEX 文件格式 - 更多信息

AEX 文件以二进制文件格式保存到磁盘，并包含用 Xbasic 编写的函数的编译代码。 Xbasic 脚本命令语句确定执行的结构和流程，包括执行或停止重复操作，或根据条件在两个或多个步骤之间做出选择。 [Xbasic 语言参考](https://documentation.alphasoftware.com/documentation/pages/Ref/Xbasic/index.xml) 可以参考它的详细信息。

## 参考

* [阿尔法五](https://www.alphasoftware.com/)
* [Alpha 5 文档](https://documentation.alphasoftware.com/documentation/pages/index.html)
* [Xbasic 指南](https://documentation.alphasoftware.com/pages/Guides/Xbasic/index.xml)

