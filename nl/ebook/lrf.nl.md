{
  "date" : "2019-12-12",
  "keywords" :[ "LRF", "bestand", "extensie", "format", "eBook", "Digitaal boek"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Meer informatie over LRF-bestandsindeling en API's die LRF-bestanden kunnen maken en openen.",
  "title" :"LRF-bestandsindeling - Een Sony Portable Reader-bestand",
  "linktitle" : "LRF",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2019-12-12"
}

## Wat is een LRF-bestand?

Een bestand met de extensie .lrf is een Broad Band eBook (BBeB)-bestand dat gegevens bevat voor een Sony BBeB, inclusief tekst, afbeeldingen en pagineringsgegevens. Het bestand wordt opgeslagen in een gecomprimeerde binaire indeling die een koptekst, een bepaald aantal objecten en een objectindex bevat. LRF- en LRX-bestanden bevatten de twee beschikbare BBeB-boekformaten. De LRF-bestanden zijn niet versleuteld en kunnen worden samengesteld uit [LRX](/nl/ebook/lrf/)-bestanden. De LRF-bestanden kunnen worden geconverteerd vanuit verschillende andere bestandstypen, waaronder PDF en HTML. Als uw computer het LRF-bestand niet kan openen, is de software waarschijnlijk niet geïnstalleerd om de LRF-bestanden te openen of te bewerken. Programma's die LRF-bestanden kunnen openen zijn Calibre, BookDesigner, Makelrf en Canon Book Creator voor Windows, Calibre voor Linux, Calibre en Sony Reader voor Macintosh.

## Korte geschiedenis

Het LRF-bestandstype wordt in de eerste plaats geassocieerd met Line Rider door [inXile entertainment](https://en.wikipedia.org/wiki/InXile_Entertainment). De Line Rider is een natuurkundig speelgoed voor internet en werd in september 2006 uitgevonden door een Sloveense universiteitsstudent, Boštjan Čadež. eBook-eReaders van het merk Sony (zoals Sony PRS-500-lezers en Sony Librie) gebruiken de LRF-bestandsextensie voor hun documenten en teksten. Dit eigen bestandstype is nu verouderd, evenals de gerelateerde LRS- en LRX-bestanden. Die drie bestandstypen vormden het BroadBand eBook (BBeB) dat in 2010 werd stopgezet toen Sony hun e-boeken in het EPUB-formaat begon te verkopen.

## LRF-bestandsindeling

Gedetailleerde specificaties van het LRF-bestandsformaat zijn beschikbaar op [webarchief](https://web.archive.org/web/20110809071744/http://www.sven.de/librie/Librie/LrfFormat). Een LRF-bestand bestaat uit:
* een kop
* een aantal objecten
* een objectindex.

Al deze waarden zijn in Intel (LSB eerste) volgorde.

### LRF-koptekst

|Offset (hex) |Size(bytes) |Naam/betekenis| Voorbeeldwaarde|
---|---|---|---|
|0 |8| LRF-handtekening| 4C 00 52 00 46 00 00 00 = "LRF" in Unicode|
|8 |2| versie?| 999 in de meeste bestanden|
|A |2| "Psuedo-codering" |keybyte 48|
|0C |4| RootObjectID| 0x0044|
|10 |8| AantalObjecten |342|
|18 |8| ObjectIndexOffset| 0x00093440|
|20 |4| onbekend| 0|
|24 |1| Vlaggen| (16 - van achteren naar voren, 1 = van voren naar achteren) 16|
|25 |1| onbekend |(padding?) 0|
|26 |2| onbekend| 1600|
|28 |2| onbekend| (vulling?) 0|
|2A |2| Hoogte?| 600|
|2C |2| Breedte?| 800|
|2E |1| onbekend| 24|
|2F |1| onbekend |(padding?) 0|
|30 |0x14| onbekend| nullen|
|44 |4| Object-ID van alleen PlaneStream (0x1E) object| 0x0042|
|48 |4| onbekend |0x1536|
|4C |2| XMLCompSize| 0x035C|


## Referenties

* [LRF-bestandsindeling](https://web.archive.org/web/20110809071744/http://www.sven.de/librie/Librie/LrfFormat)
* [BBeB - Door Wikipedia](https://en.wikipedia.org/wiki/BBeB)

