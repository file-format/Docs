{
  "date": "2022-04-01",
  "keywords": [
"nkit fil",
"nkit filformat",
"hvad er en nkit-fil",
"fil",
"nkit eksempel",
"nkit filtypenavn",
"udvidelse",
"format",
"nkit sidefod",
"filformat af nkit"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om NKIT filformat og API'er, der kan oprette og åbne NKIT filer.",
  "title": "NKIT - Diskbilledfilformat",
  "linktitle": "NKIT",
  "menu": {
    "docs": {
      "parent": "disc-and-media",
      "identifier": "disc-and-media-nki-dat"
}
},
  "lastmod": "2022-04-01"
}

## Hvad er en NKIT fil?

En NKIT-fil er et diskbillede af data udtrukket fra NintendoWii- og GameCube-spil. NKIT er til Nintendo Toolkit-format. Den resulterende komprimeringsfil [ISO](/compression/iso/) bruger hoveddataene fra disse spil til at blive kørt med emulatorprogrammer som Dolphin, Swiss og Nintendont. NKit kommer i rå (iso) og komprimerede (gcz) filformater, som begge er designet med henblik på afspilning og størrelse.

## NKIT filformat

NKit-filformatet er et format uden tab og bruges til at formindske og gendanne Nintendo Wii- og GameCube-billeder. Formaterne er tilgængelige i ISO- og GCZ-filformater for hvert af GameCube- og Wii-spil.

|System |Format |Hardware Understøttet |Dolphin Understøttet |Gendannelsesbar 1:1 |Noter|
---|---|---|---|---|---|
|GameCube| nkit.iso| Ja |Ja| Ja |Samme som komprimeret GameCube iso|
|GameCube| nkit.gcz| Nej| Ja| Ja |GCZ er Dolphin's eget bloksøgningskompressionsformat|
|Wii| nkit.iso| Nej Ja| Ja| RVT-H-format kan kun afspilles i Dolphin|
|Wii| nkit.gcz| Nej Ja| Ja| RVT-H i GCZ kan kun afspilles i Dolphin|

### NKIT Header

NKIT-filformatets overskrift er som følger.

|Offset |Længde |Navn|
---|---|---|
|0x200 |0x4 |NKit Header 'NKIT'|
|0x204 |0x4 |NKit Version 'v01'|
|0x208 |0x4 |Kildebillede original CRC32|
|0x20C |0x4 |NKit CRC - gør NKit-filen CRC32 lig med kilde-CRC ved 0x208 (ved 0x4 i GCZ)|
|0x210 |0x4 |Længde af kildebillede|
|0x214 |0x4 |Tvungen junk-id (når disk-id afviger - sjældent - kun GameCube)|
|0x218 |0x4 |Wii Opdater partition CRC32, hvis den fjernes ved konvertering|

## Referencer ##

* [NKIT-filformat - af gbatemp](https://wiki.gbatemp.net/wiki/NKit/NKitFormat)


