{
  "date" : "2021-07-29",
  "keywords" :[ "shx fájl", "shx fájlformátum", "mi az shx fájl", "fájl", "shx példa", "shx fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SHX - Shapefile Shape Index Format",
  "description":"További információ az SHX fájlformátumról és az SHX-fájlok létrehozására és megnyitására alkalmas API-król.",
  "linktitle" : "SHX",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-07-29"
}

## Mi az SHX fájl?
Az SHX fájl a shape index formátumhoz tartozik, amely a jellemző geometriájának helyzeti indexe, amely lehetővé teszi a gyors előre és hátra keresést. Az SHX egy közvetlen hozzáférésű offset fájl. Ebben a fájlban nincs adat, csak az első száz bájt másolata, a rekordszám és az eltolás a rekord kezdő bájtjához az shp-ben. Kérjük, vegye figyelembe, hogy a .shx kiterjesztésű fájl nem köti össze az [SHP](/hu/gis/shp/) és a [DBF](/hu/database/dbf/) fájlokat.

## SHX fájlformátum
Az SHX formátum tartalmazza a jellemzőgeometria pozícióindexét és az SHP-fájlhoz hasonló 100 bájtos fejlécet, majd tetszőleges számú 8 bájtos rögzített hosszúságú rekordot, amely a következő két mezőt tartalmazza:
| Bájtok | Típus | Endianness | Használat |
-------|-------|------------|---------------------------------|
| 0–3 | int32 | nagy | Rekordeltolás (16 bites szavakkal) |
| 4–7 | int32 | nagy | Rekordhossz (16 bites szavakkal) |

Ez az index lehetővé teszi, hogy visszafelé keressünk a shape fájlban, először visszafelé keresünk a shape indexben, majd beolvassuk a rekordeltolást. Ez az eltolás használható az SHP-fájl megfelelő pozíciójának megkeresésére. Előre is kereshet; tetszőleges számú rekordot ugyanazzal a módszerrel. Bár lehetőség van teljes index létrehozására egy SHP-fájllal együtt, ez azonban növelheti az SHP-fájl gyors megsérülésének esélyét.


## Hivatkozások

* [Shapefile – a Wikipédia által)](https://en.wikipedia.org/wiki/Shapefile)


