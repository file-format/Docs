{
  "date": "2021-07-29",
  "keywords": [
"shx fil",
"shx filformat",
"hvad er en shx-fil",
"fil",
"shx eksempel",
"shx filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "SHX - Shapefil Shape Index Format",
  "description": "Lær om SHX-filformat og API'er, der kan oprette og åbne SHX-filer.",
  "linktitle": "SHX",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-sh-dax"
}
},
  "lastmod": "2021-07-29"
}

## Hvad er en SHX fil?
SHX-filen tilhører shape index-formatet, som er et positionsindeks for funktionsgeometrien for at gøre det muligt at søge hurtigt frem og tilbage. SHX er en offsetfil med direkte adgang. Der er ingen data i denne fil, kun en kopi af de første hundrede bytes, postnummer og offset til startbyten for den post i shp. Bemærk venligst, at filen med filtypenavnet .shx ikke binder [SHP](/gis/shp/) og [DBF](/database/dbf/).

## SHX filformat
SHX-formatet indeholder positionsindeks for funktionsgeometrien og 100-byte-header svarende til SHP-filen, efterfulgt af et vilkårligt antal 8-byte fastlængde-poster, som indeholder følgende to felter:
| Bytes | Skriv | Endianness | Brug |
-------|-------|------------|---------------------------------|
| 0–3 | int32 | stor | Record offset (i 16-bit ord) |
| 4–7 | int32 | stor | Optagelængde (i 16-bit ord) |

Dette indeks gør det muligt at søge bagud i shapefilen ved først at søge baglæns i shape-indekset og derefter læse postoffset. Denne offset kan bruges til at søge til den korrekte position i SHP-filen. Du kan også søge fremad; et vilkårligt antal poster ved hjælp af samme metode. Selvom det er muligt at generere komplet indeks sammen med en SHP-fil, men det kan øge chancerne for at gøre SHP-filen korrupt hurtigt.


## Referencer

* [Shapefil - af Wikipedia)](https://en.wikipedia.org/wiki/Shapefile)



