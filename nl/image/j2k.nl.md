{
  "date" : "2019-10-11",
  "keywords" :[ "j2k-bestand", "j2k-bestandsindeling", "wat is een j2k-bestand", "bestand", "j2k-voorbeeld", "j2k-bestandsextensie","extensie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"J2K",
  "description":"Meer informatie over J2K-bestandsindeling en API's die J2K-bestanden kunnen maken en openen.",
  "linktitle" : "J2K",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-08-03"
}

## Wat is een J2K-bestand?

Een **J2K**-bestand is een afbeelding die is gecomprimeerd met wavelet-compressie in plaats van DCT-compressie. Dit bestandsformaat wordt gebruikt door de Joint Photographic Experts Group (JPEG) 2000-bestanden. J2K-bestanden slaan metadata-informatie over het afbeeldingsbestand op in XML, in tegenstelling tot .jpeg of .jpg die voor dit doel het EXIF-formaat gebruiken. J2K-bestanden ondersteunen 15-bits kleur, alfatransparantie en verliesvrije compressie. Er bestaan verschillende commerciële API's om JPEG 2000-afbeeldingen te decoderen, zoals J2K-Codec. Een J2K-bestand kan worden geopend op Windows OS met behulp van de standaard afbeeldingsviewers.

## J2K-bestandsindeling ##

Het J2K-bestandsformaat is hetzelfde als dat van JPEG 2000, dat vaak wordt opgeslagen als .jp2 en .jpc. Hierdoor volgen J2K-bestanden dezelfde benadering van het coderen van metagegevens in XML-indeling, waarbij de standaard 12234-1 wordt gebruikt als referentie tussen de Exif-tags en de XML-componenten. Het is verder verbeterd door de JPEG 2000 part-2-extensie die het animatiemechanisme en de codestreamconfiguraties in één enkele afbeelding combineert. Dergelijke bestanden in uitgebreide bestandsindeling worden opgeslagen als .jpx.

### Lay-out van een JPEG2000-bestand ###

JPEG2000 ondersteunt een verscheidenheid aan toepassingen op basis van de conformiteit voor uitbreidbare bestandsindelingen. Hoewel het eenvoudigste type een enkele afbeelding kan bevatten, kunnen complexere typen een reeks afbeeldingen bevatten, op elkaar gestapeld of op tijd gebaseerde volgorde.

#### JP2 Doos ####
Het is de bouwsteen op het hoogste niveau van het JP2-bestandsformaat en bevat velden voor type en lengte in de koptekst en een gegevenssectie. Het meest opvallende type box is de aaneengesloten codestream-box. Dit vak slaat in het gegevensgedeelte de JPEG2000-codestroom op.

#### JPEG2000 CodeStream ####

De JPEG2000 CodeStream is een reeks bytes die nodig is om de gecomprimeerde JPEG2000-afbeelding te decoderen. Als het bestand niets anders heeft dan deze codestream, wordt het een raw codestream-bestand genoemd. Gewoonlijk is een JPEG-codestroom de toepassing van het JPEG2000-compressie-algoritme op een afbeelding, hoewel dit niet de enige manier is.

#### Tegeldelen ####

Een JPEG2000-gecodeerde afbeelding is een verzameling gegevenseenheden die pakketten worden genoemd. Deze pakketten worden bijgehouden in de codestroom binnen pakketgroepen die tile-parts worden genoemd. Voordat een afbeelding wordt gecodeerd, verdeelt de encoder de afbeelding in een rechthoekig raster van blokken, tegels genoemd, waarbij elke tegel afzonderlijk wordt gecodeerd, ongeacht andere tegels.

{{< figure src="../JPEG2000_Codestream.png" alt="JPEG2000-bestandsindeling" >}}

## J2K-compressie ##
JPEG 2000 maakt gebruik van wavelet-compressietechnologie, waardoor het snel is gebaseerd op het feit dat er relatief weinig pixels worden weergegeven in welk kijkvenster of venster de kijker het beeld ook weergeeft. Dit kan worden benadrukt door het feit dat bij zeer grote afbeeldingen (in gigabytes) slechts enkele megabytes aan pixels op het scherm verschijnen. Dit helpt om snel alleen dat deel van de beeldgegevens op te halen en weer te geven dat nodig is om de weergavepixels te vullen. Dit vereist ook high-speed decompressietechnologie om het beeldophaalmechanisme te versnellen voor het creëren van de beelden die nodig zijn ter plekke.

J2K profiteert van snelle decompressie en haalt alleen noodzakelijke informatie op voor pixelgegevens om een deel van zichtbare afbeeldingen snel op de schermen weer te geven. J2K is in de eerste plaats ontworpen voor het bekijken van gegevens en niet voor het bewerken ervan.

## J2K-identificatie ##
JPEG 2000-bestanden hebben handtekeningbytes 6A 50 20 20.

### Mime-types ###
Geregistreerde Mime-typen voor JPEG 2000-bestanden zijn onder meer:
* afbeelding/jp2
* afbeelding/jpx
* afbeelding/jpm
* video/mj2

## Verbeteringen ten opzichte van de JPEG-standaard ##
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

