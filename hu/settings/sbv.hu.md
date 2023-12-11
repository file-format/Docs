{
"dátum": "2023-03-22",
  "keywords": [
"sbv fájl",
"mi az sbv fájl",
"hogyan kell megnyitni az sbv fájlt",
"fájl",
"sbv fájlkiterjesztés",
"kiterjesztés"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "SBV fájlformátum - YouTube feliratok fájl",
  "description":"További információ az SBV formátumról és az SBV-fájlok létrehozására és megnyitására alkalmas API-król.",
  "linktitle": "SBV",
  "menu": {
    "docs": {
      "identifier": "settings-sbv",
      "parent": "settings"
}
},
"lastmod": "2023-03-22"
}

## Mi az SBV fájl?

Az .sbv kiterjesztésű fájl egy SubViewer feliratfájl. A SubViewer a videofájlokhoz használt feliratok formátuma, amely a 2000-es évek elején keletkezett. Az .sbv fájl tartalmazza a felirat szövegét, valamint az időzítési információkat arra vonatkozóan, hogy az egyes feliratok mikor jelenjenek meg a videó lejátszása közben.

A SubViewer fájlokat gyakran használják a YouTube-videókhoz, mivel a YouTube támogatja a SubViewer formátumot a videófeliratokhoz. A SubViewer fájlok más videolejátszókkal és szoftverekkel is használhatók, amelyek támogatják a formátumot.

Ha .sbv fájlt szeretne használni egy videofájllal, a videofájlnak és az .sbv fájlnak is ugyanabban a mappában kell lennie, és azonos fájlnévvel kell rendelkeznie (kivéve a fájl kiterjesztését). Sok videolejátszó automatikusan betölti az .sbv fájlt a videó lejátszásakor, ha a fájlokat így nevezték el. Különféle feliratszerkesztő alkalmazások támogatják a SubViewer formátumot, ha .sbv fájlt kell létrehozni vagy szerkeszteni. Az Aegisub, a Subtitle Workshop és a Subtitle Edit néhány gyakran használt eszköz.

## SBV fájlformátum – További információ

Az SBV fájlformátum egy egyszerű szövegalapú formátum, amelyet a videók feliratainak tárolására használnak. Az SBV a "SubViewer" vagy a "SubRip Video" rövidítése, a fájl forrásától függően. Az SBV-fájlok a videótartalommal szinkronizált feliratokat tartalmaznak. Minden egyes felirat egy időbélyegből áll, amely jelzi a felirat kezdési és befejezési idejét, majd a felirat szövegét. Az időbélyeg jellemzően "óó:pp:pp, mmm" formátumú, ahol az "óó" az órákat, a "mm" a perceket, az "ss" a másodperceket és az "mmm" ezredmásodperceket jelöli. A felirat szövege általában egyszerű szöveges formátumú.

Íme egy példa arra, hogyan nézhet ki egy SBV fájl:

```
0:00:01.000,0:00:03.000
Hello, and welcome to our video!

0:00:04.000,0:00:06.000
In this video, we will be discussing the SBV file format.

0:00:07.000,0:00:10.000
The SBV format is commonly used for storing subtitles for videos.
```

Az SBV fájlok számos feliratszerkesztő szoftverrel hozhatók létre és szerkeszthetők, mint például a Feliratműhely, az Aegisub vagy a Feliratszerkesztés. A feliratok elkészülte után az SBV fájl importálható egy videószerkesztő programba, hogy feliratos videót készítsen. Összességében az SBV fájlformátum egy egyszerű és széles körben használt formátum a feliratok tárolására, amely számos videószerkesztő programmal és lejátszóval kompatibilis.

## SBV fájl - Mivel nyitható meg egy SBV fájl?

Az SBV fájlok szöveges fájlok, így bármilyen szövegszerkesztővel megnyithatja őket, például a Notepad vagy a Notepad++ segítségével

## Hivatkozások
* [SubViewer](https://wiki.videolan.org/SubViewer/)

