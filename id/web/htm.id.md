{
  "date" : "2019-10-11",
  "keywords" :[ "htm", "file htm", "format file htm", "jenis file htm", "file", "ketik", "apa itu file htm" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format File HTM",
  "description" :"Panduan format file Anda untuk mempelajari apa itu file HTM dan API yang dapat membuat dan membukanya.",
  "linktitle" : "HTM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Apa itu file HTM?

File dengan ekstensi **.htm** mewakili Hypertext Markup Language untuk membuat halaman web untuk ditampilkan di browser web seperti Google Chrome, Internet Explorer, Firefox, dan beberapa lainnya. Ini mendefinisikan markup untuk membuat halaman statis untuk dipublikasikan di World Wide Web (WWW) untuk diakses oleh orang lain. Markup ini memberi tahu browser cara menampilkan konten halaman web. Halaman tersebut dapat berisi teks biasa, gambar, hyperlink ke halaman lain, video, dan informasi media lainnya. Saat halaman web diterbitkan, Anda dapat melihat kode markup di belakangnya dengan melihat sumber halamannya. Browser modern memungkinkan untuk memeriksa setiap bagian dari halaman web di mana setiap sub-divisi atau elemen markup di sumber HTM diuraikan.

## Sejarah Singkat HTM

Sejak awal dan peran pertama keluar, spesifikasi HTML telah dipertahankan oleh World Wide Web Consortium (W3C) sejak tahun 1996. Pada tahun 2000, juga menjadi standar internasional (ISO/IEC 15445:2000). Pada tahun 1999, HTML 4.01 diterbitkan. Pada tahun 2004, Kelompok Kerja Teknologi Aplikasi Web Hypertext (WHATWG) mulai mengerjakan versi HTML5 yang menjadi hasil bersama dengan W3C pada tahun 2008. Itu selesai dan distandarisasi pada 28 Oktober 2014.

## Format Berkas HTML

Dokumen HTML 4 terdiri dari tiga bagian:

1. baris yang berisi informasi versi HTML
1. bagian tajuk deklaratif
1. badan, yang berisi konten aktual dokumen. Tubuh dapat diimplementasikan oleh elemen BODY atau elemen FRAMESET untuk memuat tubuh dalam bingkai

Setiap bagian dapat dipimpin atau diikuti oleh spasi putih, baris baru, tab, dan komentar. Contoh dokumen HTML sederhana adalah seperti yang ditunjukkan di bawah ini:

```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN"
   "http://www.w3.org/TR/html4/strict.dtd">
<HTML>
   <HEAD>
      <TITLE>Understanding HTML File Format</TITLE>
   </HEAD>
   <BODY>
      <P>Hello World!
   </BODY>
</HTML>
```

### Informasi Versi

Baris kode pertama,<!DOCTYPE html> , disebut deklarasi doctype dan memberi tahu browser versi HTML halaman mana yang ditulis. Bergantung pada versi HTML, ada sejumlah deklarasi doctype berbeda yang menamai definisi tipe dokumen (DTD) yang digunakan untuk dokumen. Setiap DTD berbeda dari yang lain dalam elemen yang didukungnya dan berbeda sebagai berikut:

* HTML 4.01 Strict - mencakup semua elemen dan atribut yang belum [usang](https://www.w3.org/TR/html401/conform.html#deprecated) atau tidak muncul dalam dokumen bingkai
* HTML 4.01 Transitional - mencakup segala sesuatu dalam DTD yang ketat ditambah elemen dan atribut yang tidak digunakan lagi (sebagian besar menyangkut presentasi visual
* Frameset HTML 4.01 - mencakup semua yang ada di DTD transisi plus bingkai juga

Untuk **HTML5**, informasi versinya seperti yang disebutkan di bawah ini.

```
<!DOCTYPE html>
```

### Informasi Tajuk

Header dokumen HTML dapat menyertakan sejumlah elemen HTML yang tidak dirender oleh browser. Elemen tersebut adalah metadata yang mendeskripsikan informasi tentang halaman atau menyertakan bagian yang digunakan untuk mengambil informasi dari sumber daya eksternal seperti lembar gaya CSS atau file JavaScript. Header halaman diwakili oleh \<head> tag dan diakhiri dengan \</head> menandai.

<html>Untuk mengatur judul halaman, \<title> elemen adalah satu-satunya yang diperlukan dalam tag \<head>. Hal yang sama digunakan oleh mesin pencari untuk mengidentifikasi judul halaman. </html>

### Informasi Tubuh

Ini adalah bagian utama dalam file yang berisi semua konten file yang dirender oleh browser. Badan html dapat berisi markup yang dapat merujuk ke berbagai blok penyusun dalam bentuk tag. Itu dapat berisi beberapa jenis informasi seperti teks, gambar, warna, grafik, dll. Selain itu, elemen audio dan video juga dapat disematkan di badan html untuk dirender oleh browser. Di hadapan aplikasi lembar gaya modern untuk representasi visual, atribut presentasi BODY seperti warna latar belakang, warna tautan, warna teks, dll. Telah ditinggalkan. Dengan demikian, efek yang sama dapat dicapai dengan menggunakan stylesheet seperti yang ditunjukkan di bawah ini:

```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN"
   "http://www.w3.org/TR/html4/strict.dtd">
<HTML>
<HEAD>
 <TITLE>Inline Style Sheets referencing</TITLE>
 <STYLE type#"text/css">
  BODY { background: white; color: black}
  A:link { color: red }
  A:visited { color: maroon }
  A:active { color: fuchsia }
 </STYLE>
</HEAD>
<BODY>
  ... document body...
</BODY>
</HTML>
```

Lembar gaya sebaris mudah disematkan dan untuk aplikasi cepat ke efek visual, lembar gaya eksternal membuatnya lebih nyaman untuk diterapkan sekali dan diakses di banyak tempat.

```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN"
   "http://www.w3.org/TR/html4/strict.dtd">
<HTML>
<HEAD>
 <TITLE>Linking to External style sheets</TITLE>
 <LINK rel#"stylesheet" type#"text/css" href#"smartstyle.css">
</HEAD>
<BODY>
  ... document body...
</BODY>
</HTML>

```

### Elemen HTML

Seperti disebutkan sebelumnya, konten di dalam Badan HTML diwakili oleh tag, juga dikenal sebagai Elemen Html. Setiap tag dapat memiliki informasi tambahan berupa atribut yang ditulis sebagai
```
<tag attribute1#"value1" attribute2#"value2">
```
meskipun tidak perlu memiliki atribut dengan setiap tag. Jika atribut tidak disebutkan, nilai default digunakan di setiap kasus. Berikut adalah beberapa contoh Elemen:

#### Judul

```
<head>
  <title>The Title</title>
</head>
```

#### Judul

```
<h1>Heading level 1</h1>
<h2>Heading level 2</h2>
<h3>Heading level 3</h3>
<h4>Heading level 4</h4>
<h5>Heading level 5</h5>
<h6>Heading level 6</h6>
```

#### Paragraf

```
<p>Paragraph 1</p> <p>Paragraph 2</p>
```

## Referensi

* [Struktur Global dokumen HTML](https://www.w3.org/TR/html401/struct/global.html#h-7.5.4)

