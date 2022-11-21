{
  "date" : "2019-10-11",
  "keywords": [ "M file", "M", "extension", "format", "M file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"M - File Kode Sumber Matlab",
  "description":"Pelajari tentang file Kode Sumber Matlab .m dan API yang dapat membuat dan membuka file MF.",
  "linktitle" : "M",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

# M - File Kode Sumber Matlab

## Apa itu file M (Matlab)?

File dengan ekstensi .m adalah file kode sumber yang digunakan oleh Matlab, platform komputasi pemrograman dan numerik yang digunakan untuk analisis, pengembangan algoritme, dan pemodelan simulasi. Seperti format file pemrograman lainnya, file M berisi kode sumber yang mengeksekusi perintah Matlab untuk memplot grafik, menjalankan simulasi, dan operasi matematika lainnya. Satu simulasi Matlab dapat menjangkau beberapa file .m yang dapat mengklasifikasikan aplikasi dalam skrip, kelas, fungsi, atau deklarasi. File Matlab M dapat dibuka dengan editor teks apapun.

## Format File Matlab M - Informasi Lebih Lanjut

File .m Matlab adalah file teks yang berisi kode pemrograman dalam bahasa pemrograman Matlab. Ini dapat dibuka dan diedit di editor teks apa pun, dan disimpan kembali untuk dieksekusi di perangkat lunak Matlab. Matlab sendiri berisi Live Editor yang digunakan untuk membuat skrip yang merupakan kombinasi dari kode, keluaran, dan teks yang diformat.

### Berkas Fungsi Matlab

Seperti bahasa pemrograman lainnya, Anda dapat membuat file .m yang hanya berisi definisi fungsi yang menjalankan tugas tertentu saja. File semacam itu juga disimpan dengan ekstensi .m dan mengimplementasikan fungsionalitas yang terkait dengan fungsi itu saja.

### Contoh File .M

Berikut ini adalah contoh file fungsi Matlab yang menghitung waktu yang diperlukan untuk suatu benda dijatuhkan dari ketinggian h.

```C++
function t= TimeToGround(h)  
  t=sqrt(h/4.9);
end
```

Untuk memanggil fungsi ini dari editor Matlab atau dari file .m lainnya, kode berikut dapat digunakan.
```C++
TimeToGround(100)
```

## Referensi

* [Matlab - Format File yang Didukung](https://www.mathworks.com/help/matlab/standard-file-formats.html)
* [Menggunakan Matlab](https://www.maths.unsw.edu.au/sites/default/files/MatlabSelfPaced/lesson0/MatlabLesson0_Mfiles.html)

# M - File Implementasi Objective-C

## Apa itu file M (Objective-C)?

File M juga disebut sebagai file implementasi yang berisi kode sumber kelas yang ditulis dalam bahasa Objective-C, bahasa pemrograman yang digunakan untuk menulis aplikasi perangkat lunak untuk OS X dan iOS. Objective-C adalah bahasa pemrograman utama yang digunakan oleh API utama Apple, Cocoa dan Cocoa Touch, untuk platform ini. Aplikasi perangkat lunak tunggal yang dikembangkan dalam bahasa ini dapat berisi banyak file .m, yang berisi penerapan kelas program. Ini dapat dibuka menggunakan Apple XCode, jEdit, dan editor teks umum lainnya.

## Format File Objective-C M - Informasi Lebih Lanjut

File M ditulis dalam format teks biasa menggunakan sintaks pemrograman Objective-C. Setiap metode kelas harus didefinisikan dengan semua kode yang diperlukan dalam file implementasi ini. File M implementasi ini dapat mengimpor satu atau lebih file header .h sesuai kebutuhan. Pernyataan impor memberi tahu kompiler di mana menemukan file header milik file implementasi ini. Pernyataan impor ditulis sebagai berikut.

```C++
#import "network.h"
```

Setiap implementasi file M kemudian dimulai dengan direktif `@implementation`, diikuti dengan nama file kelas implementasi. Ini kemudian diikuti oleh semua implementasi metode yang dideklarasikan dalam file header.

### Contoh Format File M

```C++
UrlConnection.m

#import "UrlConnection.h"

@implementation UrlConnection

(void)connect {
    // In here would be code to attempt a connection to the
    // specified URL, while possibly handling connection errors.
    //
}

 + (BOOL)canHandleRequest:(NSString \*)type
                   forUrl:(NSString \*)url {
    //And in here would be code to see if the given URL passed
    // in is capable of handling the HTTP request type specified
    // by the "type" parameter. It will return YES or NO.
 }

 @end
```

## Referensi
* [Tentang Objective C](https://developer.apple.com/library/archive/documentation/Cocoa/Conceptual/ProgrammingWithObjectiveC/Introduction/Introduction.html#//apple_ref/doc/uid/TP40011210-CH1-SW1)
* [Panduan Objek-C](https://blog.teamtreehouse.com/beginners-guide-objective-c-classes-objects)

