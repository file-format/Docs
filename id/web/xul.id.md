{
  "date" : "2021-05-24",
  "keywords" :["xul", "File", "Ekstensi", "Format File", "Ekstensi File", "Bahasa Antarmuka Pengguna XML"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XUL - File Bahasa Antarmuka Pengguna XML",
  "description":"Pelajari tentang format file XUL dan API yang dapat membuat dan membuka file XUL.",
  "linktitle" : "XUL",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-24"
}

## Apa itu file XUL?

File dengan ekstensi .xul ([XUL](https://wiki.mozilla.org/XUL:Home_Page) singkatan dari XML User Interface Language) adalah file bahasa markup berbasis [XML](/id/web/xml/) untuk membuat antarmuka pengguna. Itu dikembangkan oleh Mozilla untuk pengembang untuk membuat elemen antarmuka pengguna grafis yang mirip dengan bahasa markup lain yang digunakan untuk membuat halaman web. XUL telah banyak digunakan oleh Mozilla di browser Firefox di mana ia menggunakan basis kode Mozilla. Rendering XUL dilakukan dengan menggunakan
[Mesin tokek](https://en.wikipedia.org/wiki/Gecko_(software)). Garpu Firefox seperti Pale Moon, Basilisk, dan Waterfox mempertahankan dukungan untuk add-on XUL. File XUL diidentifikasi dengan tipe MIME: application/vnd.mozilla.xul+xml.

## Format File XUL

File XUL ditulis dalam teks biasa berdasarkan format file XML dan dirender menggunakan mesin Gecko. Tiga bagian utama dari struktur XUL adalah:

* `Konten` - Ini termasuk deklarasi jendela dan elemen antarmuka pengguna yang terkandung di dalamnya.
* `Skin` - Mencakup semua style sheet, gambar, dan file terkait tema lainnya. Penampilan jendela dijelaskan dalam style sheet.
* `Lokal` - Teks yang ditampilkan dalam jendela disimpan secara terpisah dan beberapa kumpulan file bahasa dapat digunakan oleh pengguna.

### Contoh XUL

Contoh berikut membuat tiga tombol yang ditumpuk satu sama lain dalam arah vertikal.

```
<?xml version="1.0"?>
<?xml-stylesheet href="chrome://global/skin/" type="text/css"?>

<window id="vbox example" title="Example 3...."
xmlns="http://www.mozilla.org/keymaster/gatekeeper/there.is.only.xul">
  <layout>
    <button id="yes1" label="Yes"/>
    <button id="no1" label="No"/>
    <button id="maybe1" label="Maybe"/>
  </layout>
</window>
```

## Referensi

* [XUL - Oleh Wikipedia](https://en.wikipedia.org/wiki/XUL)
* [Dokumentasi Arsip XUL - Oleh Mozilla](https://wiki.mozilla.org/XUL:Home_Page)

