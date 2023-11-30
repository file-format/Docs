{
  "date" : "2023-05-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Läs mer om DXL-filformat och API:er som kan skapa och öppna DTSX-filer.",
  "title" :"DXL-filformat - Domino XML-språkfilformat",
  "linktitle" : "DXL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2023-05-16"
}

## Vad är en DXL fil?

En DXL-fil är en XML-baserad datalagringsfil skapad för affärssamarbete på företagsnivå, Lotus Domino. Den innehåller data relaterade till en Lotus Domino-databas som scheman, designelement, vy, formulär, dokument och själva databasdatan. [XML](/sv/web/xml/) är ett universellt filformat som kan läsas av program som är skrivna på alla programmeringsspråk. Den är också läsbar för människor och kan öppnas med vilken textredigerare som helst. Det är därför DXL-filer ger möjlighet att exportera data i utbytbart filformat.

## DXL filformat

DXL-filer sparas i XML-filformat och är lätta att läsa av applikationer skrivna på alla programmeringsspråk. Dessa filer lagrar data och inställningar i XML-taggar som kategoriserar data samt ordnar dem i rätt ordning

### DXL-utgångsexempel

Följande är utdragstextutdraget för ett Notes-dokument.

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

## Referenser

* [DXL-format – Microsoft](https://help.hcltechsw.com/dom_designer/9.0.1/appdev/H_EXAMPLE_DOCUMENT_NOTEINFO_AND_ITEM_ELEMENTS_XML.html)

