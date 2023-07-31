{
  "date" : "2019-10-11",
  "keywords" :[ "aspx","aspx dosyası", "aspx dosya formatı", "aspx dosya türü", "dosya", "tür", "aspx dosyası nedir" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASPX Dosya Biçimi",
  "description" :"ASPX dosyasının ne olduğunu ve ASPX dosyalarını oluşturabilen ve açabilen API'leri öğrenmek için dosya biçimi kılavuzunuz.",
  "linktitle" : "ASPX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2020-09-10"
}

## ASPX dosyası nedir?

.aspx uzantılı bir dosya, web sunucularında çalışan Microsoft ASP.NET çerçevesi kullanılarak oluşturulan bir web sayfasıdır. ASPX, Active Server Pages Extended anlamına gelir ve bu sayfalar, URL'ye erişildiğinde kullanıcı tarafında web tarayıcısında görüntülenir. Yine sunucu tarafında oluşturulan ancak .NET çerçevesini kullanmayan [ASP](/tr/web/asp/) teknolojisinin halefidir. ASP.NET sayfaları, web tarayıcısında kullanıcıya sunulmak üzere web sunucusu tarafından HTML'ye çevrilen [C#](/tr/programming/cs/) veya [VB.NET](/tr/programming/vb/) komut dosyalarını içerebilir. ASPX sayfalarına .NET Web Formları da denir. Bunlar, Microsoft Visual Studio, Adobe Dreamweaver, Notepad++ gibi uygulamalar ve herhangi bir metin düzenleyici ile açılıp oluşturulabilir.

## ASPX Dosya Biçimi

ASP.NET web formları, web uygulamasıyla etkileşimler için olaya dayalı modeli temel alır. Son kullanıcı olan tarayıcı, sunucuya bir web formu gönderir ve sunucu yanıt olarak tam bir biçimlendirme sayfası veya HTML sayfası döndürür. ASP.NET bileşen modeli, ASPX sayfaları için nesne modeli sunar. Bu model şunları açıklar:

* Hemen hemen tüm HTML öğelerinin veya etiketlerinin sunucu tarafı karşılıkları, örneğin \<form> ve \<input> .
* Karmaşık kullanıcı arayüzü geliştirmeye yardımcı olan sunucu kontrolleri. Örneğin, Calendar denetimi veya Gridview denetimi.

ASPX dosyaları, bu sayfaların oluşturulması için ASP.NET **Modelin Arkasındaki Kod**'u kullanır.

### Satır İçi Kod

ASPX sayfasında satır içine katıştırılmış ve kullanıcı uygulaması için tüm işlevleri sağlayan örnek kod. Aşağıdaki [C#](/tr/programming/cs/) kodu, satır içi kod içeren örnek bir ASP.NET sayfasını temsil eder:

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

### Kod Arkası

Kod, HTML'nin sunum mantığından temiz bir şekilde ayrılması için ayrı sınıf dosyalarında yazılabilir ve saklanabilir. Bu, sunum katmanını çalıştırılabilir koddan bağımsız hale getirir. Kullanıcıya sunum için arka plan kodu aşağıdadır.

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

Sunum katmanı için gerçek mantığın C# uygulaması aşağıdaki gibidir.

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

## Referanslar

* [ASP.NET Web Uygulamaları - Microsoft](https://learn.microsoft.com/en-us/troubleshoot/webapps/welcome-webapps)

