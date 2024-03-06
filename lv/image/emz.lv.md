{
  "date": "2019-10-11",
  "keywords": [
"emz fails",
"emz faila formātā",
"kas ir emz fails",
"failu",
"emz piemērs",
"emz faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "EMZ faila formāts — Windows saspiests uzlabotais metafails",
  "description": "Uzziniet par EMZ faila formātu un API, kas var izveidot un atvērt EMZ failus.",
  "linktitle": "EMZ",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-em-lvz"
}
},
  "lastmod": "2020-10-24"
}

## Kas ir EMZ fails?

Fails ar paplašinājumu .emz ir uzlabotā metafaila ([EMF](/image/emf/) fails) saspiests konteiners. Tie tiek saspiesti, izmantojot saspiešanas metodi [GZIP](/compression/gz/), kas ir UNIX un LINUX operētājsistēmās visbiežāk izmantotā saspiešanas metode. Atsaistīt ZIP (/compression/zip/), GZIP saspiež arhīvu kopumā, nevis saspiež atsevišķus failus. EMZ faili ir mazāki, salīdzinot ar EMF failiem, un tie palīdz ātri pārsūtīt tiešsaistes failu koplietošanas laikā. Dažas lietojumprogrammas, kas var atvērt EMZ failus, ir Microsoft Visio 2019, Microsoft Office 2019, XnView MP un File Viewer Plus.

## EMZ faila formāts

EMZ faili ir [Gzip](/compression/gz/) saspiesti un satur [EMF](/image/emf/). Gzip arhīva saspiešanai izmanto algoritmu DEFLATE, un tas atšķiras saspiešanas lietošanā. EMZ failu var atspiest, izmantojot GZip saspiešanas utilītas, piemēram, GNU Zip. Faila formāts sastāv no:

 * Faila galvene
 * Izvēles galvenes
 * Saspiesti dati
 * Faila kājene

GZIP faila formāts [specifications version 4.3](https://datatracker.ietf.org/doc/html/rfc1952), ko publicējis Internet Engineering Task Force (IETF), satur detalizētu informāciju par faila formātu.

## Atsauces

 * [RFC1952: GZIP faila formāta specifikācija](https://datatracker.ietf.org/doc/html/rfc1952), [IETF](https://www.ietf.org/)
 * [Windows MetaFile — Wikipedia](https://en.wikipedia.org/wiki/Windows_Metafile)

