{
  "date" : "2022-08-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"File HDMP - Format File Windows Heap Dump",
  "description":"Pelajari tentang format file HDMP dan API yang dapat membuat dan membuka file HDMP.",
  "linktitle" : "HDMP",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2022-08-19"
}

## Apa itu file HDMP?

File HDMP adalah dump memori yang tidak terkompresi ketika aplikasi atau program macet karena kesalahan. Itu hanya dibuat oleh Windows XP/Vista dan berisi dump status aplikasi saat macet. Karena tidak terkompresi, file HDMP mengambil lebih banyak ruang pada disk dibandingkan dengan file Minidump [MDMP](/id/system/mdmp/) yang dikompresi untuk tujuan pelaporan.

Aplikasi yang dapat digunakan untuk **membuka** atau menganalisis file HDMP termasuk Microsoft Visual Studio dengan alat Debugging untuk Windows.

## Format File HDMP

File HDMP disimpan ke disk sebagai file biner dan tidak memberikan manfaat apa pun jika dibuka tanpa aplikasi yang sesuai. Ini berisi data sistem relevan yang direkam saat kesalahan terjadi.

### Perbedaan antara Format File HDMP dan MDMP

HDMP adalah file dump memori yang tidak dikompresi. Sebaliknya, MDMP adalah file dump mini yang dikompresi untuk mengurangi ukuran file dan mengirimkannya ke Microsoft untuk melaporkan masalah tersebut.

## Referensi ##

* [DMP - Microsoft](https://learn.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)

