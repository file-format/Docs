{
  "date" : "2022-02-06",
  "keywords" :[ "xsd", ".xsd", "apa itu file xsd", "cara membuka file xsd", "ekstensi", "file", "file xsd", "format file xsd", "ekstensi .xsd" ,"contoh berkas xsd"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Pelajari tentang format file XSD dan API yang dapat membuat dan membuka file XSD.",
  "title" :"Format File XSD - File Definisi Skema XML",
  "linktitle" : "XSD",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-02-06"
}

## Apa itu file Skema XSD?

File XSD adalah file definisi yang menentukan elemen dan atribut yang dapat menjadi bagian dari dokumen XML. Ini memastikan bahwa data diinterpretasikan dengan benar, dan kesalahan ditangkap, menghasilkan validasi XML yang sesuai. File XSD memastikan bahwa data yang dimasukkan mengikuti struktur yang sama seperti yang ditentukan dalam file. File XSD disimpan dalam format file [XML](/id/web/xml/) dan dapat dibuka atau diedit di editor teks apa pun seperti Microsoft Notepad, Notepad++, atau [Microsoft XML Notepad](https://microsoft.github.io /XmlNotepad/).

## Format File XSD

File XSD disimpan ke disk dalam format file teks biasa yang dapat dibaca manusia. XSD mendefinisikan elemen yang dapat digunakan dalam dokumen, terkait dengan data aktual yang akan dikodekan.

## Contoh File XSD

File XSD sederhana yang memiliki skema pesanan pembelian menentukan elemen menggunakan tag seperti yang ditampilkan dalam [contoh XSD oleh Microsoft](https://learn.microsoft.com/en-us/visualstudio/xml-tools/sample-xsd-file-simple-schema?view=vs-2022).

```
<xsd:schema xmlns:xsd="http://www.w3.org/2001/XMLSchema"
           xmlns:tns="http://tempuri.org/PurchaseOrderSchema.xsd"
           targetNamespace="http://tempuri.org/PurchaseOrderSchema.xsd"
           elementFormDefault="qualified">
 <xsd:element name="PurchaseOrder" type="tns:PurchaseOrderType"/>
 <xsd:complexType name="PurchaseOrderType">
  <xsd:sequence>
   <xsd:element name="ShipTo" type="tns:USAddress" maxOccurs="2"/>
   <xsd:element name="BillTo" type="tns:USAddress"/>
  </xsd:sequence>
  <xsd:attribute name="OrderDate" type="xsd:date"/>
 </xsd:complexType>

 <xsd:complexType name="USAddress">
  <xsd:sequence>
   <xsd:element name="name"   type="xsd:string"/>
   <xsd:element name="street" type="xsd:string"/>
   <xsd:element name="city"   type="xsd:string"/>
   <xsd:element name="state"  type="xsd:string"/>
   <xsd:element name="zip"    type="xsd:integer"/>
  </xsd:sequence>
  <xsd:attribute name="country" type="xsd:NMTOKEN" fixed="US"/>
 </xsd:complexType>
</xsd:schema>
```

Di sini, tag berikut digunakan.

* `xs:element` - Menentukan elemen.
* `xs:sequence` - Menandakan elemen anak hanya muncul dalam urutan yang disebutkan.
* `xs:complexType` - Menandakan ia mengandung elemen lain.
* `xs:simpleType` - Menandakan mereka tidak mengandung elemen lain.
* `type` - string, desimal, bilangan bulat, boolean, tanggal, waktu,

## Referensi ##

- [Microsoft XML Notepad](https://microsoft.github.io/XmlNotepad/)
- [Contoh Contoh XSD](https://learn.microsoft.com/en-us/visualstudio/xml-tools/sample-xsd-file-simple-schema?view=vs-2022)

