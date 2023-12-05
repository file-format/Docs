{
  "date" : "2023-05-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"További információ a DXL fájlformátumról és az API-król, amelyek DTSX fájlokat hozhatnak létre és nyithatnak meg.",
  "title" :"DXL fájlformátum - Domino XML nyelvi fájlformátum",
  "linktitle" : "DXL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2023-05-16"
}

## Mi az a DXL fájl?

A DXL fájl egy XML alapú adattároló fájl, amelyet a Lotus Domino vállalati szintű üzleti együttműködési szoftverhez hoztak létre. Tartalmaz egy Lotus Domino adatbázishoz kapcsolódó adatokat, például sémákat, tervezési elemeket, nézetet, űrlapokat, dokumentumokat és magát az adatbázisadatokat. Az [XML](/hu/web/xml/) egy univerzális fájlformátum, amelyet bármilyen programozási nyelven írt szoftveralkalmazások olvashatnak. Ember által is olvasható, és bármilyen szövegszerkesztővel megnyitható. Ezért a DXL fájlok lehetővé teszik az adatok cserélhető fájlformátumban történő exportálását.

## DXL fájlformátum

A DXL fájlok XML fájlformátumban kerülnek mentésre, és bármely programozási nyelven írt alkalmazások könnyen olvashatók. Ezek a fájlok XML-címkékben tárolják az adatokat és a beállításokat, amelyek az adatokat kategorizálják és megfelelő sorrendbe rendezik

### DXL kimeneti példa

Az alábbiakban látható a Notes-dokumentum kimeneti szövegrészlete.

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

## Hivatkozások

* [DXL formátum – Microsoft](https://help.hcltechsw.com/dom_designer/9.0.1/appdev/H_EXAMPLE_DOCUMENT_NOTEINFO_AND_ITEM_ELEMENTS_XML.html)

