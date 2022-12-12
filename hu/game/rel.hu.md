{
  "date" : "2021-09-08",
  "keywords" :[ "rel fájl", "rel fájl formátum", "mi az a rel fájl", "fájl", "rel példa", "rel fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"További információ a REL fájlformátumról és az API-król, amelyek REL-fájlokat hozhatnak létre és nyithatnak meg.",
  "title" :"REL – áthelyezhető modulfájl",
  "linktitle" : "REL",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## Mi az a REL fájl?
A .rel kiterjesztésű fájl többféle célra használható. Ezért a játékok besorolása szempontjából áthelyezhető modulfájlként ismert, amelyet egyes Nintendo Wii játékok, például a Brawl, a Super Smash Bros és a Mario Kart Wii használnak. Tartalmazza a játékmenet adatait, beleértve a karaktermodelleket és a szakaszokat. A REL fájlok hasonlóan működnek, mint a Microsoft Windows által használt .DLL fájlok.

## REL fájlformátum
A REL fájlformátumban a fájl több részre van osztva, hasonló hozzáférés szerint csoportosítva, pl. az egyik szakaszban csak az adatok olvashatók, az összes végrehajtható kód egy másikba kerül stb. A fájl fejlécszekcióval kezdődik, amelyet a következő követ:
- A szakasz adatait tartalmazó táblázat.
- A szakasz adatai.
- Áthelyezési információk.

### Fájlfejléc
A fájl legfeljebb 0x4C bájt méretű fejléccel kezdődik:
| Offset | Méret | Mező neve | Leírás |
--------------------|---------------|-------------------|---------------------------------|
| 0x00 | 4 | azonosító | Önkényes azonosító szám. Egyedinek kell lennie a játék által használt összes REL között. Nem lehet 0. |
| 0x04 | 4 | következő | Mutató a következő modulra, futás közben kitöltve. |
| 0x08 | 4 | előző | Mutató az előző modulra, futás közben kitöltve. |
| 0x0c | 4 | numSections | A fájl szakaszainak száma. |
| 0x10 | 4 | szakaszInfoEltolás | Eltolás a szakasztábla elejéhez. |
| 0x14 | 4 | nameOffset | Eltolás a modul nevét tartalmazó ASCII karakterláncra. Lehet NULL. A REL fájl elejéhez viszonyítva. |
| 0x18 | 4 | névMéret | A modul nevének mérete bájtban. |
| 0x1c | 4 | verzió | A REL fájlformátum verziószáma. |
| 0x20 | 4 | bssSize | A „.bss” szakasz mérete. |
| 0x24 | 4 | relOffset | Eltolás az áthelyezési táblázathoz. |
| 0x28 | 4 | impOffset | Eltolás az imp táblázathoz. |
| 0x2c | 4 | impSize | Az imp tábla mérete bájtban. |
| 0x30 | 1 | prologSection | Indexelje a szakasztáblázatba, hogy melyik prologhoz viszonyít. Ha ez a mező 0, hagyja ki. |
| 0x31 | 1 | epilogSection | Indexelje a szakasztáblázatba, hogy melyik epiloghoz tartozik. Ha ez a mező 0, hagyja ki. |
| 0x32 | 1 | megoldatlanSection | Indexelje a szakasztáblázatba, amelyhez a feloldatlanság relatív. Ha ez a mező 0, hagyja ki. |
| 0x33 | 1 | bssSection | Indexelje a szakasztáblázatba, amelyhez a bss relatív. Futás közben töltve! |
| 0x34 | 4 | prolog | Eltolás a _prolog függvény meghatározott szakaszába. |
| 0x38 | 4 | epilógus | Eltolás az _epilog függvény meghatározott szakaszába. |
| 0x3c | 4 | megoldatlan | Eltolás a _unresolved függvény meghatározott szakaszába. |
| 0x40 | 4 | igazítás | Csak a ≥ 2 verzió. Igazítási kényszer minden szakaszon, 2-es hatványban kifejezve. |
| 0x44 | 4 | bssAlign | Csak a ≥ 2 verzió. Igazítási kényszer az összes „.bss” szakaszon, 2 hatványában kifejezve. |
| 0x48 | 4 | fixSize | Csak a ≥ 3 verzió. Ha a REL az OSLinkFixedhez van kapcsolva (az OSLink helyett), a cím utáni szóköz más célokra is használható (például BSS). |

### Szakasz információs táblázat
A szakasz információs táblázata **numSections** bejegyzést tartalmaz, amelyek mindegyike 0x8 bájt hosszú:
| Offset | Méret | Leírás |
-------|------------|-------------|
| 0x0 | 30 bit | Eltolás a REL elejétől a szakaszig. Ha ez nulla, akkor a szakasz egy inicializálatlan szakasz (azaz .bss). |
| 0x3,6 | 1 bit | Ismeretlen. |
| 0x3,7 | 1 bit | Végrehajtható zászló; ha ez 1, akkor a szakasz végrehajtható. |
| 0x4 | 4 | A szakasz hossza bájtban. Ha ez nulla, akkor ez a bejegyzés kimarad. |
| 0x8 | Következő bejegyzés | Következő bejegyzés |

### Áthelyezési adatok
Az áthelyezési adatok egy vagy több 0x8 bájtos struktúrák listája. Az egyes listák végét a 203-as speciális típuskód jelöli:
| Offset | Név | Méret | Leírás |
-------|------------|------------|-----|
| 0x0 | offset | 2 | Eltolás bájtban az előző áthelyezéshez képest. Ha ez az első áthelyezés a szakaszon, akkor ez a szakasz kezdetéhez viszonyítva történik. |
| 0x2 | típus | 1 | Az áthelyezés típusa. Az alábbiakban leírt. |
| 0x3 | szakasz | 1 | A szimbólum azon része, amely ellen át kell helyezni. A 202-es speciális áthelyezési típusnál ez a fájl azon szakaszának száma, amelyre a következő áthelyezési bejegyzések vonatkoznak. |
| 0x4 | hozzá | 4 | Eltolás bájtokban az áthelyezendő szimbólumhoz, a szakasz elejéhez képest. Ez egy abszolút cím a main.dol elleni költöztetésekhez. |
| 0x8 | Következő bejegyzés | Következő bejegyzés | Következő bejegyzés |


 




## Hivatkozások


* [Relocatable Object Module Format](https://en.wikipedia.org/wiki/Relocatable_Object_Module_Format)


