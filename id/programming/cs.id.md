{
  "date" : "2019-10-11",
  "keywords" :[ "cs", "file", "ekstensi", "format file", "CSharp", "Bahasa Pemrograman" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CS - File Kode CSharp",
  "description":"Pelajari tentang format file CS dan API yang dapat membuat dan membuka file CS.",
  "linktitle" : "CS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## Apa itu file CS?

File dengan ekstensi .cs adalah file kode sumber untuk bahasa pemrograman C#. Diperkenalkan oleh Microsoft untuk digunakan dengan .NET Framework, format file menyediakan bahasa pemrograman tingkat rendah untuk menulis kode yang dikompilasi untuk menghasilkan file hasil akhir dalam bentuk EXE atau DLL. Ini dapat dibuat dan dikompilasi dengan Microsoft Visual Studio. Microsoft Visual Studio Express juga dapat digunakan untuk membuat dan memperbarui file tersebut yang merupakan IDE gratis. File CS digunakan untuk pengembangan aplikasi yang dapat berkisar dari aplikasi desktop sederhana hingga program yang lebih kompleks. Proyek Visual Studio [solusi](/id/programming/sln/) sederhana yang dibuat dengan bahasa C# dapat terdiri dari satu atau lebih file semacam itu. Berkas yang ditandai untuk dimasukkan dalam kompilasi dicantumkan dalam berkas [CSPROJ](/id/programming/csproj/) yang merupakan bagian dari proyek dan memberi tahu kompiler untuk menggunakan berkas yang ditandai.

## Format File CS ##

File CS adalah format file berbasis teks yang dapat dibuka di editor teks apa pun untuk diedit. Namun, saat dibuka di IDE yang didukung dengan penyorotan sintaks yang tepat, kode mudah dibaca dan diatur. File CS sederhana berisi:

* Deklarasi ruang nama - Untuk merujuk ke fungsi tertentu yang ditentukan oleh ruang nama tertentu
* Deklarasi variabel - Untuk mendeklarasikan variabel tingkat kelas untuk implementasi tertentu
* Deklarasi Metode - Untuk mendeklarasikan metode deklarasi untuk fungsionalitas tertentu

### Sintaks ###

* Titik koma digunakan untuk menunjukkan akhir dari suatu pernyataan.
* Tanda kurung kurawal digunakan untuk mengelompokkan pernyataan. Pernyataan umumnya dikelompokkan ke dalam metode (fungsi), metode ke dalam kelas, dan kelas ke dalam ruang nama.
* Variabel diberi tanda sama dengan, tetapi dibandingkan dengan menggunakan dua tanda sama dengan berturut-turut.
* Kurung siku digunakan dengan array, baik untuk mendeklarasikannya maupun untuk mendapatkan nilai pada indeks tertentu di salah satunya.

### Contoh ###

```
using System;

class Program
{
    static void Main()
    {
        Console.WriteLine("Hello, world!");
}
}
```

