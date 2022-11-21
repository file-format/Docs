{
  "date" : "2022-02-16",
  "keywords" :[ "file obb", "format file obb", "apa itu file obb", "file", "contoh obb", "ekstensi file obb", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format File OBB - File Blob Biner Buram Android",
  "description":"Pelajari tentang format file OBB dan API yang dapat membuat dan membuka file OBB.",
  "linktitle" : "OBB",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-02-16"
}

## Apa itu file OBB?

File OBB adalah file perluasan yang berisi data tambahan selain file Android [APK](/id/compression/apk/). Google Play store tidak mengizinkan untuk memiliki file Android APK dengan ukuran lebih dari 100 MB. Tetapi beberapa aplikasi mungkin memerlukan grafik definisi tinggi, file media, atau aset besar lainnya untuk dihosting selain file APK. Di situlah jenis file OBB masuk. Google Play memungkinkan untuk melampirkan file perluasan ini sebagai pelengkap file APK.

## Format File OBB

File OBB disimpan sebagai file biner bersama dengan file APK. Saat APK menyertai file OBB, Google Play menghosting file perluasan di servernya dan tidak ada biaya tambahan yang dibebankan kepada pengembang. File tambahan ini disimpan di penyimpanan bersama perangkat di kartu SD atau partisi yang dapat dipasang di USB saat aplikasi diunduh untuk penginstalan.

File OBB diunduh dan diinstal saat mengunduh. Namun dalam beberapa kasus, ini diunduh untuk penginstalan saat aplikasi dijalankan untuk pertama kali.

### Ukuran File Maksimum OBB

Google Play Store memungkinkan Anda mengunggah file perluasan OBB dengan ukuran hingga 2 GB. File berukuran besar disarankan untuk diunggah sebagai file [ZIP](/id/compression/zip/) terkompresi untuk pengunggahan yang efisien melalui internet.

File perluasan ini dapat dihosting sebagai file perluasan utama **utama** untuk sumber daya tambahan yang diperlukan oleh aplikasi atau file perluasan tambalan opsional yang dimaksudkan untuk pembaruan kecil pada file perluasan utama.

## Referensi

* [Pengembang Android - File Perluasan](https://developer.android.com/google/play/expansion-files)

