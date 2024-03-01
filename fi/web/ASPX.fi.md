{
  "date": "2019-10-11",
  "keywords": [
"aspx",
"aspx tiedosto",
"aspx tiedostomuoto",
"aspx tiedostotyyppi",
"tiedosto",
"tyyppi",
"mikä on aspx-tiedosto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ASPX tiedostomuoto",
  "description": "Tiedostomuoto-opas oppiaksesi mikä on ASPX-tiedosto ja API:t, jotka voivat luoda ja avata ASPX-tiedostoja.",
  "linktitle": "ASPX",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-ASP-fiX"
}
},
  "lastmod": "2020-09-10"
}

## Mikä on ASPX-tiedosto?

Tiedosto, jonka laajennus on .aspx, on web-sivu, joka on luotu Web-palvelimilla toimivalla Microsoft ASP.NET -kehyksellä. ASPX on lyhenne sanoista Active Server Pages Extended, ja nämä sivut näkyvät verkkoselaimessa käyttäjän lopussa, kun URL-osoitetta käytetään. Se on [ASP](/web/asp/)-tekniikan seuraaja, joka myös luodaan palvelinpäässä, mutta joka ei käytä .NET-kehystä. ASP.NET-sivut voivat sisältää [C#](/programming/cs/)- tai [VB.NET](/programming/vb/)-skriptejä, jotka verkkopalvelin kääntää HTML:ksi esitettäväksi käyttäjälle verkkoselaimessa. ASPX-sivuja kutsutaan myös .NET Web Formsiksi. Näitä voidaan avata ja luoda sovelluksilla, kuten Microsoft Visual Studio, Adobe Dreamweaver, Notepad++ ja millä tahansa tekstieditorilla.

## ASPX tiedostomuoto

ASP.NET-verkkolomakkeet perustuvat tapahtumapohjaiseen malliin vuorovaikutuksessa verkkosovelluksen kanssa. Selain, joka on loppukäyttäjä, lähettää verkkolomakkeen palvelimelle ja palvelin palauttaa vastauksena täyden merkintäsivun tai HTML-sivun. ASP.NET-komponenttimalli tarjoaa objektimallin ASPX-sivuille. Tämä malli kuvaa:

 * Palvelinpuolen vastineet lähes kaikille HTML-elementeille tai -tageille, kuten \<form> ja \<input> .
 * Palvelinohjaimet, jotka auttavat kehittämään monimutkaista käyttöliittymää. Esimerkiksi Kalenteri- tai Gridview-säädin.

ASPX-tiedostot käyttävät ASP.NET **Code Behind -mallia** näiden sivujen rakentamiseen.

### In-Line Code

Esimerkkikoodi, joka on upotettu upotettuna ASPX-sivulle ja tarjoaa kaikki toiminnot käyttäjän käyttöönotolle. Seuraava [C#](/programming/cs/)-koodi edustaa esimerkki-ASP.NET-sivua, joka sisältää sisäänrakennetun koodin:

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

Koodi voidaan kirjoittaa ja tallentaa erillisiin luokkatiedostoihin, jotta HTML voidaan erottaa selkeästi esityslogiikasta. Tämä tekee esityskerroksesta riippumattoman suoritettavasta koodista. Seuraavassa on koodin takana esittelyä varten käyttäjälle.

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

Esityskerroksen varsinaisen logiikan C#-toteutus on seuraava.

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

## Viitteet

 * [ASP.NET WebApps – Microsoft](https://learn.microsoft.com/en-us/troubleshoot/webapps/welcome-webapps)

