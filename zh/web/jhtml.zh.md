{
  "date" : "2019-10-11",
  "keywords" :["jhtml","jhtml文件","jhtml文件格式","jhtml文件类型","文件","类型","什么是jhtml文件"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JHTML - Java HTML 文件",
  "description":"了解 JHTML 文件格式和可以创建和打开 JHTML 文件的 API。",
  "linktitle" : "JHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-09"
}

## 什么是 .jhtml 文件？

带有 .jhtml 扩展名的文件是带有 [Java](/zh/programming/java/) 代码的 [HTML](/zh/web/html/) 文件，当客户端在浏览器中请求此页面时，它会在服务器上执行。服务器处理请求，执行函数中包含的 Java 函数，并将页面返回给客户端的浏览器。嵌入在 JHTML 页面中的 Java 对象在服务器上运行以处理对此类页面的请求。 JHTML 文件还可以使用 JDBC（Java [数据库](/zh/database/) 连接）连接从数据库中访问信息。 JHTML 文件可以在任何文本编辑器中打开并在 Web 浏览器（例如 Google Chrome、Firefox 和 Safari）中查看。

## JHTML 文件格式

JHTML 是 ATG 的专有技术，可以使用 ATG（Art Technology Group）Dynamo 文档编辑器创建。 JHTML 文件是使用标准 HTML 和 Java 代码以纯文本文件格式编写的。除了引用 Java 对象的专有标签外，这些标签还包含标准 HTML 标签。当用户请求这样的页面时，HTTP 服务器将请求转发到 Java 应用程序服务器。 JHTML 页面首先被转换为 .java 文件并被编译以生成作为 servlet 执行的 [.class](/zh/programming/class/) 文件。这会生成标准 HTTP 和 HTML 数据流，这些数据流会返回给请求浏览器以显示给用户。这有助于在服务器上运行数据库相关查询并将最终的累积结果返回到客户端的浏览器。

## 参考

* [HTML文档的全局结构](https://www.w3.org/TR/html401/struct/global.html#h-7.5.4)

