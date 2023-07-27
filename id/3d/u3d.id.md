{
  "date" : "2019-10-11",
  "keywords" :[ "file u3d", "format file u3d", "apa itu file u3d", "file", "contoh u3d", "ekstensi file u3d", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"U3D - Format Berkas 3D Universal",
  "description":"Pelajari tentang format file U3D dan API yang dapat membuka dan membuat file U3D.",
  "linktitle" : "U3D",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Apa itu file U3D?

**U3D** (Universal 3D) adalah format file terkompresi dan struktur data untuk grafik komputer 3D. Ini berisi informasi model 3D seperti jerat segitiga, pencahayaan, bayangan, data gerak, garis dan titik dengan warna dan struktur. Format ini diterima sebagai standar [ECMA-363](https://www.ecma-international.org/publications-and-standards/standards/ecma-363/) pada Agustus 2005. Dokumen 3D [PDF](/id/pdf/) mendukung U3D penyematan objek dan dapat dilihat di Adobe Reader (versi 7 dan seterusnya).

Format U3D dikembangkan dengan tujuan untuk menetapkan standar universal untuk penyimpanan dan pertukaran data tiga dimensi. Namun, format tersebut menemukan kegunaan utamanya dalam pengkodean untuk PDF 3D daripada digunakan sebagai format pertukaran. Acrobat 3D mengonversi jenis file 3D yang didukung menjadi U3D atau PRC setelah konversi ke PDF.

## Berformat U3D

File U3D dalam format file biner yang menjalani empat edisi seperti yang dijelaskan oleh dokumen referensi [ECMA-363](https://www.ecma-international.org/publications-and-standards/standards/ecma-363/), yang menghasilkan pembaruan spesifikasi dengan setiap edisi. Standar file PDF ISO-32000 menerima U3D sebagai jenis anotasi dan multimedia yang diizinkan.

Edisi pertama U3D difokuskan pada representasi kunci dari properti grafik 3D seperti geometri, warna, tekstur, pencahayaan, tulang, dan animasi berbasis transformasi. Edisi kedua dan ketiga mengoreksi beberapa kesalahan pada edisi pertama, dengan versi ketiga menjadi jenis perangkat lunak industri yang paling umum digunakan. Edisi keempat memberikan definisi untuk primitif tingkat tinggi (permukaan melengkung). [Spesifikasi U3D](https://www.ecma-international.org/publications-and-standards/standards/ecma-363/) tersedia online untuk referensi pengguna di situs web ECMA.

### Tipe Data dalam file U3D

File biner akan berisi jenis berikut: U8, U16, U32, U64, I16, I32, F32, F64, dan String.

* U8 : Bilangan bulat 8 bit yang tidak ditandatangani
* U16 : Bilangan bulat 16 bit yang tidak ditandatangani
* U32 : Bilangan bulat 32 bit yang tidak ditandatangani
* U64 : Bilangan bulat 64 bit yang tidak ditandatangani
* I16 : Bilangan bulat 16 bit bertanda
* F32: Float presisi tunggal IEEE.
* F64: Pelampung presisi ganda IEEE.
* String: String dalam file U3D dimulai dengan bilangan bulat 16-bit yang tidak ditandatangani yang menentukan panjang total karakter dalam string. String selalu diproses sebagai peka huruf besar-kecil.

## Struktur File U3D

File U3D berisi urutan blok. Ada 3 jenis blok berbeda di setiap file U3D.

* File Header Blok
* Blok Deklarasi
* Blok Lanjutan

Loader menentukan akhir dari sebuah blok jika data dalam blok tersebut tidak diperlukan atau jika decoder untuk jenis blok tersebut tidak tersedia.

{{< figure src="../u3d.png" alt="Berformat U3D" >}}

### Blok Header Berkas
Blok header file berisi informasi file yang digunakan oleh yang dimuat untuk menentukan cara membaca file.

Blok Deklarasi ###

Blok deklarasi berisi informasi tentang objek dalam file. Objek dalam blok deklarasi harus didefinisikan.

### Blok Lanjutan

Informasi tambahan untuk objek yang dideklarasikan dalam blok Deklarasi disediakan di blok lanjutan. Setiap Blok Lanjutan harus dikaitkan dengan Blok Deklarasi.


## Referensi ##

* [Format File U3D - Wikipedia](https://en.wikipedia.org/wiki/Universal_3D)
* [Spesifikasi Format File U3D ECMA](https://www.ecma-international.org/publications/standards/Ecma-363.htm)

