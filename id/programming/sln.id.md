{
  "date" : "2019-10-11",
   "keywords": [ "sln file", "how to run a sln file", "sln", "extension", "format", "What is sln file", "sln file format", "Visual Studio Solution", "Visual Studio solution VS project" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SLN",
  "description":"Pelajari tentang format file SLN dan API yang dapat membuat dan membuka file SLN.",
  "linktitle" : "SLN",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## Apa itu file SLN?
File dengan ekstensi .SLN mewakili file **solusi Visual Studio** yang menyimpan informasi tentang organisasi proyek dalam file solusi. Isi file solusi semacam itu ditulis dalam teks biasa di dalam file dan dapat diamati/diedit dengan membuka file di editor teks apa pun. Informasi yang terkandung dalam file solusi tetap ada dan digunakan untuk memuat informasi yang terkait dengan solusi seperti [projects](/id/programming/csproj/)dan informasi lain yang diperlukan. File proyek yang direferensikan oleh file solusi berisi informasi tambahan untuk memungkinkan lingkungan mengisi hierarki dengan item proyek tersebut. Tidak ada data yang disimpan dalam file .sln, meskipun informasi proyek dapat ditulis ke file .sln jika diperlukan.

## **Riwayat Versi SLN** ##

Versi format solusi telah berevolusi dengan setiap solusi Microsoft Visual Studio seiring berjalannya waktu. Rincian tentang ini adalah sebagai berikut.


|Versi Visual Studio|Versi Format Solusi
---|---|
|2003|8.00
|2005|9.00
|2008|10.00
|2010|11.00
|2013|12.00
|2015|12.00
|2017|12.00

### **Isi File Solusi** ###

File solusi terdiri dari beberapa bagian yang dibaca oleh lingkungan untuk memuat proyek. Contoh isi file .sln adalah seperti yang ditunjukkan di bawah ini.

```
Project("{F184B08F-C81C-45F6-A57F-5ABD9991F28F}") # "Project1", "Project1.vbproj", "{8CDD8387-B905-44A8-B5D5-07BB50E05BEA}"  
EndProject  
Global  
  GlobalSection(SolutionNotes) # postSolution  
  EndGlobalSection  
  GlobalSection(SolutionConfiguration) # preSolution  
       ConfigName.0 # Debug  
       ConfigName.1 # Release  
  EndGlobalSection  
  GlobalSection(ProjectDependencies) # postSolution  
  EndGlobalSection  
  GlobalSection(ProjectConfiguration) # postSolution  
   {8CDD8387-B905-44A8-B5D5-07BB50E05BEA}.Debug.ActiveCfg # Debug|x86  
   {8CDD8387-B905-44A8-B5D5-07BB50E05BEA}.Debug.Build.0 # Debug|x86  
   {8CDD8387-B905-44A8-B5D5-07BB50E05BEA}.Release.ActiveCfg # Release|x86  
   {8CDD8387-B905-44A8-B5D5-07BB50E05BEA}.Release.Build.0 # Release|x86  
  EndGlobalSection  
  GlobalSection(ExtensibilityGlobals) # postSolution  
  EndGlobalSection  
  GlobalSection(ExtensibilityAddIns) # postSolution  
  EndGlobalSection  
EndGlobal
```

### **Deklarasi Proyek** ###

File solusi dapat berisi lebih dari satu deklarasi proyek dan itu juga dari jenis proyek yang berbeda. Misalnya, satu file solusi dapat berisi proyek CSharp dan juga proyek VB.NET. Jenis ini dibedakan dalam solusi menggunakan [Project-Type-GUID](https://www.codeproject.com/Reference/720512/List-of-Visual-Studio-Project-Type-GUIDs). Deklarasi proyek di atas dapat digeneralisasikan sebagai berikut untuk pemahaman yang jelas.

```
Project("{Project-Type-GUID}") # "Project-Name", "Project-Path.extension", "{Project-GUID}"
```

`Project-Type-GUID:` Project-Type-GUID unik untuk berbagai jenis proyek dan digunakan oleh pembaca solusi untuk mengidentifikasi jenis proyek. Dalam hal ini, F184B08F-C81C-45F6-A57F-5ABD9991F28F menunjukkan bahwa ini adalah proyek VB.NET.

`Project GUID:` GUID unik proyek yang membedakannya dari proyek lain dalam solusi. ID unik proyek dalam solusi memungkinkan proyek lain dalam solusi untuk mengaksesnya.

Berdasarkan informasi yang terdapat di bagian proyek dari file .sln, lingkungan memuat setiap file proyek. Proyek itu sendiri kemudian bertanggung jawab untuk mempopulasikan hierarki proyek dan memuat setiap proyek bersarang. Setiap perubahan yang dilakukan pada solusi disimpan kembali ke file solusi setelah menyimpan atau menutup proyek.

## Proyek VS solusi Visual Studio

**Proyek:** Logikanya, saat Anda mulai membuat aplikasi atau perangkat lunak menggunakan Visual Studio, Anda memulai proyek baru. Sebuah proyek berisi semua file yang diperlukan seperti kode sumber, ikon, gambar, file data, dan banyak lagi, yang akan dikompilasi menjadi aplikasi, situs web, atau perpustakaan yang dapat dieksekusi.

**Solusi:** Solusi berisi satu atau beberapa proyek. Jadi solusinya seperti wadah untuk proyek Visual Studio. Logikanya, kita dapat mengatakan seseorang ingin mendapatkan solusi lengkap untuk bisnisnya termasuk situs web, aplikasi desktop, layanan tenang, dan aplikasi seluler.

### **Referensi** ###

* [File Solusi - Oleh MSDN](https://learn.microsoft.com/en-us/visualstudio/extensibility/internals/solution-dot-sln-file?view#vs-2017)
* [GUID Jenis Proyek](https://www.codeproject.com/Reference/720512/List-of-Visual-Studio-Project-Type-GUIDs)

