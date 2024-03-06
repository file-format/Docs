{
  "date": "2019-12-09",
  "keywords": [
"zl failu",
"zl faila formātā",
"kas ir zl fails",
"failu",
"zl piemērs",
"zl faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ZL — ZLIP saspiestā faila formāts",
  "description": "Uzziniet par ZL faila formātu un API, kas var izveidot un atvērt ZL failus.",
  "linktitle": "ZL",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-z-lvl"
}
},
  "lastmod": "2021-04-14"
}

## Kas ir ZL fails?

Fails ar paplašinājumu .zl ir ZLIP saspiests faila formāts, kas failu saspiešanai izmanto saspiešanas algoritma DEFLATE variantu. Tas nav atkarīgs no CPU veida, operētājsistēmas, failu sistēmas un rakstzīmju kopas, un tāpēc to var izmantot informācijas apmaiņai. ZLIP saspiešanas tehniskās specifikācijas ir pieejamas vietnē [IETF site](https://tools.ietf.org/html/rfc1950), un tās var atsaukties no izstrādātāja viedokļa.

## ZL faila formāts

Zlib straumei ir šāda struktūra:

 * CMF (kompresijas metode un karodziņi) — atkarībā no saspiešanas metodes šis baits ir sadalīts 4 bitu saspiešanas metodē un 4 bitu informācijas laukā.
```
bits 0 to 3  CM     Compression method
bits 4 to 7  CINFO  Compression info
```
 * CM (saspiešanas metode) — tā identificē failā izmantoto saspiešanas metodi. Tās vērtības un atbilstošā saspiešanas metode ir šāda.

| CM vērtība| Saspiešana|
|---|---|
|CM = 8|DEFLATE ar loga izmēru līdz 32K|
|CM = 15|Rezervēts|

 * CINFO (saspiešanas informācija) — ja CM = 8, CINFO ir loga LZ77 loga izmēra 2. bāzes logaritms, mīnus astoņi (CINFO=7 norāda 32 KB loga izmēru).

 * FLG (FLaGs) — šis karoga baits ir sadalīts šādi:
```
  bits 0 to 4  FCHECK  (check bits for CMF and FLG)
  bit  5       FDICT   (preset dictionary)
  bits 6 to 7  FLEVEL  (compression level)
````

## Atsauces Nr.

* [Zlib faila formāta specifikācijas](https://tools.ietf.org/html/rfc1950)


