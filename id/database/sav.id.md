{
  "date" : "2021-06-14",
  "keywords" :[ "SAV", "extension", "sav file", "sav file format", "Database File Type", "Database File Format", "apa itu file sav" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Pelajari tentang format file SAV dan API yang dapat membuat dan membuka file SAV.",
  "title" :"SAV - Berkas Data SPSS",
  "linktitle" : "SAV",
  "menu" : {
    "docs" : {
      "identifier":"database-sav",
      "parent" : "database"
}
},
  "lastmod" : "2021-06-14"
}

## Apa itu file SAV?
File SAV adalah file data yang dibuat oleh Paket Statistik untuk Ilmu Sosial (SPSS), yang merupakan aplikasi yang banyak digunakan oleh peneliti pasar, peneliti kesehatan, perusahaan survei, pemerintah, peneliti pendidikan, organisasi pemasaran, penambang data untuk analisis statistik. SAV disimpan dalam format biner berpemilik dan terdiri dari kumpulan data serta kamus yang mewakili kumpulan data, menyimpan data dalam baris dan kolom.

## Format File SAV
Format file SAV menjadi relatif stabil, tetapi kami tidak dapat mengatakannya statis. Kompatibilitas mundur dan maju tersedia secara opsional jika diperlukan, tetapi tidak dipertahankan dengan benar. Data dalam file SAV dikategorikan ke dalam bagian berikut:

### Tajuk berkas
Ini terdiri dari 176 byte. 4 byte pertama menunjukkan string **$FL2** atau **$FL3** dalam pengkodean karakter yang digunakan untuk file. Tiga byte terakhir menyatakan bahwa data dalam file dikompresi menggunakan **ZLIB**. String 60-byte berikutnya dimulai **@(#) SPSS DATA FILE** dan juga menentukan sistem operasi dan versi SPSS yang membuat file tersebut. Header kemudian dilanjutkan dengan bidang enam digit, berisi jumlah variabel per pengamatan dan kode digit untuk kompresi, dan diakhiri dengan data karakter yang menunjukkan tanggal dan waktu pembuatan serta label file.
### Catatan deskriptor variabel
Catatan berisi urutan bidang yang tetap, mengklasifikasikan jenis dan nama variabel bersama dengan informasi pemformatan yang digunakan oleh SPSS. Setiap catatan variabel secara opsional dapat berisi label variabel hingga 120 karakter dan hingga tiga spesifikasi nilai yang hilang.
### Label nilai
Label nilai bersifat opsional dan disimpan dalam pasangan record dengan tag bilangan bulat 3 dan 4. Record pertama yaitu tag 3 memiliki urutan pasangan bidang, setiap pasangan berisi nilai dan label nilai terkait. Catatan kedua yaitu tag 4, mewakili variabel mana yang diterapkan pada kumpulan nilai/label.
### Dokumen
Catatan tunggal atau ganda dengan tag bilangan bulat 6. Dokumentasi opsional. berisi baris 80 karakter.
### Data ekstensi
Catatan tunggal atau ganda dengan tag bilangan bulat 7. Catatan ekstensi memberikan informasi yang dapat diabaikan dengan aman, tetapi dipertahankan, dalam banyak situasi, memungkinkan file yang ditulis oleh perangkat lunak yang lebih baru mempertahankan kompatibilitas mundur. Catatan ekstensi memiliki tag subtipe bilangan bulat.
### Terminator kamus
Hanya rekam dengan tag integer 999. Ini memisahkan kamus dari pengamatan data.
### Pengamatan data
Ini dianggap sebagai data dalam urutan observasi, misalnya semua nilai variabel untuk observasi pertama, diikuti oleh semua nilai untuk observasi kedua, dll. Format record data bervariasi tergantung pada kode kompresi dalam record header file. Bagian data dari file .sav dapat dikompresi:
- **kode 0**: dikompresi oleh bytecode
- **kode 1**: dikompresi menggunakan kompresi ZLIB
 







## Referensi ##

* [Keluarga Format File Data Sistem SPSS (.sav)](https://www.loc.gov/preservation/digital/formats/fdd/fdd000469.shtml)

