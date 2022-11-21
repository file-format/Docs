{
  "date" : "2019-10-11",
  "keywords" :["xml", "File", "Ekstensi", "Format File", "Ekstensi File", "bahasa markup yang dapat diperluas"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format Berkas XML",
  "description":"Pelajari tentang format file XML dan API yang dapat membuat dan membuka file XML.",
  "linktitle" : "XML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Apa itu file XML?

XML adalah singkatan dari Extensible Markup Language yang mirip dengan **[HTML](/id/web/html/)** tetapi berbeda dalam penggunaan tag untuk mendefinisikan objek. Seluruh ide di balik pembuatan format file XML adalah untuk menyimpan dan mengangkut data tanpa bergantung pada perangkat lunak atau perangkat keras. Popularitasnya karena dapat dibaca oleh manusia dan mesin. Ini memungkinkannya untuk membuat protokol data umum dalam bentuk objek untuk disimpan dan dibagikan melalui jaringan seperti World Wide Web (WWW). "X" dalam XML adalah untuk dapat diperluas yang menyiratkan bahwa bahasa dapat diperluas ke sejumlah simbol sesuai kebutuhan pengguna. Untuk fitur inilah banyak format file standar memanfaatkannya seperti Microsoft Open XML, LibreOffice OpenDocument, **[XHTML](/id/web/xhtml/)** dan **[SVG](/id/page-description-language /svg/)**.

## Berformat XML

Format file XML didasarkan pada XML Document Object Model (DOM) yang merupakan API pemrograman untuk dokumen HTML dan XML. XML DOM mendefinisikan metode standar untuk mengakses dan memanipulasi elemen dokumen XML. Itu membuat tampilan struktur pohon dari dokumen XML yang dapat digunakan untuk mengakses semua elemen melalui pohon DOM. Elemen yang ada dapat dimodifikasi/dihapus serta elemen baru dapat dibuat di pohon XML. Setiap elemen dokumen XML disebut node. XML DOM seperti yang ditunjukkan pada gambar berikut.

{{< figure src="../XML DOM.png" alt="DOM XML" >}}

### Pendekatan universal XML

Kekuatan XML menjadikannya bahasa universal untuk komunikasi data melalui jaringan dengan membuat transportasi data dan perubahan platform disederhanakan. Ini juga memastikan pertukaran data antara sistem yang tidak kompatibel dimungkinkan dengan menyimpan data dalam format teks biasa. HTML adalah untuk representasi data melalui web, sedangkan XML adalah untuk pertukaran data. Pasangan tag markup yang digunakan di dalam XML menentukan elemen kunci dari struktur yang akan digunakan oleh aplikasi membaca.

## Contoh XML

Berikut adalah contoh katalog CD yang disederhanakan di mana setiap rekaman berisi informasi tentang CD seperti artis, negara, perusahaan, harga, dan tahun produksi.

```
<CATALOG>
  <CD>
    <TITLE>Empire Burlesque</TITLE>
    <ARTIST>Bob Dylan</ARTIST>
    <COUNTRY>USA</COUNTRY>
    <COMPANY>Columbia</COMPANY>
    <PRICE>10.90</PRICE>
    <YEAR>1985</YEAR>
  </CD>
  <CD>
    <TITLE>Hide your heart</TITLE>
    <ARTIST>Bonnie Tyler</ARTIST>
    <COUNTRY>UK</COUNTRY>
    <COMPANY>CBS Records</COMPANY>
    <PRICE>9.90</PRICE>
    <YEAR>1988</YEAR>
  </CD>
  <CD>
    <TITLE>Greatest Hits</TITLE>
    <ARTIST>Dolly Parton</ARTIST>
    <COUNTRY>USA</COUNTRY>
    <COMPANY>RCA</COMPANY>
    <PRICE>9.90</PRICE>
    <YEAR>1982</YEAR>
  </CD>
  <CD>
    <TITLE>Still got the blues</TITLE>
    <ARTIST>Gary Moore</ARTIST>
    <COUNTRY>UK</COUNTRY>
    <COMPANY>Virgin records</COMPANY>
    <PRICE>10.20</PRICE>
    <YEAR>1990</YEAR>
  </CD>
  <CD>
    <TITLE>Eros</TITLE>
    <ARTIST>Eros Ramazzotti</ARTIST>
    <COUNTRY>EU</COUNTRY>
    <COMPANY>BMG</COMPANY>
    <PRICE>9.90</PRICE>
    <YEAR>1997</YEAR>
  </CD>
  <CD>
</CATALOG>
```

## Referensi

* [XML - Oleh Wikipedia](https://en.wikipedia.org/wiki/XML)

