{
  "date" : "2019-12-10",
  "keywords" :[ "XLTM", "bestand", "extensie", "bestandsindeling", "Excel Open XML Macro", "Spreadsheet"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Uw gids voor bestandsindelingen om te weten wat een XLTM-bestand is en API's die ze kunnen maken en openen.",
  "title" :"Wat is een XLTM-bestand?",
  "linktitle" : "XLTM",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## Wat is een XLTM-bestand?

De XLTM-bestandsextensie vertegenwoordigt bestanden die door Microsoft Excel zijn gegenereerd als sjabloonbestanden met ingeschakelde macro's. XLTM-bestanden lijken qua structuur op [XLTX](/nl/spreadsheet/xltx/) behalve dat de laatste geen ondersteuning biedt voor het maken van sjabloonbestanden met macro's. Dergelijke sjabloonbestanden worden gebruikt om de lay-out, opmaak en andere instellingen samen met de macro's te genereren en in te stellen om het maken van vergelijkbare XLSX-bestanden te vergemakkelijken.

## Korte geschiedenis ##

Het was in het begin van 2000 toen Microsoft besloot om voor de verandering te gaan om de standaard voor **Office Open XML** te accommoderen. Documenten, van verschillende typen, onder deze nieuwe standaard werden geïdentificeerd door "X" toe te voegen in hun extensies, waarbij "X" voor XML staat. In 2007 werd dit nieuwe bestandsformaat onderdeel van Office 2007 en wordt het ook voortgezet in de nieuwe versies van Microsoft Office. Het nieuwe bestandstype heeft voordelen toegevoegd van kleine bestandsgroottes, minder veranderingen van corruptie en goed opgemaakte afbeeldingen.

## Specificaties XLTM-bestandsindeling ##

XLTM-bestanden zijn gebaseerd op de Office OpenXML-bestandsindeling en gebruiken XML en [ZIP](/nl/compression/zip/) om de bestandsgrootte te verkleinen. Deze zijn te openen met Microsoft Excel door te dubbelklikken op het bestand. De bestandsorganisatie in een XLTM-bestandsindeling kan worden bekeken door het bestand te hernoemen naar ZIP en vervolgens de inhoud op schijf uit te pakken.

### [Content_Types].xml ###

Dit is het enige bestand dat op het basisniveau wordt gevonden wanneer de zip wordt uitgepakt. Het vermeldt de inhoudstypen voor onderdelen in het pakket. Alle verwijzingen naar de XML-bestanden die in het pakket zijn opgenomen, worden in dit XML-bestand verwezen.

### \_rels (map) ###

Dit is de map Relaties die een enkel XML-bestand bevat waarin de relaties op pakketniveau zijn opgeslagen. Links naar de belangrijkste delen van de Xltx-bestanden zijn in dit bestand opgenomen als URI's. Deze URI's identificeren het type relatie van elk belangrijk onderdeel met het pakket. Dit omvat de relatie met het primaire kantoordocument dat zich bevindt als xl/workbook.xml en andere delen binnen docProps als kern- en uitgebreide eigenschappen.

### docProps ###

Deze map bevat de algemene documenteigenschappen. Deze omvatten een reeks kerneigenschappen, een reeks uitgebreide of toepassingsspecifieke eigenschappen en een miniatuurvoorbeeld van het document. Een lege werkmap heeft twee bestanden in deze map, namelijk app.xml en core.xml. De core.xml bevat informatie zoals auteur, datum gemaakt en opgeslagen en gewijzigd. App.xml bevat informatie over de inhoud van het bestand.

### xl (map) ###

Dit is de hoofdmap die alle details over de inhoud van de werkmap bevat. Standaard heeft het de volgende mappen:

* \_rels
* thema
* werkbladen

en volgende xml-bestanden:

* stijlen.xml
* werkmap.xml

## Referenties ##

* [MS-XLSX-bestandsindeling](https://msdn.microsoft.com/en-us/library/dd922181(v#office.12).aspx)
* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-xlsx.php)

