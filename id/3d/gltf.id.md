{
  "date" : "2019-12-12",
  "keywords" :[ "GLTF", "file", "extension", "format", "3D", "Khronos Group 3D" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Pelajari tentang file dan API GLTF yang dapat membuat dan membuka file GLTF.",
  "title" :"GLTF - Format File Transmisi GL",
  "linktitle" : "GLTF",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Apa itu file GLTF?

glTF (GL Transmission Format) adalah format file 3D yang menyimpan informasi model 3D dalam format JSON. Penggunaan JSON meminimalkan ukuran aset 3D dan pemrosesan runtime yang diperlukan untuk membongkar dan menggunakan aset tersebut. Itu diadopsi untuk transmisi dan pemuatan adegan dan model 3D yang efisien oleh aplikasi. glTF dikembangkan oleh Kelompok Kerja Format 3D Grup Khronos dan juga disebut sebagai [JPEG](/id/image/jpeg/) 3D oleh pembuatnya.

Format file GLTF menentukan format penerbitan umum yang dapat diperluas untuk alat dan layanan konten 3D yang merampingkan alur kerja penulisan dan memungkinkan penggunaan konten yang dapat dioperasikan di seluruh industri. Tujuan di balik pembuatan format file glTF adalah untuk menentukan format penerbitan umum yang dapat diperluas untuk alat dan layanan konten 3D yang harus merampingkan alur kerja penulisan dan memungkinkan penggunaan konten yang dapat dioperasikan di seluruh industri. Ini meminimalkan pemrosesan runtime oleh aplikasi yang menggunakan WebGL dan API lainnya.

## Sejarah Singkat File GLTF

Spesifikasi pertama untuk format file glTF 1.0 diumumkan pada Oktober 2015. Ini merupakan rangkaian upaya yang dimulai pada Maret 2012 oleh Khronos. Tujuan dari upaya ini adalah untuk menilai peluang seputar traksi WebGL. Hasilnya, demo pertama format glTF, berdasarkan format JSON dipresentasikan pada pertemuan WebGl pada tahun 2012. Format tersebut diadopsi oleh beberapa perusahaan dari waktu ke waktu termasuk Cesium, 3D Tiles, Oculus, Microsoft, Archilogic, dan lainnya.

glTF 2.0 diterbitkan pada 5 Juni 2017 di Web3D 2017 Conference. Ada daftar panjang perusahaan yang mengadopsi format file glTF setelah itu.

## Format File GLTF

Spesifikasi format file untuk glTF 2.0 tersedia [online](https://github.com/KhronosGroup/glTF/tree/main/specification/2.0) untuk referensi dan harus dikonsultasikan dalam implementasi apa pun yang terkait dengan membaca/menulis untuk dukungan format file glTF.

glTF mendefinisikan aset sebagai file JSON dengan data eksternal pendukung. Ini mewakili model 3D dengan bantuan:

* Deskripsi adegan lengkap terdapat dalam file .glTF berformat JSON yang mencakup informasi tentang hierarki node, material, kamera, serta informasi deskriptor untuk jerat, animasi, dan konstruksi lainnya
* File biner (.bin) yang berisi data geometri dan animasi, dan data berbasis buffer lainnya
* File gambar ([.jpg](/id/image/jpeg/), [.png](/id/image/png/)) untuk tekstur

Aset eksternal apa pun seperti gambar disimpan dalam file eksternal yang direferensikan melalui URI. URI ini disimpan di samping wadah GLB atau disematkan langsung ke JSON menggunakan URI data. Setiap glTF yang valid harus menentukan versinya.

glTF telah dirancang untuk mencapai ukuran file kecil, pemuatan cepat, representasi adegan 3D lengkap, dan ekstensibilitas. Tujuan desain unik ini adalah alasan utama popularitas format file glTF dalam domain 3D. Berikut ini adalah jenis mime yang didukung oleh format file glTF untuk berbagai jenis file:

* File .gltf menggunakan model/gltf+json
* File .bin menggunakan application/octet-stream
* File tekstur menggunakan tipe gambar/* resmi berdasarkan format gambar tertentu. Untuk kompatibilitas dengan browser web modern, format gambar berikut ini didukung: image/jpeg, image/png.

### Pengkodean JSON

glTF memberlakukan batasan tambahan berikut pada format file JSON

Untuk menyederhanakan implementasi sisi klien, glTF memiliki batasan tambahan pada format dan pengkodean JSON.

1. JSON harus menggunakan enkode UTF-8 tanpa BOM.
1. Semua string yang ditentukan dalam spesifikasi ini (nama properti, enum) hanya menggunakan rangkaian karakter ASCII dan harus ditulis sebagai teks biasa, misalnya, "buffer" alih-alih `"\u0062\u0075\u0066\u0066\u0065\u0072"`.
1. Nama (kunci) dalam objek JSON harus unik, yaitu kunci duplikat tidak diperbolehkan.

### URI

Buffer dan resource Gambar direferensikan melalui URI. Dua jenis URI berikut harus didukung oleh klien.

**Data URI:** Data URI ditentukan oleh RFC 2397 dan digunakan oleh glTF untuk menyematkan resource di JSON.

**Jalur URI Relatif:** atau skema jalur seperti yang didefinisikan oleh RFC 3986, [Bagian 4.2](https://datatracker.ietf.org/doc/html/rfc3986#section-4.2) — tanpa skema, otoritas, atau parameter. Karakter yang dicadangkan harus dikodekan dalam persen, sesuai RFC 3986, [Bagian 2.2](https://datatracker.ietf.org/doc/html/rfc3986#section-2.2).

## Referensi ##

* [Spesifikasi glTF 2.0 - Khronos](https://github.com/KhronosGroup/glTF)
* [Format File glTF - Oleh Wikipedia](https://en.wikipedia.org/wiki/GlTF)

