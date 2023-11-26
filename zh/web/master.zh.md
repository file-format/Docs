{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"主文件 - ASP.NET 母版页文件格式",
  "description" :"了解 MASTER 文件格式和 API 以创建和打开 MASTER 文件。",
  "linktitle" : "MASTER",
  "menu" : {
    "docs" : {
      "identifier":"web-master",
      "parent" : "web"
}
},
  "lastmod" : "2021-02-29"
}

## 什么是主文件？

MASTER 文件是使用 ASP.NET 创建的主网页模板文件。它用作创建与 MASTER 文件具有相同布局和设置的多个页面的起点。模板 MASTER 文件包括页眉、导航菜单、页脚、字体和样式信息的设置。使用主文件有助于快速创建多个网页。

您可以使用 Microsoft Visual Studio 2022 及更高版本打开 MASTER 文件。

## MASTER 文件格式 - 更多信息

MASTER 文件以 HTML 文件格式创建和保存，与任何其他网页文件类似。它分为可编辑部分和不可编辑部分。可编辑部分是可以修改以满足用户要求的部分。在 Microsoft Visual Studio 中打开 MASTER 文件时，不可编辑的部分将显示为灰色。

母版页由两部分组成，即母版页本身和一个或多个内容页。

### 母版页

母版页具有 .master 扩展名，并使用 ASP.NET 制作。它有一个预定义的布局，由静态文本、HTML 标签和服务器端控件组成。在普通的 .aspx 页面中，使用 @ Page 指令。对于 .master 文件，它被 @ Master 指令替换。

### 内容页面

内容页表示母版页占位符控件的内容。这些 .aspx 页面实际上是母版页的代码隐藏部分。内容页使用 @ Page 指令进行绑定，方法是包含指向要使用的母版页的 MasterPageFile 属性，如下所示。

```
<%@ Page Language="VB" MasterPageFile="~/MasterPages/Master2.master" Title="Content Page of Master File" %>
```

## 参考

* [ASP.NET 母版页概述](https://learn.microsoft.com/en-us/previous-versions/aspnet/wtxbf3hh(v=vs.100))

