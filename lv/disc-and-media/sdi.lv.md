{
  "date": "2021-08-13",
  "keywords": [
"sdi fails",
"sdi faila formātā",
"kas ir sdi fails",
"failu",
"sdi piemērs",
"sdi faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par SDI faila formātu un API, kas var izveidot un atvērt SDI failus.",
  "title": "SDI — Windows sistēmas izvietošanas attēla fails",
  "linktitle": "SDI",
  "menu": {
    "docs": {
      "parent": "disc-and-media",
      "identifier": "disc-and-media-sd-lvi"
}
},
  "lastmod": "2021-08-13"
}

## Kas ir SDI fails?
Fails ar paplašinājumu .sdi satur ielādes blob, sāknēšanas lāse un daļa blob; parasti izmanto Windows Embedded Studio, lai izveidotu RAM diskus vai sāknēšanas diskus Windows ielādei un instalēšanai. SDI ir saīsināts no sistēmas izvietošanas attēla. Windows Embedded Studio ir programma, ko izmanto, lai izveidotu diska attēlus operētājsistēmai Windows. Patiesībā šajā programmā ir SDI failu pārvaldnieka programma un komandrindas rīks **sdimgr.exe**. Abus var izmantot, lai ievietotu, izveidotu un rediģētu SDI attēlus.

## SDI faila formāts
SDI faila formāts tiek plaši izmantots, lai sistēmas sāknēšanai izmantotu virtuālo disku. Dažas Microsoft Windows versijas nodrošina **RAM sāknēšanu**, kas ir svarīgi, lai ielādētu SDI failu atmiņā un pēc tam palaistu no tā. SDI faila formāts nodrošina arī sāknēšanu tīklā, izmantojot PXE (Preboot Execution Environment). To izmanto arī cietā diska attēlveidošanai.
### SDI failu sadaļas
Pašu SDI failu var iedalīt šādās sadaļās:
- **Sāknēšanas BLOB**: tajā ir faktiskā sāknēšanas programma STARTROM.COM. Tas ir līdzīgs cietā diska sāknēšanas sektoram.
- **Ielādēt BLOB**: tas parasti satur NTLDR, un to palaiž sāknēšanas BLOB.
- **Part BLOB**: tas satur faktisko sāknēšanas izpildlaiku; ietver arī boot.ini un ntdetect.com failus, kuriem jāatrodas izpildlaika saknes direktorijā.
- **Diska BLOB**: šis ir plakans HDD attēls, kas sākas ar MBR. To izmanto cietā diska attēlveidošanai, nevis sāknēšanai. Arī ar Microsoft utilītprogrammām var uzstādīt tikai diska BLOB.


## Atsauces 

* [Sistēmas izvietošanas attēls — Wikipedia](https://en.wikipedia.org/wiki/System_Deployment_Image)



