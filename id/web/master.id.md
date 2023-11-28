{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"File UTAMA - Format File Halaman Master ASP.NET",
  "description" :"Pelajari tentang Format File MASTER dan API untuk membuat dan membuka file MASTER.",
  "linktitle" : "MASTER",
  "menu" : {
    "docs" : {
      "identifier":"web-master",
      "parent" : "web"
}
},
  "lastmod" : "2021-02-29"
}

## Apa itu file UTAMA?

File MASTER adalah file templat halaman web master yang dibuat dengan ASP.NET. Ini digunakan sebagai titik awal untuk membuat beberapa halaman yang memiliki tata letak dan pengaturan yang sama dengan file MASTER. File MASTER template mencakup pengaturan untuk header, menu navigasi, footer, font dan informasi gaya. Menggunakan file MASTER membantu membuat banyak halaman web dengan cepat.

Anda dapat membuka file MASTER menggunakan Microsoft Visual Studio 2022 ke atas.

## Format File UTAMA - Informasi Lebih Lanjut

File MASTER dibuat dan disimpan dalam format file HTML dan mirip dengan file halaman web lainnya. Itu dipartisi menjadi bagian yang dapat diedit dan tidak dapat diedit. Bagian yang dapat diedit adalah bagian yang dapat dimodifikasi untuk memenuhi kebutuhan pengguna. Bagian yang tidak dapat diedit berwarna abu-abu ketika file MASTER dibuka di Microsoft Visual Studio.

Halaman Master terdiri dari dua bagian yaitu halaman master itu sendiri dan satu atau lebih halaman konten.

### Halaman UTAMA

Halaman master memiliki ekstensi .master dan dibuat di ASP.NET. Ini memiliki tata letak yang telah ditentukan sebelumnya yang terdiri dari teks statis, tag HTML, dan kontrol sisi server. Di halaman .aspx biasa, direktif @ Page digunakan. Dalam hal file .master, ini digantikan oleh direktif @ Master.

### Halaman Konten

Halaman konten mewakili konten untuk kontrol placeholder halaman master. Ini adalah halaman .aspx yang sebenarnya merupakan kode di belakang halaman master. Halaman konten diikat menggunakan direktif @ Page dengan menyertakan atribut MasterPageFile yang menunjuk ke halaman master untuk digunakan seperti yang ditunjukkan di bawah ini.

```
<%@ Page Language="VB" MasterPageFile="~/MasterPages/Master2.master" Title="Content Page of Master File" %>
```

## Referensi

* [Ikhtisar Halaman Master ASP.NET](https://learn.microsoft.com/en-us/previous-versions/aspnet/wtxbf3hh(v=vs.100))

