{
  "date" : "2019-10-11",
  "keywords" :[ "ico file", "ico file format", "wat is een ico file", "file", "ico example", "ico file extension","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ICO - Afbeeldingsbestandsformaat",
  "description":"Meer informatie over ICO-bestandsindelingen en API's die ICO-bestanden kunnen maken en openen.",
  "linktitle" : "ICO",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Wat is een ICO-bestand?

Bestanden met de ICO-extensie zijn afbeeldingsbestandstypen die worden gebruikt als pictogram voor de weergave van een toepassing op [Microsoft Windows](https://www.microsoft.com/en-us/windows). Deze zijn er in verschillende groottes, kleurondersteuning en resoluties om aan de vereisten van het scherm te voldoen. Een ander vergelijkbaar bestandsformaat voor afbeeldingen op Microsoft Windows is [CUR](/nl/image/cur/) voor cursorweergave en definieert een hotspot in de afbeeldingskop. Op MacOS hebben ICNS-bestandsindelingen hetzelfde doel als ICO-bestanden. Verschillende online websites en applicaties bieden de mogelijkheid om dergelijke bestanden te maken en andere afbeeldingsformaten zoals [BMP](/nl/image/bmp/), [PNG](/nl/image/png/), enz. naar pictogrambestandsformaat te converteren. Het officiële door IANA geregistreerde internetmediatype voor ICO-bestanden is image/vnd.microsoft.icon.

## Korte geschiedenis ##

Pictogrammen werden geïntroduceerd met de lancering van Microsoft Windows 1.0. Deze waren 32x32 groot en waren monochroom. Met de komst van win32 werd ondersteuning voor pictogramafbeeldingen in ware kleuren geïntroduceerd met een afmeting tot 256x256 pixels. Windows XP was de eerste die ondersteuning bood voor 32-bits kleurenpictogramafbeeldingen, waardoor semi-transparante gebieden zoals schaduwen, anti-aliasing en glasachtige effecten aan het pictogram konden worden toegevoegd. Microsoft raadde alleen pictogramformaten tot 48×48 pixels aan voor Windows XP. Windows Vista heeft een pictogramweergave van 256 × 256 pixels toegevoegd aan Windows Verkenner, evenals ondersteuning voor het gecomprimeerde [PNG](/nl/image/png/)-formaat. Bij gebruikers die hogere resoluties en hoge DPI-modi gebruiken, worden grotere pictogramformaten (zoals 256×256) aanbevolen.

## ICO-bestandsindeling ##

Een enkel ICO-bestand bestaat uit een of meer kleine afbeeldingen van meerdere formaten en kleurdiepten. De aanwezigheid van afbeeldingen van meerdere formaten is voor de juiste schaling bij verschillende schermresoluties. Alle waarden in ICO/CUR-bestanden worden weergegeven in [little-endian](https://en.wikipedia.org/wiki/Little-endian) bytevolgorde.

Het ICO-bestand bestaat uit een Icon-header, een Icon Directory,

|Veld|Beschrijving
---|---|
|Icon Header|Slaat algemene informatie op over het ICO-bestand.
|Directory[1..n]|Slaat algemene informatie op over elke afbeelding in het bestand.
|Icoon #1|De werkelijke "gegevens" voor de eerste afbeelding in de oude AND/XOR DIB-indeling of nieuwere PNG
|...|
|Icoon #n|Gegevens voor de laatste icoonafbeelding

### Koptekst ###

|Offset|Grootte (in bytes)|Doel
---|---|---|
|0|2|Gereserveerd. Moet altijd 0 zijn.
|2|2|Specificeert afbeeldingstype: 1 voor pictogram (.ICO) afbeelding, 2 voor cursor (.CUR) afbeelding. Andere waarden zijn ongeldig.
|4|2|Specificeert het aantal afbeeldingen in het bestand.

### Telefoonboek ###

De map in een ICO-bestand, weergegeven als ICONDIR-structuur, bevat een ICONDIRECTORY-structuur voor elke afbeelding in het bestand. Hetzelfde wordt gevolgd door een aaneengesloten blok van alle beeldbitmapgegevens. Dit is zoals hieronder weergegeven.

|Offset|Grootte|Beschrijving
---|---|---|
|0 (0)|1|Breedte, moet 0 zijn als 256 pixels
|1 (1)|1|Hoogte, moet 0 zijn als 256 pixels
|2 (2)|1|Kleurtelling, moet 0 zijn als er meer dan 256 kleuren zijn
|3 (3)|1|Gereserveerd, moet 0 . zijn
|4 (4)|2|Kleurvlakken in .ICO-indeling moeten 0 of 1 zijn, of de X-hotspot in .CUR-indeling
|6 (6)|2|Bits per pixel in .ICO-formaat, of de Y-hotspot in .CUR-formaat
|8 (8)|4|Grootte van de bitmapgegevens in bytes.
|12 (C)|4|Verschuiving in het bestand.

## Referenties ##

* [ICO - Door Wikipedia](https://en.wikipedia.org/wiki/ICO_(file_format))
* [IANA - vnd.microsoft.icon](http://www.iana.org/assignments/media-types/image/vnd.microsoft.icon)

