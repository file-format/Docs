{
  "date" : "2022-08-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CON 文件 - 概念应用程序源文件格式",
  "description" :"了解什么是 CON 文件以及可以创建和打开 CON 文件的 API。",
  "linktitle" : "CON",
  "menu" : {
    "docs" : {
"identifier":"web-con",
      "parent" : "web"
}
},
  "lastmod" : "2022-08-24"
}

## 什么是一 .con 文件？

CON 文件是为**Concept Application Server** 开发的应用程序的源代码文件。它用于编写应用程序以在服务器和用户之间交换数据。如果在用户端安装了概念客户端，则托管在服务器上的 CON 文件可以通过 Web 浏览器访问。概念应用服务器是一个具有小型编程语言的网络服务器，可能具有 [SQL](/zh/database/sql/) 子集数据库引擎 (TinDB)。

CON 文件可以使用 RadGs Concept Application Server 打开/运行。

## CON 文件格式 - 更多信息

CON 文件托管在服务器上，并使用用户计算机上的 Web 浏览器进行访问。概念 [URL](/zh/web/url/) 与普通 HTTP url 不同，它以 **concept://** 开头。

### CON 文件 URL 示例

托管在 Concept Application Server 上的 CON 文件可以通过 Web 浏览器使用以下 URL 访问：

```
concept://domain.server.com/web_application/main.con.
```
## 参考

* [概念应用服务器](https://github.com/Devronium/ConceptApplicationServer)

