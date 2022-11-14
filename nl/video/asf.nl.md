{
  "date" : "2021-02-15",
  "keywords" :[ "asf-bestand", "asf-bestandsformaat", "wat is een asf-bestand", "bestand", "asf-voorbeeld", "asf-bestandsextensie","extensie", "formaat"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASF - Bestandsformaat voor geavanceerde systemen",
  "description":"Meer informatie over ASF-bestandsindelingen en API's die ASF-bestanden kunnen maken en openen.",
  "linktitle" : "ASF",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-02-16"
}

## Wat is een ASF-bestand?

Een bestand met de extensie .asf is een multimediabestandsindeling voor het opslaan en afspelen van digitale mediastreams via het netwerk. Het is een containerbestandsindeling die zowel video- als audio-inhoud kan bevatten om online te streamen. U zult zelden ASF-bestanden vinden, en u zult waarschijnlijk de Windows Media Audio ([WMA](/nl/audio/wma/)) en Windows Media Video ([WMV](/nl/video/wmv/)) bestanden tegenkomen die beide ASF-bestanden specificeren inhoud hebben die is gecodeerd met respectieve codecs. Windows-mediabestanden kunnen worden gemaakt en gelezen met behulp van de Windows Media Format SDK.

## ASF-bestandsindeling

Een ASF-bestand kan meerdere onafhankelijke of afhankelijke streams bevatten. Dit kan meerdere audiostreams zijn voor meerkanaals audio of videostreams met meerdere bitrates. De meerdere bitrates maken de streams geschikt voor verzending over verschillende bandbreedtes. Bovendien kunnen de streams in een ASF-bestand in gecomprimeerd of ongecomprimeerd formaat zijn. De beste compressie wordt bereikt met de Microsoft Windows Media Audio en Video 9 Series codecs. Volledige specificaties van het ASF-bestandsformaat zijn beschikbaar op [Microsoft-website](https://download.microsoft.com/download/7/9/0/790fecaa-f64a-4a5e-a430-0bccdab3f1b4/ASF_Specification.doc).

### ASF-bestandsstructuur op het hoogste niveau

ASF-bestanden bevatten logischerwijs drie typen objecten op het hoogste niveau:

* `Header Object` - verplicht en moet aan het begin van elk ASF-bestand worden geplaatst
* `Data Object` - verplicht en moet het header-object volgen
* `Index Object(en)` - optioneel, maar handig bij het bieden van op tijd gebaseerde willekeurige toegang tot ASF-bestanden

De volgende afbeelding toont de bestandsstructuur op het hoogste niveau van ASF-bestanden.

![ASF File Structure](../asf.png "ASF File Structure")

#### ASF Header-object op het hoogste niveau

Het Header-object biedt een bekende bytereeks aan het begin van de ASF-bestanden en kan optioneel metadata zoals bibliografische informatie bevatten. Het bevat alle informatie die nodig is om de informatie in het data-object goed te interpreteren. Het kopobject kan verschillende standaardobjecten bevatten, waaronder, maar niet beperkt tot:

* Bestandseigenschappen Object - Bevat algemene bestandskenmerken.
* Stream Properties Object - Definieert een digitale mediastream en zijn kenmerken.
* Header Extension Object - Hiermee kan extra functionaliteit worden toegevoegd aan een ASF-bestand met behoud van achterwaartse compatibiliteit.
* Inhoud Beschrijving Object - Bevat bibliografische informatie.
* Scriptopdrachtobject - Bevat opdrachten die kunnen worden uitgevoerd op de afspeeltijdlijn.
* Marker Object - Biedt benoemde springpunten in een bestand.

Het Header-object wordt weergegeven met de volgende structuur:

|Veldnaam |Veldtype |Grootte (bits)|
---|---|---|
|Object-ID| GUID| 128|
|Objectgrootte| QWORD| 64|
|Aantal kopobjecten| DWORD| 32|
|Gereserveerd1| BYTE| 8|
|Gereserveerd2| BYTE| 8|

#### ASF-gegevensobject op het hoogste niveau

Alle digitale mediagegevens voor een ASF-bestand bevinden zich in het dataobject en worden opgeslagen in de vorm van ASF-datapakketten. Elk datapakket heeft een vaste lengte en bevat data voor een of meer digitale mediastromen.

#### ASF-indexobjecten op het hoogste niveau

ASF-indexobjecten op het hoogste niveau hebben de volgende twee typen:

* `Eenvoudig indexobject` - Bevat een op tijd gebaseerde index van de videogegevens in een ASF-bestand. Het tijdsinterval tussen indexitems is constant en wordt opgeslagen in het Simple Index Object.
* `Index Object` - Verwijst naar het Index Object, het Media Object Index Object en het Timecode Index Object, waarvan de formaten vergelijkbaar zijn. Net als het eenvoudige indexobject indexeert het indexobject op tijd met een vast tijdsinterval, maar is het niet beperkt tot videostreams.

## Referenties

* [ASF-bestandsindeling - Microsoft](https://download.microsoft.com/download/7/9/0/790fecaa-f64a-4a5e-a430-0bccdab3f1b4/ASF_Specification.doc)
* [QuickTime-bestandsindeling - Wikipedia](https://en.wikipedia.org/wiki/QuickTime_File_Format)

