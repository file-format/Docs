{
  "date" : "2023-01-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Ismerje meg a GCF fájlformátumot és az API-kat, amelyekkel GCF fájlokat hozhat létre és nyithat meg.",
  "title" : "GCF fájl - Nadeo Game GCF formátum",
  "linktitle" : "GCF",
  "menu" : {
    "docs" : {
      "identifier":"game-gcf-hu",
      "parent" : "game"
}
},
  "lastmod" : "2023-01-19"
}

## Mi az a GCF fájl?

A .gcf fájl egy játék-gyorsítótár fájl, amelyet a Steam játékplatform használ. Játékadatokat, például textúrákat, modelleket és egyéb, a játék által használt fájlokat tartalmaz. Ezek a fájlok a felhasználó számítógépén tárolódnak, és a játék frissítése vagy telepítése során letöltendő adatok mennyiségének csökkentésére szolgálnak. A .gcf fájlok biztonsági másolatok készítésére is használhatók egy játék telepítéséről, vagy játék átvitelére számítógépek között.

A GCF fájlokat a nyílt forráskódú C++ programozási könyvtár, a **HLLib** tudja olvasni és írni.

## GCF fájlformátum

A GCF fájlok bináris fájlként kerülnek a lemezre. A GCF-et eredetileg a Grid Cache File (a Steam korai kódneve Grid) rövidítéseként használták, de később Game Cache File néven vették át. A GCF fájl egy archív fájl, amely Steam játékokat tárol. Minden hivatalos tartalom GCF-fájlként töltődik le. A GCF fájlok megoszthatók a játékok között is.

MEGJEGYZÉS: A GCF a [VPK file format](/game/vpk/) elődje.
## Hivatkozások

* [Valve Software](https://www.valvesoftware.com/en/)

* [GCF fájlformátum](https://developer.valvesoftware.com/wiki/GCF)

* [HLLib – nyílt forráskódú C++ programozási könyvtár GCF-fájlok olvasásához](https://developer.valvesoftware.com/wiki/HLLib)


