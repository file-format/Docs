{
  "date" : "2022-04-07",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format File HAML - File Kode Sumber Haml",
  "description":"Pelajari tentang format file HAML dan API yang dapat membuat dan membuka file HAML.",
  "linktitle" : "HAML",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-07"
}

## Apa itu file HAML?

File HAML adalah file bahasa markup abstraksi HTML yang berisi kode sumber yang ditulis dalam bahasa [Haml](https://haml.info/). Ini dapat digunakan sebagai pengganti ERB (skrip templat Ruby). File HAML berisi kode sumber template yang untuk menghasilkan HTML dari dokumen web. File ERB dapat diganti hanya dengan mengganti file-file ini di folder app/views ke Haml dengan mengubah ekstensi file. File HAML dapat dibuka dengan editor teks apa saja seperti Microsoft Notepad, Notepad++, Apple TextEdit,

## Format File HAM

File HAML adalah file sumber yang disimpan ke disk sebagai file teks biasa. Ini berisi kode yang ditulis dalam sintaks HAML. HAML mengganti tag ****<>** dengan tanda **%** untuk membuat kode lebih sederhana dan mudah. File ERB adalah drop-in yang dapat diganti oleh HAML seperti yang ditunjukkan pada contoh sederhana berikut.

```
app/views/account/login.html.erb → app/views/account/login.html.haml
```

### Contoh HAML

Berikut ini adalah contoh Hello World contoh HAML.

```
%p{:class => "sample", :id => "welcome"} Hello, World!
%p.sample#welcome Hello, World!
```
yang merender ke output HTML berikut.

```
<p class="sample" id="welcome">Hello, World!</p>
```

## Referensi

* [HAML - Github](https://github.com/haml/haml)

