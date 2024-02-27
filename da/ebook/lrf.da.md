{
  "date": "2019-12-12",
  "keywords": [
"LRF",
"fil",
"udvidelse",
"format",
"e-bog",
"Digital bog"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om LRF filformat og API'er, der kan oprette og åbne LRF filer.",
  "title": "LRF-filformat - En Sony Portable Reader-fil",
  "linktitle": "LRF",
  "menu": {
    "docs": {
      "parent": "ebook",
      "identifier": "ebook-lr-daf"
}
},
  "lastmod": "2019-12-12"
}

## Hvad er en LRF fil?

En fil med filtypenavnet .lrf er en Broad Band eBook (BBeB)-fil, der indeholder data for en Sony BBeB, inklusive tekst, billeder og pagineringsdata. Filen gemmes i et komprimeret binært format, som indeholder en header, et specificeret antal objekter og et objektindeks. LRF- og LRX-filer omslutter de to tilgængelige BBeB-bogformater. LRF-filerne er ikke krypteret og kan kompileres fra [LRX](/ebook/lrf/) filer. LRF-filerne kan konverteres fra flere andre filtyper, herunder PDF og HTML. Hvis din computer ikke kan åbne LRF-filen, har du sandsynligvis ikke softwaren installeret til at åbne eller redigere LRF-filerne. Programmer, der kan åbne LRF-filer, er Caliber, BookDesigner, Makelrf og Canon Book Creator til Windows, Caliber til Linux, Caliber og Sony Reader til Macintosh.

## Kort historie

LRF filtype er først og fremmest forbundet med Line Rider af [inXile entertainment](https://en.wikipedia.org/wiki/InXile_Entertainment). Line Rider er et fysiklegetøj på internettet og blev opfundet i september 2006 af en slovensk universitetsstuderende, Boštjan Čadež. Sony-mærket eBook eReaders (såsom Sony PRS-500 læsere og Sony Librie) bruger LRF filtypenavnet til deres dokumenter og tekster. Denne proprietære filtype er nu forældet, såvel som de relaterede LRS- og LRX-filer. Disse tre filtyper udgjorde BroadBand eBook (BBeB), som blev afbrudt i 2010, da Sony begyndte at sælge deres e-bøger i EPUB-formatet.

## LRF filformat

Detaljerede specifikationer for LRF-filformat er tilgængelige på [web archive](https://web.archive.org/web/20110809071744/http://www.sven.de/librie/Librie/LrfFormat). En LRF-fil består af:
* en overskrift

* en række genstande

* et objektindeks.


Alle disse værdier er i Intel (LSB first) rækkefølge.

### LRF header

|Offset (hex) |Størrelse(bytes) |Navn/betydning| Eksempelværdi|
---|---|---|---|
|0 |8| LRF Signatur| 4C 00 52 00 46 00 00 00 = LRF i Unicode|
|8 |2| version?| 999 i de fleste filer|
|A |2| Psuedo-kryptering |nøglebyte 48|
|0C |4| RootObjectID| 0x0044|
|10 |8| NumberOfObjects |342|
|18 |8| ObjectIndexOffset| 0x00093440|
|20 |4| ukendt | 0|
|24 |1| Flag| (16 - bagside til forside, 1 = forside mod bagside) 16|
|25 |1| ukendt |(polstring?) 0|
|26 |2| ukendt | 1600|
|28 |2| ukendt | (polstring?) 0|
|2A |2| Højde?| 600|
|2C |2| Bredde?| 800|
|2E |1| ukendt | 24|
|2F |1| ukendt |(polstring?) 0|
|30 |0x14| ukendt | nuller|
|44 |4| Objekt-id for kun PlaneStream (0x1E) objekt| 0x0042|
|48 |4| ukendt |0x1536|
|4C |2| XMLCompSize| 0x035C|


## Referencer

* [LRF-filformat](https://web.archive.org/web/20110809071744/http://www.sven.de/librie/Librie/LrfFormat)

* [BBeB - Af Wikipedia](https://en.wikipedia.org/wiki/BBeB)


