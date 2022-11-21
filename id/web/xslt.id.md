{
  "date" : "2021-01-20",
  "keywords" :["xslt", "File", "Extension", "File Format", "File Extension", "Extensible Stylesheet Language"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format Berkas XSLT",
  "description":"Pelajari tentang format file XSLT dan API yang dapat membuat dan membuka file XSLT.",
  "linktitle" : "XSLT",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-01-20"
}

## Apa itu file XSLT?

File dengan ekstensi .xslt adalah file Extensible Stylesheet Language Transformation yang digunakan untuk mengubah dan memberi gaya pada file XML menggunakan instruksi XSL. Format ini digunakan untuk mengubah dokumen XML menjadi format keluaran standar seperti dokumen teks atau halaman web .html. Transformasi ini membuat dokumen baru berdasarkan konten dokumen XML yang ada. XSLT membuatnya secara teoritis mampu melakukan perhitungan arbitrer.

## Format File XSLT

Format file XLST berisi instruksi transformasi dalam format teks biasa yang dapat dilihat di editor teks apa pun. Ada tiga revisi bahasa.

* `XSLT 1.0` - XSLT 1.0 diterbitkan sebagai rekomendasi W3C pada November 1999.
* `XSLT 2.0` - Ini termasuk modifikasi seperti manipulasi String menggunakan ekspresi reguler, fungsi dan operator untuk memanipulasi tanggal, waktu, dan durasi, beberapa dokumen keluaran, pengelompokan, dan sistem tipe yang lebih kaya dan pengecekan tipe yang kuat.
* `XSLT 3.0` - Ini menjadi bagian dari Rekomendasi W3C pada 8 Juni 2017 dan fitur baru utama termasuk transformasi streaming, Paket untuk meningkatkan modularitas lembar gaya besar, peningkatan penanganan kesalahan dinamis dengan, misalnya, instruksi xsl:coba, dan dukungan untuk peta dan larik, memungkinkan XSLT untuk menangani JSON serta XML.

### Contoh XSLT

Contoh berikut diambil dari [w3schools](https://www.w3schools.com/xml/xsl_intro.asp).
```
<?xml version="1.0"?>

<xsl:stylesheet version="1.0"
xmlns:xsl="http://www.w3.org/1999/XSL/Transform">

<xsl:template match="/">
  <html>
  <body>
    <h2>My CD Collection</h2>
    <table border="1">
      <tr bgcolor="#9acd32">
        <th>Title</th>
        <th>Artist</th>
      </tr>
      <xsl:for-each select="catalog/cd">
        <tr>
          <td><xsl:value-of select="title"/></td>
          <td><xsl:value-of select="artist"/></td>
        </tr>
      </xsl:for-each>
    </table>
  </body>
  </html>
</xsl:template>

</xsl:stylesheet>
```
## Referensi ##

* [XSLT - Oleh Wikipedia](https://en.wikipedia.org/wiki/XSLT)
* [Elemen XSLT](https://en.wikipedia.org/wiki/XSLT_elements)

