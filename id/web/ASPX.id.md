{
  "date" : "2019-10-11",
  "keywords" :[ "aspx", "file aspx", "format file aspx", "tipe file aspx", "file", "type", "apa itu file aspx" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format File ASPX",
  "description" :"Panduan format file Anda untuk mempelajari apa itu file ASPX dan API yang dapat membuat dan membuka file ASPX.",
  "linktitle" : "ASPX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2020-09-10"
}

## Apa itu file ASPX?

File dengan ekstensi .aspx adalah halaman web yang dihasilkan menggunakan kerangka kerja Microsoft ASP.NET yang berjalan di server web. ASPX adalah singkatan dari Active Server Pages Extended dan halaman ini ditampilkan di browser web di sisi pengguna saat URL diakses. Ini adalah penerus teknologi [ASP](/id/web/asp/) yang juga dihasilkan di ujung server tetapi tidak menggunakan .NET framework. Halaman ASP.NET mungkin berisi skrip [C#](/id/programming/cs/) atau [VB.NET](/id/programming/vb/) yang diterjemahkan ke HTML oleh server web untuk dipresentasikan kepada pengguna di browser web. Halaman ASPX juga disebut .NET Web Forms. Ini dapat dibuka dan dibuat dengan aplikasi seperti Microsoft Visual Studio, Adobe Dreamweaver, Notepad ++, dan editor teks apa pun.

## Format File ASPX

Formulir web ASP.NET didasarkan pada model berbasis kejadian untuk interaksi dengan aplikasi web. Browser, sebagai pengguna akhir, mengirimkan formulir web ke server dan server mengembalikan halaman markup lengkap atau halaman HTML sebagai tanggapan. Model komponen ASP.NET menawarkan model objek untuk halaman ASPX. Model ini menjelaskan:

* Mitra sisi server dari hampir semua elemen atau tag HTML, seperti \<form> dan \<input> .
* Kontrol server, yang membantu dalam mengembangkan antarmuka pengguna yang kompleks. Misalnya, kontrol Kalender atau kontrol Gridview.

File ASPX menggunakan ASP.NET **Code Behind model** untuk pembuatan halaman ini.

### Kode Sebaris

Kode contoh yang disematkan sebaris di halaman ASPX dan menyediakan semua fungsionalitas untuk implementasi pengguna. Kode [C#](/id/programming/cs/) berikut ini menunjukkan contoh halaman ASP.NET yang menyertakan kode sebaris:

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

### Dibalik Kode

Kode dapat ditulis dan disimpan dalam file kelas terpisah untuk memisahkan HTML dari logika presentasi. Ini membuat lapisan presentasi tidak bergantung pada kode yang dapat dieksekusi. Berikut ini adalah kode di belakang untuk presentasi ke pengguna.

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

Implementasi C# dari logika sebenarnya untuk lapisan presentasi adalah sebagai berikut.

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

## Referensi

* [ASP.NET WebApps - Microsoft](https://docs.microsoft.com/en-us/troubleshoot/webapps/welcome-webapps)

