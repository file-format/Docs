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
"title":"BIN fájlformátum - Unix végrehajtható fájl",
   "description":"További információ a BIN formátumról és az API-król, amelyek BIN fájlokat hozhatnak létre és nyithatnak meg.",
"linktitle":"BIN",
   "menu":{
      "docs":{
         "identifier":"executable-bin",
         "parent":"executable"
}
},
"lastmod":"2023-07-20"
}

## Mi az a BIN fájl?

A BIN fájl egy Unix alapú operációs rendszeren, például Linuxon vagy FreeBSD-n futtatható fájl. A forráskódból származó bináris kódból összeállított programot tartalmaz, így kompatibilis az alapul szolgáló rendszerarchitektúrával. A Unix végrehajtható BIN fájlok futtatható formátumban betöltött szerepüket tekintve összehasonlíthatók a Windows .EXE fájlokkal és a macOS .APP fájlokkal.

A Unix rendszerek szoftverfejlesztésének területén a fejlesztők általában a BIN fájlokat használják programok csomagolására és terjesztésére. Kényelmes eszközt kínálnak a szoftverek felhasználókhoz való eljuttatására, lehetővé téve az egyszerű telepítést és végrehajtást. A BIN fájlok mellett léteznek más típusú Unix végrehajtható fájlok is, például [.ELF](/hu/executable/elf/), .X86, [.RUN](/hu/executable/run/) és .X86_64, amelyek mindegyike meghatározott hardverhez vagy rendszerkövetelmények.

Ha a BIN-fájl belső szerkezetéről van szó, az olyan kódolt adatokból áll, amelyeket a Unix operációs rendszer a mellékelt program azonosítására, olvasására és végrehajtására használ fel. A rendszer meghatározott fájlaláírásokra vagy fejlécekre támaszkodik, hogy a BIN fájlt végrehajthatóként ismerje fel, majd értelmezi és végrehajtja a benne található bináris utasításokat.

A BIN fájlokhoz gyakran egy **INSTALL.TXT** fájl is tartozik, amely részletes utasításokat ad a program megfelelő telepítéséhez és beállításához. Ez a dokumentáció biztosítja, hogy a felhasználók sikeresen navigálhassanak a telepítési folyamatban, és komplikációk nélkül kezdhessék meg a szoftver használatát.

## Hogyan lehet megnyitni a BIN fájlt?

A BIN fájlok nem közvetlenül megnyithatók és megtekinthetők. Azonban végrehajthatja a programokat, vagy kivonhatja a bennük lévő adatokat. A BIN-fájl tartalmának eléréséhez kövesse az alábbi lépéseket a parancssorban, feltételezve, hogy a BIN-fájl neve "sample.bin":

1. **Győződjön meg a végrehajtható engedélyekről:**

A BIN-fájl végrehajtása előtt győződjön meg arról, hogy rendelkezik a szükséges engedélyekkel ahhoz, hogy végrehajtható fájlként futhasson. Használja a parancsot:

```
$ chmod +x sample.bin
```

Ez a parancs végrehajtási jogosultságokat ad a fájlnak.

2. **Futtassa a BIN fájlt:**

A végrehajtható engedélyek beállítása után a következő parancs beírásával futtathatja a BIN fájlt:

```
$ ./sample.bin
```

**Figyelem**

_Legyen körültekintő a letöltött vagy e-mailben elküldött BIN-fájlok kezelésekor, mivel ezeket potenciálisan a kiberbűnözők felhasználhatják rosszindulatú programok terjesztésére. Csak megbízható forrásból származó BIN-fájlokat futtasson a rosszindulatú végrehajtható támadások kockázatának csökkentése érdekében._

## Egyéb BIN fájlok

Íme más fájltípusok, amelyek a **.bin** fájlkiterjesztést használják.

- [BIN - MacBinary Encoded File](/hu/compression/bin/)
- [BIN - Bináris lemezképfájl](/hu/disc-and-media/bin/)
- [BIN - BlackBerry IT szabályzatfájl](/hu/settings/bin/)
- [BIN - Sega Genesis Game ROM](/hu/game/bin/)
- [BIN - PSX PlayStation BIOS Image](/hu/game/bin-pcsx/)

## Hivatkozások

* [Hogyan futtassunk bináris fájlokat Linux alatt](https://linuxhint.com/execute-binary-files-in-linux/)


