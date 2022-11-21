{
  "date" : "2019-12-10",
  "keywords" :[ "CSV", "file", "ekstensi", "format file", "Nilai Terpisah Koma", "Spreadsheet" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Pelajari tentang format file CSV dan API yang dapat membuat dan membuka file CSV.",
  "title" :"Format Berkas CSV",
  "linktitle" : "CSV",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## Apa itu file CSV?

File dengan ekstensi .csv (Comma Separated Values) mewakili file teks biasa yang berisi rekaman data dengan nilai yang dipisahkan koma. Setiap baris dalam file CSV adalah record baru dari kumpulan record yang terdapat dalam file. File semacam itu dihasilkan saat transfer data dimaksudkan dari satu sistem penyimpanan ke sistem penyimpanan lainnya. Karena semua aplikasi dapat mengenali record yang dipisahkan dengan koma, impor file data tersebut ke database dapat dilakukan dengan sangat mudah. Hampir semua aplikasi spreadsheet seperti Microsoft Excel atau OpenOffice Calc dapat mengimpor CSV tanpa banyak usaha. Data yang diimpor dari file tersebut diatur dalam sel spreadsheet untuk direpresentasikan ke pengguna.

## Sejarah Singkat ##

Berikut adalah beberapa fakta singkat tentang asal dan sejarah format file CSV.

* 1972 - Compiler IBM Fortran (level H extended) mendukungnya di bawah OS/360

* 1978 - Input/output yang diarahkan ke daftar didukung oleh FORTRAN 77 yang menggunakan koma dan spasi untuk pembatas

* 2005 - CSV distandarisasi dengan [RFC4180](https://tools.ietf.org/html/rfc4180) sebagai Jenis Konten MIME.

* 2013 - Kekurangan RFC4180 ditangani oleh rekomendasi W3C

* 2015 - W3C membuat draf rekomendasi pertama untuk standar metadata CSV, yang dimulai sebagai rekomendasi pada Desember 2015

## Konversi File CSV ##

File CSV dapat dikonversi ke beberapa format file berbeda menggunakan aplikasi yang dapat membuka file ini. Misalnya, Microsoft Excel dapat mengimpor data dari format file CSV dan menyimpannya ke XLS, [XLSX](/id/spreadsheet/xlsx/), [PDF](/id/pdf/), [TXT](/id/word-processing/txt/) , XML dan format file [HTML](/id/web/html/). Demikian pula, layanan desktop dan online lainnya menyediakan kemampuan untuk mengekspor file CSV ke HTML, ODS, dan [RTF](/id/word-processing/rtf/).

## Format File CSV ##

Format file CSV diketahui ditentukan berdasarkan [RFC4180](https://tools.ietf.org/html/rfc4180). Ini mendefinisikan file apa pun yang sesuai dengan CSV jika:

* Setiap record terletak pada baris terpisah, dibatasi oleh jeda baris (CRLF). Sebagai contoh:
* aaa,bbb,ccc CRLF
* zzz,yyy,xxx CRLF
* Catatan terakhir dalam file mungkin atau mungkin tidak memiliki jeda baris akhir. Sebagai contoh:
* aaa,bbb,ccc CRLF
* zzz,yyy,xxx
* Mungkin ada baris tajuk opsional yang muncul sebagai baris pertama file dengan format yang sama seperti baris rekaman biasa. Header ini akan berisi nama yang sesuai dengan bidang dalam file dan harus berisi jumlah bidang yang sama dengan catatan di file lainnya (ada atau tidaknya baris tajuk harus ditunjukkan melalui parameter "tajuk" opsional dari ini jenis MIME). Sebagai contoh:
* nama_bidang, nama_bidang, nama_bidang CRLF
* aaa,bbb,ccc CRLF
* zzz,yyy,xxx CRLF
* ﻿Di dalam header dan setiap record, mungkin ada satu atau beberapa kolom, dipisahkan dengan koma. Setiap baris harus berisi jumlah bidang yang sama di seluruh file. Spasi dianggap sebagai bagian dari bidang dan tidak boleh diabaikan. Bidang terakhir dalam catatan tidak boleh diikuti dengan koma. Sebagai contoh:
* aaa, bbb, ccc
* Setiap bidang mungkin diapit atau tidak diapit oleh tanda kutip ganda (namun beberapa program, seperti Microsoft Excel, sama sekali tidak menggunakan tanda kutip ganda). Jika bidang tidak diapit dengan tanda kutip ganda, tanda kutip ganda mungkin tidak muncul di dalam bidang. Sebagai contoh:\
* "aaa", "bbb", "ccc" CRLF
* zzz,yyy,xxx
* Bidang yang berisi jeda baris (CRLF), tanda kutip ganda, dan koma harus diapit dengan tanda kutip ganda. Sebagai contoh:
* "aaa", "b CRLF
* bb", "ccc" CRLF
* zzz,yyy,xxx
* Jika tanda kutip ganda digunakan untuk mengapit bidang, maka tanda kutip ganda yang muncul di dalam bidang harus di-escape dengan mengawalinya dengan tanda kutip ganda lainnya. Sebagai contoh:
* "aaa", "b", "bb", "ccc"

Namun, mengingat penggunaan modern, pembatas tidak terbatas pada koma saja dan dapat berupa titik koma, tab, atau spasi juga. Aplikasi seperti Microsoft Excel menyediakan opsi untuk menentukan karakter pembatas untuk mengimpor rekaman dari file CSV.

## Referensi

* [RFC 4180](https://tools.ietf.org/html/rfc4180)
* [RFC 2048](https://tools.ietf.org/html/rfc2048)
* [CSV - Wikipedia](https://en.wikipedia.org/wiki/Comma-separated_values)

