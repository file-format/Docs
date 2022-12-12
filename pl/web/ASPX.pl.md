{
  "date" : "2019-10-11",
  "keywords" :["aspx","plik aspx", "format pliku aspx", "typ pliku aspx", "plik", "typ", "co to jest plik aspx"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format Pliku ASPX",
  "description" :"Twój przewodnik po formacie pliku, aby dowiedzieć się, co to jest plik ASPX i interfejsy API, które mogą tworzyć i otwierać pliki ASPX.",
  "linktitle" : "ASPX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2020-09-10"
}

## Czym jest plik ASPX?

Plik z rozszerzeniem .aspx to strona internetowa wygenerowana przy użyciu platformy Microsoft ASP.NET działającej na serwerach WWW. ASPX oznacza Active Server Pages Extended, a strony te są wyświetlane w przeglądarce internetowej po stronie użytkownika, gdy uzyskuje się dostęp do adresu URL. Jest następcą technologii [ASP](/pl/web/asp/), która również jest generowana po stronie serwera, ale nie wykorzystuje frameworka .NET. Strony ASP.NET mogą zawierać skrypty [C#](/pl/programming/cs/) lub [VB.NET](/pl/programming/vb/), które są tłumaczone na HTML przez serwer WWW w celu prezentacji użytkownikowi w przeglądarce internetowej. Strony ASPX są również nazywane formularzami sieci Web platformy .NET. Można je otwierać i tworzyć za pomocą aplikacji takich jak Microsoft Visual Studio, Adobe Dreamweaver, Notepad++ i dowolnego edytora tekstu.

## Format pliku ASPX

Formularze internetowe ASP.NET są oparte na sterowanym zdarzeniami modelu interakcji z aplikacją internetową. Przeglądarka będąca użytkownikiem końcowym przesyła formularz internetowy do serwera, a serwer zwraca w odpowiedzi pełną stronę ze znacznikami lub stronę HTML. Model komponentów ASP.NET oferuje model obiektowy dla stron ASPX. Ten model opisuje:

* Odpowiedniki po stronie serwera prawie wszystkich elementów HTML lub tagów, takie jak \<form> oraz \<input> .
* Kontrolki serwera, które pomagają w tworzeniu złożonego interfejsu użytkownika. Na przykład formant Calendar lub formant Gridview.

Pliki ASPX używają modelu ASP.NET **Code Behind** do budowy tych stron.

### Kod liniowy

Przykładowy kod, który jest osadzony w tekście na stronie ASPX i zapewnia wszystkie funkcje implementacji użytkownika. Poniższy kod [C#](/pl/programming/cs/) reprezentuje przykładową stronę ASP.NET zawierającą kod w wierszu:

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

### Za kodem

Kod można pisać i przechowywać w oddzielnych plikach klas, aby wyraźnie oddzielić HTML od logiki prezentacji. Dzięki temu warstwa prezentacji jest niezależna od kodu wykonywalnego. Poniżej znajduje się kod związany z prezentacją dla użytkownika.

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

Implementacja rzeczywistej logiki w języku C# dla warstwy prezentacji jest następująca.

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

## Bibliografia

* [ASP.NET WebApps — Microsoft](https://docs.microsoft.com/en-us/troubleshoot/webapps/welcome-webapps)

