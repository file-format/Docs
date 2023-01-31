{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HTX 文件 - HTML 扩展文件格式",
  "description" :"您的文件格式指南，了解什么是 HTX 文件以及可以创建和打开 HTX 文件的 API。",
  "linktitle" : "HTX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## 什么是一 .htx 文件？

HTX 文件实际上是一个 HTML 文件，其中包含用于将数据库查询结果显示为网页的数据变量。大多数使用 Microsoft FrontPage Web 开发软件创建，HTX 文件保存在与相应的 Internet 数据库连接器 (.IDC) 文件相同的文件夹中。

HTX 文件可以使用 Microsoft FrontPage 等应用程序和记事本、TextEdit 或 Atom 等任何文本编辑器打开。

## HTX 文件格式

HTX 文件保存为纯文本文件，其中包含用于从数据库中检索数据并保存在变量中以供显示的代码。


### HTX 文件示例

下面是一个 HTX 文件的例子，它定义了一个用于显示查询限制的页眉和用于显示给用户的页面上显示的文档。

```
<H4>
<%if CiMatchedRecordCount eq 0%>
No documents matched the query "<%EscapeHTMLCiRestriction%>".</H4>
<%else%>
<H4>Documents <%CiFirstRecordNumber%> to <%CiLastRecordNumber%> of
<%if CiMatchedRecordCount eq CiMaxRecordsInResultSet%>
the first
<%endif%>
<%CiMatchedRecordCount%> matching the query
"<%EscapeHTMLCiRestriction%>".
<%endif%>
</H4>
```

此示例代码的输出如下。

```
Documents 1 to 10 of the first 150 matching the query "cache".
```

可以看出，HTX 文件是一个模板，用于格式化结果返回和显示给最终用户的方式。它以 HTML 格式编写，带有一些 IIS 扩展和索引服务。这些扩展包括变量名称和其他用于处理结果的代码。

## 参考

* [在 .Htx 文件中格式化结果](https://learn.microsoft.com/en-us/previous-versions/windows/desktop/indexsrv/formatting-the-results--htx-file-)

