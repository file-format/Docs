{
  "date" : "2019-10-11",
  "keywords" :[ ".mel", "Bahasa Tertanam Maya", "file", "ekstensi", "format file", "Maya 3D", "Panduan Pemrograman" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MEL - Format File Bahasa Tertanam Maya",
  "description":"Pelajari tentang format file MEL dan API yang dapat membuat dan membuka file MEL.",
  "linktitle" : "MEL",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-03-08"
}

## Apa itu file MEL?

File dengan ekstensi .mel (Maya Embedded Language) adalah bahasa skrip yang digunakan oleh Autodesk Maya untuk membuat antarmuka grafis. Ini memungkinkan Anda mengotomatiskan pembuatan elemen grafis menggunakan skrip yang dapat dieksekusi selain antarmuka grafis Maya. MEL memberdayakan Anda untuk membuat antarmuka grafis tanpa mempelajari pemrograman. Ini dicapai dengan membuat Makro dan tindakan khusus yang mempercepat tugas berulang. Prosedur dan skrip ini memungkinkan Anda membuat pemodelan kustom, animasi, dinamika, dan perenderan tugas. Autodesk Maya 2020 dapat digunakan untuk membuka dan melihat konten file EML.

## Format File MEL - Informasi Lebih Lanjut

[Manual referensi](https://download.autodesk.com/us/maya/2009help/index.html?url=Glossary_M_.mb_file_format.htm,topicNumber=d0e193865) programmer tersedia untuk developer di bagian dokumentasi Maya. MEL didasarkan pada perintah skrip shell, mirip dengan UINX, untuk mencapai sesuatu. Perintah berbasis skrip membuatnya tidak relevan dengan pemrograman konvensional dan berorientasi objek (OOP), sehingga tidak ada penggunaan struktur data, fungsi pemanggilan, atau penggunaan OOP seperti dalam bahasa lain.

Beberapa poin penting tentang MEL adalah sebagai berikut.

`Komentar` - Setiap pernyataan di MEL harus diakhiri dengan titik koma (;), bahkan di akhir blok.

`Mengembalikan Nilai` - Menyatakan ekspresi yang mengembalikan nilai tidak secara otomatis mencetak nilai di MEL. Sebaliknya itu menyebabkan kesalahan.
```
3 + 5;
// Error: 3 + 5; //
// Error: Syntax error //
print(3+5);
8
```
`Perintah untuk Membuat, Mengedit, dan Menghapus` - Perintah yang sama digunakan untuk membuat sesuatu, mengedit sesuatu, atau meminta informasi tentang sesuatu yang sudah ada. Namun, bendera mengontrol apa (buat, edit, atau kueri) yang dilakukan oleh perintah.

```
// Create a sphere named "mySphere" with radius 5
sphere -radius 5 -name "mySphere";
// Edit the radius of mySphere
sphere -edit -radius "mySphere";
// Print the radius of mySphere
sphere -query -radius

```
`Return Value from Function` - Sintaks fungsi secara otomatis mengembalikan nilai. Untuk mendapatkan nilai pengembalian menggunakan sintaks perintah, Anda harus menyertakan perintah dalam tanda kutip balik.

```
$a = getAttr("mySphere.translateX"); // Function syntax
$b = `getAttr mySphere.translateY`; // Command syntax
```

## Referensi

* [MEL](https://download.autodesk.com/us/maya/2009help/index.html?url=Glossary_M_.mb_file_format.htm,topicNumber=d0e193865)

