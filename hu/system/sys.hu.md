{
  "date" : "2021-07-08",
  "keywords" :[ "SYS", "extension", "file", "format", "system", "Driver", "System File", "programs", "computer", "application" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SYS - Rendszerfájl formátum",
  "description":"További információ a SYS fájlformátumról és az API-król, amelyek SYS fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "SYS",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-08"
}

## Mi az a SYS fájl? ##

A SYS fájlok a Windows operációs rendszerben és az MS-DOS alkalmazásokban használt "rendszerfájlok". Ezek a fájlok nem nyithatók meg közvetlenül, és az eszköz illesztőprogramjából és konfigurációjából állnak. A SYS fájlok felelősek az operációs rendszer alapvető funkcióit tartalmazó fájlokért. Ezek az eszközmeghajtó kritikus fájljai, és akkor is használhatók, ha a versenyzővel kapcsolatos problémákat meg kell oldani. Ezek felelősek a számítógépes rendszer megfelelő működéséért, és a .sys fájloknak helyesnek és teljesnek kell lenniük.


## Műszaki specifikáció ##

A .sys fájlok valójában a [BMP](/hu/image/bmp/) formátum részhalmazai, mivel csak meghatározott kombinációkat tesz lehetővé. A fájlok szokásos formátuma a LOGOS.SYS, LOGOW.SYS és LOGO.SYS. A többi fájl nem rendelkezik ezzel a formátummal.

Ezeket a fájlokat többnyire a Windows *C* könyvtárában használják a telepítéskor. Az eszközillesztőkkel kapcsolatos legtöbb probléma megoldható a Windows operációs rendszer frissítésével. A fájlok részleteit és információit a Windows operációs rendszer beépített programjaival tekintheti meg. Ezek tartalmazzák az operációs rendszer különböző moduljaira való hivatkozásokat is.
Néhány példa a rendszerfájlokra:

* IO.SYS (ezek a lemezes operációs rendszer eszközillesztőit tárolják)
* MSDOS.SYS (Ezek tartalmazzák a kernelt vagy az operációs rendszer alapkódját)
* CONFIG.SYS (Ezek különböző konfigurációs lehetőségeket tartalmaznak)
* KEYBOARD.SYS (Ezek a billentyűzetkiosztással kapcsolatos információkat tartalmaznak)
* COUNTRY.SYS (Ezek az országgal és kódlappal kapcsolatos információkat tartalmazzák)

## SYS fájlformátum ##

A Microsoft .sys kiterjesztésű fájlokat fejlesztett ki. A változókat és a függvényeket a SYS-fájlok tartalmazzák. Ezeket leginkább a Microsoft operációs rendszer használja. Ezek a fájlok főként a lemez gyökérkönyvtárában találhatók:

* C:\Windows\system32\drivers
* C:\Windows\WinSxS

A SYS fájlokkal kapcsolatos gyakori figyelmeztetések a következők:

* A fájlok neveit nem szabad megváltoztatni, mivel ezek a fájlok felelősek az operációs rendszer alapvető funkcióiért és változóiért
* Ezeket a fájlokat nem szabad törölni, mert ezek hiánya hibákat okozhat
* A .sys fájlokat addig ne töltse le az internetről, amíg nem biztos a forrás jogosságában
* Nem szabad foglalkozni ezekkel a fájlokkal, mivel ezek megváltoztatása vagy hibázása súlyos rendszerhibákat okoz
* Ha ezeket a fájlokat valamilyen vírus vagy rosszindulatú program megsérti, azokat újra kell telepíteni

## SYS példa ##

A következő példa egy egyszerű SYS rendszerkonfigurációs fájlra:

```
DEVICE=C:\Windows\HIMEM.SYS
DOS=HIGH,UMB
DEVICE=C:\Windows\EMM386.EXE NOEMS
FILES=30
STACKS=0,0
BUFFERS=20
DEVICEHIGH=C:\Windows\COMMAND\ANSI.SYS
DEVICEHIGH=C:\MTMCDAI.SYS /D:123
```
