{
  "date" : "2019-10-11",
  "keywords" :[ "file j2c", "format file j2c", "apa itu file j2c", "file", "contoh j2c", "ekstensi file j2c", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"J2C",
  "description":"Pelajari tentang format file J2C dan API yang dapat membuat dan membuka file J2C.",
  "linktitle" : "J2C",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-02-14"
}

## Apa itu file J2C?

File dengan ekstensi .j2c adalah varian dari format file JPEG dan dikompresi dengan kompresi wavelet. Ini memiliki sistem penanda dan segmen yang hampir identik dengan format file JPEG 2000. Format file J2C sebagaimana didefinisikan dalam Bagian 1 dari dudukan JPEG 2000 yang mendukung kompresi lossy dan lossless. Codestream JPEG 2000 dirancang untuk disematkan dalam [JP2](/id/image/jp2/) atau format file lain, meskipun mungkin muncul dalam file dengan sendirinya. File J2C dapat dibuka menggunakan Adobe Photoshop 2020, Adobe Illustrator 2020, dan Corel Paintshop Pro.

## Format File J2C

Format file J2C sama dengan format JPEG 2000 yang sering disimpan sebagai .jp2 dan .jpc. Ini membuat file J2C mengikuti pendekatan pengkodean metadata yang sama dalam format XML di mana Standar 12234-1 digunakan sebagai referensi antara tag Exif dan komponen XML. Ini lebih ditingkatkan dengan ekstensi JPEG 2000 part-2 yang menggabungkan mekanisme animasi dan konfigurasi aliran kode menjadi satu gambar tunggal. File format file yang diperluas tersebut disimpan sebagai [.jpx](/id/image/jpx/).

### Tata Letak File JPEG2000

JPEG2000 mendukung berbagai aplikasi berdasarkan kesesuaian untuk format file yang dapat diperluas. Meskipun tipe yang paling sederhana dapat berisi satu gambar, tipe yang lebih kompleks dapat menyertakan serangkaian gambar, ditumpuk satu sama lain atau diurutkan berdasarkan waktu.

#### Kotak JP2
Ini adalah blok bangunan tingkat atas dari format file JP2 dan berisi kolom tipe dan panjang di header, dan bagian data. Jenis kotak yang paling terkenal adalah kotak codestream yang bersebelahan. Kotak ini menyimpan codestream JPEG2000 di bagian datanya.

#### Stream Kode JPEG2000

CodeStream JPEG2000 adalah urutan byte yang diperlukan untuk mendekode gambar terkompresi JPEG2000. Jika file tidak memiliki apa pun selain codestream ini, itu disebut file codestream mentah. Biasanya codestream JPEG adalah penerapan algoritma kompresi JPEG2000 pada gambar, meskipun itu bukan satu-satunya cara.

#### Bagian Ubin ####

Gambar yang disandikan JPEG2000 adalah kumpulan unit data yang disebut paket. Paket-paket ini dipertahankan dalam codestream di dalam grup paket yang disebut tile-parts. Sebelum menyandikan gambar, pembuat enkode membagi gambar menjadi kotak blok persegi panjang, yang disebut petak di mana setiap petak dikodekan secara terpisah terlepas dari petak lainnya.

{{< figure src="../JPEG2000_Codestream.png" alt="Format File JPEG2000" >}}

## Kompresi J2C
JPEG 2000 menggunakan teknologi kompresi wavelet membuatnya cepat berdasarkan fakta bahwa relatif sedikit piksel yang ditampilkan di viewport atau jendela apa pun yang ditampilkan oleh penampil gambar. Ini dapat ditekankan oleh fakta bahwa hanya beberapa megabyte piksel yang akan muncul di layar untuk gambar berukuran sangat besar (dalam gigabyte). Ini membantu mengambil dan merender hanya bagian data gambar yang diperlukan untuk mengisi piksel tampilan dengan cepat. Ini juga membutuhkan teknologi dekompresi kecepatan tinggi untuk mempercepat mekanisme pengambilan gambar untuk membuat citra yang diperlukan dengan cepat.

J2C memanfaatkan dekompresi cepat dan hanya mengambil informasi yang diperlukan untuk data piksel guna merender sebagian gambar yang terlihat dengan cepat ke layar. J2C dirancang terutama untuk melihat data dan bukan mengeditnya.

## Identifikasi J2C
File JPEG 2000 memiliki byte tanda tangan `FF 4F FF 51`.

### Jenis Mime
Jenis Mime Terdaftar untuk file JPEG 2000 meliputi:
* gambar/j2c
* gambar/jpx
* gambar/jpm
* video/mj2

## Perbaikan atas standar JPEG
Perbaikan atas standar JPEG meliputi:
* Kinerja kompresi yang unggul
* Beberapa representasi resolusi
* Transmisi progresif dengan piksel dan akurasi resolusi
* Pilihan kompresi lossless atau lossy
* Ketahanan kesalahan, Format file yang fleksibel
* Dukungan rentang dinamis tinggi
* Informasi spasial saluran samping

## Referensi ##
* [Taubman, Daud; Marcellin, Michael (2012)](https://books.google.com/books?id=y7HeBwAAQBAJ&pg=PA402)

