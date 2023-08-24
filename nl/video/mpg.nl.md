{
  "date" : "2021-04-15",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MPG-bestandsindeling",
  "keywords" :[ "MPG", "bestand", "extensie", "formaat", "videoformaat", "wat is een mpg-bestandsformaat", "mpg-bestandsformaat", "mpg-bestandsspeler", "mpeg-compressie", "video ", "MPEG", "MPEG-1", "MPEG-2"],
  "description":"Meer informatie over MPG-bestandsindeling en API's die kunnen maken en laten zien hoe u de MPG-bestanden opent.",
  "linktitle" : "MPG",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-07-26"
}

## Wat is een MPG-bestandsformaat? ##

Het bestand met de extensie .mpg behoort tot de groep bestandsextensies voor MPEG-1 of MPEG-2 audio- en videocompressie. MPEG-1 Part 2 video is niet gemakkelijk beschikbaar, en deze extensie (MPG-bestandsformaat) verwijst meestal naar een MPEG-programmastroom die is gedefinieerd in MPEG-1 en MPEG-2, of een MPEG-transportstroom die is gedefinieerd in MPEG-2 . Er bestaan ook andere extensies zoals .m2ts die de juiste container specificeren, in dit geval MPEG-2 TS, maar dit heeft weinig relevantie voor MPEG-1-media. De [.mp3](/audio/mp3/) is de meest voorkomende extensie voor bestanden die MP3-audio bevatten. Een MP3-bestand is een typische stroom van onbewerkte audio; de traditionele manier om MP3-bestanden te taggen is door streamgegevens naar "vuilnis"-segmenten van elk frame te schrijven, die de media-informatie opslaan maar worden weggegooid door de **mpg-bestandsspeler**. Dit is een vergelijkbare techniek die wordt gebruikt om de AAC-bestanden te taggen, maar tegenwoordig minder ondersteund.

## MPEG-compressie ##

De naam MPEG staat voor Moving Pictures Experts Group. MPEG is een hulpmiddel voor videocompressie, waarbij afbeeldingen en geluiden worden gecomprimeerd en beide worden gesynchroniseerd.
Er zijn momenteel verschillende MPEG-standaarden.

- MPEG-1 wordt voorgesteld voor intermediaire datasnelheden, in de orde van 1,5 Mbit/sec.
- MPEG-2 wordt voorgesteld voor hoge datasnelheden van minimaal 10 Mbit/sec.
- MPEG-3 werd voorgesteld voor HDTV-compressie, maar bleek overbodig te zijn en werd samengevoegd met MPEG-2.
- MPEG-4 wordt voorgesteld voor zeer lage datasnelheden van minder dan 64 Kbit/sec.


## Programmastroom van MPG-bestandsformaat ##

De programmastroom is een container voor het multiplexen van digitale audio, video en meer. Het formaat van de programmastream wordt gespecificeerd in het 1e deel van MPEG-1 (ISO/IEC 11172-1) en het 1e deel van MPEG-2, Systems (ISO/IEC-standaard 13818-1/ITU-T H.222.0). De MPEG-2 Program Stream is analoog-gebaseerd en vergelijkbaar met ISO/IEC 11172 Systems Layer en voorwaarts compatibel.

### Coderingsdetails ###

Hier zijn de coderingsdetails van het gedeeltelijke MPEG-2 Program Stream pack-headerformaat:

| Naam | Aantal bits | Beschrijving |
---|---|---|
| sync bytes | 32 | 0x000001BA |
| markeringsbits | 2 | 01b voor MPEG-2-versie. De markeringsbits voor de MPEG-1-versie zijn 4 bits met de waarde 0010b. |
| Systeemklok [32..30] | 3 | Systeemklokreferentie (SCR) bits 32 tot 30 |
| markeringsbit | 1 | 1 bit altijd ingesteld. |
| Systeemklok [29..15] | 15 | Systeemklokbits 29 tot 15 |
| markeringsbit | 1 | 1 bit altijd ingesteld. |
| Systeemklok [14..0] | 15 | Systeemklokbits 14 tot 0 |
| markeringsbit | 1 | 1 bit altijd ingesteld. |
| SCR-extensie | 9 | |
| markeringsbit | 1 | 1 bit altijd ingesteld. |
| bitsnelheid | 22 | In eenheden van 50 bytes per seconde. |
| markeringsbits | 2 | 11 bits altijd ingesteld. |
| gereserveerd | 5 | gereserveerd voor toekomstig gebruik |
| vulling lengte | 3 | |
| bytes vullen | 8 * vulling lengte | |
| systeemkop (optioneel) | 0 of meer | als de startcode van de systeemkop volgt: 0x000001BB |

De volgende tabel toont het gedeeltelijke systeemkopformaat:

| Naam | Aantal bytes | Beschrijving |
---|---|---|
| sync bytes | 4 | 0x000001BB |
| kop lengte | 2 | |
| snelheidsgebonden en markeringsbits | 3 | |
| audio gebonden en vlaggen | 1 | |
| vlaggen, markeringsbit en videogebonden | 1 | |
| Pakketsnelheidsbeperking en gereserveerde byte | 1 | |


## Referenties ##

- [MPEG-1 - Wikipedia](https://en.wikipedia.org/wiki/MPEG-1)



