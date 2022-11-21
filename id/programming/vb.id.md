{
  "date" : "2019-10-11",
  "keywords" :[ "vb", "file", "ekstensi", "format file", "Visual Basic", "Panduan Pemrograman" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VB - File Kode Visual Basic",
  "description":"Pelajari tentang format file VB dan API yang dapat membuat dan membuka file VB.",
  "linktitle" : "VB",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## Apa itu file VB?

File VB adalah file kode sumber yang dibuat dalam bahasa Visual Basic yang dibuat oleh Microsoft untuk pengembangan aplikasi .NET. Bahasa serupa lainnya dengan sintaks berbeda adalah C# yang filenya disimpan dengan ekstensi file [.CS](/id/programming/cs/). Format file menyediakan bahasa pemrograman tingkat rendah untuk menulis kode yang dikompilasi untuk menghasilkan file keluaran akhir dalam bentuk EXE atau DLL. Ini dapat dibuat dan dikompilasi dengan Microsoft Visual Studio. Microsoft Visual Studio Express juga dapat digunakan untuk membuat dan memperbarui file tersebut yang merupakan IDE gratis. Proyek Visual Studio [solusi](/id/programming/sln/) sederhana yang dibuat dengan bahasa VB dapat terdiri dari satu atau lebih file semacam itu. Berkas yang ditandai untuk dimasukkan dalam kompilasi dicantumkan dalam berkas [CSPROJ](/id/programming/csproj/) yang merupakan bagian dari proyek dan memberi tahu kompiler untuk menggunakan berkas yang ditandai.

## Format File VB - Informasi Lebih Lanjut

File VB adalah format file berbasis teks yang dapat dibuka di editor teks apa pun untuk diedit. Namun, saat dibuka di IDE yang didukung dengan penyorotan sintaks yang tepat, kode mudah dibaca dan diatur. File VB sederhana berisi:

* Deklarasi ruang nama - Untuk merujuk ke fungsi tertentu yang ditentukan oleh ruang nama tertentu
* Deklarasi variabel - Untuk mendeklarasikan variabel tingkat kelas untuk implementasi tertentu
* Deklarasi Metode - Untuk mendeklarasikan metode deklarasi untuk fungsionalitas tertentu

## Contoh Format File VB

```
Imports System
Module Module1
   'This program will display Hello World
   Sub Main()
      Console.WriteLine("Hello World")
      Console.ReadKey()
   End Sub
End Module
```



