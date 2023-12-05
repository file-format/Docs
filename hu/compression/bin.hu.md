{
"dátum":"2023-07-20",
   "keywords":[
"KUKA",
"BIN fájl",
"fájl",
"BIN fájlkiterjesztés",
"kiterjesztés",
"fájl"
],
   "author":{
"display_name":"Shakeel Faiz"
},
"draft":"false",
"toc":true,
"title":"BIN fájlformátum - MacBináris kódolású fájl",
   "description":"További információ a BIN-formátumról és az API-król, amelyek BIN-fájlokat hozhatnak létre és nyithatnak meg.",
"linktitle":"BIN",
   "menu":{
      "docs":{
         "identifier":"compression-bin",
         "parent":"compression"
}
},
"lastmod":"2023-07-20"
}

## Mi az a BIN fájl?

A BIN-fájl a Macintosh számítógépeken MacBinary formátumban mentett fájlra utalhat. A MacBinary egy olyan fájlformátum, amelyet kifejezetten Macintosh fájlok interneten, e-mailen, FTP-n vagy hordozható adathordozón keresztüli átvitelére terveztek. A MacBinary célja, hogy egyetlen fájlon belül megőrizze a Macintosh-fájlok teljes fájlszerkezetét és attribútumait, beleértve az adat- és erőforrás-ellát is.

A MacBinary formátum ezt úgy éri el, hogy a Macintosh Hierarchical File System (HFS) erőforrás-elágazását és adatvillát tömörített fájlba foglalja. Tartalmaz egy keresőfejlécet is, amely fontos metaadatokat tartalmaz a fájlról. Ezen összetevők egy fájlba való egyesítése révén a MacBinary biztosítja, hogy a fájl megőrizze integritását, és könnyen átvihető és megosztható legyen a különböző platformokon.

Az Apple fájlrendszereinek és fájlátviteli protokolljainak fejlődésével a BIN fájlok és a MacBinary formátum használata kevésbé gyakori. Az olyan fájlformátumok bevezetése, mint a ZIP, és a modernebb fájlrendszerekre, például a HFS+-ra és az APFS-re való átállás csökkentette a MacBinary kódolású fájlok iránti igényt. Ezek az újabb fájlrendszerek hatékonyabb módszereket kínálnak a fájlattribútumok, erőforrás-elágazások és adatforkok kezelésére, így a MacBinary formátum kevésbé szükséges a mai számítástechnikai környezetben.

## BIN fájlformátum – További információ

A Macintosh számítógépek kezdeti napjaiban az adatkorlátok miatt a fájlokat két külön "villában" tárolták. Az "erőforrás-elágazás" strukturált adatokat tartalmazott, míg az "adatvilla" strukturálatlan adatokat tartalmazott. Míg a klasszikus Mac OS ezeket a villákat egyetlen fájlként kezelte, a fájlok nem Mac rendszerekre való átvitele adatvesztést eredményezett, mivel nem ismerték fel a villákat egyetlen entitásként. Ennek megoldására a MacBinary formátumot olyan személyek hozták létre, mint a Dennis Brothers, Harry Chesley és Yves Lempereur. A MacBinary tömörítette és egyesítette a fork-okat egyetlen fájlba, amely BIN-fájlként ismert, a nem Mac rendszerekre való átvitelhez. A Mac OS-hez való visszatéréskor a villák ismét szétválnak. A 2000-es években a villa alapú HFS-ről való átállással a MacBinary formátum használata jelentősen visszaesett. Ma ritkán találkozunk MacBinary kódolású BIN fájlokkal, hacsak nem találunk egy régi fájlt egy nem Mac rendszeren, vagy nem töltünk le egyet az internetről.

A MacBinary formátum több verzión ment keresztül az idők során, hogy alkalmazkodjon a Macintosh rendszerek és a fájlkezelés változásaihoz. Íme néhány a MacBinary formátum különböző verziói közül:

- **MacBinary I:** A MacBinary kezdeti verziója, amelyet az 1980-as évek végén vezettek be. Egyetlen bináris fájlba egyesítette az erőforrás- és adatvillát, lehetővé téve a Macintosh-fájlok platformok közötti átvitelét.

- **MacBinary II:** Ez az 1990-es évek elején megjelent verzió az eredeti MacBinary formátumhoz képest további információkkal, például fájltípussal és létrehozói kódokkal javított a bináris fájl fejlécében. Ezek a kódok segítettek megőrizni a Macintosh-fájlok integritását és azonosítását az átvitel során.

- **MacBinary III:** Az 1990-es évek közepén bevezetett MacBinary III formátum továbbfejlesztette a korábbi verziókat azáltal, hogy a bináris fájl fejlécében további metaadatokat, például fájlnevet, valamint a fájl létrehozásának és módosításának dátumát helyezte el. Ez lehetővé tette a Macintosh fájlattribútumok átfogóbb megőrzését az átvitel során.

- **MacBinary IV:** A MacBinary IV-et a 2000-es évek elején a feltörekvő Mac OS X operációs rendszerrel kapcsolatos kompatibilitási problémák megoldására fejlesztették ki. Változásokat tartalmazott a Mac OS X-ben bevezetett új fájlrendszer-struktúrához és attribútumokhoz való alkalmazkodás érdekében.

## BIN fájl - Mivel nyitható meg egy BIN fájl?

A MacBinary Encoded BIN fájlok különféle tömörítési segédprogramokkal nyithatók meg. A macOS-felhasználók számára az **Apple Archive Utility** megfelelő lehetőség. A Windows-felhasználók olyan szoftvereket használhatnak, mint a **Smith Micro StuffIt Deluxe** a MacBinary Encoded BIN fájl tartalmának kibontására. Egy másik lehetőség a macOS-felhasználók számára a **The Unarchiver**, amely egy sokoldalú eszköz, amely képes többféle fájlformátum kezelésére, beleértve a MacBinary-t is.

Fontos megjegyezni, hogy a .bin fájlkiterjesztést különféle fájlformátumok használják, nem csak a MacBinary. Ezért, ha olyan BIN fájlt talál, amelyet nem lehet megnyitni a fent említett segédprogramokkal, előfordulhat, hogy más formátumban menti. Ilyen esetekben előfordulhat, hogy meg kell határoznia az adott fájlformátumot, és az ehhez a formátumhoz tervezett megfelelő szoftvert vagy segédprogramot kell használnia a fájltartalom eléréséhez.

## Egyéb BIN fájlok

Íme más fájltípusok, amelyek a **.bin** fájlkiterjesztést használják.

- [BIN - Bináris lemezképfájl](/hu/disc-and-media/bin/)
- [BIN - Unix végrehajtható fájl](/hu/executable/bin/)
- [BIN - BlackBerry IT szabályzatfájl](/hu/settings/bin/)
- [BIN - Sega Genesis Game ROM](/hu/game/bin/)
- [BIN - PSX PlayStation BIOS Image](/hu/game/bin-pcsx/)

## Hivatkozások

* [MacBinary](https://en.wikipedia.org/wiki/MacBinary)

