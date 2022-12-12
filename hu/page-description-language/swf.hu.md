{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "keywords" :[ "SWF", "fájl", "kiterjesztés", "formátum", "videóformátum", "Mi az SWF fájl", "swf fájlformátum", "swf fájllejátszó", "swf fájl megnyitása"] ,
  "title" :"SWF fájl – Shockwave Flash Movie File Format",
  "description":"További információ az SWF-fájlokról és az API-król, amelyek létrehozhatják és megmutathatják, hogyan kell megnyitni az SWF-fájlt.",
  "linktitle" : "SWF",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az SWF fájl?

Az SWF-fájl egy Adobe Flash programmal létrehozott animációs fájl. Tartalmazhat különböző típusú elemeket, például szöveget, vektoros képeket, raszteres képeket, műveleti szkripteket, objektumokat, például köröket, vonalakat, négyzeteket és téglalapot az animáció létrehozásához. Az SWF-fájlok ezeket a multimédiás elemeket képkockákba rendezik, amelyek másodpercenként különböző képkockákon (fps) játszhatók le. Az SWF rövid webfájlt jelent, de Shockwave formátumú is.

Azok az alkalmazások, amelyek képesek voltak *SWF-fájlokat nyitni**, többek között az Adobe Flash Player (most már megszűnt) és az Eltima Elmedia Player.

## SWF fájlformátum – További információ

Az SWF-fájlokat bináris fájlként tárolták a lemezen. Az SWF fájlformátumot olyan animációk és játékok fejlesztésére használták, amelyek beágyazhatók weboldalakba, és önállóan is lejátszhatók. Támogatta a videókat és a hangokat is, amelyek sok választási lehetőséget biztosítottak a fejlesztőknek az interaktív multimédiás alkalmazások létrehozásához. Az SWF-fájlok lejátszhatók olyan webböngészőkkel, amelyekre telepítve van az Adobe Shockwave. Az Adobe Flash hiányosságai és biztonsági problémái miatt 2020 decemberében megszűnt.

## Az SWF fájlformátum rövid története

Az SWF fájlformátumot eredetileg a FutureWave Software tervezte, hogy animációkat jelenítsen meg azzal a szándékkal, hogy a lejátszószoftveren futni lehessen bármely lassabb hálózati kapcsolattal rendelkező rendszeren, miközben a fájl mérete kicsi marad. 1996 decemberében a Macromedia a FutureWave tulajdonában volt, és Macromedia Flash 1.0-ra alakították át.

2005-ben a Macromedia felvásárolta az Adobe, aki 2008-ban bejelentette az SWF-et nyílt forráskódú projektjének részeként. Ugyanebben az évben az Adobe kódot adott ki a világ népszerű webmotorjainak, hogy lehetővé tegye számukra az SWF-fájlok feltérképezését és indexelését. Mivel azonban úgy tűnik, hogy az SWF-fájlok a Flash-tartalom internetes közzétételének szabványos formátumává válnak, az SWF-et úgy módosították, hogy kis webformátumot jelentsen.

## SWF fájl szerkezet

Az útvonal az SWF alapvető grafikus eleme, amely alapvető elemek szegmenseinek sorozata, az egyszerű vonalaktól a Bezier-görbékig. Ezek az egyszerű elemek további primitívek, például kockák, ellipszisek és akár szövegek létrehozásában is segítenek. Az SWF grafikus primitívei hasonlóak más formátumok, például az SVG és az MPEG-4 BIFS grafikus elemeihez.

A formátum lehetővé teszi a listák megjelenítését és a már meghatározott elemek újrafelhasználását/átnevezését is. Az SWF bináris adatfolyam-formátuma a QuickTime atomokhoz hasonlítható, amelyek hasonlóak a címke, a méret és a hasznos terhelés tekintetében. A bináris adatfolyam formátum lehetővé teszi a régebbi lejátszók számára, hogy kihagyják a nem támogatott tartalmakat. Bár az SWF eredeti verziói csak vektorgrafikát és képeket kínáltak, ezért az új verziók lehetővé teszik a hang- és videótartalmakat is.

A Flash Player új, alacsony szintű 3D API-ját „Stage3D” néven a 11-es verzióban vezették be. Ezt az API-t az OpenGL vagy a Direct3D megfelelőjeként képzelték el. A Stage3D az Adobe Graphics Assembly Language (AGAL) nevű alacsony szintű nyelven határozza meg a színeket. Az alábbiakban az SWF fájlformátum néhány alapvető adattípusát ismertetjük.

### Koordináták

Az SWF fájlformátum XY koordinátái egész számokként vannak tárolva, és a twipnek nevezett egységben mérik. A twip egy logikai pixel 1/20-ából áll. A logikai pixel és a képernyő képpontja megegyezik, ha a fájlt 100%-os méretezés nélkül játssza le.

### Egész számtípusok és bájtsorrend

A 8, 16, 32 és 64 bites előjeles és előjel nélküli egész számok megengedettek SWF fájlformátumban. Little-endian byte order az egész értékek tárolására szolgál. Bár bájton belül, a bitsorrend big-endianban tárolódik. Minden egész értéknek bájtokhoz kell igazodnia. Az előjeles egész számokat hagyományos 2-komplement bitmintákkal ábrázoljuk.

### Fixpontos számok

Kétféle fixpontos számot támogat az SWF fájlformátum, azaz a 32 és 16 bites.

### Lebegőpontos számok

Az SWF 8 és újabb verziói háromféle lebegőpontos számot használnak (FLOAT, FLOAT 16, DOUBLE), amelyek kompatibilisek az IEEE 754 lebegőpontos típusokkal.

### Kódolt egész számok

A kódolt egész számok egyik típusát az SWF 9 és újabb verziók támogatják változó számú bájttal.

## Hivatkozások

* [SWF-fájlformátum](https://en.wikipedia.org/wiki/Swf)

