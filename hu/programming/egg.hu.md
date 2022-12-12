{
  "date" : "2022-03-15",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EGG fájlformátum - Python terjesztési fájl",
  "description":"További információ az EGG fájlformátumról és az EGG-fájlok létrehozására és megnyitására alkalmas API-król.",
  "linktitle" : "EGG",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-03-15"
}

## Mi az EGG fájl?

Az EGG fájl, más néven Python eggs, egy régebbi Python disztribúciós formátum. Ez egy [ZIP](/hu/compression/zip/) tömörített archívum .egg kiterjesztéssel, és tartalmazza a Python-alkalmazás forrásfájljait, valamint a terjesztés metainformációit. Az EGG fájlok a Windows végrehajtható [EXE](/hu/executable/exe/) fájlok alternatívái, de többplatformosak. A Python disztribúciók e régebbi formátumát az újabb Wheel (WHL) fájlformátum váltotta fel 2010 elején.

## EGG fájlformátum

Az EGG-fájlok tömörített ZIP-archívumként kerülnek mentésre. Ez azt jelenti, hogy ha az .egg kiterjesztést .zip-re cseréli, akkor meg tudja nyitni szabványos kicsomagoló segédprogramokkal, mint például a Corel WinZIP, a Microsoft Explorer vagy a RARLAB WinRAR.

Az EGG fájlokat a Python által elérhető **distutils** csomag segítségével lehet létrehozni. Egy másik eszköz, amellyel EGG fájlokat hozhat létre és nyithat meg, a **SetupTools**. Az EGG fájlok csomagként telepíthetők az **easy_install** használatával.

`MEGJEGYZÉS – Az EGG fájlformátum elavult, és az új WHL kerék fájlformátum javára vált.

## Hivatkozási szám

* [Python EGGs](https://python101.pythonlibrary.org/chapter38_eggs.html)

