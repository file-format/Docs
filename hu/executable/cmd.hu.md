{
  "date" : "2021-07-12",
  "keywords" :[ "cmd fájl", "mi az a cmd fájl", "fájl", "cmd példa", "cmd fájlkiterjesztés", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"További információ a CMD fájlformátumról és az API-król, amelyek CMD fájlokat hozhatnak létre és nyithatnak meg.",
  "title" :"CMD - Windows parancsfájl formátum",
  "linktitle" : "CMD",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-07-12"
}

## Mi az a CMD fájl?
A CMD-fájl egy parancsfájlból áll, amely egy vagy több parancsot tartalmaz egyszerű szöveg formájában, amelyek különböző feladatok végrehajtására futnak. Ez hasonló a [BAT](/hu/executable/bat/) fájlhoz, amelyet általában végrehajtható parancsok kötegének tárolására is használnak. A CMD fájlokat széles körben használják a Microsoft Windows operációs rendszerben. Ezeket a fájlokat a 90-es években vezették be, de még mindig a legújabb Windows operációs rendszerben használják. Ezeket a fájlokat általában úgy írják, hogy egynél több parancsot hajtsanak végre egy sorozatban.

## CMD fájlformátum
A CMD a CP/M stílusú futtatható programok által használt fájlformátum. Általában összehasonlítható a [COM](/hu/executable/com/)-vel CP/M-80-ban és [EXE](/hu/executable/exe/)-vel DOS-ban. Egy CMD-fájl 1-8 kód- vagy adatcsoportot és egy 128 bájtos fejlécet tartalmaz. Minden csoport legfeljebb 1 MB méretű lehet. A CMD-fájlok későbbi verzióiban áthelyezési információkat és Resident System Extensions-eket (RSX) is tartalmazhatnak. A CMD új a [BAT](/hu/executable/bat/) fájlhoz képest; MS-DOS-hoz használták a Windows kiadása előtt MS-DOS-ban. Bár ma is menthet fájlokat .bat kiterjesztéssel, sokan a .cmd kiterjesztést használják futtatható szkriptjeik mentésére.

### CMD formátum specifikáció

A fejléc elején található a fájlban található csoportok listája típusaikkal együtt. Mindegyik típus legfeljebb egyszer használható. Ezek a típusok:

- Kód
- Adatok
- Extra
- Kazal
- Felhasználó 1
- Felhasználó 2
- Felhasználó 3
- Felhasználó 4
- Megosztott kód

A DOS-ban a Program Segment Prefixhez hasonlóan az adatcsoport első 256 bájtja nulla. Ezeket a CP/M-86 fogja kitölteni a nulla oldallal. Ha nincs adatcsoport, akkor helyette a kódcsoport első 256 bájtja kerül felhasználásra.
## CMD fájl példa
Az alábbiakban egy példa látható a rendszerinformációkat megjelenítő CMD-szkriptre.
```
@ECHO OFF

:: This CMD script provides you with your operating system, hardware and network information.

TITLE My System Info

ECHO Please wait... Gathering system information.

ECHO =========================

ECHO OPERATING SYSTEM

systeminfo | findstr /c:"OS Name"

systeminfo | findstr /c:"OS Version"

ECHO =========================

ECHO BIOS

systeminfo | findstr /c:"System Type"

ECHO =========================

ECHO MEMORY

systeminfo | findstr /c:"Total Physical Memory"

ECHO =========================

ECHO CPU

wmic cpu get name

ECHO =========================

ECHO NETWORK ADDRESS

ipconfig | findstr IPv4

ipconfig | findstr IPv6

PAUSE
```



## Hivatkozások

* [Hogyan írjunk CMD-szkriptet](https://smallbusiness.chron.com/write-cmd-script-53226.html)
* [CMD-fájl (CP/M) – a Wikipédia által](https://en.wikipedia.org/wiki/CMD_file_(CP/M))

