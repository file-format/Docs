{
  "date" : "2022-06-20",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Pelajari tentang format file FZP dan API yang dapat membuat dan membuka file FZP.",
  "title" :"Format File FZP - File Deskripsi Bagian Fritzing XML",
  "linktitle" : "FZP",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2022-06-20"
}

## Apa itu file FZP?

File FZP adalah file XML yang dibuat oleh aplikasi desain dan prototipe sirkuit elektronik [Fritzing](https://fritzing.org/). Ini berisi informasi tentang properti bagian, konektor, dan bus dalam format file [XML](/id/web/xml/). File FPZ tidak dapat digunakan secara independen di Fritzing. Sebaliknya, mereka diimpor sebagai bagian dari file arsip FZPZ.

## Format File FZP - Informasi Lebih Lanjut

File FZP adalah file XML yang berisi informasi tentang properti, konektor, dan bus bagian. Selain itu, file FZP juga berisi informasi tentang judul, deskripsi, penulis, dan tanggal penerbitan file FZP. Saat file komponen Fritzing diekspor, aplikasi Fritzing membuat arsip terkompresi [FZPZ](/id/compression/fzpz/) yang berisi file FZP dan empat file [SVG](/id/page-description-language/svg/).

[Spesifikasi format file FZP](https://github.com/fritzing/fzp/blob/master/docs/README.md) tersedia di Github oleh Fritzing.

## Contoh Struktur File FZP

File FZP tipikal memiliki struktur XML berikut.

```
<?xml version="1.0" encoding="UTF-8"?>
<module fritzingVersion="x.y.z" moduleId="mod-id-rev" referenceFile="ref.file">
  <version>x.y.z</version>
  <title>part-name</title>
  <description>some words about the part</description>
  <author>your-name</author>
  <date>yyyy-mm-dd</date>
  <url>http://part.org</url>
  <label>IC</label>
  <tags>...</tags>
  <taxonomy>...</taxonomy>
  <language>...</language>
  <family>...</family>
  <variant>...</variant>
  <properties>...</properties>
  <views>...</views>
  <connectors>...</connectors>
  <buses>...</buses>
</module>
```
## Referensi

* [Spesifikasi Format File FZP](https://github.com/fritzing/fzp/blob/master/docs/README.md)
* [Bagian baru dengan ekstensi fzpz](https://forum.fritzing.org/t/new-parts-with-fzpz-extension/8007/2)

