{
  "date" : "2022-02-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format File WSDL - File Bahasa Deskripsi Layanan Web",
  "description":"Pelajari tentang apa itu file WSDL dan API yang dapat membuat dan membuka file WSDL.",
  "linktitle" : "WSDL",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-02-03"
}

## Apa itu file WSDL?

File WSDL adalah file Bahasa Deskripsi Layanan Web yang ditulis dalam bahasa XML untuk mendeskripsikan layanan Web. Ini berisi informasi tentang titik akhir atau antarmuka untuk konektivitas ke dunia luar dalam format yang diterima secara universal. [spesifikasi format file WSDL](https://www.w3.org/TR/2007/REC-wsdl20-20070626/) (dikelola oleh W3C.org) menentukan persyaratan untuk memublikasikan feed data untuk pertukaran data agar memiliki akses aplikasi jarak jauh melalui port dan titik akhir.

## Format File WSDL - Informasi Lebih Lanjut

File WSDL disimpan sebagai file XML yang dapat dibaca manusia dan dapat dibuka di editor teks apa pun untuk melihat kontennya.

## Deskripsi Layanan WSDL

Spesifikasi format file WSDL 2.0 menjelaskan layanan WSDL terdiri dari dua tahap:

- Tahap abstrak
- Tahap beton

Penggunaan kembali deskripsi dan desain perhatian independen diatur oleh layanan Web. Ini dicapai dengan menggunakan beberapa jenis elemen yang berbeda termasuk tipe (definisi tipe data), pesan (data yang dikomunikasikan), operasi (tindakan), dan protokol yang digunakan oleh layanan. Ini semua dikelola pada tingkat abstrak. Pengikatan detail format transportasi dan kabel ditentukan oleh pengikatan, yang mengelompokkan titik akhir bersama-sama untuk mengimplementasikan antarmuka umum.

### Teknologi apa yang dapat digunakan untuk berinteraksi dengan layanan WSDL?

Beberapa teknologi berbeda dapat digunakan untuk berinteraksi dengan layanan WSDL termasuk aplikasi ASP.NET, C/C++, dan Java.

## Contoh WSDL

```
<message name="getTermRequest">
  <part name="term" type="xs:string"/>
</message>

<message name="getTermResponse">
  <part name="value" type="xs:string"/>
</message>

<portType name="glossaryTerms">
  <operation name="getTerm">
    <input message="getTermRequest"/>
    <output message="getTermResponse"/>
  </operation>
</portType>
```

Dalam contoh ini, portType "glossaryTerms" mendefinisikan operasi satu arah yang disebut "setTerm".

## Referensi

* [WSDL XML](https://www.w3schools.com/xml/xml_wsdl.asp)
* [spesifikasi format file WSDL](https://www.w3.org/TR/2007/REC-wsdl20-20070626/)

