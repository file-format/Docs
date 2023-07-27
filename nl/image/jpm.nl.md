{
  "date" : "2019-11-25",
  "keywords" :[ "jpm-bestand", "jpm-bestandsindeling", "wat is een jpm-bestand", "bestand", "jpm-voorbeeld", "jpm-bestandsextensie","extensie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JPM - JPEG 2000 samengesteld bestandsformaat",
  "description":"Meer informatie over JPM-bestandsindeling en API's die JPM-bestanden kunnen maken en openen.",
  "linktitle" : "JPM",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-02-08"
}

## Wat is een JPM-bestand?

JPM verwijst naar het JPEG 2000-beeldcoderingssysteem Deel 6 dat wordt gebruikt voor documentbeeldvorming. Het is gebaseerd op de Mixed Raster Content Standard (ISO/IEC 16485) en bevat gelaagde stilstaande beelden die JPEG 2000 en andere coderingen gebruiken. Naast zijn eigen specificaties, erft het JPM-bestandsformaat functies van zijn ouder, namelijk het [jp2](/nl/image/jp2/) bestandsformaat.

## JPM-bestandsindeling

Het JPM-bestandsformaat wordt gedefinieerd door [ISO/IEC 15444-6:2003](https://www.iso.org/standard/61124.html) -- de JPEG 2000-afbeelding coderingssysteem -- Deel 6: Samengesteld beeldbestandsformaat. Een samengestelde afbeelding kan gescande afbeeldingen, synthetische afbeeldingen of beide bevatten, waarvoor een combinatie van continue toon- en bi-level compressiemethoden nodig zijn. Het JPM-bestandsformaat definieert een compositiemodel dat de methode beschrijft voor het combineren van meerdere afbeeldingen om een samengestelde afbeelding te genereren met behulp van het multi-layer Mixed Raster Content (MRC) beeldvormingsmodel, gedefinieerd in ITU-T T.44 | ISO/IEC16485.

### JPM-specificaties
De JPM-bestandsindelingsstandaard specificeert dat het een binaire container is om een samengestelde afbeelding weer te geven waarmee meerdere afbeeldingen kunnen worden gecombineerd tot een enkele afbeelding. Het stelt het mechanisme in voor het groeperen van meerdere afbeeldingen in een hiërarchie van lay-outobjecten, pagina's en paginaverzamelingen om JPEG 2000 en andere gecomprimeerde afbeeldingsgegevensformaten op te slaan. Het formaat omvat het mechanisme van het opnemen van metadata (vaak aangeduid als structurele metadata in digitale bibliotheekprojecten).

## Referenties

* [ITU-T Rec. T.805](https://www.itu.int/rec/T-REC-T.805/en)
* [ISO/IEC 15444-6:2013](https://www.iso.org/standard/61124.html)
* [Wikipedia:JPEG 2000](https://en.wikipedia.org/wiki/JPEG_2000)

