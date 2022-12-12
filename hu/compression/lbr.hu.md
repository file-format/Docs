{
  "date" : "2021-04-08",
  "keywords" :[ "mst fájl", "mst fájl formátum", "mi az mst fájl", "fájl", "mst példa", "mst fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
	

},
  "draft" : "false",
  "toc" : true,
  "title" :"LBR - LU Library Archive File Format",
  "description":"További információ az LBR fájlformátumról és az LBR-fájlok létrehozására és megnyitására alkalmas API-król.",
  "linktitle" : "LBR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-19"
}

## Mi az LBR fájl?

Az .lbr kiterjesztésű fájl olyan archív fájl, amelyet LU programmal hoztak létre, és CP/M és DOS operációs rendszereken használták az 1980-as években. Már nem használják, és a modern archiváló fájlformátumok váltották fel. A formátum nem tömöríti a tagfájlokat, és konténerarchívumként működik ezekhez. Az archiválási funkciót leginkább az archivált fájlok interneten keresztüli átvitelére használták. Mivel az LBR nem kínált tömörítést, más segédprogramokat, például az SQ-t vagy a CRUNCH-t használták a tagfájlok előzetes archiválására vagy az eredményül kapott archív fájl utólagos archiválására a méretének csökkentése érdekében.

## LBR fájlformátum

Az LBR fájlformátumot Gary P. Novosielski tervezte, és nem tartalmaz nyilvánosan elérhető műszaki részleteket. Az LBR-fájlok 0x00 bájttal kezdődnek, ezt követi 11 szóköz (0x20), majd két 0x00 bájt, majd két bájt, amelyek nem 0x00. A konténerfájl formátumaként a LU.COM és a NULU.COM használatával kibontható.

## Hivatkozások

* [LBR – Wikipedia](https://en.wikipedia.org/wiki/LBR_(file_format))

