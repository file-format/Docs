{
  "date": "2019-10-11",
  "keywords": [
"aspx",
"aspx failą",
"aspx failo formatas",
"aspx failo tipas",
"failą",
"tipo",
"kas yra aspx failas"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ASPX failo formatas",
  "description": "Jūsų failo formato vadovas, kad sužinotumėte, kas yra ASPX failas ir API, kurios gali kurti ir atidaryti ASPX failus.",
  "linktitle": "ASPX",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-ASP-ltX"
}
},
  "lastmod": "2020-09-10"
}

## Kas yra ASPX failas?

Failas su plėtiniu .aspx yra tinklalapis, sukurtas naudojant Microsoft ASP.NET sistemą, veikiančią žiniatinklio serveriuose. ASPX reiškia Active Server Pages Extended ir šie puslapiai rodomi žiniatinklio naršyklėje vartotojo pabaigoje, kai pasiekiamas URL. Tai yra [ASP](/web/asp/) technologijos, kuri taip pat generuojama serverio gale, įpėdinė, bet nenaudoja .NET sistemos. ASP.NET puslapiuose gali būti [C#](/programming/cs/) arba [VB.NET](/programming/vb/) scenarijų, kuriuos žiniatinklio serveris išverčia į HTML, kad jie būtų pateikti vartotojui žiniatinklio naršyklėje. ASPX puslapiai taip pat vadinami .NET žiniatinklio formomis. Juos galima atidaryti ir sukurti naudojant tokias programas kaip Microsoft Visual Studio, Adobe Dreamweaver, Notepad++ ir bet kurią teksto rengyklę.

## ASPX failo formatas

ASP.NET žiniatinklio formos yra pagrįstos įvykiais pagrįstu sąveikos su žiniatinklio programa modeliu. Naršyklė, būdama galutinis vartotojas, serveriui pateikia žiniatinklio formą, o serveris atsakydamas grąžina visą žymėjimo puslapį arba HTML puslapį. ASP.NET komponento modelis siūlo objekto modelį ASPX puslapiams. Šis modelis apibūdina:

 * Beveik visų HTML elementų ar žymų serverio atitikmenys, pvz., \<form> ir \<input> .
 * Serverio valdikliai, padedantys sukurti sudėtingą vartotojo sąsają. Pavyzdžiui, valdiklis Kalendorius arba valdiklis Gridview.

ASPX failuose šiems puslapiams sukurti naudojamas ASP.NET **Code Behind modelis**.

### In-Line Code

Pavyzdinis kodas, kuris yra įterptas į ASPX puslapį ir suteikia visas vartotojo diegimo funkcijas. Šis [C#](/programming/cs/) kodas yra pavyzdinis ASP.NET puslapis, kuriame yra eilutinis kodas:

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

### Užpakalinis kodas

Kodas gali būti parašytas ir saugomas atskiruose klasės failuose, kad būtų galima aiškiai atskirti HTML nuo pateikimo logikos. Dėl to pateikimo sluoksnis nepriklauso nuo vykdomojo kodo. Toliau pateikiamas kodas, skirtas pateikti vartotojui.

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

Pateikimo sluoksnio tikrosios logikos C# įgyvendinimas yra toks.

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

## Nuorodos

 * [ASP.NET WebApps – Microsoft](https://learn.microsoft.com/en-us/troubleshoot/webapps/welcome-webapps)

