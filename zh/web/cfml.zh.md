{
  "date" : "2021-08-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CFML - ColdFusion 标记语言文件",
  "description" :"了解什么是 CFML 文件以及可以创建和打开 CFML 文件的 API。",
  "linktitle" : "CFML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-08-19"
}

## 什么是一 .cfml 文件？

扩展名为 .cfml 的文件是用于创建网页的 ColdFusion 标记语言文件。它指的是一组规则，用于定义程序员将如何开发 ColdFusion 应用程序。 ColdFusion 是一种编程语言，用于快速创建服务器端 Web 应用程序，并且使用的技术少于 [ASP](/zh/web/asp/)、[PHP](/zh/programming/php/) 等其他技术。一些可以打开 CML 文件的应用程序包括 Adobe ColdFusion 2018、Adobe ColdFusion Builder 和 Adobe Dreamweaver。

## CFML 文件格式 - 更多信息

CFML 文件是标记文件，包含标签形式的 Web 元素。这些是可以在任何文本编辑器中打开和编辑的文本文件。 CFML 文件由几个类似于 [HTML](/zh/web/html/) 的标签组成，通常由一个开始和一个结束标签组成。这些标签还可以包含一个或多个属性。

### 标签语法

以下是 CFML 标签的通用语法。

```
<tagname>
  Code/text that is affected by the surrounding tags.
</tagname>
```

大多数标签接受属性并定义如下。

```
<tagname attribute="value">
  Code/text that is affected by the surrounding tags.
</tagname>
```

其中一些标签还接受具有以下语法的多个属性。

```
<tagname attribute1="value" attribute2="value">
  Code/text that is affected by the surrounding tags.
</tagname>
```

## CFML 代码示例

这是一个使用实际 CFML 标签的示例 - `cfoutput` 标签：

```
<cfoutput>
  #firstname#
</cfoutput>
```

## 参考

* [ColdFusion](https://www.quackit.com/coldfusion/tutorial/)

