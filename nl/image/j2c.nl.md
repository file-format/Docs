{
  "date" : "2019-10-11",
  "keywords" :[ "j2c-bestand", "j2c-bestandsindeling", "wat is een j2c-bestand", "bestand", "j2c-voorbeeld", "j2c-bestandsextensie","extensie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"J2C",
  "description":"Meer informatie over J2C-bestandsindelingen en API's die J2C-bestanden kunnen maken en openen.",
  "linktitle" : "J2C",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-02-14"
}

## Wat is een J2C-bestand?

Een bestand met de extensie .j2c is een variant van het JPEG-bestandsformaat en wordt gecomprimeerd met de wavelet-compressie. Het heeft een bijna identiek systeem van markeringen en segmenten als het JPEG 2000-bestandsformaat. Het J2C-bestandsformaat is zoals gedefinieerd in deel 1 van de JPEG 2000-standaard en ondersteunt zowel lossy als lossless compressie. De JPEG 2000-codestroom is ontworpen om te worden ingesloten in [JP2](/nl/image/jp2/) of een ander bestandsformaat, hoewel het op zichzelf in een bestand kan verschijnen. Een J2C-bestand kan worden geopend met Adobe Photoshop 2020, Adobe Illustrator 2020 en Corel Paintshop Pro.

## J2C-bestandsindeling

Het J2C-bestandsformaat is hetzelfde als dat van JPEG 2000, dat vaak wordt opgeslagen als .jp2 en .jpc. Hierdoor volgen J2C-bestanden dezelfde benadering van het coderen van metagegevens in XML-indeling, waarbij de standaard 12234-1 wordt gebruikt als referentie tussen de Exif-tags en de XML-componenten. Het is verder verbeterd door de JPEG 2000 part-2-extensie die het animatiemechanisme en de codestroomconfiguraties in één enkele afbeelding combineert. Dergelijke bestanden in uitgebreide bestandsindeling worden opgeslagen als [.jpx](/nl/image/jpx/).

### Lay-out van een JPEG2000-bestand

JPEG2000 ondersteunt een verscheidenheid aan toepassingen op basis van de conformiteit voor uitbreidbare bestandsindelingen. Hoewel het eenvoudigste type een enkele afbeelding kan bevatten, kunnen complexere typen een reeks afbeeldingen bevatten, op elkaar gestapeld of op tijd gebaseerde volgorde.

#### JP2 Doos
Het is de bouwsteen op het hoogste niveau van het JP2-bestandsformaat en bevat velden voor type en lengte in de koptekst en een gegevenssectie. Het meest opvallende type box is de aaneengesloten codestream box. Dit vak slaat in het gegevensgedeelte de JPEG2000-codestroom op.

#### JPEG2000 CodeStream

De JPEG2000 CodeStream is een reeks bytes die nodig is om de gecomprimeerde JPEG2000-afbeelding te decoderen. Als het bestand niets anders heeft dan deze codestream, wordt het een raw codestream-bestand genoemd. Gewoonlijk is een JPEG-codestroom de toepassing van het JPEG2000-compressie-algoritme op een afbeelding, hoewel dit niet de enige manier is.

#### Tegeldelen ####

Een JPEG2000-gecodeerde afbeelding is een verzameling gegevenseenheden die pakketten worden genoemd. Deze pakketten worden bijgehouden in de codestroom binnen pakketgroepen die tile-parts worden genoemd. Voordat een afbeelding wordt gecodeerd, verdeelt de encoder de afbeelding in een rechthoekig raster van blokken, tegels genoemd, waarbij elke tegel afzonderlijk wordt gecodeerd, ongeacht andere tegels.

{{< figure src="../JPEG2000_Codestream.png" alt="JPEG2000-bestandsindeling" >}}

## J2C-compressie
JPEG 2000 maakt gebruik van wavelet-compressietechnologie, waardoor het snel is gebaseerd op het feit dat er relatief weinig pixels worden weergegeven in welk kijkvenster of venster de kijker het beeld ook weergeeft. Dit kan worden benadrukt door het feit dat bij zeer grote afbeeldingen (in gigabytes) slechts enkele megabytes aan pixels op het scherm verschijnen. Dit helpt om snel alleen dat deel van de beeldgegevens op te halen en weer te geven dat nodig is om de weergavepixels te vullen. Dit vereist ook high-speed decompressietechnologie om het beeldophaalmechanisme te versnellen voor het creëren van de beelden die nodig zijn tijdens de vlucht.

J2C maakt gebruik van snelle decompressie en haalt alleen noodzakelijke informatie voor pixelgegevens op om een deel van zichtbare afbeeldingen snel op de schermen weer te geven. J2C is in de eerste plaats ontworpen voor het bekijken van gegevens en niet voor het bewerken ervan.

## J2C-identificatie
JPEG 2000-bestanden hebben handtekeningbytes `FF 4F FF 51`.

### Mime-typen
Geregistreerde Mime-typen voor JPEG 2000-bestanden zijn onder meer:
* afbeelding/j2c
* afbeelding/jpx
* afbeelding/jpm
* video/mj2

## Verbeteringen ten opzichte van de JPEG-standaard
Verbeteringen ten opzichte van de JPEG-standaard zijn onder meer:
* Superieure compressieprestaties
* Meerdere resolutie weergave
* Progressieve transmissie per pixel en resolutienauwkeurigheid
* Keuze uit lossless of lossy compressie
* Foutbestendigheid, flexibele bestandsindeling
* Ondersteuning voor hoog dynamisch bereik
* Zijkanaal ruimtelijke informatie

## Referenties ##
* [Taubman, David; Marcellin, Michael (2012)](https://books.google.com/books?id=y7HeBwAAQBAJ&pg=PA402)

