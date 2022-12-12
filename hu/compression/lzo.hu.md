{
  "date" : "2021-06-16",
  "keywords" :[ "LZO", "Compressed", "File", "Extension", "File Format", "Lempel-Ziv-Oberhume" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LZO fájlformátum",
  "description":"További információ az LZO fájlformátumról és az LZO-fájlok létrehozására és megnyitására alkalmas API-król.",
  "linktitle" : "LZO",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-06-16"
}

## Mi az LZO fájl? ##

Az .lzo kiterjesztésű fájlokat olyan fájlarchiválási szolgáltatásokkal kombinálják, amelyek csökkenthetik a tömörített fájlban lévő összes fájl méretét. Az összes tömörített fájl tartalmazhat egy vagy több fájlt, vagy akár iratgyűjtők csoportjait több különböző típusú és méretű fájllal. A tömörített fájl mérete kisebb az LZO tömörített fájlban tárolt összes fájl és mappa együttes méretéhez képest. Az összes LZO tömörített fájl LZO formátumban van tárolva, és kifejezetten az LZOP fájltömörítő és kicsomagoló szoftver által használt tömörítési funkciókkal hajtják végre. A Lempel-Ziv-Oberhume fájltömörítési könyvtárból származó összes tömörítési specifikáció össze van kapcsolva ebben a fájltömörítő és kitömörítő programban. A gyorsabb kitömörítési sebesség és a fejlett tömörítési arányok is kombinálódnak ezekben az LZO-fájlokban.

## LZO specifikáció ##

Markus Franz Xaver Johannes Oberhumer 1996-ban fejlesztette ki az eredeti "lzop" algoritmust Abraham Lempel és Jacob Ziv korábbi algoritmusai alapján. Ez a könyvtár számos algoritmust valósít meg a következő jellemzőkkel:

* Gyorsabb tömörítés, mint a DEFLATE
* Gyors dekompresszió
* További pufferek, amelyekre szükség van a tömörítés során (8 KB vagy 64 KB méretű, a tömörítési szinttől függően)
* A forrás és a cél puffer a kibontáshoz szükséges összes memória
* Szabályozást biztosít a tömörítési arány és a tömörítési sebesség felett

Blokktömörítési algoritmusként az LZO átfedő tömörítést, valamint helyben történő kitömörítést hajt végre. Az átfedő tömörítés eléréséhez a tömörítés és a kicsomagolás blokkméretének meg kell egyeznie. Az LZO tömörítési algoritmus a bemeneti adatokat egyezésekre (egy csúszószótár) és nem egyező literálokra bontja, így jó eredményeket ad erősen redundáns adatokkal, és elfogadható eredményeket nem tömöríthető adatokkal, csak az eredeti 1/64-ével növeli a tömöríthetetlen adatokat. méret.

## Problémák az LZO fájl megnyitásakor ##

Az alábbiakban felsorolunk néhány problémát, amelyek az LZO fájlformátum rossz működését okozhatják:
  


* Lehet, hogy a fájl sérült. A probléma megoldásához töltse le újra a fájlt, vagy kérje meg a feladót, hogy küldje el újra a fájlt
* A második ok a fertőzött fájl, ebben az esetben ellenőrizze a fájlt megfelelően
* Nem megfelelő hivatkozások az LZO fájlhoz
* Az LZO leírásának eltávolítása
* Nincs elég hardver erőforrás
* A berendezés elavult illesztőprogramjai
  


## Referenciák ##

* [LZO – a Wikipedia által](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Oberhumer)

