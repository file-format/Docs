{
  "date" : "2021-03-02",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RDLC - Sisi Klien Bahasa Definisi Laporan",
  "keywords" :["rdlc", "laporkan bahasa definisi", "format mkv", "XSD", "laporkan sisi klien bahasa definisi"],
  "description":"Pelajari tentang format file RDLC yang merupakan representasi XML dari definisi laporan Layanan Pelaporan SQL Server.",
  "linktitle" : "RDLC",
  "menu" : {
    "docs" : {
      "parent" : "reporting"
}
},
  "lastmod" : "2021-03-02"
}

## Apa itu file RDLC? ##

RDLC adalah singkatan dari sisi Klien Bahasa Definisi Laporan. Sebenarnya Ini adalah perpanjangan dari file laporan yang dibuat dengan menggunakan teknologi pelaporan Microsoft. Versi SQL Server 2005 Report Designer digunakan untuk membuat file-file ini. Kontrol **ReportViewer** di sisi klien dapat langsung menjalankan laporan RDLC.

## File RDL VS RDLC
|.rdl Berkas |.rdlc berkas|
---|---|
|File RDL dibuat oleh Report Designer versi SQL Server 2005|File RDLC dibuat oleh Report Designer versi Visual Studio 2005|
|Hal ini digunakan dalam Layanan Pelaporan SQL Server|Hal ini digunakan dalam Visual Studio|
|Ini adalah laporan jarak jauh|Ini adalah laporan lokal|
|Perlu instance Layanan Pelaporan untuk menjalankannya|Tidak perlu instance Layanan Pelaporan|

## Membuat File Definisi Laporan Klien (.rdlc).
Kontrol ReportViewer digunakan untuk menjalankan file definisi laporan klien (.rdlc) menggunakan kemampuan pemrosesan bawaan kontrol. Laporan klien yang Anda jalankan dalam mode pemrosesan lokal dapat dengan mudah dibuat di proyek aplikasi Anda. Berikut ini adalah pendekatan untuk membuat laporan:

- Gunakan **Report Wizard** untuk membuat definisi laporan klien baru (.rdlc).

- Buat file definisi laporan klien baru (.rdlc) dengan menggunakan Visual Studio.

- Menghasilkan definisi laporan pemrograman.


Anda hanya dapat mempratinjau laporan dengan menjalankannya di kontrol **ReportViewer**. Harap Perhatikan bahwa Anda dapat membuka dan mengedit definisi laporan kapan saja, lalu membangun atau menggunakan aplikasi untuk memeriksa hasilnya.

## Referensi ##

- [Membuat File Client Report Definition (.rdlc)](https://docs.microsoft.com/en-us/previous-versions/visualstudio/visual-studio-2010/ms252067(v=vs.100))

