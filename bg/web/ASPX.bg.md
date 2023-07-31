{
  "date" : "2019-10-11",
  "keywords" :[ "aspx", "aspx файл", "aspx файлов формат", "aspx тип файл", "файл", "тип", "какво е aspx файл" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Файлов формат ASPX",
  "description" :"Вашето ръководство за файлов формат, за да научите какво е ASPX файл и API, които могат да създават и отварят ASPX файлове.",
  "linktitle" : "ASPX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2020-09-10"
}

## Какво е ASPX файл?

Файл с разширение .aspx е уеб страница, генерирана с помощта на рамката на Microsoft ASP.NET, работеща на уеб сървъри. ASPX означава Active Server Pages Extended и тези страници се показват в уеб браузъра на потребителя, когато URL адресът е достъпен. Той е наследник на технологията [ASP](/bg/web/asp/), която също се генерира в края на сървъра, но не използва .NET framework. ASP.NET страниците могат да съдържат [C#](/bg/programming/cs/) или [VB.NET](/bg/programming/vb/) скриптове, които се превеждат в HTML от уеб сървъра за представяне на потребителя в уеб браузъра. ASPX страниците се наричат още .NET Web Forms. Те могат да се отварят и създават с приложения като Microsoft Visual Studio, Adobe Dreamweaver, Notepad++ и всеки текстов редактор.

## ASPX файлов формат

Уеб формулярите на ASP.NET са базирани на управляван от събития модел за взаимодействия с уеб приложението. Браузърът, като краен потребител, изпраща уеб формуляр на сървъра и сървърът връща пълна страница за маркиране или HTML страница в отговор. Компонентният модел на ASP.NET предлага обектен модел за ASPX страници. Този модел описва:

* Съответствия от страна на сървъра на почти всички HTML елементи или тагове, като \<form> и \<input> .
* Сървърни контроли, които помагат при разработването на сложен потребителски интерфейс. Например контролата Календар или контролата Gridview.

ASPX файловете използват ASP.NET **Code Behind model** за изграждане на тези страници.

### Вграден код

Примерен код, който е вграден в ASPX страницата и предоставя цялата функционалност за потребителско внедряване. Следният [C#](/bg/programming/cs/) код представлява примерна ASP.NET страница, която включва вграден код:

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

Кодът може да бъде написан и съхранен в отделни клас файлове за чисто отделяне на HTML от логиката на представяне. Това прави презентационния слой независим от изпълнимия код. Следва кодът за представяне на потребителя.

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

Изпълнението на C# на действителната логика за презентационния слой е както следва.

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

## Препратки

* [ASP.NET WebApps - Microsoft](https://learn.microsoft.com/en-us/troubleshoot/webapps/welcome-webapps)

