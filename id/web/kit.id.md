{
  "date" : "2022-07-04",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Pelajari tentang format file KIT dan API yang dapat membuat dan membuka file KIT.",
  "title" :"Format File KIT - File CodeKit",
  "linktitle" : "KIT",
  "menu" : {
    "docs" : {
      "identifier":"web-kit",
      "parent" : "web"
}
},
  "lastmod" : "2022-07-04"
}

## Apa itu file KIT?

File dengan ekstensi .kit adalah file HTML yang dibuat dengan aplikasi bahasa pemrograman [CodeKit](https://codekitapp.com/). Ini berisi `imports` dan `variables` selain file [HTML](/id/web/html/) yang sudah ada, menjadikannya ideal untuk situs statis. CodeKit mengkompilasi file KIT ke HTML yang dapat langsung digunakan sebagai file situs web statis.

## Format File KIT

File KIT adalah file HTML yang juga menyertakan impor dan variabel. Ini disimpan sebagai file teks biasa dan dapat dibuka dengan editor teks atau editor file web apa pun.

### Impor Berkas KIT

Hampir semua jenis file dapat diimpor ke file Kit. Berikut adalah sintaks impor yang digunakan untuk mengimpor file ke dalam file .kit.

```
<!-- @import "someFile.kit" -->
<!-- @import "file.html" -->
```

Ketika impor ditambahkan ke file KIT dan disimpan, itu diganti dengan teks file yang sedang diimpor. Anda juga dapat menggunakan @include daripada @import.

### Beberapa Impor dalam file KIT

Anda juga dapat mengimpor lebih dari satu file sekaligus dengan menggunakan daftar yang dipisahkan koma:

```
<!-- @import someFile, otherFile.html, ../thirdFile.kit -->
```

## Referensi

* [Apa itu Kit?](https://codekitapp.com/help/kit/)

