{
  "date" : "2019-10-11",
  "keywords" :["aspx","aspx 文件","aspx 文件格式","aspx 文件类型","文件","类型","什么是 aspx 文件"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASPX 文件格式",
  "description" :"您的文件格式指南,了解什么是 ASPX 文件以及可以创建和打开 ASPX 文件的 API。",
  "linktitle" : "ASPX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2020-09-10"
}

## 什么是一 .aspx 文件？

扩展名为 .aspx 的文件是使用运行在 Web 服务器上的 Microsoft ASP.NET 框架生成的网页。 ASPX 代表 Active Server Pages Extended，当访问 URL 时，这些页面会显示在用户端的 Web 浏览器中。它是 [ASP](/zh/web/asp/) 技术的继承者，同样在服务器端生成，但不使用 .NET 框架。 ASP.NET 页面可能包含 [C#](/zh/programming/cs/) 或 [VB.NET](/zh/programming/vb/) 脚本，这些脚本由 Web 服务器转换为 HTML，以便在 Web 浏览器中呈现给用户。 ASPX 页面也称为 .NET Web 窗体。这些可以使用 Microsoft Visual Studio、Adobe Dreamweaver、Notepad++ 和任何文本编辑器等应用程序打开和创建。

## ASPX 文件格式

ASP.NET Web 表单基于用于与 Web 应用程序交互的事件驱动模型。作为最终用户的浏览器向服务器提交 Web 表单，服务器返回完整的标记页面或 HTML 页面作为响应。 ASP.NET 组件模型为 ASPX 页面提供对象模型。该模型描述：

* 几乎所有 HTML 元素或标签的服务器端对应物，例如 \<form>和 \<input> .
* 服务器控件，有助于开发复杂的用户界面。例如，日历控件或 Gridview 控件。

ASPX 文件使用 ASP.NET **代码隐藏模型** 来构建这些页面。

### 内嵌代码

内嵌在 ASPX 页面中并为用户实现提供所有功能的示例代码。以下 [C#](/zh/programming/cs/) 代码表示包含内嵌代码的示例 ASP.NET 页面：

```
<%@ Language=C# %>
<HTML>
    <script runat="server" language="C#">
        void MyButton_OnClick(Object sender, EventArgs e)
        {
            MyLabel.Text = MyTextbox.Text.ToString();
    }
    </script>
    <body>
        <form id="MyForm" runat="server">
            <asp:textbox id="MyTextbox" text="Hello World" runat="server"></asp:textbox>
            <asp:button id="MyButton" text="Echo Input" OnClick="MyButton_OnClick" runat="server"></asp:button>
            <asp:label id="MyLabel" runat="server"></asp:label>
        </form>
    </body>
</HTML>
```

### 代码隐藏

代码可以编写并存储在单独的类文件中，以便将 HTML 与表示逻辑完全分离。这使得表示层独立于可执行代码。以下是展示给用户的代码隐藏。

```
<%@ Language="C#" Inherits="MyStuff.MyClass" %>
<HTML>
    <body>
        <form id="MyForm" runat="server">
            <asp:textbox id="MyTextBox" text="Hello World" runat="server"></asp:textbox>
            <asp:button id="MyButton" text="Echo Input" Onclick="MyButton_Click" runat="server"></asp:button>
            <asp:label id="MyLabel" runat="server" />
        </form>
    </body>
</HTML>
```

表示层实际逻辑的 C# 实现如下。

```
using System;
using System.Web;
using System.Web.UI;
using System.Web.UI.WebControls;

namespace MyStuff
{
    public class MyClass : Page
    {
        protected System.Web.UI.WebControls.Label MyLabel;
        protected System.Web.UI.WebControls.Button MyButton;
        protected System.Web.UI.WebControls.TextBox MyTextBox;

        public void MyButton_Click(Object sender, EventArgs e)
        {
            MyLabel.Text = MyTextBox.Text.ToString();
    }
}
}
```

## 参考

* [ASP.NET WebApps - Microsoft](https://docs.microsoft.com/en-us/troubleshoot/webapps/welcome-webapps)

