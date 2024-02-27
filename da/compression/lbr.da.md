{
  "date": "2021-04-08",
  "keywords": [
"mst fil",
"mst filformat",
"hvad er en mst-fil",
"fil",
"mst eksempel",
"mst filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "LBR - LU Library Archive File Format",
  "description": "Lær om LBR-filformat og API'er, der kan oprette og åbne LBR-filer.",
  "linktitle": "LBR",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-lb-dar"
}
},
  "lastmod": "2021-04-19"
}

## Hvad er LBR fil?

En fil med filtypenavnet .lbr er en arkivfil oprettet med LU-programmet og brugt på CP/M- og DOS-operativsystemer i 1980'erne. Det bruges ikke længere og er blevet erstattet af moderne arkiveringsfilformater. Formatet komprimerer ikke medlemsfilerne og fungerer som containerarkiv for disse. Arkiveringsfunktionen blev mest brugt til overførsel af arkiverede filer over internettet. Da LBR ikke tilbød komprimering, blev andre værktøjer såsom SQ eller CRUNCH brugt til at komprimere medlemsfilerne før arkivering eller den resulterende arkivfil efter arkivering for at reducere dens størrelse.

## LBR filformat

LBR file format was designed by Gary P. Novosielski and has no technical details available publicly. LBR files start with a 0x00 byte, followed by 11 spaces (0x20), then two 0x00 bytes, then two bytes that are not both 0x00. Da det er containerfilformat, kan det udpakkes ved hjælp af LU.COM og NULU.COM.

## Referencer

* [LBR - Wikipedia](https://en.wikipedia.org/wiki/LBR_(file_format))


