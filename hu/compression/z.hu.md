{
  "date" : "2021-06-22",
  "keywords" :[ "Z", "Tömörített", "Fájl", "Kiterjesztés", "Fájlformátum", "UNIX", "Kartz" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Z tömörített fájlformátum",
  "description":"További információ a Z fájlformátumról és az API-król, amelyek Z fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "Z",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-06-22"
}

## Mi az a Z fájl? ##

Az AZ fájl a UNIX tömörített adatfájlokhoz tartozó fájlok kategóriája. A tömörített Unix fájlok a Z fájl legnépszerűbb és legszélesebb körben használt kiterjesztési típusa. A Z fájl megkönnyíti a fájlok formázását, futtatását és megnyitását, mivel kisméretű számítógépes fájlok létrehozására szolgál, amelyek könnyen futtathatók Linux/Unix operációs rendszeren. Előnyös azoknak a felhasználóknak, akik lemezterületet szeretnének megtakarítani, mivel a nagy fájlok egy Z-fájlba tömörítésével a felhasználók sok tárhelyet takaríthatnak meg, és fájljaikat rendezettebbé tehetik. Ezek a tömörített Z fájlok könnyen kicsomagolhatók a Unix rendszerben egy egyszerű „uncompress abc.z” paranccsal az „abc” nevű fájlhoz.


## Rövid története ##

A Z fájlt a gyors archiváló iránti megingathatatlan igény eredményeként hozták létre a '80-as évek végén és a '90-es évek elején. Mivel az internet akkoriban nem volt túl népszerű és elérhető, a felhasználóknak meg kellett küzdeniük az alapvető fájlok megosztásával és az internet elérésével. A fájlok átvitelének egyik módja az archiváló használata volt. A Z fájlt Phil Katz vezette be, mint az Archiver gyorsabb és jobban támogató formáját, amelyen keresztül hatalmas fájlokat lehetett egyben tömöríteni és átvinni. A végső Kartz verziót 1989-ben, egy jogi csata után mutatták be, és a Kartz bejelentette, hogy a közkincsnek szentelték.


## Műszaki specifikáció ##

A Z fájl egy olyan fájl, amely támogatja az archív fájlformátumot. Ez az egyik első olyan fájltípus, amely gyors és veszteségmentes adattömörítést és kicsomagolást tesz lehetővé Unix és Linux operációs rendszerekkel. Egyes operációs rendszerekben a kis Z (.z) betűs fájlkiterjesztés a GNU által tömörített fájlt, míg a nagy Z (.Z) betűvel rendelkező fájl tömörített fájlt jelent. A Z fájlnak számos verziója van, amelyeket támogat, például a 2.0, 2.1, 4.5, 4.6, többek között. Különféle algoritmusok léteznek a különböző Z fájlverziókban, és a legnépszerűbb a DEFLATE.




