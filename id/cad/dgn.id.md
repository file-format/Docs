{
  "date" : "2020-01-12",
  "keywords" :[ "DGN", "File", "Format", "Open", "Read", "API", "MicroStation", "Intergraph Interactive Graphics Design System" ],
  "author" :{
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DGN - Format File Desain CAD MicroStation",
  "description" :"Pelajari tentang format file DGN dan API yang dapat membuat dan membuka file DGN.",
  "linktitle" : "DGN",
  "menu" :{
    "docs" :{
      "parent" : "cad"
}
},
  "lastmod" : "2020-01-12"
}

## Apa itu file DGN?

File dengan ekstensi .dgn (Desain) adalah file gambar yang dibuat oleh dan didukung oleh aplikasi CAD seperti MicroStation dan Intergraph Interactive Graphics Design System. Ini digunakan untuk membuat dan menyimpan desain untuk proyek konstruksi seperti jalan raya, jembatan, dan bangunan. Formatnya mirip dengan format file [DWG](/id/cad/dwg/) Autodesk dan dianggap sebagai pesaingnya. File DNG dapat disimpan sebagai Intergraph Standard File Format atau V8 DGN. DGN dapat dikonversi ke beberapa format lain seperti DWG, [BMP](/id/image/bmp/), [JPEG](/id/image/jpeg/), [PDF](/id/pdf/), [GIF](/id/image/gif/) dan lainnya. Itu dapat dibuka dengan Autodesk AutoCAD, Bentley View dan Bentley Systems MicroStation selain aplikasi perangkat lunak lain seperti versi Corel PaintShop Photo Pro dan IMSI TurboCAD Deluxe.

## Format File DGN V8

File DGN MicroStation V8 terdiri dari satu atau lebih model. Model adalah wadah untuk elemen. V8 DGN menghapus semua batasan berbasis format file yang ada di versi MicroStation sebelumnya. Berikut adalah daftar perbaikan dalam format file DGN.

* Batas jumlah level dalam file DGN telah dihapus, dan setiap level diberi nama dan disimpan sebagai elemen.
* Ukuran fisik maksimum file DGN tidak memiliki batasan apa pun dan hanya dibatasi oleh sistem operasi (seperti batas NT adalah 4 GB)
* Ukuran maksimal satu elemen adalah 128 KB.
* Tidak ada batasan ukuran maksimum sel.
* Nama sel dibatasi sekitar 500 karakter.
* Tidak ada batasan jumlah referensi yang dapat dilampirkan ke file DGN.
* Tali garis, bentuk, atau kurva titik dapat memiliki hingga 5.000 simpul.
* Tidak ada batasan jumlah komponen dalam rantai kompleks atau bentuk kompleks.
* Tidak ada batasan jumlah grup grafik dalam file DGN.
* Pagar sejajar dengan tampilan di mana ia ditempatkan.
* Satu baris teks dapat berisi 65.535 karakter.
* Tidak ada batasan ukuran maksimum node teks.
* Tidak ada batasan jumlah node teks dalam file DGN.
* Setiap elemen memiliki pengidentifikasi 64-bit unik yang tidak berubah selama siklus hidup elemen.
* Setiap elemen memiliki stempel waktu yang menunjukkan waktu perubahan terbaru.

## Referensi

* [DNG - Oleh Wikipedia](https://en.wikipedia.org/wiki/DGN)
* [Format File MicroStation V8 DGN](https://web.archive.org/web/20120713013730/http://docs.bentley.com/ko/MicroStation/ustnhelp47.html)

