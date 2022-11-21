{
  "date" : "2021-04-20",
  "keywords": [ "JSPF file", "jspf", "JSPF example", "extension", "format", "jspf tutorial", "jsp fragment", "JSPF file format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JSPF - Format File Fragmen JSP",
  "description":"Pelajari tentang format file JSPF dan API yang dapat membuat dan membuka file JSPF.",
  "linktitle" : "JSPF",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-21"
}

## Apa itu file JSPF?
File dengan ekstensi .jspf disebut fragmen JSP; file statis yang disertakan dalam file JSP lain. File JSPF tidak dikompilasi sendiri, namun dikompilasi di samping halaman yang disertakan. Sintaksnya mirip dengan kode Java Server Pages (JSP). Ini hanya berisi sebuah fragmen dari JSP; tidak termasuk semua seluruh dokumen JSP.

## format file JSPF
Istilah "segmen JSP" digunakan sebagai gantinya karena istilah "fragmen JSP" kelebihan muatan dalam Spesifikasi JSP 2.0. Fragmen JSP dapat menggunakan ekstensi .jsp atau .jspf dan harus ditempatkan di **/WEB-INF/jspf** atau dengan file statis lainnya. Fragmen JSP yang bukan halaman lengkap harus menggunakan ekstensi .jspf dan harus ditempatkan di **/WEB-INF/jspf**

### Organisasi File Fragmen JSP atau JSP
File JSP berisi bagian-bagian berikut dalam urutan yang dicantumkan:

1. Membuka komentar
2. Arahan halaman JSP
3. Direktif pustaka tag opsional
4. Deklarasi JSP opsional
5. Kode HTML dan JSP

File JSP atau JSPF keduanya dimulai dengan komentar gaya sisi server yang disebut **Komentar Pembuka**:

```
<%-- 
  - Author(s):
  - Date:
  - Copyright Notice:
  - @(#)
  - Description: 
  --%>
```
Komentar ini hanya dapat dilihat di sisi server karena dihapus selama rendering halaman JSP.

## Kapan menggunakan file Fragmen JSP?
Ketika halaman JSP memerlukan struktur tertentu namun kompleks yang juga dapat digunakan kembali di halaman JSP lainnya, salah satu cara untuk mengatasinya adalah dengan memecahnya menjadi beberapa bagian, menggunakan pola Tampilan Komposit (bagian Pola dari Cetak Biru Java). Misalnya, halaman JSP terkadang memiliki tata letak logis berikut dalam struktur presentasinya:

{{< figure src="../jspf.png" alt="Format File JSPF" >}}

Dalam situasi ini, halaman JSP komposit ini dapat diubah menjadi berbagai modul, masing-masing akan disebut sebagai fragmen JSP yang terpisah. Fragmen JSP kemudian dapat ditempatkan di lokasi yang sesuai di halaman JSP komposit. Oleh karena itu, file JSPF digunakan saat arahan penyertaan statis digunakan untuk menyertakan halaman yang tidak akan dipanggil dengan sendirinya, file dengan ekstensi .jspf harus ditempatkan di direktori /WEB-INF/jspf/ dari arsip aplikasi Web ( perang).

## Contoh JSPF
```
<%@ include file="/WEB-INF/jspf/header.jspf" %>
...
<%@ include file="/WEB-INF/jspf/menuBar.jspf" %>
...
<jsp:include page="<%= currentBody %>" />
...
<%@ include file="/WEB-INF/jspf/footnote.jspf" %>
...
<%@ include file="/WEB-INF/jspf/footer.jspf" %>
...
```

## Referensi

* [Konvensi Kode untuk Halaman JavaServer](https://www.oracle.com/technical-resources/articles/javase/code-convention.html)

