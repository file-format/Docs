{
  "date" : "2019-12-10",
  "keywords" :[ "XLTX", "bestand", "extensie", "bestandsindeling", "Excel Open XML", "Spreadsheet" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Uw gids voor bestandsindelingen om te weten wat een XLTX-bestand is en API's die ze kunnen maken en openen.",
  "title" :"Wat is een XLTX-bestand?",
  "linktitle" : "XLTX",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## Wat is een XLTX-bestand?

Bestanden met de extensie .xltx vertegenwoordigen Microsoft Excel-sjabloonbestanden die zijn gebaseerd op de specificaties van de Office OpenXML-bestandsindeling. Het wordt gebruikt om een standaard sjabloonbestand te maken dat kan worden gebruikt om [XLSX](/nl/spreadsheet/xlsx/)-bestanden te genereren die dezelfde instellingen hebben als gespecificeerd in het XLTX-bestand.

## Korte geschiedenis

Het was in het begin van 2000 toen Microsoft besloot om voor de verandering te gaan om de standaard voor **Office Open XML** te accommoderen. Documenten, van verschillende typen, onder deze nieuwe standaard werden geïdentificeerd door "X" toe te voegen in hun extensies, waarbij "X" voor XML staat. In 2007 werd dit nieuwe bestandsformaat onderdeel van Office 2007 en wordt het ook voortgezet in de nieuwe versies van Microsoft Office. Het nieuwe bestandstype heeft voordelen toegevoegd van kleine bestandsgroottes, minder veranderingen van corruptie en goed opgemaakte afbeeldingen.

## Specificaties XLTX-bestandsindeling

XLTX-bestanden zijn gebaseerd op de Office OpenXML-bestandsindeling en gebruiken XML en [ZIP](/nl/compression/zip/) om de bestandsgrootte te verkleinen. Het is gemaakt met de release van Microsoft Office 2007 om het binaire XLT-bestandsformaat te vervangen. Net als XLTX kan het XLT-bestandsformaat worden gebruikt om [XLS](/nl/spreadsheet/xls/)-bestanden te maken met Microsoft Excel 2003 en 2007. Deze kunnen worden geopend met Microsoft Excel door op het bestand te dubbelklikken. De bestandsorganisatie in een XLTX-bestandsindeling kan worden waargenomen door het bestand te hernoemen naar ZIP en vervolgens de inhoud op schijf uit te pakken.

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

* [[MS-XLSX] - .Xlsx-bestandsindeling](https://msdn.microsoft.com/en-us/library/dd922181(v#office.12).aspx)
* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-xlsx.php)

