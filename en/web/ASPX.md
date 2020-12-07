{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "true",
  "toc" : true,
  "description" : "Your file format guide to learn what is an ASPX file and APIs that can create and open them.",
  "title" : "ASPX File Format",
  "linktitle" : "ASPX",
  "menu" : {
    "docs" : {
      "parent" : "web"
    }
  },
  "lastmod" : "2019-09-10"
}

## What is an ASPX file?

A file with .aspx extension is a webpage generated using Microsoft ASP.NET framework running on web servers. ASPX stands for Active Server Pages Extended and these pages are displayed in web browser at user end when the URL is accessed. It is successor of [ASP](/web/asp/) technology which are also generated at server end but does not use .NET framework. ASP.NET pages may contain [C#](/programming/cs/) or [VB.NET](/programming/vb/) scripts that are translated to HTML by the web server for presentation to user in web browser. ASPX pages are also called .NET Web Forms. These can be opened and created with applications like Microsoft Visual Studio, Adobe Dreamweaver, Notepad++, and any text editor.

## ASPX File Format

ASP.NET web forms are based on the event-driven model for interactions with the web application. The browser, being an end user, submits a web form to the server and the server returns a full markup page or HTML page in response. ASP.NET component model offers object model for ASPX pages. This model describes:

 * Server side counterparts of almost all HTML elements or tags, such as \<form> and \<input>.
 * Server controls, which help in developing complex user-interface. For example, the Calendar control or the Gridview control.

ASPX files use the ASP.NET **Code Behind model** for construction of these pages.

### In-Line Code

Sample code that is embedded inline in the ASPX page and provides all the functionality for the user implementation.The following [C#](/programming/cs/) code represents a sample ASP.NET page that includes in-line code:

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

### Code-Behind

Code can be written and stored in separate class files for clean separation of HTML from presentation logic. This makes the presentation layer independent of the executable code. Following is the code-behind for presentation to user.

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

The C# implementation of the actual logic for the presentation layer is as follow.

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

## References

 * [ASP.NET WebApps - Microsoft](https://docs.microsoft.com/en-us/troubleshoot/webapps/welcome-webapps)
