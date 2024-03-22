{
  "date" : "2022-07-21",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format File HDR - Apa itu file gambar HDR?",
  "description":"Pelajari tentang format file HDR dan API yang dapat membuat dan membuka file HDR.",
  "linktitle" : "HDR",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2022-07-21"
}

## Apa itu file HDR?

File HDR adalah format file gambar raster Rentang Dinamis Tinggi (HDR) untuk menyimpan foto kamera digital. Ini memungkinkan editor foto untuk meningkatkan warna dan kecerahan gambar digital yang memiliki rentang dinamis terbatas. Modifikasi ini dapat meningkatkan kecerahan di sekitar sudut, sehingga menghasilkan gambar yang mendekati alami. File HDR biasanya disimpan sebagai gambar raster 32-bit. Adobe Photoshop dapat membuat dan membuka file HDR.

File HDR juga dikenal sebagai HDRI.

## Format File HDR - Informasi Lebih Lanjut

Format file HDR didasarkan pada format file Radiance Picture (.pic) asli. Data piksel dari file HDR biasanya disimpan tidak terkompresi, tetapi dalam beberapa kasus dikompresi menggunakan sistem pengkodean panjang proses langsung.

### Struktur Berkas HDR

File gambar HDR terdiri dari tiga bagian berikut:

* **Header:** File HDR diidentifikasi dengan byte pertama dalam file gambar yaitu "#?RADIANCE".
* **String Resolusi:** Header diikuti oleh satu baris resolusi yang terdiri dari 4 nilai; label X dan Y masing-masing diikuti dengan nilai integer numerik. Urutan X dan Y menunjukkan rotasi. Kombinasi X dan Y dengan nilai positif dan negatif mencakup semua kemungkinan orientasi dan rotasi gambar.
* **Data Piksel:** Data piksel file HDR tidak dikompresi atau dikompresi menggunakan enkode durasi proses standar.

## API HDR/HDRI Sumber Terbuka

* **[imageinfo](https://github.com/xiaozhuai/imageinfo)** - Pustaka [C++](/id/programming/cpp/) header tunggal super cepat lintas platform untuk mendapatkan ukuran dan format gambar tanpa memuat/decoding.
* **[imgaeinfo-rs](https://github.com/xiaozhuai/imageinfo-rs)** - Rust library untuk mendapatkan ukuran dan format gambar tanpa memuat/decoding. Mendukung [.avif](/id/image/avif/), [.bmp](/id/image/bmp/), [.cur](/id/image/cur/), [.dds](/id/image/dds/), [. gif](/id/image/gif/), hdr (gambar), [heic (heif)](/id/image/heic/), [.icns](/id/image/icns/), [.ico](/id/image/ico/), [.jp2](/id/image/jp2/), [jpeg (jpg)](/id/image/jpeg/), [jpx](/id/image/jpx/), ktx, [png](/id/image/png/), [psd](/id/image/psd/), qoi, tga, tiff (tif), dan webp.
* **[HdrHistogram](https://github.com/HdrHistogram/HdrHistogram)** - Implementasi Java untuk HdrHistogram.

## Referensi

* [HDR Cahaya](http://paulbourke.net/dataformats/pic/)
* [info gambar](https://github.com/xiaozhuai/imageinfo)

