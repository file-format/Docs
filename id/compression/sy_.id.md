{
  "date" : "2022-06-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format File SY_ - File SYS Terkompresi",
  "description":"Pelajari tentang format file SY_ dan API yang dapat membuat dan membuka file SY_.",
  "linktitle" : "SY_",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-24"
}

## Apa itu file SY_?

File SY_ adalah file .sys terkompresi yang digunakan oleh penginstal perangkat lunak untuk mengurangi ukuran file penginstalan yang dikemas di dalam penginstal. Ini mengurangi ukuran keseluruhan penginstal. File SY_ dapat diperluas menggunakan utilitas baris perintah Microsoft Expand yang memperluas satu atau lebih file terkompresi.

## SY_ Format File - Informasi Lebih Lanjut

File SY_ disimpan ke disk sebagai file biner terkompresi. Namun, format file internal mereka tidak tersedia untuk umum. Utilitas baris perintah Microsoft Expand dapat memperluas file SY_ menggunakan salah satu dari baris perintah berikut.

```
expand [/r] <source> <destination>
expand /r <source> [<destination>]
expand /i <source> [<destination>]
expand /d <source>.cab [/f:<files>]
expand <source>.cab /f:<files> <destination>
```
Saat diperluas, file SY_ dikonversi menjadi file [SYS](https://docs.fileformat.com/system/sys/).

File SY_ mirip dengan file EX_ dan DL_.

## Referensi

* [StuffIt - Oleh Wikipedia](https://en.wikipedia.org/wiki/StuffIt)
* [Microsoft Expand](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/expand)

