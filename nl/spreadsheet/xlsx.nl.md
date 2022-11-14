{
  "date" : "2019-12-10",
  "keywords" :[ "XLSX", "bestand", "extensie", "bestandsindeling", "Excel", "Spreadsheet"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Meer informatie over wat een XLSX-bestand is en API's die XLSX-bestanden kunnen maken en openen.",
  "title" :"XLSX-bestandsindeling - Wat is een XLSX-bestand?",
  "linktitle" : "XLSX",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## Wat is een XLSX-bestand?

**XLSX** is een bekende indeling voor Microsoft Excel-documenten die door Microsoft is geïntroduceerd met de release van Microsoft Office 2007. Gebaseerd op een structuur die is georganiseerd volgens de Open Packaging Conventions zoals beschreven in [Deel 2](https://www .ecma-international.org/publications/standards/Ecma-376.htm) van de OOXML-standaard ECMA-376, is het nieuwe formaat een zip-pakket dat een aantal XML-bestanden bevat. De onderliggende structuur en bestanden kunnen worden onderzocht door het .xlsx-bestand eenvoudig uit te pakken.

## Korte geschiedenis van XLSX-bestandsindeling

Het XLSX-bestandsformaat werd geïntroduceerd in 2007 en maakt gebruik van de Open XML-standaard die in 2000 door Microsoft is aangepast. Vóór XLSX was het gebruikelijke bestandsformaat [XLS](/nl/spreadsheet/xls/) dat een puur binair bestandsformaat was. Het nieuwe bestandstype heeft voordelen toegevoegd van kleine bestandsgroottes, minder veranderingen van corruptie en goed opgemaakte afbeeldingen. Het was in het begin van 2000 toen Microsoft besloot om voor de verandering te gaan om de standaard voor **Office Open XML** te accommoderen. In 2007 werd dit nieuwe bestandsformaat onderdeel van Office 2007 en wordt het ook voortgezet in de nieuwe versies van Microsoft Office.

## Specificaties XLSX-bestandsindeling

De officiële [specificaties van XLSX-bestandsindelingen](https://docs.microsoft.com/en-us/openspecs/office_standards/ms-xlsx/2c5dee00-eff2-4b22-92b6-0738acd4475e) zijn online beschikbaar bij Microsoft. Om te zien wat er in het XLSX-bestand staat, hernoemt u het naar het bestand [ZIP](/nl/compression/zip/) door de extensie te wijzigen en het vervolgens uit te pakken om de samenstellende bestanden van deze Excel-werkmap te bekijken. Een lege werkmap heeft, wanneer deze wordt uitgepakt naar zijn bestanden, de volgende samenstellende bestanden en mappen.

### [Content_Types].xml ###

Dit is het enige bestand dat op het basisniveau wordt gevonden wanneer de zip wordt uitgepakt. Het vermeldt de inhoudstypen voor onderdelen in het pakket. Alle verwijzingen naar de XML-bestanden die in het pakket zijn opgenomen, worden in dit XML-bestand verwezen.

### \_rels (map) ###

Dit is de map Relaties die een enkel XML-bestand bevat waarin de relaties op pakketniveau zijn opgeslagen. Koppelingen naar de belangrijkste delen van de Xlsx-bestanden zijn als URI's in dit bestand opgenomen. Deze URI's identificeren het type relatie van elk belangrijk onderdeel met het pakket. Dit omvat de relatie met het primaire kantoordocument dat zich bevindt als xl/workbook.xml en andere delen binnen docProps als kern- en uitgebreide eigenschappen.

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

## XLSX-formaat voorbeeld ##


Voor elk Excel-werkblad in een werkmap is er één XML-bestand. U vindt deze XML-bestanden in de map xl/worksheets. Alle informatie in een werkblad is georganiseerd in verschillende secties in het XML-bestand. Laten we een voorbeeldwerkblad bekijken uit een werkmap die wordt weergegeven in de volgende afbeelding.

{{< figure src="../XLSX file format.png" alt="XLSX-bestandsindeling" >}}

Zoals te zien is, bevat dit werkblad inhoud in de cellen A1 tot en met B2 en een afbeelding. Bovendien is cel G13 momenteel de actieve cel in het werkblad. Laten we nu het bestand xl/worksheets/sheet1.xml bekijken om te zien hoe deze informatie wordt weergegeven in het XML-bestand. De inhoud van dit XML-bestand is zoals hieronder weergegeven.

{{< figure src="../XLSX File Format Details.png" alt="XPS-bestandsindeling" >}}

1. Op het tabblad is een themakleur toegepast. Het wordt vermeld in het XML-bestand met tag<tabColor> na de thema-ID.
1. De tabGeselecteerde waarde is ingesteld op 1, wat aangeeft dat dit het geselecteerde blad is
1. Zoals te zien is in de eerste afbeelding hierboven, is cel G13 in het werkblad een actieve cel die ook wordt vermeld in het XML-bestand.
1. Het tabblad sheetData vertegenwoordigt de gegevens in het werkblad. U kunt echter zien dat de originele inhoud van het werkblad nergens in deze sectie staat. Dit komt omdat de tekst indirect wordt verwezen vanuit het XML-blad "sharedStrings". Deze koppeling zorgt ervoor dat elke tekst slechts één keer wordt opgeslagen en opnieuw kan worden geraadpleegd om ruimte te besparen.
1. De afbeelding zoals te zien is, wordt verwezen met referentie-id "rId2"

## Bijdrage leveren

Moet u iets delen over XLSX- of Spreadsheet-bestandsindelingen? U kunt uw bevindingen posten in het gedeelte [Spreadsheet File Format News](https://news.fileformat.com/t/Spreadsheet).

## Referenties

* [[MS-XLSX] - XLSX-bestandsindeling](https://docs.microsoft.com/en-us/openspecs/office_standards/ms-xlsx/2c5dee00-eff2-4b22-92b6-0738acd4475e)
* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-xlsx.php)

