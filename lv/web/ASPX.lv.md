{
  "date": "2019-10-11",
  "keywords": [
"aspx",
"aspx failu",
"aspx faila formātā",
"aspx faila tips",
"failu",
"veids",
"kas ir aspx fails"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ASPX faila formāts",
  "description": "Jūsu faila formāta ceļvedis, lai uzzinātu, kas ir ASPX fails un API, kas var izveidot un atvērt ASPX failus.",
  "linktitle": "ASPX",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-ASP-lvX"
}
},
  "lastmod": "2020-09-10"
}

## Kas ir ASPX fails?

Fails ar paplašinājumu .aspx ir tīmekļa lapa, kas ģenerēta, izmantojot Microsoft ASP.NET ietvaru, kas darbojas tīmekļa serveros. ASPX apzīmē Active Server Pages Extended, un šīs lapas tiek parādītas tīmekļa pārlūkprogrammā lietotāja beigās, kad tiek piekļūts URL. Tā ir [ASP](/web/asp/) tehnoloģijas pēctece, kas arī tiek ģenerēta servera galā, bet neizmanto .NET ietvaru. ASP.NET lapās var būt [C#](/programming/cs/) vai [VB.NET](/programming/vb/) skripti, kurus tīmekļa serveris pārtulko HTML formātā, lai tos prezentētu lietotājam tīmekļa pārlūkprogrammā. ASPX lapas sauc arī par .NET Web Forms. Tos var atvērt un izveidot, izmantojot tādas lietojumprogrammas kā Microsoft Visual Studio, Adobe Dreamweaver, Notepad++ un jebkuru teksta redaktoru.

## ASPX faila formāts

ASP.NET tīmekļa veidlapas ir balstītas uz notikumiem balstītu modeli mijiedarbībai ar tīmekļa lietojumprogrammu. Pārlūkprogramma, kas ir gala lietotājs, serverim iesniedz tīmekļa veidlapu, un serveris atbildē atgriež pilnu iezīmēšanas lapu vai HTML lapu. ASP.NET komponenta modelis piedāvā objektu modeli ASPX lapām. Šis modelis apraksta:

 * Servera līdzinieki gandrīz visiem HTML elementiem vai tagiem, piemēram, \<form> un \<input> .
 * Servera vadīklas, kas palīdz izstrādāt sarežģītu lietotāja interfeisu. Piemēram, vadīkla Kalendārs vai Gridview vadīkla.

ASPX faili izmanto ASP.NET **Code Behind modeli** šo lapu izveidei.

### In-Line Code

Koda paraugs, kas ir iegults ASPX lapā un nodrošina visas lietotāja ieviešanas funkcionalitātes. Šis [C#](/programming/cs/) kods ir ASP.NET lapas paraugs, kurā ir ietverts kods:

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

### Kods aiz muguras

Kodu var rakstīt un uzglabāt atsevišķos klases failos, lai tīri atdalītu HTML no prezentācijas loģikas. Tas padara prezentācijas slāni neatkarīgu no izpildāmā koda. Tālāk ir sniegts aizmugures kods prezentēšanai lietotājam.

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

Prezentācijas slāņa faktiskās loģikas C# ieviešana ir šāda.

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

## Atsauces

 * [ASP.NET WebApps — Microsoft](https://learn.microsoft.com/en-us/troubleshoot/webapps/welcome-webapps)

