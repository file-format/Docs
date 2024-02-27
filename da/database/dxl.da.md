{
  "date": "2023-05-16",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om DXL-filformat og API'er, der kan oprette og åbne DTSX-filer.",
  "title": "DXL-filformat - Domino XML-sprogfilformat",
  "linktitle": "DXL",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-dx-dal"
}
},
  "lastmod": "2023-05-16"
}

## Hvad er en DXL fil?

En DXL-fil er en XML-baseret datalagringsfil, der er oprettet til virksomhedens samarbejdssoftware, Lotus Domino. Den indeholder data relateret til en Lotus Domino-database, såsom skemaer, designelementer, visning, formularer, dokumenter og selve databasedataene. [XML](/web/xml/) er et universelt filformat, der kan læses af softwareprogrammer skrevet på ethvert programmeringssprog. Den kan også læses af mennesker og kan åbnes med enhver teksteditor. Det er derfor, DXL-filer giver mulighed for at eksportere data i udskifteligt filformat.

## DXL filformat

DXL-filer gemmes i XML-filformat og kan let læses af applikationer skrevet på ethvert programmeringssprog. Disse filer gemmer data og indstillinger i XML-tags, der kategoriserer data samt arrangerer dem i den rigtige rækkefølge

### Eksempel på DXL-output

Følgende er output-tekstuddraget for et Notes-dokument.

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

## Referencer

 * [DXL-format - Microsoft](https://help.hcltechsw.com/dom_designer/9.0.1/appdev/H_EXAMPLE_DOCUMENT_NOTEINFO_AND_ITEM_ELEMENTS_XML.html)

