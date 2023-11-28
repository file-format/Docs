{
  "date" : "2023-05-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Pelajari tentang format file DXL dan API yang dapat membuat dan membuka file DTSX.",
  "title" :"Format File DXL - Format File Bahasa XML Domino",
  "linktitle" : "DXL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2023-05-16"
}

## Apa itu file DXL?

File DXL adalah file penyimpanan data berbasis XML yang dibuat untuk perangkat lunak kolaborasi bisnis tingkat perusahaan, Lotus Domino. Ini berisi data yang terkait dengan database Lotus Domino seperti skema, elemen desain, tampilan, formulir, dokumen, dan data database itu sendiri. [XML](/id/web/xml/) adalah format file universal yang dapat dibaca oleh aplikasi perangkat lunak yang ditulis dalam bahasa pemrograman apa pun. Itu juga dapat dibaca manusia dan dapat dibuka dengan editor teks apa pun. Itulah sebabnya file DXL menyediakan kemampuan untuk mengekspor data dalam format file yang dapat dipertukarkan.

## Format File DXL

File DXL disimpan dalam format file XML dan mudah dibaca oleh aplikasi yang ditulis dalam bahasa pemrograman apa pun. File-file ini menyimpan data dan pengaturan dalam tag XML yang mengkategorikan data serta mengaturnya dalam urutan yang benar

### Contoh Keluaran DXL

Berikut ini adalah keluaran kutipan teks keluaran untuk dokumen Notes.

```
<document form="Customers">
	<noteinfo noteid="942" unid="431A199A6FCC9C0985256A54005041A1" sequence="1">
		<created>
			<datetime dst="true">20010522T103636,81-04</datetime>
		</created>
		<modified>
			<datetime dst="true">20010522T103709,78-04</datetime>
		</modified>
		<revised>
			<datetime dst="true">20010522T103709,77-04</datetime>
		</revised>
		<lastaccessed>
			<datetime dst="true">20010522T103709,77-04</datetime>
		</lastaccessed>
		<addedtofile>
			<datetime dst="true">20010522T103709,77-04</datetime>
		</addedtofile>
	</noteinfo>
	<updatedby>
		<name>CN=Michelle Lally/OU=CAM/O=Acme</name>
	</updatedby>
	<item name="date">
		<datetime>20010601</datetime>
	</item>
	<item name="name">
		<text>Harry Hill</text>
	</item>
	</document>
```

## Referensi

* [Format DXL - Microsoft](https://help.hcltechsw.com/dom_designer/9.0.1/appdev/H_EXAMPLE_DOCUMENT_NOTEINFO_AND_ITEM_ELEMENTS_XML.html)

