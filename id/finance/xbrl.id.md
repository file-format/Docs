{
  "date" : "2019-10-11",
  "keywords" :[ "xbrl", "file xbrl", "format file xbrl", "jenis file xbrl", "file", "ketik", "apa itu file xbrl" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XBRL - Format File Pelaporan Bisnis dan Keuangan",
  "description":"Pelajari tentang format file XBRL dan API yang dapat membuat dan membuka file XBRL.",
  "linktitle" : "XBRL",
  "menu" : {
    "docs" : {
      "identifier":"finance-xbrl",
      "parent" : "finance"
}
},
  "lastmod" : "2021-02-25"
}

## Apa itu file XBRL?

File dengan ekstensi .xbrl (eXtensible Business Reporting Language) adalah kerangka kerja global yang tersedia secara gratis untuk bertukar informasi bisnis. Sekarang banyak digunakan sebagai salah satu format standar yang telah menggantikan laporan berbasis kertas yang lebih tua dengan catatan digital yang lebih berguna dan akurat. Pertukaran data menggunakan file XBRL termasuk buku besar, detail keuangan, dan neraca. Ini mendukung tag data yang memungkinkan pemrosesan data dari persiapan hingga tahap analisis informasi bisnis dari semua jenis. File XBRL dapat dibuka menggunakan software seperti Rivet Software Dragon View XBRL Viewer dan API seperti [Aspose.Finance](https://products.aspose.com/finance/).

## Format File XBRL

XBRL adalah standar internasional terbuka untuk pelaporan bisnis digital yang banyak digunakan secara global. Ini adalah bahasa berbasis [XML](/id/web/xml/) yang menggunakan elemen XBRL, yang dikenal sebagai tag, untuk menjelaskan setiap item data bisnis untuk merumuskan data untuk penyortiran dan analisis laporan. Spesifikasi format file XBRL dikembangkan dan diterbitkan oleh XBRL International, Inc, dengan [XBRL versi 2.1](https://specifications.xbrl.org/work-product-index-group-base-spec-base-spec.html) saat ini tersedia untuk pengguna.

### Struktur Dokumen XBRL

Informasi lengkap tentang [XBRL 2.1 tag](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31+corrected-errata-2013-02-20.html) dapat dirujuk oleh pemrogram untuk menulis aplikasi untuk mengerjakan format file ini. XBRL terdiri dari instance XBRL, dan kumpulan taksonomi.

**`XBRL Instance`** - Instance XBRL diawali dengan<xbrl> elemen akar. Dokumen XML yang besar dapat berisi lebih dari satu contoh XBRL yang disematkan di dalamnya.

**`Taksonomi XBRL`** - [Taksonomi XBRL](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31+corrected-errata-2013-02-20.html#_5) didefinisikan sebagai struktur skema XML dan kumpulan elemen tautan eksternal yang dirujuk langsung. Skema taksonomi terukur yang menunjukkan referensi linkbase adalah sebagai berikut.

```
<schema
  xmlns:link="http://www.xbrl.org/2003/linkbase"
  xmlns:ci="http://www.mycompany.com/taxonomy/2003-10-19"
  xmlns="http://www.w3.org/2001/XMLSchema" targetNamespace="http://www.mycompany.com/taxonomy/2003-10-19">
<annotation>
<appinfo>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_presentation.xml" xlink:role="http://www.xbrl.org/2003/role/presentationLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_calculation.xml" xlink:role="http://www.xbrl.org/2003/role/calculationLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_definition.xml" xlink:role="http://www.xbrl.org/2003/role/definitionLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_label.xml" xlink:role="http://www.xbrl.org/2003/role/labelLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_reference.xml" xlink:role="http://www.xbrl.org/2003/role/referenceLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
</appinfo>
</annotation>
<import namespace="http://www.xbrl.org/2003/instance" schemaLocation="http://www.xbrl.org/2003/xbrl-instance-2003-12-31.xsd"/>
<!-- ... taxonomy elements declaration starts here ... -->
</schema>
```


## Referensi ##

* [XBRL - Oleh Wikipedia](https://en.wikipedia.org/wiki/XBRL)
* [Extensible Business Reporting Language (XBRL) 2.1](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31+corrected-errata-2013-02-20.html)

