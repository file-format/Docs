{
  "date": "2022-04-01",
  "keywords": [
"nkit failu",
"nkit faila formātā",
"kas ir nkit fails",
"failu",
"nkit piemērs",
"nkit faila paplašinājums",
"pagarinājumu",
"formātā",
"nkit kājene",
"nkit faila formāts"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par NKIT faila formātu un API, kas var izveidot un atvērt NKIT failus.",
  "title": "NKIT - diska attēla faila formāts",
  "linktitle": "NKIT",
  "menu": {
    "docs": {
      "parent": "disc-and-media",
      "identifier": "disc-and-media-nki-lvt"
}
},
  "lastmod": "2022-04-01"
}

## Kas ir NKIT fails?

NKIT fails ir no NintendoWii un GameCube spēlēm iegūto datu diska attēls. NKIT ir paredzēts Nintendo Toolkit formātam. Iegūtajā saspiešanas failā [ISO](/compression/iso/) tiek izmantoti galvenie šo spēļu dati, lai tās palaistu ar emulatora programmām, piemēram, Dolphin, Swiss un Nintendont. NKit ir pieejams neapstrādātos (iso) un saspiestos (gcz) failu formātos, kas tika izstrādāti, ņemot vērā atskaņojamību un izmēru.

## NKIT faila formāts

NKit faila formāts ir nezaudējošs formāts, un to izmanto Nintendo Wii un GameCube attēlu samazināšanai un atjaunošanai. Formāti ir pieejami ISO un GCZ failu formātos katrai GameCube un Wii spēlei.

|Sistēma |Formāts |Atbalstīta aparatūra |Atbalstīts Dolphin |Atjaunojams 1:1 |Piezīmes|
---|---|---|---|---|---|
|GameCube| nkit.iso| Jā |Jā| Jā |Tas pats kā kompaktais GameCube iso|
|GameCube| nkit.gcz| Nē| Jā| Jā |GCZ ir paša Dolphin bloku meklējamais saspiešanas formāts|
|Wii| nkit.iso| Nē Jā| Jā| RVT-H formātā var atskaņot tikai Dolphin|
|Wii| nkit.gcz| Nē Jā| Jā| RVT-H GCZ spēlē tikai Dolphin|

### NKIT galvene

NKIT faila formāta galvene ir šāda.

|Nobīde |Garums |Vārds|
---|---|---|
|0x200 |0x4 |NKit galvene 'NKIT'|
|0x204 |0x4 |NKit versija ' v01'|
|0x208 |0x4 |Avota attēla oriģināls CRC32|
|0x20C |0x4 |NKit CRC — padara NKit failu CRC32 vienādu ar avota CRC pie 0x208 (pie 0x4 GCZ)|
|0x210 |0x4 |Avota attēla garums|
|0x214 |0x4 |Forced Junk ID (ja diska ID atšķiras — reti — tikai GameCube)|
|0x218 |0x4 |Wii atjauniniet CRC32 nodalījumu, ja konvertēšanas laikā tiek noņemts|

## Atsauces Nr.

* [NKIT faila formāts — gbatemp](https://wiki.gbatemp.net/wiki/NKit/NKitFormat)


