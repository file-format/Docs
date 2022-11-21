{
  "date" : "2021-04-22",
  "keywords": [ "appx file", "extension", "format","how to open appx file","appx file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"APPX - Apa itu file APPX?",
  "description":"Pelajari tentang format file APPX dan API yang dapat membuat dan membuka file APPX.",
  "linktitle" : "APPX",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-12-16"
}

## Apa itu file APPX?

File APPX adalah format file paket yang dapat didistribusikan yang digunakan untuk distribusi dan pemasangan aplikasi. Itu diperkenalkan dengan Windows 8 untuk dipublikasikan di Microsoft Windows Store. Ini berisi semua file yang diperlukan untuk menginstal aplikasi Windows. Ini termasuk metadata, file, dan informasi kredensial. Format file pengemasan yang lebih modern adalah MSIX yang saat ini lebih umum digunakan dibandingkan dengan APPX.

## Format File APPX - Informasi Lebih Lanjut

File APPX disimpan sebagai file terkompresi dalam format file [ZIP](/id/compression/zip/). Ini menjadikan seluruh paket sebagai file arsip dengan ukuran file yang diperkecil yang mudah diunggah ke Microsoft Store.

## Bagaimana cara melihat file dalam file APPX?

Untuk melihat konten atau file di dalam file APPX, langkah-langkah berikut harus diikuti.

1. Karena file APPX disimpan sebagai file ZIP terkompresi, ganti nama file menjadi ekstensi .zip
1. Gunakan alat dekompresi seperti 7-Zip, WinZip, atau WinRAR untuk mengekstrak file yang terdapat dalam file APPX

## Bagaimana cara membuat file APPX?

Ada dua metode yang dapat digunakan untuk membuat file APPX.

1. Menggunakan MakeApp.exe - [MakeApp.exe](https://docs.microsoft.com/en-us/windows/msix/package/create-app-package-with-makeappx-tool) digunakan untuk membuat keduanya paket aplikasi (.msix atau .appx) dan file bundel paket aplikasi .msixbundle atau .appxbundle). Selain itu, dapat mengekstrak file dari paket aplikasi. MakeApp.exe tersedia dengan Windows 10 SDK dan dapat digunakan dari command prompt.
1. Menggunakan Microsoft Visual Studio - Pengembang biasanya [membuat file APPX](https://docs.microsoft.com/en-us/windows/msix/desktop/vs-package-overview) menggunakan Microsoft Visual Studio. Setelah pengembangan aplikasi selesai dan aplikasi siap dipublikasikan, file paket APPX dapat dibuat dengan menerbitkannya dari dalam Visual Studio.

## Referensi

* [Buat paket atau bundel MSIX dengan MakeAppx.exe](https://docs.microsoft.com/en-us/windows/msix/package/create-app-package-with-makeappx-tool)
* [Buat file APPX menggunakan Microsoft Visual Studio](https://docs.microsoft.com/en-us/windows/msix/desktop/vs-package-overview)

