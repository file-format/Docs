{
  "date" : "2019-10-11",
  "keywords" :["asax","asax 文件","asax 文件格式","asax 文件类型","文件","类型","什么是 asax 文件"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASAX - ASP.NET 服务器应用程序文件",
  "description" :"了解什么是 ASAX 文件以及可以创建和打开 ASAX 文件的 API。",
  "linktitle" : "ASAX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-07"
}

## 什么是一 .asax 文件？

扩展名为 .asax 的文件是驻留在服务器端的 ASP.NET 应用程序使用的文件。它包含响应由 ASP.NET 或 HTTP 模块引发的应用程序级和会话级事件的代码。这还包括在应用程序启动或关闭时处理某些事件。 ASAX 文件是可选的，只有一个单独的 ASAX 文件被添加到 Web 应用程序中来处理全局级别的应用程序级事件和错误。与 ASPX 页面不同，ASAX 文件不包含任何代码来实现应用程序的功能。

## ASAX 文件格式

ASAX 文件以纯文本文件格式编写，并且是人类可读的。最常用的 ASAX 文件是 Global.asax，它位于 ASP.NET 应用程序的根目录中。 Web 服务器被配置为拒绝对该文件的任何传入呼叫，以禁止用户下载或查看该文件的代码。

### Global.ASAX - ASAX 文件格式示例

单个 ASAX 文件由多个部分组成，这些部分用于处理应用程序级事件。这些如下。

* **应用程序指令** - 应用程序指令是用于定义可选的特定于应用程序的设置的标记，供 ASP.NET 解析器在处理 Global.asax 文件时使用。这些指令位于 Global.asax 文件的开头，定义如下。

```
<%@指令属性=值[属性=值…]%>
```
* **代码声明块** - 代码声明块用于定义嵌入在 \ 中的 ASP.NET 应用程序文件中的服务器代码部分<script> blocks marked with a runat="server" attribute. The following example shows how you can define event-handling logic for the EnterBtn_Click event.

```
<html>
  <script language="C#" runat="server">
      void EnterBtn_Click(Object Src, EventArgs E) {
          Message.Text = "Hi " + Name.Text + ", welcome to ASP.NET!";
  }
  </script>

  <body>
   <form runat="server">
    Enter your name: <asp:textbox id="Name" runat=server/>
                     <asp:button text="Enter" Onclick="EnterBtn_Click" runat="server"/>
        <p>
        <asp:label id="Message" runat=server/>
    </form>
  </body>
</html>
```
* **代码渲染块** - 这些定义了在渲染页面时执行的内联代码或表达式。两种样式的代码渲染块包括内联代码和内联表达式。前者用于定义独立的行或代码块，而横向则用作调用 Write 方法的快捷方式。

## 参考

* [HTTP 处理程序和 HTTP 模块概述](https://msdn.microsoft.com/en-us/library/bb398986(v=vs.100))
* [Global.asax 语法](https://learn.microsoft.com/en-us/previous-versions/dotnet/netframework-4.0/2027ewzw(v=vs.100))

