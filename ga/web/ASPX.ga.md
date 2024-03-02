{
  "date": "2019-10-11",
  "keywords": [
"aspx",
"comhad aspx",
"formáid comhaid aspx",
"cineál comhaid aspx",
"comhad",
"cineál",
"cad is comhad aspx ann"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "Formáid Chomhaid ASPX",
  "description": "Do threoir formáid comhaid chun a fháil amach cad is comhad ASPX agus APIs ann ar féidir comhaid ASPX a chruthú agus a oscailt.",
  "linktitle": "ASPX",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-ASP-gaX"
}
},
  "lastmod": "2020-09-10"
}

## Cad is comhad ASPX ann?

Is leathanach gréasáin é comhad le síneadh .aspx a ghintear trí úsáid a bhaint as creat Microsoft ASP.NET a fheidhmíonn ar fhreastalaithe gréasáin. Seasann ASPX do Leathanaigh Freastalaí Gníomhacha Leathnaithe agus taispeántar na leathanaigh seo sa bhrabhsálaí gréasáin ag deireadh an úsáideora nuair a bhíonn rochtain ar an URL. Tagann sé i gcomharbacht ar theicneolaíocht [ASP](/web/asp/) a ghintear ag deireadh an fhreastalaí freisin ach nach n-úsáideann creat .NET. D'fhéadfadh go mbeadh [C#](/programming/cs/) nó [VB.NET](/programming/vb/) scripteanna a aistríonn an freastalaí gréasáin go HTML le cur i láthair don úsáideoir sa bhrabhsálaí gréasáin ar leathanaigh ASP.NET. Tugtar .NET Web Forms ar leathanaigh ASPX freisin. Is féidir iad seo a oscailt agus a chruthú le feidhmchláir mar Microsoft Visual Studio, Adobe Dreamweaver, Notepad++, agus aon eagarthóir téacs.

## Formáid Chomhaid ASPX

Tá foirmeacha gréasáin ASP.NET bunaithe ar an tsamhail atá bunaithe ar imeachtaí le haghaidh idirghníomhaíochtaí leis an bhfeidhmchlár gréasáin. Is úsáideoir deiridh é an brabhsálaí, cuireann sé foirm ghréasáin isteach chuig an bhfreastalaí agus seolann an freastalaí leathanach marcála iomlán nó leathanach HTML mar fhreagra. Cuireann samhail chomhpháirt ASP.NET samhail réad ar fáil do leathanaigh ASPX. Déanann an tsamhail seo cur síos ar:

 * Comhghleacaithe taobh freastalaí de bheagnach gach eilimint HTML nó clib, mar \ \<form> agus \<input> .
 * Rialuithe freastalaí, a chuidíonn le comhéadan úsáideora casta a fhorbairt. Mar shampla, an rialú Calendar nó an rialú Gridview.

Úsáideann comhaid ASPX an múnla **Code Behind** ASP.NET chun na leathanaigh seo a thógáil.

### Cód In-Líne

Cód samplach atá leabaithe inlíne sa leathanach ASPX agus a sholáthraíonn an fheidhmiúlacht go léir le haghaidh fheidhmiú an úsáideora. Léiríonn an cód [C#](/programming/cs/) seo a leanas leathanach samplach ASP.NET a chuimsíonn cód inlíne:

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

### Cód Taobh thiar

Is féidir cód a scríobh agus a stóráil i gcomhaid ranga ar leith chun HTML a scaradh go glan ó loighic an chur i láthair. Déanann sé seo an ciseal léirithe neamhspleách ar an gcód inrite. Seo a leanas an cód-taobh thiar le cur i láthair don úsáideoir.

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

Seo a leanas cur i bhfeidhm C# an loighic iarbhír don chiseal cur i láthair.

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

## Tagairtí

 * [ASP.NET WebApps - Microsoft](https://learn.microsoft.com/en-us/troubleshoot/webapps/welcome-webapps)

