{
  "date": "2021-04-08",
  "keywords": [
"lz4 fil",
"lz4 filformat",
"hvad er en lz4 fil",
"fil",
"lz4 eksempel",
"lz4 filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "LZ4 - LZ4 komprimeret filformat",
  "description": "Lær om LBR filformat og API'er, der kan oprette og åbne LZ4 filer.",
  "linktitle": "LZ4",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-lz-da4"
}
},
  "lastmod": "2021-04-19"
}

## Hvad er en LZ4 fil?

En fil med filtypenavnet .lz4 er en komprimeret arkivfil, der er oprettet med programmer/værktøjer, der understøtter [LZ4](https://en.wikipedia.org/wiki/LZ4_(compression_algorithm)) komprimering. LZ4-algoritmen fokuserer på afvejning mellem hastighed og kompressionsforhold. Komprimerede LZ4-arkiver kan oprettes ved hjælp af LZ4-kommandolinjeværktøjet og kan dekomprimeres ved hjælp af det samme.

## LZ4 filformat

LZ4-filformatet, baseret på LZ4-komprimeringsalgoritmen, er uafhængigt af CPU-type, operativsystem, filsystem og tegnsæt. Den er velegnet til filkomprimering og streamingkomprimering ved hjælp af LZ4-algoritmen. Den indledende implementering af LZ4-formatet blev udført på sproget [C](/programming/c/) af Yann Collet i 2011 og er tilgængelig for udviklerens reference på [Github](https://github.com/lz4/lz4).

### LZ4-rammeformat

Den generelle struktur af LZ4-filformatet er som vist nedenfor.

|MagicNb|F. Beskrivelse| Bloker|(...)|EndMark |C. Kontrolsum|
---|---|---|---|---|---|
|4 bytes| 3-15 bytes||| 4 bytes| 0-4 bytes|

#### Magisk tal

4 bytes, lille endian-format. Værdi: 0x184D2204

#### Rammebeskrivelse

Rammebeskrivelsen består af 3 t0 15 bytes og er den vigtigste del af specifikationerne. Tilsammen omtales felterne Magic_Number og Frame_Descriptor som LZ4 Frame Header, og størrelsen varierer mellem 7 og 19 bytes. Det er som vist nedenfor.

|FLG| BD| (Indholdsstørrelse)| (Ordbogs-ID)| HC|
---|---|---|---|---|
|1 byte| 1 byte| 0 - 8 bytes| 0 - 4 bytes| 1 byte|

#### Datablokke

Hver datablok følger følgende rækkefølge.

|Blokstørrelse| data| (Blok kontrolsum)|
---|---|---|
|4 bytes| |0 - 4 bytes|

#### EndMark

Blokkestrømmen slutter, når den sidste datablok efterfølges af 32-bit værdien 0x00000000.

#### Indholdskontrolsum

Content_Checksum verificerer gyldigheden af indholdet, der dekodes korrekt, og udføres ved hjælp af resultatet af xxHash-32-algoritmen. Det validerer resultaterne af vellykket transmission af alle blokke i den korrekte rækkefølge og uden nogen fejl.

## Referencer

* [LZ4 Frame Format](https://github.com/lz4/lz4/blob/dev/doc/lz4_Frame_format.md)

* [LZ4-komprimeringsalgoritme - Wikipedia](https://en.wikipedia.org/wiki/LZ4_(compression_algorithm))


