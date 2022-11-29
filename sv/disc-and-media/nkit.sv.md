{
  "date" : "2022-04-01",
  "keywords" :[ "nkit-fil", "nkit-filformat", "vad är en nkit-fil", "fil", "nkit-exempel", "nkit filtillägg", "tillägg", "format", "nkit sidfot", "fil format för nkit"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Läs mer om NKIT-filformat och API:er som kan skapa och öppna NKIT-filer.",
  "title" :"NKIT - Disk Image File Format",
  "linktitle" : "NKIT",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2022-04-01"
}

## Vad är en NKIT fil?

En NKIT-fil är en diskbild av data som extraherats från NintendoWii- och GameCube-spel. NKIT är för Nintendo Toolkit-format. Den resulterande komprimeringsfilen [ISO](/sv/compression/iso/) använder huvuddata för dessa spel för att köras med emulatorprogram som Dolphin, Swiss och Nintendont. NKit kommer i råa (iso) och komprimerade (gcz) filformat som båda designades för att hålla spelbarhet och storlek i sikte.

## NKIT filformat

NKit-filformatet är ett format utan förlust och används för att krympa och återställa Nintendo Wii- och GameCube-bilder. Formaten är tillgängliga i ISO- och GCZ-filformat för vart och ett av GameCube- och Wii-spelen.

|System |Format |Hårdvara som stöds |Dolphin stöds |Återställbar 1:1 |Anmärkningar|
---|---|---|---|---|---|
|GameCube| nkit.iso| Ja |Ja| Ja |Samma som komprimerad GameCube iso|
|GameCube| nkit.gcz| Nej| Ja| Ja |GCZ är Dolphins eget blocksökbara komprimeringsformat|
|Wii| nkit.iso| Nej Ja| Ja| RVT-H-format kan endast spelas i Dolphin|
|Wii| nkit.gcz| Nej Ja| Ja| RVT-H i GCZ kan endast spelas i Dolphin|

### NKIT Header

NKIT-filformatets rubrik är som följer.

|Offset |Längd |Namn|
---|---|---|
|0x200 |0x4 |NKit Header 'NKIT'|
|0x204 |0x4 |NKit Version ' v01'|
|0x208 |0x4 |Källbild original CRC32|
|0x20C |0x4 |NKit CRC - gör NKit-filen CRC32 lika med käll-CRC vid 0x208 (vid 0x4 i GCZ)|
|0x210 |0x4 |Källbildens längd|
|0x214 |0x4 |Tvingat skräp-ID (när skiv-ID skiljer sig - sällsynt - endast GameCube)|
|0x218 |0x4 |Wii Update-partition CRC32 om den tas bort vid konvertering|

## Referenser ##

* [NKIT-filformat - av gbatemp](https://wiki.gbatemp.net/wiki/NKit/NKitFormat)

