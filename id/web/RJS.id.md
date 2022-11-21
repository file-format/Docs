{
  "date" : "2021-05-24",
  "keywords" :["rjs", "File", "Ekstensi", "Format File", "Ekstensi File", "RJS", "File Javascript Ruby"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RJS - Berkas Javascript Ruby",
  "description":"Pelajari tentang apa itu format file RJS dan API yang dapat membuat dan membuka file RJS.",
  "linktitle" : "RJS",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-24"
}

## Apa itu file RJS?

File dengan ekstensi .rjs adalah kombinasi kode Ruby dan JavsScript yang memungkinkan pengembang Rails menggunakan Ruby untuk menghasilkan kode JavaScript dinamis. Kode Ruby tertanam dalam fungsi Java dan dikompilasi di server web yang membutuhkan mesin Ruby untuk dapat berjalan di server. RJS mirip dengan [RHTML](/id/web/rhtml/); satu-satunya perbedaan adalah bahwa lateral berisi kode Ruby di [HTML](/id/web/html/) sementara itu berisi kode Ruby di fungsi Javascript.

## Format File RJS

File RJS dikodekan dalam teks biasa seperti skrip atau bahasa pemrograman lainnya. Ketika halaman seperti itu diminta oleh klien, kode Ruby dijalankan di server, dan hanya kode HTML dan Javascript yang dikembalikan ke browser klien. Sintaks file RJS mirip dengan kombinasi sintaks Ruby dan JavaScript sehingga hanya kode Ruby yang tertanam dalam fungsi JavaScript.

### Contoh RJS

Contoh berikut menunjukkan kode Ruby sederhana secara mandiri dan kemudian disematkan dalam fungsi JavaScript.

```Ruby
### Default Ruby Functions

def foo
  "bar"
end
```

```JavaScript
# JS style which looks like JS

foo = -> { return "bar" }
```
dan berikut adalah RubyJS:
```Ruby
# here you go!

foo = -> { "bar" }
```
## Referensi

* [RJS](https://github.com/makevoid/rjs)

