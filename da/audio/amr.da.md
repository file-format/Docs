{
  "date": "2021-04-29",
  "keywords": [
"amr",
".amr",
"fil",
"udvidelse",
"format",
"hvad er en amr fil",
"musik",
"amr filformat",
"amr fil",
"konverter amr-fil til mp3",
"afspil amr-fil"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om AMR-filformat og API'er, der kan oprette, konvertere og åbne AMR-filer.",
  "title": "AMR - Adaptiv Multi-Rate Codec-fil",
  "linktitle": "AMR",
  "menu": {
    "docs": {
      "parent": "audio",
      "identifier": "audio-am-dar"
}
},
  "lastmod": "2021-04-29"
}

## Hvad er AMR fil?
Filen med .amr-udvidelsen er et lyddataformat, der er relevant for **Adaptive Multi-Rate** audio-codec; består af en multi-rate smalbånds tale-codec, som koder smalbåndssignaler ved 4,75-12,2 kbit/s bithastighed med afgiftskvalitet tale startende ved 7,4 kbit/s; bruger linktilpasning til at vælge mellem en af otte forskellige bithastigheder baseret.

## AMR filformat
AMR file format uses many coding techniques, the ACELP (Algebraic Code Excited Linear Prediction) algorithm one of the best technique; designed for compressing human spoken audio in a more efficient way. The AMR was set as the standard voice or speech codec by 3GPP in 1999. AMR-filformatet bruges også til at gemme den talte lyd ved at bruge **Adaptive Multi-Rate** audio-codec, som bruges af mange smartphones til at gemme optagede taler.

### Filformatstruktur
AMR( Adaptive Multi-Rate) er et lydformat; udbredt i forskellige mobile applikationer og enheder, typisk i lydafspiller/optager eller i VoIP applikationer. AMR kan yderligere klassificeres som:

1. AMR-NB( NarrowBand)
2. AMR-WB( WideBand)

Normalt refererer AMR til AMR-NB. AMR-filformatet har følgende struktur:

Hver AMR-fil indeholder en 6-byte header, der genkender filen som en AMR-lyd. Denne overskrift er altid indstillet til:
- 0x23
- 0x21
- 0x41
- 0x4D
- 0x52
- 0x0A

Dette er normalt simialr på tværs af alle AMR-NB-filer. Hvis overskriften følger en standard, er det sandsynligt, at filen er beskadiget og ikke bør bruges. AMR-filen består af et helt antal pakkede frames af lyd. Disse frames komponerer hver 20 ms lyd. Hver frame kan kodes ved hjælp af en af de gyldige AMR-NB-tilstande (0-7, 8 SID i DTX-tilstand). Da rammerne kan kodes ved forskellige bithastigheder, kaldes denne typiske metode Adaptive Multi-Rate (AMR).
#### AMR-tilstande
Følgende er de forskellige AMR-tilstande og deres tilsvarende bithastigheder:

|MODE| BIT PRISER|
---|---|
|0| AMR 4,75 - Koder ved 4,75 kbit/s|
|1 | AMR 5.15 - Koder ved 5.15kbit/s|
|2 | AMR 5.9 - Koder ved 5,9 kbit/s|
|3 | AMR 6.7 - Koder ved 6,7 kbit/s|
|4 | AMR 7.4 - Koder ved 7,4 kbit/s|
|5 | AMR 7,95 - Koder ved 7,95 kbit/s|
|6 | AMR 10.2 - Koder ved 10,2 kbit/s|
|7 | AMR 12.2 - Koder ved 12,2 kbit/s|

Rammestørrelse for AMR-tilstande i bytes (inklusive header-byte) er angivet nedenfor:

|CMR |MODE |FRAME STØRRELSE( i bytes )|
---|---|---|
|0 |AMR 4,75 |13|
|1 |AMR 5,15 |14|
|2 |AMR 5.9 |16|
|3 |AMR 6.7 |18|
|4 |AMR 7.4 |20|
|5 |AMR 7,95 |21|

## Referencer ##

* [Adaptive Multi-Rate audio codec - af Wikipedia](https://en.wikipedia.org/wiki/Adaptive_Multi-Rate_audio_codec)

* [RTP Payload Format og File Storage Format for AMR og AMR-WB Audio codecs](https://tools.ietf.org/html/rfc4867#page-35)


