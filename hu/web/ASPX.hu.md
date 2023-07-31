{
  "date" : "2019-10-11",
  "keywords" :[ "aspx", "aspx fájl", "aspx fájlformátum", "aspx fájltípus", "fájl", "típus", "mi az aspx fájl" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASPX fájlformátum",
  "description" :"Fájlformátum-útmutató, hogy megtudja, mi az ASPX fájl és API-k, amelyek ASPX fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "ASPX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2020-09-10"
}

## Mi az ASPX fájl?

Az .aspx kiterjesztésű fájl egy webszervereken futó Microsoft ASP.NET keretrendszer segítségével létrehozott weboldal. Az ASPX az Active Server Pages Extended rövidítése, és ezek az oldalak a webböngészőben jelennek meg a felhasználó végén az URL elérésekor. Ez az [ASP](/hu/web/asp/) technológia utódja, amely szintén a szerver végén jön létre, de nem használ .NET-keretrendszert. Az ASP.NET oldalak [C#](/hu/programming/cs/) vagy [VB.NET](/hu/programming/vb/) szkripteket tartalmazhatnak, amelyeket a webszerver lefordít HTML-be, hogy a webböngészőben a felhasználónak bemutassa. Az ASPX oldalakat .NET webes űrlapoknak is nevezik. Ezek megnyithatók és létrehozhatók olyan alkalmazásokkal, mint a Microsoft Visual Studio, az Adobe Dreamweaver, a Notepad++ és bármilyen szövegszerkesztő.

## ASPX fájlformátum

Az ASP.NET webes űrlapjai a webalkalmazással való interakció eseményvezérelt modelljén alapulnak. A böngésző, mint végfelhasználó, elküld egy webes űrlapot a szervernek, és a szerver válaszul egy teljes jelölőoldalt vagy HTML-oldalt küld vissza. Az ASP.NET komponens modell objektummodellt kínál az ASPX oldalakhoz. Ez a modell a következőket írja le:

* Szinte az összes HTML elem vagy címke szerveroldali megfelelői, mint pl.<form> és \<input> .
* Szervervezérlők, amelyek segítenek a komplex felhasználói felület kialakításában. Például a Naptár vezérlő vagy a Rácsnézet vezérlő.

Az ASPX fájlok az ASP.NET **Code Behind modellt** használják ezen oldalak felépítéséhez.

### Soron belüli kód

Mintakód, amely soron belül van beágyazva az ASPX oldalba, és biztosítja a felhasználói megvalósítás összes funkcióját. A következő [C#](/hu/programming/cs/) kód egy minta ASP.NET oldalt képvisel, amely soron belüli kódot tartalmaz:

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

A kód külön osztályfájlokban írható és tárolható a HTML és a prezentációs logika tiszta elkülönítése érdekében. Ez függetlenné teszi a megjelenítési réteget a végrehajtható kódtól. Az alábbiakban a felhasználónak való bemutatásra szolgáló kód mögött látható.

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

A megjelenítési réteg tényleges logikájának C# megvalósítása a következő.

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

## Hivatkozások

* [ASP.NET WebApps – Microsoft](https://learn.microsoft.com/en-us/troubleshoot/webapps/welcome-webapps)

