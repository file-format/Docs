
{
  "date" : "2022-02-06",
  "keywords": [ ".apks file", "extension", "format","APK Set Archive", "how to open .apks file","apks file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"File APK - Arsip Kumpulan APK",
  "description":"Pelajari tentang apa itu file APKS?",
  "linktitle" : "APKS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-02-06"
}

## Apa itu file APKS?

File dengan ekstensi .apks adalah file arsip yang merupakan kumpulan file **APK** paket Android. Setiap file APK individual dalam file APKS dihasilkan dengan tetap memperhatikan berbagai aspek perangkat. Ini termasuk arsitektur, bahasa, kepadatan layar, dan fitur perangkat lainnya. File APKS dihasilkan oleh **bundletool**. Ini digunakan untuk membangun Android App Bundle dan mengonversi bundel aplikasi menjadi APK yang berbeda untuk penerapan di perangkat.

## Format File APKS - Informasi Lebih Lanjut

File APKS disimpan sebagai file terkompresi menggunakan format file [ZIP](/id/compression/zip/).

## Bagaimana cara menghasilkan file APKS?

Saat Android App Bundle (AAB) sudah siap, perilakunya di Google Play Store dapat diuji untuk penerapan ke perangkat. File APKS dapat dibuat, untuk tujuan ini, dari file AAB dan diinstal pada perangkat uji menggunakan [bundletool] Android Google (https://developer.android.com/studio/command-line/bundletool). Ini menyediakan alat baris perintah untuk membuat file arsip APKS dari APK menggunakan perintah berikut.

```
bundletool build-apks --bundle=/MyApp/my_app.aab --output=/MyApp/my_app.apks
```

Untuk menerapkan APK ke perangkat, file APKS dapat ditandatangani dengan informasi penandatanganan perangkat sebagai berikut.

```
bundletool build-apks --bundle=/MyApp/my_app.aab --output=/MyApp/my_app.apks
--ks=/MyApp/keystore.jks
--ks-pass=file:/MyApp/keystore.pwd
--ks-key-alias=MyKeyAlias
--key-pass=file:/MyApp/key.pwd
```

## Referensi

* [bundletool - baris perintah](https://developer.android.com/studio/command-line/bundletool)

