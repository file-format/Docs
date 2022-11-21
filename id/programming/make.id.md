{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Buat File - File Skrip Xcode Makefile",
  "description":"Pelajari tentang XCode MakeFile Format dan API yang dapat membuat dan membuka file MakeFile.",
  "linktitle" : "MAKE",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}


## Apa itu file MAKE?

File MAKE adalah file skrip XCode yang mengatur kompilasi kode. Ini digunakan untuk mengkompilasi dan menautkan program dari berbagai file kode sumber. Bantuan ini memutuskan bagian mana dari aplikasi besar yang perlu dikompilasi ulang saat aplikasi perlu diperbarui. Buat file menggunakan serangkaian instruksi untuk dijalankan tergantung pada file apa yang telah diubah.

## MAKE Contoh Format File

Konten berikut dijalankan menggunakan utilitas Make dan hasilnya adalah sebagai berikut.

```
hello:
	echo "hello world"
```
**Buat Keluaran**

```
$ make
echo "hello world"
hello world
```

## Referensi
* [XCode dan Make - Forum Apple](https://developer.apple.com/forums/thread/657458)
* [Panduan Objek-C](https://blog.teamtreehouse.com/beginners-guide-objective-c-classes-objects)

