{
  "date" : "2023-05-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Erfahren Sie mehr über das DXL-Dateiformat und APIs, mit denen DTSX-Dateien erstellt und geöffnet werden können.",
  "title" :"DXL-Dateiformat – Domino XML-Sprachdateiformat",
  "linktitle" : "DXL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2023-05-16"
}

## Was ist eine DXL-Datei?

Eine DXL-Datei ist eine XML-basierte Datenspeicherdatei, die für die unternehmensweite Business-Collaboration-Software Lotus Domino erstellt wurde. Es enthält Daten im Zusammenhang mit einer Lotus Domino-Datenbank wie Schemata, Designelemente, Ansichten, Formulare, Dokumente und die Datenbankdaten selbst. [XML](/web/xml/) ist ein universelles Dateiformat, das von Softwareanwendungen gelesen werden kann, die in jeder Programmiersprache geschrieben sind. Es ist außerdem für Menschen lesbar und kann mit jedem Texteditor geöffnet werden. Aus diesem Grund bieten DXL-Dateien die Möglichkeit, Daten in austauschbaren Dateiformaten zu exportieren.

## DXL-Dateiformat

DXL-Dateien werden im XML-Dateiformat gespeichert und können von Anwendungen, die in einer beliebigen Programmiersprache geschrieben sind, problemlos gelesen werden. Diese Dateien speichern Daten und Einstellungen in XML-Tags, die Daten kategorisieren und in der richtigen Reihenfolge anordnen

### DXL-Ausgabebeispiel

Im Folgenden finden Sie die Ausgabe eines Textauszugs für ein Notes-Dokument.

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

## Verweise

* [DXL-Format – Microsoft](https://help.hcltechsw.com/dom_designer/9.0.1/appdev/H_EXAMPLE_DOCUMENT_NOTEINFO_AND_ITEM_ELEMENTS_XML.html)

