{
  "date" : "2019-10-11",
  "keywords" :[ "vbproj", "file", "ekstensi", "format file", "File Proyek VB", "Panduan Pemrograman" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VBPROJ",
  "description":"Pelajari tentang format file VBPROJ dan API yang dapat membuat dan membuka file VBPROJ.",
  "linktitle" : "VBPROJ",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## Apa itu file VBPROJ?

File dengan ekstensi .vbproj adalah file proyek Microsoft Visual Basic yang digunakan oleh mesin MSBuild Microsoft untuk membangun proyek dalam solusi Visual Studio. Mirip dengan file [CSPROJ](/id/programming/csproj/) untuk proyek .NET yang ditulis dalam [C#](/id/programming/cs/). Mesin MSBuild membaca informasi yang terkandung dalam grup yang berbeda dari file VBPROJ dan menghasilkan file keluaran. File VBPROJ dapat berisi informasi yang terkait dengan pengidentifikasi global, kelas, dan properti yang menentukan proyek. File VBPROJ dapat dibuka dan diedit menggunakan Microsoft Visual Studio dan editor teks biasa seperti Notepad pada Sistem Operasi Windows dan MacOS.

## Format File VBPROJ - Informasi Lebih Lanjut

File VBPROJ adalah file tekstual yang ditulis dalam format file [XML](/id/web/xml/) berdasarkan [Skema MSBuild XML](https://learn.microsoft.com/en-us/visualstudio/msbuild/msbuild-project-file-schema-reference?view=vs-2019). File VBPROJ berisi informasi dalam bentuk tag XML yang menentukan informasi yang terkait dengan grup pengaturan tertentu. Sangat disarankan untuk membuka dan mengedit file pengaturan ini di Microsoft Visual Studio IDE.

### Elemen VBPROJ

Elemen penyusun file Pengaturan VB adalah seperti yang ditunjukkan pada gambar berikut.

{{< figure src="../vbproj.png" alt="Format File VBPROJ" >}}

Tabel berikut memberikan gambaran singkat tentang unsur-unsur tersebut.

|Elemen|Deskripsi|
---|---|
|Proyek| Elemen root dari setiap file proyek dan dapat menyertakan atribut untuk menentukan titik masuk untuk proses pembangunan selain untuk mengidentifikasi skema XML untuk file proyek|
|Properti dan Ketentuan| Properti terdiri dari pasangan Key-value dan didefinisikan dengan elemen PropertyGroup. Nama elemen properti mewakili kunci properti dan konten elemen menentukan nilai properti.|
|Item dan ItemGroups|Item dalam file proyek adalah input untuk proses pembangunan seperti file-file kode, file konfigurasi, file perintah, dan lainnya yang diperlukan sebagai bagian dari proses pembangunan. Item adalah dan harus didefinisikan dalam elemen ItemGroup.|
|Target dan Tugas| Elemen Tugas mewakili instruksi pembangunan individu (atau tugas). MSBuild menyertakan banyak tugas yang telah ditentukan sebelumnya seperti Salin, CSC, VBC, Exec. Tugas harus selalu dimuat dalam Elemen `Target` yang merupakan kumpulan dari satu atau lebih tugas yang dijalankan secara berurutan, dan file proyek dapat berisi beberapa target.|

## Referensi

* [Memahami File Proyek](https://learn.microsoft.com/en-us/aspnet/web-forms/overview/deployment/web-deployment-in-the-enterprise/understanding-the-project-file)
* [Elemen Skema MSBuild](https://learn.microsoft.com/en-us/visualstudio/msbuild/msbuild-project-file-schema-reference?view=vs-2019)

