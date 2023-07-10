{
  "date" : "2019-10-11",
  "keywords" :[ "ascx", "file ascx", "format file ascx", "tipe file ascx", "file", "type", "apa itu file ascx" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format File ASCX",
  "description" :"Pelajari tentang apa itu file ASCX dan API yang dapat membuat dan membuka file ASCX.",
  "linktitle" : "ASCX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2020-09-10"
}

## Apa itu file ASCX?

File dengan ekstensi .ascx adalah kontrol pengguna yang digunakan sebagai komponen yang dapat digunakan kembali di halaman web. Itu direferensikan di situs web ASP mana pun dengan menyeretnya dari kotak kontrol ke halaman. Kontrol pengguna ASCX ditambahkan ke proyek sebagai sumber utama, sehingga setiap perubahan dalam kontrol pengguna akan tercermin di seluruh situs web. Tidak seperti file ASMX yang menentukan mekanisme untuk berkomunikasi dalam 2 objek melalui internet, file ASCX adalah kontrol pengguna untuk disematkan di halaman atau situs web.

## Format File ASCX

File ASCX ditulis dalam format teks biasa dan dapat menggunakan kode di belakang fitur seperti halaman web yang diakhiri dengan .ascx.cs. Kode markup kontrol pengguna dimulai dengan direktif @Control seperti yang diperlihatkan dalam contoh berikut.

```
<%@ Control Language="VB" AutoEventWireup="false" CodeFile="WebUserControl.ascx.vb" Inherits="WebUserControl" %>
<p>A simple web user control with static HTML only.</p>
```

Kontrol pengguna web ini dapat digunakan kembali di banyak halaman seperti footer halaman, header atau semacam navigasi situs. Kontrol pengguna web memiliki properti, metode, dan peristiwa seperti kontrol lainnya yang membuatnya berguna dalam mengatur perilaku visualnya.

### Contoh Mendaftarkan kontrol pengguna di web.config

Untuk menggunakan kontrol pengguna tunggal pada banyak halaman, kontrol web dapat didaftarkan di web.config. Ini memungkinkan untuk menggunakan kontrol atas semua situs web alih-alih mendaftar di setiap halaman satu per satu. Kode contoh berikut menentukan cara mendaftarkan kontrol web di web.config untuk ditampilkan sebagai footer di seluruh situs web.

```
<configuration>
  <system.web>
    <pages>
      <controls>
        <add src="Footer.ascx" tagPrefix="bs" tagName="footer" />
      </controls >
    </pages >
  </system.web>
</configuration>
```
## Referensi

* [ASCX vs ASMX](https://social.msdn.microsoft.com/Forums/en-US/a27d4c2f-b972-439e-a7fe-f4b7e3637700/how-to-work-with-ascx-files?forum=aspwebforms)
* [Kontrol Pengguna ASCX](http://www.beansoftware.com/ASP.NET-Tutorials/User-Control.aspx)

