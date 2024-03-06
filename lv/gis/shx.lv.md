{
  "date": "2021-07-29",
  "keywords": [
"shx failu",
"shx faila formātā",
"kas ir shx fails",
"failu",
"shx piemērs",
"shx faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "SHX — Shapefile formas indeksa formāts",
  "description": "Uzziniet par SHX failu formātu un API, kas var izveidot un atvērt SHX failus.",
  "linktitle": "SHX",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-sh-lvx"
}
},
  "lastmod": "2021-07-29"
}

## Kas ir SHX fails?
SHX fails pieder formas indeksa formātam, kas ir objekta ģeometrijas pozicionālais indekss, kas ļauj ātri meklēt uz priekšu un atpakaļ. SHX ir tiešas piekļuves ofseta fails. Šajā failā nav datu, ir tikai pirmo simts baitu dublikāts, ieraksta numurs un nobīde pret šī ieraksta sākuma baitu shp. Lūdzu, ņemiet vērā, ka fails ar paplašinājumu .shx nesaista [SHP](/gis/shp/) un [DBF](/database/dbf/).

## SHX faila formāts
SHX formāts satur objekta ģeometrijas pozīcijas indeksu un 100 baitu galveni, kas ir līdzīga SHP failam, kam seko jebkurš 8 baitu fiksēta garuma ierakstu skaits, kas satur šādus divus laukus:
| Baiti | Tips | Endianness | Lietošana |
-------|-------|------------|---------------------------------|
| 0–3 | int32 | liels | Ieraksta nobīde (16 bitu vārdos) |
| 4–7 | int32 | liels | Ieraksta garums (16 bitu vārdos) |

Šis indekss ļauj meklēt atpakaļ shape failā, vispirms meklējot atpakaļ formas indeksā un pēc tam nolasot ieraksta nobīdi. Šo nobīdi var izmantot, lai meklētu pareizo pozīciju SHP failā. Varat arī meklēt uz priekšu; patvaļīgs ierakstu skaits, izmantojot to pašu metodi. Lai gan ir iespējams ģenerēt pilnu indeksu kopā ar SHP failu, taču tas var palielināt iespēju ātri sabojāt SHP failu.


## Atsauces

* [Shapefile — Wikipedia)](https://en.wikipedia.org/wiki/Shapefile)



