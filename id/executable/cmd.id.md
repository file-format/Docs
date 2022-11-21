{
  "date" : "2021-07-12",
  "keywords" :[ "file cmd", "apa itu file cmd", "file", "contoh cmd", "ekstensi file cmd", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Pelajari tentang format file CMD dan API yang dapat membuat dan membuka file CMD.",
  "title" :"CMD - Format File Perintah Windows",
  "linktitle" : "CMD",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-07-12"
}

## Apa itu file CMD?
File CMD terdiri dari skrip yang berisi satu atau beberapa perintah dalam bentuk teks biasa yang dijalankan untuk menjalankan berbagai tugas. Ini mirip dengan file [BAT](/id/executable/bat/), yang umumnya juga digunakan untuk menyimpan sekumpulan perintah yang dapat dieksekusi. File CMD banyak digunakan di sistem operasi Microsoft Windows. File-file ini diperkenalkan hampir di tahun 90-an tetapi masih digunakan di sistem operasi Windows terbaru. File-file ini umumnya ditulis untuk menjalankan lebih dari satu perintah secara berurutan.

## format file CMD
CMD adalah format file yang digunakan oleh program yang dapat dieksekusi dengan gaya CP/M. Hal ini umumnya sebanding dengan [COM](/id/executable/com/) di CP/M-80 dan [EXE](/id/executable/exe/) di DOS. File CMD berisi 1 hingga 8 grup kode atau data dan header 128 byte. Setiap grup dapat berukuran hingga 1 mb. File CMD juga dapat berisi informasi relokasi dan Resident System Extensions (RSXs) di versi yang lebih baru. CMD adalah pendatang baru dibandingkan dengan file [BAT](/id/executable/bat/); digunakan untuk MS-DOS sebelum rilis windows Di MS-DOS. Meskipun, Anda masih dapat menyimpan file dengan ekstensi .bat hari ini, banyak orang menggunakan ekstensi .cmd untuk menyimpan skrip yang dapat dieksekusi.

Spesifikasi format ### CMD

Awal header berisi daftar grup yang ada di file beserta tipenya. Setiap jenis dapat digunakan paling banyak satu kali. Jenis-jenis ini adalah:

- Kode
- Data
- Ekstra
- Tumpukan
- Pengguna 1
- Pengguna 2
- Pengguna 3
- Pengguna 4
- Kode Bersama

Demikian juga Program Segment Prefix di DOS, 256 byte pertama dari grup data adalah nol. Mereka akan diisi oleh CP/M-86 dengan halaman nol. Jika tidak ada grup data, maka 256 byte pertama dari grup kode akan digunakan sebagai gantinya.
## Contoh file CMD
Berikut adalah contoh skrip CMD untuk menampilkan informasi sistem.
```
@ECHO OFF

:: This CMD script provides you with your operating system, hardware and network information.

TITLE My System Info

ECHO Please wait... Gathering system information.

ECHO =========================

ECHO OPERATING SYSTEM

systeminfo | findstr /c:"OS Name"

systeminfo | findstr /c:"OS Version"

ECHO =========================

ECHO BIOS

systeminfo | findstr /c:"System Type"

ECHO =========================

ECHO MEMORY

systeminfo | findstr /c:"Total Physical Memory"

ECHO =========================

ECHO CPU

wmic cpu get name

ECHO =========================

ECHO NETWORK ADDRESS

ipconfig | findstr IPv4

ipconfig | findstr IPv6

PAUSE
```



## Referensi

* [Cara Menulis Skrip CMD](https://smallbusiness.chron.com/write-cmd-script-53226.html)
* [file CMD (CP/M) - oleh Wikipedia](https://en.wikipedia.org/wiki/CMD_file_(CP/M))

