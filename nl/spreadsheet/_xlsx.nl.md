{
  "date" : "2019-12-10",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Uw gids voor bestandsindelingen om te weten wat een _XLSX-bestand is en API's die _XLSX-bestanden kunnen maken en openen.",
  "title" :"Wat is een _XLSX-bestand?",
  "linktitle" : "_XLSX",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2021-11-22"
}

## Wat is een _XLSX-bestand?

Een bestand met de extensie .\_xlsx is eigenlijk een [XLSX](/nl/spreadsheet/xlsx/) bestand dat door een andere toepassing is hernoemd. Dit kan in bepaalde gevallen gebeuren wanneer de bestandsnaam een . aan het einde van de bestandsnaam. De \_XLSX-bestanden kunnen net als de XLSX-bestanden in Microsoft Excel worden geopend door deze opnieuw te hernoemen naar de extensie .xlsx.

## _XLSX-bestandsindeling - Meer informatie

De _XLSX-bestanden zijn niet anders dan de XLSX-bestanden en gebruiken de Open XML-standaard die in 2000 door Microsoft werd aangenomen. Vóór XLSX was [XLS](/nl/spreadsheet/xls/) de primaire bestandsindeling die werd gebruikt voor het werken met Excel-spreadsheets om documenten op te slaan in binair formaat. Dit nieuwe op XML gebaseerde bestandsformaat kwam met voordelen zoals kleine bestandsgroottes, weerstand tegen bestandscorruptie en goed opgemaakte afbeeldingen. Dit nieuwe op XML gebaseerde bestandsformaat werd onderdeel van Office 2007 en wordt ook uitgevoerd in de nieuwe versies van Microsoft.

## \_XLSX Specificaties bestandsformaat

Omdat een \_XLSX-bestand een XLSX-bestand is hernoemd, heeft het dezelfde specificaties als het originele bestand. Het is gewoon een archiefbestand dat is gebaseerd op het [ZIP](/nl/compression/zip/) archiefbestandsformaat. Als u de inhoud van dit archief wilt zien, hernoemt u het bestand naar de extensie .zip en extraheert u het om de samenstellende bestanden van deze Excel-werkmap te bekijken. Een lege werkmap heeft, wanneer deze wordt uitgepakt naar zijn bestanden, de volgende samenstellende bestanden en mappen.

### [Content_Types].xml

Dit is het enige bestand dat op het basisniveau wordt gevonden wanneer de zip wordt uitgepakt. Het vermeldt de inhoudstypen voor onderdelen in het pakket. Alle verwijzingen naar de XML-bestanden die in het pakket zijn opgenomen, worden in dit XML-bestand verwezen.

### \_rels (map)

Dit is de map Relaties die een enkel XML-bestand bevat waarin de relaties op pakketniveau zijn opgeslagen. Koppelingen naar de belangrijkste delen van de Xlsx-bestanden zijn als URI's in dit bestand opgenomen. Deze URI's identificeren het type relatie van elk belangrijk onderdeel met het pakket. Dit omvat de relatie met het primaire kantoordocument dat zich bevindt als xl/workbook.xml en andere delen binnen docProps als kern- en uitgebreide eigenschappen.

### docProps

Deze map bevat de algemene documenteigenschappen. Deze omvatten een reeks kerneigenschappen, een reeks uitgebreide of toepassingsspecifieke eigenschappen en een miniatuurvoorbeeld van het document. Een lege werkmap heeft twee bestanden in deze map, namelijk app.xml en core.xml. De core.xml bevat informatie zoals auteur, datum gemaakt en opgeslagen en gewijzigd. App.xml bevat informatie over de inhoud van het bestand.

### xl (map)

Dit is de hoofdmap die alle details over de inhoud van de werkmap bevat. Standaard heeft het de volgende mappen:

* \_rels
* thema
* werkbladen

en volgende xml-bestanden:

* stijlen.xml
* werkmap.xml

## Referenties

* [MS-XLSX - .xlsx-bestandsindeling](https://msdn.microsoft.com/en-us/library/dd922181(v#office.12).aspx)
* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-xlsx.php)

