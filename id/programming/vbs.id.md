{
  "date" : "2021-08-24", 
  "keywords" :[ "vbs", "file", "extension", "file format", "Visual Basic Script", "Panduan Pemrograman", "contoh vbs", "Microsoft Visual Basic", "VBScript" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VBS - File Skrip Visual Basic",
  "description":"Pelajari tentang format file VBS dan API yang dapat membuat dan membuka file VBS.",
  "linktitle" : "VBS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-08-24"
}

## Apa itu file VBS?

VBS atau VBScript terhubung dengan edisi skrip Microsoft Visual Basic. Dalam lingkungan komputasi, pengguna diperbolehkan untuk mengakses dan mengontrol banyak aspeknya. VBScript diizinkan menggunakan model bernama **Component Object Model** untuk memanfaatkan elemen dan alat lingkungan. Lingkungan ini ditentukan untuk bekerja dan menjalankan VBScript.

Ini berfungsi mirip dengan Javascript ketika diakses oleh klien di bidang pengembangan Web. Ini juga digunakan oleh server untuk memproses halaman web. Ini dapat dipertimbangkan dalam beberapa jenis file skrip lain seperti aplikasi [HTML](/id/web/html/).


## Sejarah Singkat ##

Ini pertama kali diluncurkan pada tahun 1996, sebagai bagian dari teknologi yang digunakan oleh Microsoft yang ditentukan untuk Skrip Windows. Itu secara khusus dikembangkan untuk bantuan pengembang Web pada awalnya. Pada tahun yang sama, penjelajah Microsoft Windows bernama Internet Explorer dirilis bersama dengan fitur Visual Basic Script.

Dengan kemajuan teknologi dan pengembangan web, banyak versi VBScript bersama dengan banyak fitur canggih diluncurkan. Apalagi di tahun mendatang, bahasa scripting ini akan menjadi bagian dari Microsoft Windows dengan fitur-fitur baru.

## Spesifikasi Teknis ##

Untuk halaman web di sisi server, alat seperti **Halaman Server Aktif** digunakan bersama dengan VBScript. Bahasa skrip ini juga dapat digunakan dalam komponen skrip Windows. File bahasa ini disimpan dengan ekstensi .vbs di Windows.

Ada banyak struktur kontrol seperti loop yang digunakan dalam kode bahasa ini. Itu juga termasuk argumen yang merupakan baris perintah dan dapat diberi nama atau tidak disebutkan namanya. File bahasa ini dapat disimpan hanya di folder atau di desktop sistem operasi Windows. Meskipun tidak ada lingkungan pengembangan terintegrasi khusus untuk program VBScript seperti Microsoft Script Editor menyediakan fasilitas pengembangan bahasa ini.

Ketika VBScript dihosting oleh host Script Windows, VBScript menyediakan berbagai fitur yang cukup umum untuk bahasa skrip tetapi tidak tersedia di Visual Basic 6.0. Fitur yang melibatkan akses mudah atau langsung melibatkan Printer Jaringan, argumen baris perintah tanpa nama dan nama, stdout, dan stdin, Berbagi Jaringan, Instrumentasi Manajemen Windows, informasi pengguna jaringan seperti keanggotaan grup, dan banyak lagi.

## Contoh Format File VBS ##

```
<% Option Explicit %>
 <!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">
 <html>
 	<head>
 		<title>VBScript Example</title>
 	</head>
 	<body>
 		<div><% 
 			' Grab current time from Now() function.
 			' An '=' sign occurring after a context switch (<%) is shorthand 
 			' for a call to the Write() method of the Response object.
 			Dim timeValue : timeValue = Now %>
 			The time, in 24-hour format, is 
 			<%=Hour(timeValue)%>:<%=Minute(timeValue)%>:<%=Second(timeValue)%>.
 		</div>
 	</body>
 </html>
```

## Referensi ##

* [VBS - oleh Wikipedia](https://en.wikipedia.org/wiki/VBScript)



