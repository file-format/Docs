{
  "date" : "2021-05-24",
  "keywords" :["zul", "File", "Ekstensi", "Format File", "Ekstensi File", "buka"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ZUL - File Antarmuka Pengguna ZK",
  "description":"Pelajari tentang format file ZUL dan API yang dapat membuat dan membuka file ZUL.",
  "linktitle" : "ZUL",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-24"
}

## Apa itu file ZUL?

File dengan ekstensi .zul adalah file web yang dibuat dengan Bahasa Markup Antarmuka Pengguna (ZUML) dan berisi definisi untuk elemen antarmuka pengguna. Kelas Ajax dan Java mendukung penggunaan ZUML berbasis [XML](/id/web/xml/) untuk mengembangkan file sisi server. Format file ZUL dikembangkan oleh ZK, kerangka kerja UI yang memungkinkan Anda membuat aplikasi web dan seluler tanpa sepengetahuan JavaScript atau AJAX.

## Format File ZUL

File ZUL berbasis XML, terdiri dari berbagai elemen untuk membangun antarmuka pengguna. Loader ZK menggunakan setiap elemen XML untuk membuat komponen. Keseluruhan pemrosesan elemen halaman seperti judul halaman, deskripsi, dll. Dijelaskan oleh setiap instruksi pemrosesan XML dari ZUML.

### Contoh ZUL

Dalam contoh kode ZUML berikut, baris pertama menentukan judul halaman, baris kedua membuat komponen root dengan judul dan batas, dan baris ketiga membuat tombol dengan label dan pendengar acara.

```
<?page title="Super Application"?>
<window title="Super Hello" border="normal">
    <button label="hi" onClick='alert("hi")'/>
```
Skema ZUL dapat diunduh dari http://www.zkoss.org/2005/zul/zul.xsd.
## Referensi

* [ZUL - Oleh ZK](https://www.zkoss.org/wiki/ZK_Getting_Started/Tutorial)
* [Skema ZUL](http://www.zkoss.org/2005/zul/zul.xsd)

