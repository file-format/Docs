{
  "date" : "2019-10-11",
  "keywords" :[ "file dng", "format file dng", "apa itu file dng", "file", "contoh dng", "ekstensi file dng", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DNG - Format File Gambar Kamera Digital",
  "description":"Pelajari tentang format file DNG dan API yang dapat membuat dan membuka file DNG.",
  "linktitle" : "DNG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Apa itu file DNG?

DNG adalah format gambar kamera digital yang digunakan untuk penyimpanan file mentah. Ini telah dikembangkan oleh Adobe pada bulan September 2004. Pada dasarnya dikembangkan untuk fotografi digital. DNG adalah ekstensi dari format standar [TIFF](/id/image/tiff/)/EP dan menggunakan metadata secara signifikan. Untuk memanipulasi data mentah dari kamera digital dengan kemudahan fleksibilitas dan kontrol artistik, fotografer memilih file mentah kamera. Format JPEG dan TIFF menyimpan gambar yang diproses oleh kamera, oleh karena itu, tidak banyak ruang untuk perubahan yang tersedia dalam format tersebut.

## Sejarah dan Versi Format File DNG

Hingga saat ini sudah ada 5 versi spesifikasi DNG sejauh ini. Versi 1.0.0.0 diluncurkan pada bulan September 2004 bersamaan dengan dirilisnya "2.3" (ACR dan DNG Converter). Pada Februari 2005 versi 1.1.0.0 diterbitkan. Pada Mei 2008 versi 1.2.0.0 dirilis dan digunakan di "4.4". Versi 1.3.0.0 diterbitkan pada Juni 2009. Versi 1.4.0.0 muncul pada 2012.

## Berformat DNG

Sedangkan file mentah kamera menangkap data yang belum diproses atau diproses rendah langsung dari sensor. Karena mirip dengan negatif film, maka format mentah kamera juga dikenal sebagai "Negatif Digital". Manfaat format mentah adalah peningkatan kontrol artistik bagi pengguna akhir. Pengguna dapat menyesuaikan berbagai rentang parameter sesuai dengan persyaratan seperti white balance, pemetaan nada, pengurangan kebisingan, penajaman, dan sebagainya. Di sisi lain, file mentah kamera harus diproses untuk penggunaan apa pun melalui perangkat lunak apa pun atau melalui konverter.

Karena tidak ada format standar yang tersedia untuk file mentah kamera, hal itu menimbulkan banyak masalah bagi pengguna akhir. Masalah ini telah diatasi oleh Adobe dan menentukan format non-eksklusif untuk file mentah kamera. Formatnya dikenal sebagai Digital Negative atau DNG. DNG dapat digunakan oleh berbagai perangkat keras dan perangkat lunak untuk memproses file mentah. Selain itu, DNG juga dapat digunakan sebagai format perantara untuk menyimpan gambar yang awalnya diambil oleh kamera yang memiliki format mentah miliknya sendiri.

### Spesifikasi Format File DNG

Pada bagian ini kami akan menjelaskan format DNG sebagai perpanjangan dari TIFF 6.0.

* **Ekstensi File**: DNG menggunakan ekstensi “.DNG” atau “.TIF”.
* **Pohon SubIFD**: DNG tidak mendukung rantai SubIFD, sebaliknya DNG merekomendasikan penggunaan pohon SubIFD sebagaimana disebutkan dalam spesifikasi TIFF-EP. Kualitas dan resolusi tertinggi dapat menggunakan NewSubFileType dari 0, sedangkan thumbnail dengan kualitas yang lebih rendah harus menggunakan NewSubFileType sama dengan 1. Meskipun tidak diharuskan, IFD pertama harus memiliki thumbnail dengan kualitas atau resolusi rendah.
* **Urutan Byte**: Urutan byte harus didukung oleh pembaca DNG, juga untuk file dari model kamera tertentu.
* **Masked Pixels**: Sebagian besar sensor kamera menghitung piksel yang disamarkan sepenuhnya di bagian tepi sensor melalui enkode hitam. Piksel ini dapat disertakan atau dipangkas sebelum gambar disimpan dalam format DNG. Jika piksel bertopeng tidak dipangkas, area piksel ini harus disebutkan dalam tag ActiveArea. Informasi yang dikumpulkan dari piksel ini tentang tingkat pengkodean hitam harus digunakan sebelum data mentah disimpan atau dapat disertakan dalam file DNG yang menentukan tingkat hitam.
* **Pixel Rusak**: Sebelum menyimpan data mentah sebagai DNG, piksel yang rusak harus dikecualikan.
* **Metadata**: Metadata dapat disertakan dalam DNG dengan salah satu cara berikut:
** Dengan menggunakan tag metadata TIFF-EP atau EXIF
** Melalui tag metadata IPTC (33723)
** Menggunakan tag metadata XMP (700)
* **Data Hak Milik**: Biasanya vendor menyertakan data hak milik dalam file mentah untuk digunakan oleh pengonversi mereka sendiri. DNG menyimpan data hak milik mereka dalam tag pribadi, IFD pribadi, dan di MakerNote pribadi. Vendor harus menggunakan tag DNGPrivateData dan MakerNoteSafety untuk memastikan aplikasi yang mengedit file DNG menyimpan data kepemilikan ini.

Berikut adalah beberapa batasan penting dan ekstensi tag TIFF.

**BitsPerSample**

8 hingga 32 bit/sampel didukung. Harus ada kedalaman yang sama untuk setiap sampel ketika SamplesPerPixel tidak sama dengan 1. Tetapi jika BitsPerSample tidak sama dengan 8 atau 16 atau 32, maka bit harus dikemas ke dalam byte menggunakan FillOrder default TIFF 1 (big-endian).

**Kompresi**

Dua nilai tag Kompresi didukung:

* Nilai #1: Data tidak terkompresi.
* Nilai #7: Data terkompresi JPEG, baik baseline DCT JPEG, atau kompresi JPEG lossless.

**Interpretasi Fotometrik**

Nilai berikut hanya didukung untuk thumbnail dan pratinjau IFD:

* 1 = HitamIsZero. Diasumsikan berada dalam ruang warna gamma 2.2.
* 2 = RGB. Diasumsikan berada dalam ruang warna sRGB.
* 6 = YCbCr. Digunakan untuk gambar pratinjau yang disandikan JPEG.

Nilai berikut didukung untuk IFD mentah, dan dianggap sebagai ruang warna asli kamera:

* 32803 # CFA (Larik Filter Warna).
* 34892 # LinearRaw.

**Orientasi**

Tag orientasi digunakan untuk browser file sehingga mereka dapat melakukan rotasi tanpa kehilangan file DNG. Pembaca DNG harus mendukung semua kemungkinan orientasi, termasuk orientasi cermin.

## Fitur dalam DNG Versi Terbaru

DNG Versi 1.4 Oktober 2012 memiliki fitur lanjutan berikut.

* Pemotongan Pengguna Default
* Transparansi
* Titik Mengambang (HDR)
* Kompresi Rugi
* Proksi

## Referensi ##

* [Spesifikasi DNG - Oleh Adobe](https://www.kronometric.org/phot/processing/DNG/dng_spec_1.4.0.0.pdf)
* [Negatif Digital - Wikipedia](https://en.wikipedia.org/wiki/Digital_Negative)
* [DNG - Format arsip publik untuk data mentah kamera digital](https://helpx.adobe.com/photoshop/digital-negative.html)

