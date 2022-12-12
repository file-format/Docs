{
  "date" : "2022-08-05",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"APPCACHE fájl – HTML5 gyorsítótár-jegyzékfájl formátum",
  "description" :"További információ arról, hogy mi az APPCACHE fájl és az API-k, amelyek APPCACHE fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "APPCACHE",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-08-05"
}

## Mi az APPCACHE fájl?

Az APPCACHE fájl egy szöveges fájl, amely a böngészők által a webalkalmazások offline eléréséhez gyorsítótárba helyezendő erőforrások listáját tartalmazza. Ez akkor hasznos, ha nincs internetkapcsolat. Ilyen helyzetben a böngésző az offline gyorsítótár erőforrásait használja a webtartalom eléréséhez. Az APPCACHE fájl internetes forrásokat tartalmaz, például képeket (például **[PNG](/hu/image/png/)**, **[WEBP](/hu/image/webp/)** stb.), stíluslapokat **([ CSS])(/hu/web/css/)** és szkriptfájlok (például Javascript **[JS](/hu/web/js/)** fájlok).

A **APPCACHE-fájlokat** megnyitni képes alkalmazások közé tartoznak a webböngészők, például a Google Chrome, a Safari és a Firefox.

## APPCACHE fájlformátum - További információ

Az APPCACHE fájlok egyszerű szöveges fájlok, amelyek offline hozzáférést biztosítanak a weboldalakhoz internetkapcsolat nélkül. Az APPCACHE jelenléte offline módban elérhetőnek jelöl egy oldalt.

### Hogyan hivatkozhatok egy APPCACHE fájlra?

A HTML-oldalon az alábbiak szerint hivatkozunk egy APPCACHE fájlra.

```
<html manifest="example.appcache">
  ...
</html>
```

## Egy APPCACHE Manifest fájl szerkezete

Egy egyszerű APPCACHE jegyzékfájl a következőképpen néz ki.

```
CACHE MANIFEST
index.html
stylesheet.css
images/logo.png
scripts/main.js
http://cdn.example.com/scripts/main.js
```

Ez a legegyszerűbb példa, és lehetnek bonyolultabb szerkezetek is.

## Az APPCACHE Manifest előnyei

A cache interfész használata a következő előnyöket nyújtja a webes alkalmazásoknak.

1. Offline böngészés – A gyorsítótár felület lehetővé teszi a végfelhasználók számára, hogy offline állapotban böngészhessék a teljes webhelyet
1. Sebesség – a gyorsítótár nagy sebességű hozzáférést tesz lehetővé az offline tartalomhoz közvetlenül a lemezről
1. Folyamatos hozzáférhetőség – Ha webhelye leáll, a felhasználók továbbra is hozzáférhetnek a webes tartalmakhoz, és offline élményben is részesülhetnek

## Hivatkozások

* [Útmutató kezdőknek az AppCache Manifesthez](https://web.dev/appcache-beginner/)

