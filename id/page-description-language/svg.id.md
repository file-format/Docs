{
  "date" : "2020-03-02",
  "keywords" :[ "SVG", "file", "format file", "Bahasa Deskripsi Halaman", "Skalar" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Pelajari tentang format file SVG dan API yang dapat membuat dan membuka file SVG.",
  "title" :"Apa itu file SVG?",
  "linktitle" : "SVG",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2020-03-02"
}

## Apa itu file SVG? ##

File SVG adalah file Grafik Vektor Skalar yang menggunakan format teks berbasis XML untuk menggambarkan tampilan gambar. Kata Scalable mengacu pada fakta bahwa SVG dapat diskalakan ke berbagai ukuran tanpa kehilangan kualitas apa pun. Deskripsi berbasis teks dari file semacam itu membuatnya terlepas dari resolusi. Ini adalah salah satu format yang paling banyak digunakan untuk membangun situs web dan mencetak grafik untuk mencapai skalabilitas. Format tersebut hanya dapat digunakan untuk grafik dua dimensi. File SVG dapat dilihat/dibuka di hampir semua browser modern termasuk Chrome, Internet Explorer, Firefox, dan Safari.

## Sejarah Singkat ##

Spesifikasi SVG tersedia sebagai standar terbuka oleh World Wide Web Consortium (W3C) sejak tahun 1999. Sebelum ini, spesifikasi format file serupa dalam enam format berbeda diajukan ke W3C hingga tahun 1998. Pembaruan diterapkan pada spesifikasi pada tahun 2011 dan versi 1.1 . Pada tahun 2016, SVG 2 diterbitkan sebagai versi yang lebih baru termasuk fitur-fitur selain yang ada di SVG 1.1.

## Spesifikasi Format File ##

Model Objek Dokumen (DOM) SVG meletakkan dasar untuk semua spesifikasi dan antarmuka yang sesuai dengan bagian tertentu dari spesifikasi. Pemirsa SVG harus mengimplementasikan antarmuka DOM SVG sebagaimana ditentukan di seluruh spesifikasi W3C. DOM-nya memperlihatkan beberapa antarmuka untuk tipe dan elemen data yang berbeda.

### Bentuk SVG ###

SVG memiliki beberapa elemen bentuk standar yang dapat digunakan oleh pengembang:

* Persegi panjang<rect>
* Lingkaran<circle>
* Elips<ellipse>
* Garis<line>
* Polilin<polyline>
* Poligon<polygon>
* Jalur<path>

Berdasarkan bentuk dan spesifikasi tersebut, area fungsional SVG adalah sebagai berikut.

**Jalur** - Jalur digunakan untuk merepresentasikan garis besar bentuk sederhana dan gabungan. Pengkodean digunakan untuk menentukan sifat operasi. Misal M digunakan untuk Move To, L digunakan untuk Line To, Z digunakan untuk menutup path dan seterusnya.

**Bentuk Dasar** - Jalur garis lurus dan jalur yang terdiri dari serangkaian segmen garis lurus yang terhubung (polyline), serta poligon tertutup, lingkaran, dan elips dapat digambar. Persegi panjang dan persegi panjang bersudut bulat juga merupakan elemen standar.

**Teks** - Representasi teks dinyatakan sebagai data karakter XML tempat banyak efek visual dapat diterapkan ke teks. Spesifikasi memungkinkan untuk menangani teks dua arah, teks vertikal, dan karakter di sepanjang jalur melengkung.

**Lukisan** - Bentuk dapat diisi dan/atau digarisbawahi dengan warna, gradien, atau pola, yang memungkinkan kemampuan membuatnya buram atau memiliki tingkat transparansi apa pun. Fitur ujung garis seperti mata panah atau simbol yang muncul di simpul poligon diwakili oleh Penanda.

**Warna** - Spesifikasi SVG memungkinkan penerapan warna ke semua elemen SVG yang terlihat, baik secara langsung atau melalui isian, coretan, dan properti lainnya. Pengkodean warna yang berbeda dapat digunakan untuk menentukan seperti hitam atau biru, representasi hex, desimal atau sebagai persentase dari bentuk RGB.

**Gradien dan Pola** - Bentuk dalam file SVG dapat diisi atau dibatasi dengan warna solid, gradien, atau pola berulang.

**Filter Effects** - Ini sebenarnya adalah serangkaian operasi grafik yang diterapkan pada grafik vektor sumber tertentu untuk menghasilkan hasil yang dimodifikasi.

**Interaktivitas** - Pengguna dapat berinteraksi dengan file SVG dengan mengubah fokus, klik mouse, menggulir atau memperbesar gambar. Interaktivitas memungkinkan gambar SVG berinteraksi dengan pengguna dalam berbagai cara seperti yang telah disebutkan sebelumnya.

**Menautkan** - Gambar SVG dapat memiliki hyperlink ke dokumen lain. Ini dicapai melalui XML Linking Language atau XLink. Ini memungkinkan untuk membuat status tampilan tertentu yang digunakan untuk memperbesar/memperkecil area tertentu atau untuk membatasi tampilan ke elemen tertentu.

**Scripting** - Serupa dengan HTML, semua aspek dokumen SVG dapat diakses untuk dimanipulasi menggunakan skrip. Objek DOM SVG menyediakan panduan untuk mencapai ini menggunakan elemen dan atribut SVG. Skrip dilampirkan dalam elemen tag `script` dan dapat dijalankan sebagai respons terhadap peristiwa pointer, keyboard, atau dokumen sesuai kebutuhan.

**Animasi** - Elemen DOM<animate> ,<animateMotion> dan<animateColor> memungkinkan Anda untuk memasukkan animasi untuk konten SVG. Tentu saja, ini tidak dapat dicapai tanpa menggunakan skrip dan pengatur waktu bawaan. Animasi ini dapat terus menerus dan dapat diulang serta diulang sementara pada saat yang sama menanggapi acara pengguna.

**Font** - Teks dalam SVG dapat mereferensikan file font eksternal seperti font sistem. Dengan tidak adanya font seperti itu, teks dalam SVG tidak akan dirender ke output. Hal ini dapat diatasi dengan memasukkan glyph yang diperlukan dalam file seperti font yang kemudian dirender menggunakan<text> elemen.

## Contoh ##
Baris berikut menunjukkan bagaimana Lingkaran direpresentasikan menggunakan skrip SVG.

```
<html>
<body>

<h1>My first SVG</h1>

<svg width#"100" height#"100">
  <circle cx#"50" cy#"50" r#"40" stroke#"green" stroke-width#"4" fill#"yellow" />
</svg>

</body>
</html>
```

Baris kode berikut menunjukkan cara menggunakan<text> blok untuk merender teks ke SVG.

```
<svg height#"30" width#"200">
  <text x#"0" y#"15" fill#"red">I love SVG!</text>
</svg>
```

## Referensi ##

* [Spesifikasi SVG W3C](https://www.w3.org/TR/SVG2/Overview.html)
* [SVG - Wikipedia](https://en.wikipedia.org/wiki/Scalable_Vector_Graphics)

