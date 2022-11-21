{
  "date" : "2019-10-11",
  "keywords" :[ "asmx", "file asmx", "format file asmx", "jenis file asmx", "file", "ketik", "apa itu file asmx" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASMX - File Layanan Web ASP.NET",
  "description" :"Pelajari tentang apa itu file ASMX dan API yang dapat membuat dan membuka file ASMX.",
  "linktitle" : "ASMX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-10"
}

## Apa itu file ASMX?

File dengan ekstensi .asmx adalah file ASP.NET Web Service yang menyediakan komunikasi antara dua objek melalui internet menggunakan Simple Object Access Protocol (SOAP). Itu digunakan sebagai layanan di Server Web berbasis Windows untuk memproses permintaan masuk dan mengembalikan respons. Tidak seperti file [ASPX](/id/web/aspx/) yang berisi kode untuk tampilan visual halaman web ASP.NET, file ASMX berjalan di server di latar belakang dan melakukan tugas yang berbeda seperti menghubungkan ke database, mengambil data, dan mengembalikannya di format di mana permintaan dibuat. Ini digunakan secara khusus untuk layanan web XML.

## Format File ASMX

File ASMX dalam format teks biasa dan dapat dibuka atau diedit dalam aplikasi seperti Microsoft Visual Studio atau editor teks. Ini adalah format file milik Microsoft dan memiliki sintaks yang terdefinisi dengan baik untuk pembuatan layanan web. Respons oleh file ASMX dalam bentuk SOAP XML memiliki elemen berikut.

* `Envelop` - Elemen root yang mengidentifikasi dokumen XML sebagai pesan SOAP.
* `Header` - Elemen opsional yang berisi informasi khusus aplikasi seperti data autentikasi. Jika ada elemen Header, itu harus menjadi elemen anak pertama dari elemen Envelope.
* `Body` - Berisi pesan SOAP yang ditujukan untuk penerima.
* `Fault` - Elemen opsional yang digunakan untuk menunjukkan pesan kesalahan. Jika ada elemen Fault, itu pasti merupakan elemen turunan dari elemen Body.

File ASMX dapat ditulis dalam bahasa .NET seperti [C#](/id/programming/cs/), [Visual Basic](/id/programming/vb/) atau JScript.

## Apa perbedaan ASMX dari ASPX dan ASCX?

File ASMX berbeda dari file ASPX dan ASCX.

* ASPX, Active Server Pages, file adalah file pemrograman yang dihasilkan menggunakan framework Microsoft ASP.NET yang berjalan di server web. Ini ditampilkan di browser web klien saat permintaan pengguna untuk mengakses halaman tersebut.
* ASCX, Kontrol Pengguna Server Aktif, menentukan kontrol pengguna yang digunakan untuk menentukan kontrol yang dapat digunakan kembali di halaman web ASP.NET atau seluruh situs web.

## Referensi

* [Mengkonsumsi Layanan ASMX](https://docs.microsoft.com/en-us/xamarin/xamarin-forms/data-cloud/web-services/asmx)
* [Kontrol Pengguna ASCX](http://www.beansoftware.com/ASP.NET-Tutorials/User-Control.aspx)

