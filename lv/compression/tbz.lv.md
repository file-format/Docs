{
  "date": "2019-10-11",
  "keywords": [
"tbz failu",
"tbz faila formātā",
"kas ir tbz fails",
"failu",
"tbz piemērs",
"tbz faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "TBZ — Bzip saspiestais darvas arhīvs",
  "description": "Uzziniet par TBZ failu formātu un API, kas var izveidot un atvērt TBZ failus.",
  "linktitle": "TBZ",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-tb-lvz"
}
},
  "lastmod": "2021-04-05"
}

## Kas ir TBZ fails?

Fails ar paplašinājumu .tbz ir saspiests arhīvs, kas izmanto BZIP saspiešanu, lai samazinātu satura failu lielumu. TBZ faili patiesībā ir UNIX [TAR](/compression/tar/) arhivēti faili, kas pēc tam tiek saspiesti ar BZIP. Jaunākā otrā līmeņa saspiešana ir [BZIP2](/compression/bz2/), kas aizstāja BZIP. TBZ faila formāts ir piemērots lielu failu pārsūtīšanai. TBZ failus var atvērt/izvilkt, izmantojot tādas lietojumprogrammas kā 7-Zip, PeaZip un jZip. Linux un macOS lietotāji var arī atvērt TBZ ar komandu BZIP2 no termināļa loga.

## TBZ faila formāts

TBZ faili faktiski ir saspiesti arhīvi, kas izveidoti ar BZIP/[BZIP2](/compression/bz2/) saspiešanu. Šim faila formātam nav pieejamas oficiālas specifikācijas. Tomēr neoficiāls [reverse engineered specifications](https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf) liecina, ka .bz2 straume sastāv no 4 baitu galvenes, kurai seko nulle vai vairāk saspiestu bloku.

## Atsauces Nr.

* [BZIP2 formāta specifikācijas](https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf)


