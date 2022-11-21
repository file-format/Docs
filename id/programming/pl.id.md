{
  "date" : "2021-07-23",
  "keywords" :[ "PL", "file", "ekstensi", "format", "Perl", "bahasa Perl", "file PL", "pemrograman"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "description":"Pelajari tentang format file PL dan API yang dapat membuat dan membuka file PL.",
  "title" :"File PL - Format File Skrip Perl",
  "linktitle" : "PL",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-07-23"
}

## Apa itu file PL?

File dengan ekstensi .pl adalah file Perl Script yang merupakan bahasa scripting. Ini dikompilasi dan dijalankan menggunakan perangkat lunak Perl Interpreter. File skrip PL berisi baris kode, variabel, dan komentar. Bahasa scripting relatif sulit untuk dilakukan
memahami format file pemrograman lain seperti [PHP](/id/programming/php/). File PL dapat dibuat dan kompatibel dengan Windows, macOS, dan Linux.

## Sejarah Singkat Bahasa Perl Scripting

Bahasa ini pertama kali digunakan pada tahun 1987, jadi file-file ini berasal dari tahun itu. Pada tahun 1989 Perl 2 dirilis. Nantinya telah diupdate dan dimodifikasi hingga versi 5.35, dan versi berikutnya ditargetkan rilis tahun depan.

Di setiap pembaruan, telah ditambahkan alat tentang fungsionalitas, kinerja, dan tampilan bahasa dan file. Ada banyak revisi tentang versi di tahun-tahun ini. Ini awalnya bahasa scripting dasar tetapi sekarang terdiri dari banyak modul lain juga. Awalnya, itu adalah bahasa yang sangat sederhana, tetapi skrip bahasa ini cukup sulit untuk dipahami karena padat.

## Spesifikasi Ekstensi Format File Perl

Ada beberapa properti atau spesifikasi dari file-file pemrograman tersebut, beberapa di antaranya adalah sebagai berikut:

* Kode yang disertakan dalam file-file ini dalam format teks biasa dan digunakan untuk pengembangan skrip
* Scripting server, penguraian teks, dan administrasi server adalah aspek utama yang dicakup oleh skrip bahasa ini
* Banyak program populer yang terkait dengan bahasa ini adalah Active state Active Perl dan Bare Bones BBEdit (kompatibel dengan Mac OS)
* Bahasa ini dianggap sebagai bahasa tingkat tinggi
* Untuk Win32, pengguna mungkin harus menginstal distribusi biner asli dari bahasa tersebut
* Diperlukan beberapa alat skrip untuk dapat dieksekusi di berbagai Kit Sumber Daya Windows
* Visual Studio .NET adalah framework terkenal untuk pengembangan bahasa pemrograman. Alat Status Aktif yang dikenal sebagai Visual Perl digunakan untuk menambahkan Perl ke dalam Visual studio
* Dalam file, baris pertama kode sumber menjelaskan informasi tentang juru bahasa yang digunakan. File PL biasanya dimulai dengan baris **#!/usr/bin/perl** yang memberi tahu komputer Anda untuk menjalankan skrip ini menggunakan juru bahasa Perl yang terpasang di komputer


## Contoh Skrip PL

```
#!/usr/bin/perl
print "Hello, world\n";
```

Ini akan dicetak

```
Hello, World
```

### Komentar baris tunggal ###

```
#!/usr/bin/perl
# This is a single line comment
print "Hello Perl\n";
```

### Komentar multi baris ###

```
#!/usr/bin/perl
=begin comment
This is a multiline comment.
Line 1
Line 2
=cut
print "Hello Perl\n";
```

### Penetapan variabel ###

```
#!/usr/bin/perl
$a = 10;
print "Variable a = $a\n";
```

### Penetapan variabel skalar ###

```
#!/usr/bin/perl
$age = 35; # Assigning an integer
$name = "Tony Stark"; # Assigning a string
$pi = 3.14; # Assigning a floating point
```

### Operasi skalar sederhana ###

```
#!/usr/bin/perl
$constr = "hi" . "perl";# Concatenates two or more strings.
$add = 40 + 10; # addition of two numbers.
$prod = 4 * 51;# multiplication of two numbers.
$connumstr = $constr . $add;# concatenation of string and number.
```

## Referensi ##

- [Python (bahasa pemrograman) - Wikipedia](https://en.wikipedia.org/wiki/Python_(programming_language))

