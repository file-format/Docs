{
  "date" : "2021-04-08",
  "keywords" :[ "lz4 fil", "lz4 filformat", "vad är en lz4 fil", "fil", "lz4 exempel", "lz4 filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LZ4 - LZ4 komprimerat filformat",
  "description":"Läs mer om LBR-filformat och API:er som kan skapa och öppna LZ4-filer.",
  "linktitle" : "LZ4",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-19"
}

## Vad är en LZ4 fil?

En fil med tillägget .lz4 är en komprimerad arkivfil skapad med applikationer/verktyg som stöder [LZ4](https://en.wikipedia.org/wiki/LZ4_(compression_algorithm)) komprimering. LZ4-algoritmen fokuserar på avvägning mellan hastighet och kompressionsförhållande. Komprimerade LZ4-arkiv kan skapas med kommandoradsverktyget LZ4 och kan dekomprimeras med detsamma.

## LZ4 filformat

LZ4-filformatet, baserat på LZ4-komprimeringsalgoritmen, är oberoende av CPU-typ, operativsystem, filsystem och teckenuppsättning. Den är lämplig för filkomprimering och strömningskomprimering med LZ4-algoritmen. Den initiala implementeringen av LZ4-formatet utfördes på [C](/sv/programming/c/) språk av Yann Collet 2011 och är tillgänglig för utvecklarens referens på [Github](https://github.com/lz4/lz4) .

### LZ4 ramformat

Den allmänna strukturen för LZ4-filformatet är som visas nedan.

|MagicNb|F. Beskrivning| Block|(...)|EndMark |C. Kontrollsumma|
---|---|---|---|---|---|
|4 byte| 3-15 byte||| 4 byte| 0-4 byte|

#### Magiskt nummer

4 byte, Little endian-format. Värde: 0x184D2204

#### Frame Descriptor

Rambeskrivningen består av 3 t0 15 byte och är den viktigaste delen av specifikationerna. Tillsammans kallas fälten Magic_Number och Frame_Descriptor som LZ4 Frame Header, och dess storlek varierar mellan 7 och 19 byte. Det är som visas nedan.

|FLG| BD| (Innehållsstorlek)| (Ordbok ID)| HC|
---|---|---|---|---|
|1 byte| 1 byte| 0 - 8 byte| 0 - 4 byte| 1 byte|

#### Datablock

Varje datablock följer följande ordning.

|Blockstorlek| data| (Blockera kontrollsumma)|
---|---|---|
|4 byte| |0 - 4 byte|

#### EndMark

Flödet av block slutar när det sista datablocket följs av 32-bitarsvärdet 0x00000000.

#### Innehållskontrollsumma

Content_Checksum verifierar giltigheten av innehållet som avkodas korrekt och utförs med hjälp av resultatet av xxHash-32-algoritmen. Den validerar resultaten av framgångsrik överföring av alla block i rätt ordning och utan några fel.

## Referenser

* [LZ4 ramformat](https://github.com/lz4/lz4/blob/dev/doc/lz4_Frame_format.md)
* [LZ4-komprimeringsalgoritm - Wikipedia](https://en.wikipedia.org/wiki/LZ4_(compression_algorithm))

