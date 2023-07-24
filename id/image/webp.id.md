{
  "date" : "2019-10-11",
  "keywords" :[ "file webp", "format file webp", "apa itu file webp", "file", "contoh webp", "ekstensi file webp", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"WEBP - Format File Gambar Raster Google",
  "description":"Pelajari tentang format file WEBP dan API yang dapat membuat dan membuka file WEBP.",
  "linktitle" : "WEBP",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Apa itu file WEBP?

WebP, diperkenalkan oleh Google, adalah format file gambar web raster modern yang didasarkan pada kompresi lossless dan lossy. Ini memberikan kualitas gambar yang sama sambil sangat mengurangi ukuran gambar. Karena sebagian besar halaman web menggunakan gambar sebagai representasi data yang efektif, penggunaan gambar WebP di halaman web menghasilkan pemuatan halaman web yang lebih cepat. Menurut Google, gambar lossless WebP berukuran 26% lebih kecil dibandingkan dengan [PNG](/id/image/png/), sedangkan gambar lossless WebP berukuran 25-34% lebih kecil daripada gambar [JPEG](/id/image/jpeg/) yang sebanding. Gambar dibandingkan berdasarkan indeks Structural Similarity (SSIM) antara WebP dan format file gambar lainnya. WebP adalah proyek saudara dari format wadah multimedia [WebM](https://en.wikipedia.org/wiki/WebM).

## Ikhtisar Fitur WebP ##

Gambar WebP menggunakan proses kompresi berdasarkan prediksi piksel dari blok di sekitarnya, menghasilkan piksel untuk digunakan berkali-kali dalam satu file. Ini mendukung gambar animasi dan diharapkan mendukung lebih banyak fitur di masa mendatang. Google telah menyediakan kode sumber [online](https://developers.google.com/speed/webp/download) untuk pembuat enkode dan dekodernya agar dapat digunakan jika diperlukan. Gambar WebP menyediakan dukungan untuk:

* **Kompresi lossy:** Kompresi lossy didasarkan pada enkode bingkai kunci [VP8](https://en.wikipedia.org/wiki/VP8). VP8 adalah format kompresi video yang dibuat oleh On2 Technologies sebagai penerus format VP6 dan VP7.
* **Kompresi lossless:** Format kompresi lossless dikembangkan oleh tim WebP.
* **Transparansi:** Saluran alfa 8-bit berguna untuk gambar grafis. Saluran Alpha dapat digunakan bersama dengan RGB lossy, fitur yang saat ini tidak tersedia dengan format lain.
* **Animasi:** Ini mendukung gambar animasi dengan warna asli.
* **Metadata:** Ini mungkin memiliki metadata EXIF dan XMP (digunakan oleh kamera, misalnya).
* **Profil Warna:** Ini mungkin memiliki profil ICC tersemat.

Kompresi Lossy WebP menggunakan pengkodean prediktif untuk menyandikan gambar, metode yang sama digunakan oleh codec video VP8 untuk mengompresi keyframe dalam video. Pengodean prediktif menggunakan nilai di blok tetangga piksel untuk memprediksi nilai di blok, dan kemudian hanya mengkodekan perbedaannya.

Kompresi WebP lossless menggunakan fragmen gambar yang sudah terlihat untuk merekonstruksi piksel baru dengan tepat. Itu juga bisa menggunakan palet lokal jika tidak ditemukan kecocokan yang menarik.

## Format File ##

Format file WebP didasarkan pada format dokumen RIFF (resource interchange file format). Wadah WebP menyediakan dukungan untuk fitur di atas dan di atas daripada hanya berisi satu gambar yang disandikan sebagai bingkai kunci VP8. Elemen dasar dari file RIFF adalah potongan yang terdiri dari:


|Bidang|Deskripsi
---|---|
|Chunk FourCC: 32 bit|ASCII kode empat karakter yang digunakan untuk identifikasi chunk
|Ukuran Potongan: 32 bit (uint32)|Ukuran potongan tidak termasuk bidang ini, pengidentifikasi atau padding potongan
|Muatan Potongan: Ukuran Potongan byte|Muatan data. Jika Ukuran Chunk ganjil, satu padding byte ~-~- yang seharusnya 0 ~-~- ditambahkan
|ChunkHeader ('ABCD')|Digunakan untuk mendeskripsikan FourCC dan Chunk Size dari masing-masing chunk, di mana 'ABCD' adalah FourCC untuk chunk tersebut. Ukuran elemen ini adalah 8 byte.

### Tajuk WebP ###

Header file WebP adalah sebagai berikut:

* RIFF Header - 32 bit mewakili karakter ASCII 'R' 'I' 'F' 'F'
* Ukuran File - 32 bit (uint32) mewakili ukuran file dalam byte mulai dari offset 8. Nilai maksimum bidang ini adalah 2^32 dikurangi 10 byte sehingga ukuran keseluruhan file paling banyak 4GiB dikurangi 2 byte .
* 'WEBP' - 32 bit mewakili karakter ASCII 'W' 'E' 'B' 'P'

### Format Berkas Rugi ###

Gambar WebP menggunakan format file lossy jika gambar didasarkan pada pengkodean lossy dan tidak memerlukan fitur lanjutan/diperpanjang seperti transparansi, animasi, alfa, dll. Gambar lossy lebih kecil dan juga didukung oleh aplikasi yang lebih lama.

File WebP, dalam hal ini, terdiri dari:

* 12 byte header file WebP
* Potongan VP8

[Panduan Dekode dan Format Data VP8](https://tools.ietf.org/html/rfc6386) mengilustrasikan spesifikasi format bitstream VP8.

### Format File Tanpa Rugi ###

Tata letak ini digunakan saat gambar didasarkan pada pengkodean lossless dan tidak memerlukan fitur lanjutan yang disediakan oleh format eksternal. Aplikasi yang lebih lama mungkin tidak dapat membaca file seperti itu.

File WebP, dalam hal ini, terdiri dari:

* 12 byte header file WebP
* Potongan VP8L

## Referensi ##

* [Referensi Pengembang WebP - Oleh Google](https://developers.google.com/speed/webp/)
* [Format File WebP - Oleh Wikipedia](https://en.wikipedia.org/wiki/WebP)

