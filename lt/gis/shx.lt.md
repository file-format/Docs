{
  "date": "2021-07-29",
  "keywords": [
"shx failą",
"shx failo formatas",
"kas yra shx failas",
"failą",
"shx pavyzdys",
"shx failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "SHX – Shapefile Shape Index formatas",
  "description": "Sužinokite apie SHX failo formatą ir API, kurios gali kurti ir atidaryti SHX failus.",
  "linktitle": "SHX",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-sh-ltx"
}
},
  "lastmod": "2021-07-29"
}

## Kas yra SHX failas?
SHX failas priklauso formos indekso formatui, kuris yra objekto geometrijos padėties indeksas, leidžiantis greitai ieškoti pirmyn ir atgal. SHX yra tiesioginės prieigos ofsetinis failas. Šiame faile nėra duomenų, tik dublikatas pirmųjų šimtų baitų, įrašo numeris ir poslinkis į pradinį to įrašo baitą shp. Atminkite, kad failas su plėtiniu .shx nesusieja [SHP](/gis/shp/) ir [DBF](/database/dbf/).

## SHX failo formatas
SHX formate yra objekto geometrijos padėties indeksas ir 100 baitų antraštė, panaši į SHP failą, o po to bet koks skaičius 8 baitų fiksuoto ilgio įrašų, kuriuose yra šie du laukai:
| Baitai | Tipas | Endianness | Naudojimas |
-------|-------|------------|---------------------------------|
| 0–3 | int32 | didelis | Įrašo poslinkis (16 bitų žodžiais) |
| 4–7 | int32 | didelis | Įrašo ilgis (16 bitų žodžiais) |

Šis indeksas leidžia ieškoti atgal Shape faile, pirmiausia ieškant atgal formos rodyklėje ir tada nuskaitant įrašo poslinkį. Šis poslinkis gali būti naudojamas norint rasti tinkamą SHP failo vietą. Taip pat galite ieškoti į priekį; savavališkas įrašų skaičius naudojant tą patį metodą. Nors galima sugeneruoti visą indeksą kartu su SHP failu, tačiau tai gali padidinti galimybę greitai sugadinti SHP failą.


## Nuorodos

* [Shapefile – pateikė Vikipedija)](https://en.wikipedia.org/wiki/Shapefile)



