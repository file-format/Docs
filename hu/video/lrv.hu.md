{
"dátum": "2023-06-21",
  "keywords": [
"lrv fájl",
"mi az lrv fájl",
"GoPro LRV fájl",
"THM File GoPro",
"hogyan lehet megnyitni az LRV fájlokat",
"fájl",
"lrv fájlkiterjesztés",
"kiterjesztés"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "LRV fájlformátum - alacsony felbontású videofájl a GoPro-tól",
  "description":"További információ az LRV-formátumról és az LRV-fájlok létrehozására és megnyitására alkalmas API-król.",
"linktitle": "LRV",
  "menu": {
    "docs": {
      "identifier": "video-lrv",
      "parent": "video"
}
},
"lastmod": "2023-06-21"
}

## Mi az LRV fájl?

Az LRV-fájl, más néven alacsony felbontású videófájl, egy olyan videofájl-formátum, amely a videó kisebb felbontású változatát tartalmazza, és általában a videószerkesztési munkafolyamatok során és a nagy felbontású videofájlok kis felbontású másolatainak létrehozására használt videógyártásban használatos. a gyorsabb és gördülékenyebb szerkesztési folyamatok megkönnyítése érdekében, különösen nagy videofájlok vagy korlátozott feldolgozási teljesítményű rendszerek használatakor.

Az LRV fájlokat jellemzően kamerarendszerek generálják, például a GoPro kamerák, amelyek a felvételi folyamat során az eredeti videó alacsonyabb felbontású változatát hozzák létre, lehetővé téve a felhasználók számára a felvételek gyors áttekintését, az alapvető szerkesztési feladatok elvégzését és a kijelölések elvégzését anélkül, hogy nagyobb, magas felbontást kellene kezelniük. -felbontású fájlok.

Az LRV fájlformátum gyakran használ H.264 vagy H.265 videotömörítési kodeket a fájl méretének csökkentésére, miközben fenntartja a megfelelő minőségi szintet, de továbbra is képesek a tartalom megfelelő előnézetét biztosítani. A kamera beállításaitól függetlenül az LRV videót folyamatosan 240p felbontásban rögzítik, 29,97 képkocka/másodperc képkocka sebességgel.

## GoPro LRV fájl

A GoPro kamerák a felvételi folyamatuk részeként LRV (Low-Resolution Video) fájlokat generálnak. Az LRV fájlok nagy felbontású videofájlok mellett jönnek létre (általában MP4 formátumban), és gyengébb minőségű proxyként szolgálnak a könnyebb és gyorsabb szerkesztés érdekében.

A GoPro kamerákban található LRV-fájlok célja, hogy a rögzített felvételek könnyű változatát biztosítsák, amely könnyen kezelhető szerkesztő szoftverekkel és korlátozott feldolgozási teljesítményű rendszerekkel. Ezek a fájlok lehetővé teszik a felhasználók számára, hogy megtekinthessék és szerkeszthessék videóikat anélkül, hogy közvetlenül a nagyobb, nagy felbontású fájlokkal kellene dolgozniuk, amelyek erőforrás-igényesek lehetnek.

A GoPro LRV fájlok általában alacsonyabb felbontásúak, alacsonyabb bitsebességgel és tömörített kodekekkel rendelkeznek, mint az eredeti nagy felbontású fájlok. Vizuális referenciaként szolgálnak a szerkesztési folyamat során, és simább lejátszást és súrolást tesznek lehetővé a szerkesztő szoftveren belül.

GoPro felvételekkel történő szerkesztéskor a legtöbb videószerkesztő szoftver automatikusan felismeri a nagy felbontású videókhoz társított LRV fájlokat. Ez a zökkenőmentes integráció lehetővé teszi a felhasználók számára, hogy a proxyfájlok segítségével szerkesszenek, majd a végső projektet újra összekapcsolják a nagy felbontású fájlokkal renderelés és exportálás céljából.

## THM File GoPro

A THM fájlok GoPro kamerák által generált kis miniatűr fájlok. Ezek a fájlok a megfelelő videofájlok mellett jönnek létre, és vizuális előnézetként vagy miniatűrként szolgálnak a rögzített felvételek könnyebb azonosítása és rendszerezése érdekében.

Ha videót rögzít GoPro kamerával, az egy THM-fájlt hoz létre, amelynek alapneve megegyezik a videofájléval, de .THM kiterjesztéssel. Például, ha van egy "example.MP4" nevű videója, akkor a megfelelő miniatűr fájl "example.THM" lesz.

A THM-fájlok általában kis méretűek, és alacsony felbontású képet tartalmaznak, amely a megfelelő videó képkockáját ábrázolja. Bármilyen képnézegetővel vagy médialejátszóval megtekinthetők, amely támogatja a JPEG képformátumot.

A THM-fájlok fő célja, hogy gyors vizuális referenciaként szolgáljanak a kapcsolódó videofájlok tartalmának azonosításához anélkül, hogy le kellene játszani vagy megnyitni őket. Általában GoPro kamerákon való felvételek böngészésére és rendszerezésére, vagy fájlok számítógépre való átvitelére használják.

## LRV fájlokat hogyan lehet megnyitni?

Az LRV (Low-Resolution Video) fájlok megnyitásához és megtekintéséhez kövesse az alábbi lépéseket:

- **Átnevezés MP4-re:** LRV-fájl megnyitásához és lejátszásához egyszerűen megteheti, ha átnevezi a fájl kiterjesztését [.MP4]-re (/hu/video/mp4/), és bármilyen olyan alkalmazást használ, amely képes .MPEG4-videófájlok lejátszására. .

- **Videószerkesztő szoftver:** Az LRV fájlok megnyitásának és kezelésének leggyakoribb módja a videószerkesztő szoftver. A legtöbb professzionális videószerkesztő szoftver, mint például az _Adobe Premiere Pro_, a _Final Cut Pro_ vagy a _Davinci Resolve_, képes felismerni és importálni az LRV fájlokat. Egyszerűen importálja az LRV fájlokat a projektbe, és megtekintheti és szerkesztheti a felvételt.

- **GoPro szoftver:** A GoPro saját, _GoPro Quik_ nevű szoftvert kínál, amelyet kifejezetten a GoPro felvételekkel való munkához terveztek. A GoPro Quik letölthető és telepíthető a hivatalos GoPro webhelyről. A telepítés után nyissa meg a szoftvert, importálja LRV fájljait, és megtekintheti és szerkesztheti őket az alkalmazáson belül.

- **Médialejátszók:** Bár az LRV-fájlokat általában nem közvetlen lejátszásra szánják, használhat bizonyos médialejátszókat, amelyek képesek ezeket a fájlokat lejátszani. A _VLC_ médialejátszó népszerű választás, amely különféle videoformátumokat és kodekeket támogat. Letöltheti és telepítheti a VLC-t, majd megnyithatja az LRV fájlt közvetlenül a médialejátszón keresztül.

- **Fájlkonverzió:** Ha inkább az LRV fájlokat szeretné szélesebb körben támogatott videoformátumba konvertálni, használhat videokonverziós szoftvert. Az olyan eszközök, mint a _Handbrake_ vagy a _Freemake Video Converter_, lehetővé teszik az LRV-fájlok konvertálását olyan formátumokba, mint például [MP4](/hu/video/mp4/), amelyeket számos médialejátszó vagy videoszerkesztő szoftver nyithat meg.

## Hivatkozások
* [GoPro LRV- és THM-fájlok](https://shotkit.com/lrv-thm-file/)

