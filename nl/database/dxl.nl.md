{
  "date" : "2023-05-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Leer meer over het DXL-bestandsformaat en API's die DTSX-bestanden kunnen maken en openen.",
  "title" :"DXL-bestandsindeling - Domino XML-taalbestandsindeling",
  "linktitle" : "DXL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2023-05-16"
}

## Wat is een DXL-bestand?

Een DXL-bestand is een op XML gebaseerd gegevensopslagbestand gemaakt voor de zakelijke samenwerkingssoftware op ondernemingsniveau, Lotus Domino. Het bevat gegevens die verband houden met een Lotus Domino-database, zoals schema's, ontwerpelementen, weergaven, formulieren, documenten en de databasegegevens zelf. [XML](/nl/web/xml/) is een universeel bestandsformaat dat kan worden gelezen door softwaretoepassingen die in elke programmeertaal zijn geschreven. Het is ook voor mensen leesbaar en kan met elke teksteditor worden geopend. Dat is de reden waarom DXL-bestanden de mogelijkheid bieden om gegevens in uitwisselbaar bestandsformaat te exporteren.

## DXL-bestandsformaat

DXL-bestanden worden opgeslagen in XML-bestandsformaat en zijn gemakkelijk leesbaar door toepassingen die in elke programmeertaal zijn geschreven. Deze bestanden slaan gegevens en instellingen op in XML-tags die gegevens categoriseren en in de juiste volgorde rangschikken

### DXL-uitvoervoorbeeld

Hieronder volgt het uitvoertekstfragment voor een Notes-document.

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

## Referenties

* [DXL-indeling - Microsoft](https://help.hcltechsw.com/dom_designer/9.0.1/appdev/H_EXAMPLE_DOCUMENT_NOTEINFO_AND_ITEM_ELEMENTS_XML.html)

