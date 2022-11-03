{
  "date" : "2019-10-11",
  "keywords" :[ "aspx", "файл aspx", "формат файла aspx", "тип файла aspx", "файл", "тип", "что такое файл aspx" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Формат файла ASPX",
  "description" :"Ваше руководство по формату файла, чтобы узнать, что такое файл ASPX и API, которые могут создавать и открывать файлы ASPX.",
  "linktitle" : "ASPX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2020-09-10"
}

## .ASPX вариант №

Файл с расширением .aspx представляет собой веб-страницу, созданную с использованием платформы Microsoft ASP.NET, работающей на веб-серверах. ASPX расшифровывается как Active Server Pages Extended, и эти страницы отображаются в веб-браузере на стороне пользователя при доступе к URL-адресу. Это преемник технологии [ASP](/ru/web/asp/), которая также создается на стороне сервера, но не использует платформу .NET. Страницы ASP.NET могут содержать сценарии [C#](/ru/programming/cs/) или [VB.NET](/ru/programming/vb/), которые веб-сервер переводит в HTML для представления пользователю в веб-браузере. Страницы ASPX также называются веб-формами .NET. Их можно открывать и создавать с помощью таких приложений, как Microsoft Visual Studio, Adobe Dreamweaver, Notepad++ и любого текстового редактора.

## Формат файла ASPX

Веб-формы ASP.NET основаны на управляемой событиями модели взаимодействия с веб-приложением. Браузер, будучи конечным пользователем, отправляет веб-форму на сервер, и сервер возвращает в ответ полную страницу разметки или HTML-страницу. Компонентная модель ASP.NET предлагает объектную модель для страниц ASPX. Эта модель описывает:

* Аналоги почти всех HTML-элементов или тегов на стороне сервера, например \<form> а также \<input> .
* Серверные элементы управления, которые помогают в разработке сложного пользовательского интерфейса. Например, элемент управления Calendar или элемент управления Gridview.

Файлы ASPX используют модель ASP.NET **Code Behind** для построения этих страниц.

### Встроенный код

Пример кода, встроенного в страницу ASPX и предоставляющего все функциональные возможности для пользовательской реализации. Следующий код [C#](/ru/programming/cs/) представляет пример страницы ASP.NET, которая включает встроенный код:

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

### Код программной части

Код можно писать и хранить в отдельных файлах классов для четкого отделения HTML от логики представления. Это делает уровень представления независимым от исполняемого кода. Ниже приведен код программной части для представления пользователю.

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

Реализация C# фактической логики для уровня представления выглядит следующим образом.

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

## использованная литература

* [ASP.NET WebApps — Microsoft] (https://docs.microsoft.com/en-us/troubleshoot/webapps/welcome-webapps)

