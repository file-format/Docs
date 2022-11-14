{
  "date" : "2019-12-09",
  "keywords" :[ "zl-bestand", "zl-bestandsformaat", "wat is een zl-bestand", "bestand", "zl-voorbeeld", "zl-bestandsextensie","extensie", "formaat"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ZL - ZLIP gecomprimeerd bestandsformaat",
  "description":"Meer informatie over ZL-bestandsindelingen en API's die ZL-bestanden kunnen maken en openen.",
  "linktitle" : "ZL",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-14"
}

## Wat is een ZL-bestand?

Een bestand met de extensie .zl is een ZLIP-gecomprimeerd bestandsformaat dat een variant van het DEFLATE-compressiealgoritme gebruikt voor het comprimeren van bestanden. Het is onafhankelijk van het CPU-type, het besturingssysteem, het bestandssysteem en de tekenset en kan daarom worden gebruikt voor het uitwisselen van informatie. Technische specificaties van ZLIP-compressie zijn beschikbaar op de [IETF-site](https://tools.ietf.org/html/rfc1950) en kunnen worden geraadpleegd vanuit het perspectief van de ontwikkelaar.

## ZL-bestandsindeling

Een zlib-stream heeft de volgende structuur:

* `CMF (Compression Method and flags)` - Deze byte is verdeeld in een 4-bits compressiemethode en een 4-bits informatieveld, afhankelijk van de compressiemethode.
```
bits 0 to 3  CM     Compression method
bits 4 to 7  CINFO  Compression info
```
* `CM (Compressiemethode)` - Het identificeert de compressiemethode die in het bestand wordt gebruikt. De waarden en bijbehorende compressiemethode zijn als volgt.

| CM-waarde| Compressie|
|---|---|
|CM = 8|DEFLATE met een venstergrootte tot 32K|
|CM = 15|Gereserveerd|

* `CINFO (Compressie-info)` - Voor CM = 8 is CINFO de logaritme met grondtal-2 van de LZ77-venstergrootte, minus acht (CINFO=7 geeft een 32K-venstergrootte aan).

* `FLG (FLaGs)` - Deze vlagbyte is als volgt verdeeld:
```
  bits 0 to 4  FCHECK  (check bits for CMF and FLG)
  bit  5       FDICT   (preset dictionary)
  bits 6 to 7  FLEVEL  (compression level)
````

## Referenties ##

* [Zlib-bestandsformaatspecificaties](https://tools.ietf.org/html/rfc1950)

