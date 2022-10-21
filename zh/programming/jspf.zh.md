{
  "date" : "2021-04-20",
  "keywords": [ "JSPF file", "jspf", "JSPF example", "extension", "format", "jspf tutorial", "jsp fragment", "JSPF file format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JSPF - JSP 片段文件格式",
  "description":"了解 JSPF 文件格式和可以创建和打开 JSPF 文件的 API。",
  "linktitle" : "JSPF",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-21"
}

## 什么是一 .jsf 文件？
扩展名为.jspf 的文件称为JSP 片段；包含在另一个 JSP 文件中的静态文件。 JSPF 文件不是单独编译的，但是，它们是与它们包含的页面一起编译的。它的语法类似于 Java Server Pages (JSP) 代码。它只包含 JSP 的一个片段；没有包含整个 JSP 文档。

## JSPF 文件格式
代替使用术语“JSP 段"，因为术语“JSP 片段"在 JSP 2.0 规范中被重载。 JSP 片段可以使用 .jsp 或 .jspf 扩展名，并且应该放置在 **/WEB-INF/jspf** 中或与其余静态文件一起放置。非完整页面的JSP片段必须使用.jspf扩展名，必须放在**/WEB-INF/jspf**

### JSP 或 JSP 片段文件组织
JSP 文件按列出的顺序包含以下部分：

1. 开场评论
2. JSP 页面指令
3. 可选标签库指令
4. 可选的 JSP 声明
5. HTML和JSP代码

JSP 或 JSPF 文件都以称为 **Opening Comment** 的服务器端样式注释开头：

```
<%-- 
  - Author(s):
  - Date:
  - Copyright Notice:
  - @(#)
  - Description: 
  --%>
```
此注释只能在服务器端可见，因为它在 JSP 页面呈现期间被删除。

## 何时使用 JSP 片段文件？
当一个 JSP 页面需要一个特定但复杂的结构，该结构也可以在其他 JSP 页面中重用时，处理这种情况的一种方法是使用复合视图模式（Java 蓝图的模式部分）将其分解为多个部分。例如，JSP 页面有时在其表示结构中具有以下逻辑布局：

{{< figure src="../jspf.png" alt="JSPF 文件格式" >}}

在这种情况下，这个复合 JSP 页面可以转换成各种模块，每个模块都称为一个单独的 JSP 片段。然后可以将 JSP 片段放置在复合 JSP 页面中的适当位置。因此，当使用静态包含指令来包含不会被自身调用的页面时，使用 JSPF 文件，扩展名为 .jspf 的文件应放在 Web 应用程序存档的 /WEB-INF/jspf/ 目录中（战争）。

## JSPF 示例
```
<%@ include file="/WEB-INF/jspf/header.jspf" %>
...
<%@ include file="/WEB-INF/jspf/menuBar.jspf" %>
...
<jsp:include page="<%= currentBody %>" />
...
<%@ include file="/WEB-INF/jspf/footnote.jspf" %>
...
<%@ include file="/WEB-INF/jspf/footer.jspf" %>
...
```

## 参考

* [JavaServer 页面的代码约定](https://www.oracle.com/technical-resources/articles/javase/code-convention.html)

