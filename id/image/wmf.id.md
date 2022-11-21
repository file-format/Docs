{
  "date" : "2019-10-11",
  "keywords" :[ "file wmf", "format file wmf", "apa itu file wmf", "file", "contoh wmf", "ekstensi file wmf", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"WMF - Format Metafile Microsoft Windows",
  "description":"Pelajari tentang format file WMF dan API yang dapat membuat dan membuka file WMF.",
  "linktitle" : "WMF",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Apa itu file WMF?

File dengan ekstensi WMF mewakili Microsoft Windows Metafile (WMF) untuk menyimpan data gambar format vektor dan bitmap. Agar lebih akurat, WMF termasuk dalam kategori format file vektor dari format file Grafik yang tidak bergantung pada perangkat. Antarmuka Perangkat Grafis Windows (GDI) menggunakan fungsi yang disimpan dalam file WMF untuk menampilkan gambar di layar. Versi WMF yang lebih disempurnakan, yang dikenal sebagai Enhanced Meta Files (EMF), diterbitkan kemudian yang membuat formatnya lebih kaya fitur. Secara praktis, WMF mirip dengan SVG.

## Spesifikasi Format File WMF ##

File WMF mengacu pada format file 16-bit pada saat diluncurkan dengan Windows 3.0. Format file terdiri dari serangkaian catatan panjang variabel yang berisi perintah menggambar grafik, definisi objek, dan properti. Karena file WMF didasarkan pada perintah yang diberikan ke GDI untuk menggambar gambar, itu juga dikenal sebagai rekaman digital dari gambar yang dapat diputar ulang untuk mereproduksi gambar tersebut. Spesifikasi lengkap format file WMF tersedia online dan harus dirujuk untuk pengembangan aplikasi agar dapat bekerja dengan file WMF. File WMF disusun menjadi:

* Rekaman Tajuk WMF
* Catatan WMF
* Catatan Akhir File WMF

### Rekaman Header WMF ###

**META_HEADER Record** berisi informasi yang mendefinisikan karakteristik metafile, termasuk:

* Jenis metafile
* Versi metafile
* Ukuran metafile
* Jumlah objek yang ditentukan dalam metafile
* Ukuran rekaman tunggal terbesar di metafile

### Catatan Header yang Dapat Ditempatkan WMF ###

**META_PLACEABLE Record** berisi informasi tambahan terkait gambar, termasuk:

* Persegi panjang pembatas
* Ukuran unit logis, untuk penskalaan
* Sebuah checksum, untuk validasi

### Catatan WMF ###

Catatan WMF memiliki format generik, yang ditentukan dalam dokumen spesifikasi. Setiap catatan WMF berisi informasi berikut:

* Ukuran catatan
* Fungsi rekam
* Parameter, jika ada, untuk fungsi rekam

## Referensi ##

* [[MS-WMF]: Format Metafile Windows](https://msdn.microsoft.com/en-us/library/cc250370.aspx)
* [Windows MetaFile - Wikipedia](https://en.wikipedia.org/wiki/Windows_Metafile)

