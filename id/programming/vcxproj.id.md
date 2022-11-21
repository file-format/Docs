{
  "date" : "2019-10-11",
  "keywords" :[ "vcxproj", "file", "ekstensi", "format file", "Proyek Visual C++", "Panduan Pemrograman" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VCXPROJ",
  "description":"Pelajari tentang format file VCXPROJ dan API yang dapat membuat dan membuka file VCXPROJ.",
  "linktitle" : "VCXPROJ",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## Apa itu file VCXPROJ?

File dengan ekstensi .vcxproj adalah file proyek Microsoft Visual C++ yang menyimpan informasi proyek [C++](/id/programming/cpp/). Ini berisi informasi yang digunakan oleh sistem proyek MSBuild untuk menyusun dan membangun hasil akhir. VCXPROJ proyek Visual C++ sama dengan [CSPROJ](/id/programming/csproj/) untuk proyek .NET. File VCXPROJ tidak berisi kode apa pun tetapi merujuk ke semua kelas, target, dan properti yang ditentukan untuk proyek untuk membangun proyek. Ini dapat dibuka di editor teks biasa atau sebaiknya di Microsoft Visual Studio IDE.


## Format File VCXPROJ - Informasi Lebih Lanjut

File VCXPROJ adalah file teks yang dibuat dalam format file [XML](/id/web/xml/). Ini dapat dibuka di editor teks apa pun tetapi sangat disarankan untuk menggunakan Microsoft Visual Studio IDE untuk membuka dan mengedit file-file ini. Ini tidak dirancang untuk pengeditan manual. Kesalahan dapat menyebabkan IDE mogok atau berperilaku dengan cara yang tidak terduga.

Isi dari file sampel VCXPROJ adalah sebagai berikut.

```
<Project DefaultTargets="Build" ToolsVersion="4.0" xmlns='http://schemas.microsoft.com/developer/msbuild/2003'>
  <ItemGroup Label="ProjectConfigurations" />
  <PropertyGroup Label="Globals" />
  <Import Project="$(VCTargetsPath)\Microsoft.Cpp.default.props" />
  <PropertyGroup Label="Configuration" />
  <Import Project="$(VCTargetsPath)\Microsoft.Cpp.props" />
  <ImportGroup Label="ExtensionSettings" />
  <ImportGroup Label="PropertySheets" />
  <PropertyGroup Label="UserMacros" />
  <PropertyGroup />
  <ItemDefinitionGroup />
  <ItemGroup />
  <Import Project="$(VCTargetsPath)\Microsoft.Cpp.targets" />
  <ImportGroup Label="ExtensionTargets" />
</Project>
```
### Elemen Berkas VCXPROJ

File VCXPROJ biasa berisi sejumlah elemen seperti yang dapat dilihat pada contoh XML di atas. [Struktur VCXPROJ](https://docs.microsoft.com/en-us/cpp/build/reference/vcxproj-file-structure?view=msvc-160) oleh Microsoft menjelaskan setiap elemen file secara mendetail dan dapat dirujuk dari perspektif pengembang.

#### Elemen Proyek

Ini adalah simpul root dari file VCXPROJ. MSBuild menggunakan elemen ini untuk membaca versi build dan target default untuk kompilasi.

#### Elemen ItemGroup ProjectConfigurations

Ini berisi informasi konfigurasi proyek yang dapat mencakup metode build (Debug atau Rilis), kompilasi 32 atau 64-bit, opsi pengoptimalan, dan lainnya. Informasi dalam grup ini digunakan oleh IDE untuk memuat proyek.

#### Elemen Konfigurasi Proyek

Elemen ProjectConfiguration dalam file VCXPROJ berisi informasi tentang build dan platform tempat proyek dimuat. Namanya harus mengikuti format `$(Configuration)|$(Platform)`.

#### Elemen Grup Properti Global

Bagian ini berisi pengaturan yang memberikan informasi untuk tingkat proyek seperti:

* Panduan Proyek
* RootNamespace
* Jenis Aplikasi atau Revisi Jenis Aplikasi


## Referensi

* [Struktur VCXPROJ - MSDN](https://docs.microsoft.com/en-us/cpp/build/reference/vcxproj-file-structure?view=msvc-160)
* [File Proyek C++](https://docs.microsoft.com/en-us/cpp/build/reference/project-files?view=msvc-160)

