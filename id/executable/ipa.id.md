{
  "date" : "2021-08-30",
  "keywords" :[ "file ipa", "format file ipa", "apa itu file ipa", "file", "contoh ipa", "ekstensi file ipa", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Pelajari tentang format file IPA dan API yang dapat membuat dan membuka file IPA.",
  "title" :"IPA - File Paket Aplikasi iOS",
  "linktitle" : "IPA",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-08-30"
}

## Apa itu file IPA?
File dengan ekstensi .ipa milik iOS dan dikenal sebagai file paket aplikasi. Ini adalah file arsip (dikompres menggunakan kompresi [ZIP](/id/compression/zip/) yang menyimpan aplikasi iOS, tetapi aplikasi tersebut hanya dapat diinstal pada perangkat MacOS berbasis iOS atau ARM, seperti iPad, iPhone, atau iPod Touch. Terutama, iTunes, Apple Configurator 2, atau perangkat lunak pihak ketiga lainnya dapat digunakan untuk menginstal file IPA.

## format file IPA
Pengembang iOS yang sedang mengembangkan aplikasi menggunakan Apple Xcode sangat akrab dengan file IPA karena mereka perlu mengemas aplikasi yang mereka kembangkan sebagai file IPA baik untuk pengujian tujuan penyebaran app store. Meskipun file IPA diketahui diinstal sebagai aplikasi iOS, Anda juga dapat mendekompresnya untuk melihat data aplikasi yang ada. Karena file IPA hanya berisi satu biner untuk arsitektur ARM ponsel dan tidak berisi biner untuk arsitektur x86, Banyak file .ipa tidak dapat diinstal di Simulator iPhone.
### Struktur file .ipa
Contoh berikut menunjukkan struktur IPA:

```
/Payload/
/Payload/Application.app/
/iTunesArtwork
/iTunesArtwork@2x
/iTunesMetadata.plist
/WatchKitSupport/WK
/META-INF
```
Di atas adalah struktur bawaan untuk mengenali iTunes dan App Store. Sesuai struktur ini:
- Direktori Payload berisi semua data aplikasi.
- File iTunes Artwork adalah gambar PNG 512×512 piksel, berisi ikon aplikasi untuk ditampilkan di iTunes dan aplikasi App Store di iPad.
- iTunesMetadata.plist berisi berbagai bit informasi, mulai dari nama dan ID pengembang, informasi hak cipta, pengidentifikasi bundel, nama aplikasi, genre, tanggal rilis, tanggal pembelian, dll.
- Folder META-INF hanya berisi metadata tentang program apa yang digunakan untuk membuat IPA.


## Referensi

* [.ipa - oleh Wikipedia](https://en.wikipedia.org/wiki/.ipa)


