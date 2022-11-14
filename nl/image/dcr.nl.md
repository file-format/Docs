{
  "date" : "2021-26-08",
  "keywords" :[ "dcr file", "dcr file format", "wat is een dcr file", "file", "dcr example", "dcr file extension","extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DCR - RAW-beeldbestand voor digitale camera's",
  "description":"Meer informatie over DCR-bestandsindeling en API's die DCR-bestanden kunnen maken en openen.",
  "linktitle" : "DCR",
  "menu" : {
    "docs" : {
      "identifier":"image-dcr",
      "parent" : "image"
}
},
  "lastmod" : "2021-26-08"
}

## Wat is een DCR-bestand? ##
Een bestand met de extensie dcr bevat de inhoud van een digitale foto die is opgeslagen in de Kodak Digital Camera RAW (DCR)-indeling. De DCR is een afkorting voor **Digital Camera Raw**; bevat de niet-gecomprimeerde en verliesvrije versie van de afbeeldingsgegevens die zijn vastgelegd met een Kodak digitale camera. De professionele fotografen gebruiken deze bestanden graag, omdat ze afbeeldingen met een hogere kwaliteit opslaan dan gecomprimeerde afbeeldingsformaten van lage kwaliteit.

## DCR-bestandsindeling
De DCR is een eigen formaat ontwikkeld door Eastman Kodak Company; kortweg Kodak genoemd. Een Digital Camera Raw (DCR)-beeldbestand bevat minimaal verwerkte gegevens van de beeldsensor een digitale camera. Deze bestanden zijn nog niet verwerkt en zijn daarom niet klaar om te worden afgedrukt of bewerkt met een grafische bitmap-editor.
Gewoonlijk verwerkt een raw-converter de afbeelding in een interne kleurruimte met een groot kleurbereik, waar nauwkeurigheid en verfijning kunnen worden aangebracht voordat deze wordt omgezet naar een rasterbestandsindeling zoals TIFF of JPEG voor opslag, afdrukken of verdere manipulatie.
### Bestandsinhoud
De structuur van onbewerkte bestanden volgt vaak een generiek patroon:
- Een korte bestandsheader die een indicator bevat van de byte-volgorde van het bestand.
- Metadata van camerasensoren die nodig zijn om de sensorbeeldgegevens te interpreteren, inclusief de attributen van de CFA, de grootte van de sensor en het kleurprofiel.
- Metadata van afbeeldingen die nuttig kunnen zijn voor opname in elke CMS-omgeving of database. Sommige onbewerkte bestanden bevatten een gestandaardiseerde metadatasectie met gegevens in Exif-formaat.
- Een miniatuurafbeelding.
- Een JPEG-conversie op volledige grootte van de afbeelding, die wordt gebruikt om een voorbeeld van het bestand op het LCD-paneel van de camera te bekijken.
- In het geval van filmscans, ofwel de tijdcode, sleutelcode of framenummer in de bestandsreeks die de framereeks op een gescande spoel vertegenwoordigt.
- De sensorbeeldgegevens
### Sensorbeeldgegevens
Het onbewerkte bestand speelt de rol in de digitale fotografie, net zoals fotografische film speelt in filmfotografie. Raw-bestanden bevatten dus de volledige resolutiegegevens zoals uitgelezen van elk van de beeldsensorpixels van de camera. De sensor van de camera is bijna constant bedekt met een CFA (Color Filter Array. Het kan worden gebruikt in beeldconversie met hoog dynamisch bereik wanneer onbewerkte gegevens beschikbaar zijn; als een eenvoudiger alternatief voor de multi-exposure HDI-benadering van het vastleggen van drie afzonderlijke afbeeldingen.


## Referenties ##

* [Indeling onbewerkte afbeelding - Door Wikipedia](https://en.wikipedia.org/wiki/Raw_image_format)
* [Wat is een DCR-bestand](https://expertphotography.com/dcr-file/)

