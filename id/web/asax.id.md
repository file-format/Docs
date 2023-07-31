{
  "date" : "2019-10-11",
  "keywords" :[ "asax","asax file", "format file asax", "tipe file asax", "file", "type", "apa itu file asax" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASAX - File Aplikasi Server ASP.NET",
  "description" :"Pelajari untuk mengetahui apa itu file ASAX dan API yang dapat membuat dan membuka file ASAX.",
  "linktitle" : "ASAX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-07"
}

## Apa itu file ASAX?

File dengan ekstensi .asax adalah file yang digunakan oleh aplikasi ASP.NET yang berada di sisi server. Ini berisi kode untuk menanggapi peristiwa tingkat aplikasi dan tingkat sesi yang diangkat oleh ASP.NET atau oleh modul HTTP. Ini juga termasuk menangani peristiwa tertentu saat aplikasi diluncurkan atau dimatikan. File ASAX bersifat opsional dan hanya satu file ASAX yang ditambahkan ke aplikasi web untuk menangani peristiwa dan kesalahan tingkat aplikasi di tingkat global. Tidak seperti halaman ASPX, file ASAX tidak berisi kode apa pun untuk mengimplementasikan fungsionalitas aplikasi.

## Format File ASAX

File ASAX ditulis dalam format file teks biasa dan dapat dibaca manusia. File ASAX yang paling umum digunakan adalah Global.asax yang berada di direktori root aplikasi ASP.NET. Server Web dikonfigurasi untuk menolak panggilan masuk ke file ini untuk melarang pengguna mengunduh atau melihat kode file ini.

### Global.ASAX - Contoh Format File ASAX

File ASAX tunggal terdiri dari beberapa bagian yang ditulis untuk menangani kejadian tingkat aplikasi. Ini adalah sebagai berikut.

* **Application Directive** - Application directives adalah tag yang digunakan untuk menentukan pengaturan khusus aplikasi opsional untuk digunakan oleh parser ASP.NET saat memproses file Global.asax. Direktif ini terletak di awal file Global.asax dan didefinisikan sebagai berikut.

```
<%@ direktif atribut=nilai [atribut=nilai … ]%>
```
* **Blok Deklarasi Kode** - Blok deklarasi kode digunakan untuk menentukan bagian kode server yang disematkan dalam file aplikasi ASP.NET di dalam \<script> blocks marked with a runat="server" attribute. The following example shows how you can define event-handling logic for the EnterBtn_Click event.

```
<html>
  <script language="C#" runat="server">
      void EnterBtn_Click(Object Src, EventArgs E) {
          Message.Text = "Hi " + Name.Text + ", welcome to ASP.NET!";
  }
  </script>

  <body>
   <form runat="server">
    Enter your name: <asp:textbox id="Name" runat=server/>
                     <asp:button text="Enter" Onclick="EnterBtn_Click" runat="server"/>
        <p>
        <asp:label id="Message" runat=server/>
    </form>
  </body>
</html>
```
* **Code Render Blocks** - Ini menentukan kode sebaris atau ekspresi yang dijalankan saat halaman dirender. Dua gaya blok render kode mencakup kode sebaris dan ekspresi sebaris. Yang pertama digunakan untuk mendefinisikan baris atau blok kode mandiri, sedangkan lateral digunakan sebagai jalan pintas untuk memanggil metode Write.

## Referensi

* [Ringkasan HTTP Handler dan Modul HTTP](https://msdn.microsoft.com/en-us/library/bb398986(v=vs.100))
* [Sintaks Global.asax](https://learn.microsoft.com/en-us/previous-versions/dotnet/netframework-4.0/2027ewzw(v=vs.100))

