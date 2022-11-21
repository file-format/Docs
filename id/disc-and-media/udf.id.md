{
  "date" : "2021-08-17",
  "keywords" :[ "file udf", "format file udf", "apa itu file udf", "file", "contoh udf", "ekstensi file udf", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Pelajari tentang format file UDF dan API yang dapat membuat dan membuka file UDF.",
  "title" :"UDF - File Format Disk Universal",
  "linktitle" : "UDF",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-17"
}

## Apa itu file UDF?
File dengan ekstensi .udf adalah format pencitraan disk yang biasanya digunakan untuk menyimpan file di media optik; dapat digunakan untuk membakar DVD, CD, dan media optik lainnya; menyimpan kumpulan file menggunakan struktur direktori yang ditentukan dalam standar UDF; memungkinkan file untuk dihapus dan dimodifikasi pada disk target bahkan setelah ditulis. Asosiasi Teknologi Penyimpanan Optik menetapkan sistem file UDF sebagai standar untuk membentuk sistem file umum untuk semua media optik seperti untuk media optik yang dapat ditulis ulang dan media hanya baca.

## format file UDF
Format file UDF adalah sistem file netral-vendor terbuka untuk penyimpanan data komputer untuk berbagai media. Ini telah digunakan secara umum untuk DVD dan format cakram optik yang lebih baru. Biasanya, perangkat lunak menguasai sistem file UDF dalam proses batch dan menulisnya ke media optik dalam sekali jalan. Namun, ketika menulis paket ke media yang dapat ditulis ulang, UDF memungkinkan file dibuat, dihapus, dan diubah pada disk serupa dengan sistem file tujuan umum pada media yang dapat dilepas seperti flash drive atau floppy disk.
### Spesifikasi UDF
Standar UDF mendefinisikan tiga variasi sistem file berikut:

- **Plain Build**: Ini adalah format asli yang didukung di semua revisi UDF. Itu diperkenalkan pada versi standar pertama, format ini dapat digunakan pada semua jenis disk yang memungkinkan akses baca atau tulis acak, seperti DVD+RW, hard disk, dan media DVD-RAM.
- **VAT build**: Digunakan khusus untuk menulis ke media sekali tulis. PPN adalah struktur tambahan pada disk yang memungkinkan penulisan paket; yaitu, memetakan kembali blok fisik ketika file atau data lain pada disk diubah atau dihapus. Untuk media sekali tulis, seluruh disk divirtualisasi, menjadikan sifat sekali tulis transparan bagi pengguna; disk dapat diperlakukan dengan cara yang sama seperti memperlakukan disk yang dapat ditulis ulang.
- **Spared (RW) build**: Digunakan khusus untuk menulis ke media yang dapat ditulis ulang. Itu menambahkan Tabel Penghematan ekstra untuk mengelola kesalahan yang pada akhirnya akan terjadi pada bagian disk yang telah ditulis ulang berkali-kali. Tabel ini menyimpan jejak sektor yang usang dan memetakannya kembali ke sektor yang berfungsi. Manajemen kecacatan UDF tidak berlaku untuk sistem yang telah mengimplementasikan bentuk lain dari manajemen kecacatan, seperti Mount Rainier (MRW) untuk cakram optik, atau pengontrol disk untuk hard drive.
 




## Referensi


* [Format Pencitraan Windows - oleh Wikipedia](https://en.wikipedia.org/wiki/Windows_Imaging_Format)


