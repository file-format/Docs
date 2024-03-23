{
  "date" : "2019-10-11",
  "keywords" :[ "file rtf", "format file rtf", "apa itu file rtf", "file", "contoh rtf", "ekstensi file rtf", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RTF - Format Teks Kaya",
  "description":"Pelajari tentang format file RTF dan API yang dapat membuat dan membuka file RTF.",
  "linktitle" : "RTF",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2019-09-10"
}

## Apa itu file RTF?

Diperkenalkan dan didokumentasikan oleh Microsoft, Rich Text Format (**RTF**) mewakili metode pengkodean teks dan grafik yang diformat untuk digunakan dalam aplikasi. Format ini memfasilitasi pertukaran dokumen lintas platform dengan Produk Microsoft lainnya, sehingga melayani tujuan interoperabilitas. Kemampuan ini menjadikannya standar transfer data antara perangkat lunak pengolah kata dan, karenanya, konten dapat ditransfer dari satu sistem operasi ke sistem operasi lainnya tanpa kehilangan pemformatan dokumen. Spesifikasi format file tersedia oleh Microsoft untuk umum unduh dan dapat dirujuk dari perspektif pengembang.

## Sejarah Singkat Format File RTF ##

Format file RTF telah mengalami beberapa kali revisi sejak dipublikasikan. Versi resminya untuk baca/tulis diterbitkan sebagai bagian dari Microsoft Word 3.0 untuk Macintosh dengan spesifikasi versi 1.0. Versi final dari spesifikasi, 1.9.1 diterbitkan oleh Microsoft pada Maret 2008. Tidak ada lagi penyempurnaan spesifikasi yang dilakukan setelah ini. Saat ini, hampir semua sistem operasi memiliki lebih banyak aplikasi kaya fitur yang telah meminimalkan/menghilangkan penggunaan format file RTF.

## Spesifikasi Format File RTF ##

RTF berfungsi sebagai standar transfer data antara perangkat lunak pengolah kata dan transfer konten dari satu sistem operasi ke sistem operasi lainnya. Ini dicapai dengan menggunakan kata-kata kontrol yang diperkenalkan oleh Microsoft Office Word hingga tahun 2007. File RTF standar terdiri dari ASCII untuk mewakili teks kaya dan dengan karakter non-ASCII yang diubah menjadi nilai kode yang sesuai. Versi Word yang lebih baru dapat membaca file RTF yang dibuat dengan versi sebelumnya, sedangkan versi yang lebih lama mengabaikan kata dan grup kontrol yang tidak mereka pahami.

### Memahami Dasar RTF ###

File RTF menggunakan teks biasa ASCII 7-bit, yang terdiri dari:

* mengontrol kata-kata
* kontrol simbol, dan
* kelompok.

Ini bertindak sebagai blok bangunan untuk representasi data RTF sebagai teks yang dapat dimengerti dan pengkodean karakter.

#### Kata Kontrol ####

Ini mewakili perintah yang diformat khusus yang digunakan untuk menandai karakter untuk ditampilkan dan tidak boleh lebih dari 32 huruf. Kata kontrol didefinisikan oleh:

\<ASCII Letter Sequence> //<//Delimiter//> //

Setiap kata kontrol peka huruf besar-kecil dan dimulai dengan garis miring terbalik. Urutan Huruf ASCII dapat berisi Abjad ASCII (a sampai z dan A sampai Z). Itu<Delimite> menandai akhir nama kata kontrol dan dapat berupa salah satu dari yang berikut:

* Sebuah ruang. Ini hanya berfungsi untuk membatasi kata kontrol dan diabaikan dalam pemrosesan selanjutnya.
* Angka numerik atau tanda minus ASCII, yang menunjukkan bahwa parameter numerik dikaitkan dengan kata kontrol. Urutan digital berikutnya kemudian dibatasi oleh karakter apa pun selain digit ASCII (biasanya kata kontrol lain yang dimulai dengan garis miring terbalik). Parameter dapat berupa angka desimal positif atau negatif. Kisaran nilai untuk angka tersebut secara nominal –32768 hingga 32767, yaitu bilangan bulat 16-bit yang ditandatangani. Sejumlah kecil kata kontrol mengambil nilai dalam rentang‌ −2.147.483.648 hingga 2.147.483.647 (integer bertanda 32-bit). Kata-kata kontrol ini termasuk **\binN**, **\revdttmN//**, **\rsidN** kata kontrol terkait dan beberapa properti gambar seperti **\bliptagN**. Di sini **N** adalah singkatan dari parameter numerik. Pengurai RTF harus mengizinkan hingga 10 digit, secara opsional didahului dengan tanda minus. Jika pembatasnya berupa spasi, maka akan dibuang, artinya, tidak disertakan dalam pemrosesan berikutnya.
* Karakter apa pun selain huruf atau angka. Dalam hal ini, karakter pembatas mengakhiri kata kontrol dan bukan bagian dari kata kontrol. Seperti garis miring terbalik “\”, yang berarti kata kontrol baru atau simbol kontrol mengikuti.

#### Simbol Kontrol ####

Simbol Kontrol mewakili kejadian khusus yang memiliki arti khusus tergantung pada isinya. Ini terdiri dari garis miring terbalik diikuti oleh karakter khusus (karakter non-alfabet) dan tidak memiliki pembatas.

#### Grup ####

Grup dapat terdiri dari teks, kata kontrol, atau simbol kontrol yang diapit tanda kurung (**{ }**). Kurung buka (**{** ) menunjukkan awal grup dan kurung kurawal penutup ( **}**) menunjukkan akhir grup. Setiap grup menentukan teks yang dipengaruhi oleh grup dan atribut berbeda dari teks tersebut.

### Struktur Berkas RTF ###

File RTF memiliki sintaks Standar berikut:

Diperkenalkan dan didokumentasikan oleh Microsoft, Rich Text Format (**RTF**) mewakili metode pengkodean teks dan grafik yang diformat untuk digunakan dalam aplikasi. Format ini memfasilitasi pertukaran dokumen lintas platform dengan Produk Microsoft lainnya, sehingga melayani tujuan interoperabilitas. Kemampuan ini menjadikannya standar transfer data antara perangkat lunak pengolah kata dan, karenanya, konten dapat ditransfer dari satu sistem operasi ke sistem operasi lainnya tanpa kehilangan pemformatan dokumen. Spesifikasi format file tersedia oleh Microsoft untuk umum unduh dan dapat dirujuk dari perspektif pengembang.

#### Tajuk RTF ####

Header RTF memiliki representasi berikut.

|Bidang|Deskripsi
---|---|
|\<header> |**\rtf1\fbidis**? \<character set> \<from> ? \<deffont> \<deflang> \<fonttbl> ? \<filetbl> ? \<colortbl> ? \<stylesheet> ? \<stylerestrictions> ? \<listtables> ? \<revtbl> ? \<rsidtable> ? \<mathprops> ? \<generator> ?

Tabel header harus muncul dalam urutan ini jika ada. File RTF dapat menyertakan grup untuk font, gaya, warna layar, gambar, catatan kaki, komentar (anotasi), header dan footer, informasi ringkasan, bidang, bookmark, properti pemformatan dokumen, bagian, paragraf, dan karakter, matematika, gambar, dan objek. Jika font, file, gaya, warna, tanda revisi, dan grup informasi ringkasan dan properti pemformatan dokumen disertakan dalam file, mereka harus muncul di header RTF, yang mendahului badan RTF. Jika konten grup mana pun tidak digunakan, grup tersebut dapat dihilangkan. Setiap grup yang menggunakan properti yang ditentukan dalam grup lain harus muncul setelah grup yang mendefinisikan properti tersebut. Misalnya, properti warna dan font harus mendahului grup gaya.

#### Versi RTF ####

Dokumen RTF harus dimulai dengan enam karakter berikut:

```
{\rtf1
```
di mana 1 menunjukkan nomor versi RTF.

#### Set karakter ####

Setelah {\rtf1, dokumen harus mendeklarasikan rangkaian karakter yang digunakannya. Cara untuk mendeklarasikan kumpulan karakter adalah dengan salah satu dari perintah berikut:

`\ansi` - Dokumen berada dalam kumpulan karakter ANSI, juga dikenal sebagai Kode Halaman 1252, kumpulan karakter MSWindows biasa.

`\mac` - Dokumen ada dalam kumpulan karakter MacAscii, kumpulan karakter biasa di bawah versi lama (pra-10) dari Mac OS.

`\pc` - Dokumen ada di Halaman Kode DOS 437, set karakter default untuk MS-DOS. Pengetik dengan otot-memori yang baik akan mencatat bahwa ini adalah rangkaian karakter yang masih digunakan untuk menginterpretasikan kode "Alt numerik"—yakni, saat Anda menahan Alt dan mengetik "130" pada keypad numerik, menghasilkan é, karena karakter 130 di CP437 adalah é. Itulah satu-satunya penggunaan yang dilihat CP437 saat ini.

`\pca` - Dokumen ada di Halaman Kode DOS 850, juga dikenal sebagai Halaman Kode Multibahasa MS-DOS.

#### Perintah Font ####

Definisi set Karakter diikuti oleh perintah `\deffN`. Ini mendefinisikan bahwa nomor font N adalah font default untuk dokumen ini. Nomor font N dirujuk dari tabel font. Perintah `\deffN` secara teknis opsional, tetapi harus ada di sisi aman sebagai prolog umum seperti berikut mengambil font 0 sebagai font default.

`{\rtf1\ansi\deff0`

#### Tabel Font ####

Semua font yang dapat digunakan dalam dokumen dicantumkan dalam tabel font di mana setiap font diwakili oleh nomor font. Dokumen harus memiliki tabel font meskipun beberapa program juga akan berfungsi tanpa itu.

Sintaks untuk tabel font adalah {\fonttbl //...deklarasi//...}, di mana setiap deklarasi memiliki sintaks dasar ini:

`{\fnumber\familycommand Fontname;}`

Tabel font dengan empat deklarasi adalah sebagai berikut:

```
{\fonttbl
{\f0\froman Times;}
{\f1\fswiss Arial;}
{\f2\fmodern Courier New;}
}
```

Dalam dokumen dengan tabel font tersebut, `{\f2 stuff}` akan mencetak “stuff” di Courier New. Font tidak dapat digunakan dalam dokumen hingga dicantumkan dalam tabel font.

### Akhir Dokumen ###

Setiap dokumen RTF harus diakhiri dengan }, untuk menutup grup yang dibuka oleh { yang merupakan karakter pertama dalam dokumen. Tidak ada yang bisa mengikuti final }, kecuali mungkin baris baru.

## Referensi ##

* [Format Teks Kaya](https://en.wikipedia.org/wiki/Rich_Text_Format)
