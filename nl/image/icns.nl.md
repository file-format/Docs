{
  "date" : "2021-06-29",
  "keywords" :[ "ICNS", "extensie", "bestand", "format", "afbeelding", "Apple Icon Image", "macOS", "Apple", "Icon"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ICNS - Apple-pictogramafbeelding",
  "description":"Meer informatie over ICNS-bestandsindelingen en API's die ICNS-bestanden kunnen maken en openen.",
  "linktitle" : "ICNS",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-06-29"
}

## Wat is een ICNS-bestand? ##

Een pictogramformaat dat door macOS-programma's wordt gebruikt, wordt een ICNS-bestand genoemd. Het staat 1-bits en 8-bits alfabanden toe en slaat een of meer afbeeldingen op, meestal gemaakt van [PNG](/nl/image/png/)-documenten. Het programmapictogram in de macOS-browser en -interface wordt weergegeven met behulp van ICNS-bestanden.

Op basis van de locatie kan hetzelfde stijlicoon meerdere instellingen hebben. Het ICNS-formaat heeft talloze wijzigingen ondergaan en is zo geëvolueerd dat het nu kan worden gebruikt als basis voor verschillende compatibele formaten. Hier zijn enkele andere belangrijke punten die u moet weten:

* IconFamily Resource, Macintosh Icon, Macintosh OS X Icon, Mac OS Icon, Apple Icon, Mac OS X Icon Resource en Mac OS iconen Resource zijn enkele van de andere namen.
* Voor pictograminformatie wordt een bron in de resource branch gebruikt.
* In de meeste gevallen bevat een bestand meerdere afbeeldingen. 1612 pixels vierkant en 1024, 512, 256, 128, 48, 32 en 16 pixels vierkant zijn ondersteunde afbeeldingsformaten.


## ICNS-bestandsindeling ##

Het ICNS-gegevensformaat is een capsule voor een of meer afbeeldingen, die 1-bit-banden en talrijke afbeeldingsstatussen ondersteunt.
Het besturingssysteem kan de grootte van pictogramafbeeldingen aanpassen aan de vereiste weergavegrootte. De grotere pictogramafbeeldingen worden meestal opgeslagen als [JPEG](/nl/image/jpeg/) 2000- of [PNG](/nl/image/png/)-bestanden. Een type van zowel gecomprimeerde als niet-gecomprimeerde ICNS-bestanden is mogelijk.

Een header en binaire pictogramgegevens vormen de structuur van een ICNS-bestand. De header bevat 8 bytes aan gegevens, waarvan vier de magische letterlijke waarde en vier de lengte van het bestand. Het type en de grootte van elke pictogramafbeelding worden opgeslagen in de pictogramgegevenssectie, gevolgd door de binaire afbeeldingsgegevens. De afbeeldingsgrootte bepaalt de grootte van de binaire sectie.

## Technische specificatie ##

### Koptekst ###

|Offset|Grootte|Doelstelling
---|---|---|
|0|4|Magische letterlijke waarde, moet "icns" zijn (0x69, 0x63, 0x6e, 0x73)
|4|4|Lengte van bestand, in bytes, msb eerst


### Pictogramgegevens ###

|Offset|Grootte|Doelstelling
---|---|---|
|0|4|Icoontype
|4|4|Lengte van gegevens, in bytes (inclusief type en lengte), msb eerst
|8|Variabele|Pictogramgegevens

### Compressie ###

De pixelgegevens zijn tot op zekere hoogte gecomprimeerd. De 32-bits ("is32", "il32", "ih32", "it32") en ARGB ("ic04", "ic05") pixels worden vaak gecomprimeerd (per kanaal) op een vergelijkbare manier als PackBits.

|Leadwaarde|Staartbytes|Resultaat (ongecomprimeerd)
---|---|---|
|0 - 127|1 - 128|1 - 128 Bytes
|128 - 255|1 byte|3 - 130 kopieën

## Referentie ##

* [ICNS - Wikipedia](https://en.wikipedia.org/wiki/Apple_Icon_Image_format)

