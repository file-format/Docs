{
  "date" : "2019-10-11",
  "keywords" :[ "aspx", "файл aspx", "формат файлу aspx", "тип файлу aspx", "файл", "тип", "що таке файл aspx" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Формат файлу ASPX",
  "description" :"Посібник із формату вашого файлу, щоб дізнатися, що таке файл ASPX та API, які можуть створювати та відкривати файли ASPX.",
  "linktitle" : "ASPX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2020-09-10"
}

## Що таке файл ASPX?

Файл із розширенням .aspx — це веб-сторінка, створена за допомогою Microsoft ASP.NET framework, що працює на веб-серверах. ASPX означає Active Server Pages Extended, і ці сторінки відображаються у веб-браузері на стороні користувача під час доступу до URL-адреси. Це наступник технології [ASP](/uk/web/asp/), яка також генерується на сервері, але не використовує .NET framework. Сторінки ASP.NET можуть містити сценарії [C#](/uk/programming/cs/) або [VB.NET](/uk/programming/vb/), які веб-сервер переводить у HTML для представлення користувачеві у веб-браузері. Сторінки ASPX також називаються веб-формами .NET. Їх можна відкрити та створити за допомогою таких програм, як Microsoft Visual Studio, Adobe Dreamweaver, Notepad++ і будь-якого текстового редактора.

## Формат файлу ASPX

Веб-форми ASP.NET базуються на керованій подіями моделі взаємодії з веб-програмою. Браузер, будучи кінцевим користувачем, надсилає веб-форму на сервер, а сервер у відповідь повертає повну сторінку розмітки або HTML-сторінку. Компонентна модель ASP.NET пропонує об’єктну модель для сторінок ASPX. Ця модель описує:

* Серверні аналоги майже всіх елементів або тегів HTML, таких як \<form> і \<input> .
* Елементи керування сервером, які допомагають у розробці складного інтерфейсу користувача. Наприклад, елемент керування Календар або елемент керування Сітка.

Файли ASPX використовують модель ASP.NET **Code Behind** для створення цих сторінок.

### Внутрішній код

Зразок коду, який вбудовано в сторінку ASPX і надає всі функції для реалізації користувачем. Наступний код [C#](/uk/programming/cs/) представляє зразок сторінки ASP.NET, яка містить вбудований код:

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

### Код позаду

Код можна писати та зберігати в окремих файлах класів для чіткого відокремлення HTML від логіки представлення. Це робить презентаційний рівень незалежним від виконуваного коду. Нижче наведено код для представлення користувачеві.

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

Реалізація C# фактичної логіки для рівня презентації така.

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

## Список літератури

* [ASP.NET WebApps – Microsoft](https://learn.microsoft.com/en-us/troubleshoot/webapps/welcome-webapps)

