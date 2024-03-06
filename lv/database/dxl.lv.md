{
  "date": "2023-05-16",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par DXL faila formātu un API, kas var izveidot un atvērt DTSX failus.",
  "title": "DXL faila formāts — Domino XML valodas faila formāts",
  "linktitle": "DXL",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-dx-lvl"
}
},
  "lastmod": "2023-05-16"
}

## Kas ir DXL fails?

DXL fails ir uz XML balstīts datu krātuves fails, kas izveidots uzņēmuma līmeņa biznesa sadarbības programmatūrai Lotus Domino. Tajā ir dati, kas saistīti ar Lotus Domino datu bāzi, piemēram, shēmas, dizaina elementi, skats, veidlapas, dokumenti un paši datu bāzes dati. [XML](/web/xml/) ir universāls faila formāts, ko var nolasīt lietojumprogrammas, kas rakstītas jebkurā programmēšanas valodā. Tas ir arī cilvēkiem lasāms, un to var atvērt ar jebkuru teksta redaktoru. Tāpēc DXL faili nodrošina iespēju eksportēt datus maināmā faila formātā.

## DXL faila formāts

DXL faili tiek saglabāti XML faila formātā un ir viegli lasāmi lietojumprogrammās, kas rakstītas jebkurā programmēšanas valodā. Šie faili saglabā datus un iestatījumus XML tagos, kas klasificē datus, kā arī sakārto tos pareizā secībā

### DXL izvades piemērs

Tālāk ir sniegta piezīmju dokumenta izvades teksta fragmenta izvade.

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

## Atsauces

 * [DXL formāts — Microsoft](https://help.hcltechsw.com/dom_designer/9.0.1/appdev/H_EXAMPLE_DOCUMENT_NOTEINFO_AND_ITEM_ELEMENTS_XML.html)

