{
  "date" : "2019-10-11",
  "keywords" :[ "tga fájl", "tga fájl formátum", "mi az a tga fájl", "fájl", "tga példa", "tga fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TGA fájlformátum - TARGA grafikus képfájl",
  "description":"További információ a TGA fájlformátumról és az API-król, amelyek TGA-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "TGA",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az a TGA fájl?

A .tga kiterjesztésű fájl egy raszteres grafikai formátum, amelyet a Truevision Inc. hozta létre. A TARGA (Truevision Advanced Raster Adapter) kártyákhoz tervezték, és Highcolor/truecolor megjelenítési támogatást nyújtott az IBM-kompatibilis PC-k számára. Támogatja a 8, 16, 24 és 32 bit/pixel és 8 bites alfa csatornát. Támogatja a veszteségmentes RLE tömörítést is, amely a képméret csökkentésére alkalmazható. A digitális fényképek és textúrák a TGA képformátumot használják.

## Rövid története

A TGA fájlformátumot 1984-ben hozta létre az AT&T EPICenter (később kibontották és független entitásként alakult Truevision néven), amely az AT&T által a színes keretpufferekhez kifejlesztett új technológiák marketingjén dolgozott. Az EPICenter már dolgozott az első két kártyáján, a VDA-n (Video Display Adapter) és az ICB-n (képrögzítő kártya), amelyek esetében két fájltípuson, a .vda-n és az .icb-n már folyamatban volt a munka. Ezeket a fájlformátumokat kodifikálták, és bevezették a kevésbé specifikus TGA fájlformátumot. A TGA a már használatban lévők kiterjesztése volt, és olyan információkat szolgáltatott, mint a szélesség, magasság, pixelmélység, a kapcsolódó színtérkép és a kép eredete.

A TGA 1989-ben megjelent 2.0-s verziója számos továbbfejlesztett funkciót tartalmazott, mint például:

* Bélyegképek
* Alfa csatorna
* Gamma érték
* Szöveges metaadatok

A TGA 2.0-s verziójának fő közreműködői közé tartozik a Truevision munkatársa, Shawn Steiner, Kevin Fiedly és David Spoelstra.

## A TGA TARGA fájlformátum specifikációi

A TGA-fájl 2 fő részből áll:

* Fejléc
* Színes pixel információk

A TGA-fájlban lévő összes érték a formátum specifikációi szerint kis-endian nyelven van megadva.

### TGA fejléc

A TGA-fájl fejléce a következő 5 mezőből áll.

|Mezőszám|Hosszú |Mezőnév |Leírás|
---|---|---|---|
|1| 1 bájt |ID hossza| A képazonosító mező hossza (0-255)|
|2| 1 bájt |Színtérkép típusa| Színtérképet tartalmaz-e (0 - azt jelzi, hogy a kép nem tartalmaz színtérképet. 1 - azt jelzi, hogy a kép színtérképet tartalmaz.)|
|3| 1 bájt |Képtípus| Tömörítés és színtípusok (0 – Nincs képadat. 1 – Tömörítetlen, Színleképezett kép, 2 – Tömörítetlen, Valódi Színes kép, 9 – Futáshosszú kódolás, Színes leképezésű kép, 11 – Futáshosszú kódolás, Fekete-fehér kép )|
|4| 5 bájt |Színtérkép specifikáció| Leírja a színtérképet|
|5| 10 bájt |Képspecifikáció| Kép méretei és formátuma|

### Kép és színes térképadatok

|Mező sz. |Hosszú |Mező |Leírás|
---|---|---|---|
|6 |A képazonosító hosszmezőből| Képazonosító| Azonosító információkat tartalmazó opcionális mező|
|7 |Színes térkép specifikációs mezőből| Színes térképadatok| Színtérképadatokat tartalmazó keresőtábla|
|8 |A képspecifikációs mezőből| Képadatok| A képleíró szerint tárolva|

### Fejlesztői terület (opcionális)

A TGA 2.0-s verziója támogatja a további fejlesztéseket/extrákat, amelyekről sok fejlesztő több információt szeretett volna tárolni. Az információ nem kötelező, így ha egy TGA dekóder nem tudja értelmezni, akkor figyelmen kívül hagyja.

### Bővítési terület (opcionális)

|Mezőszám| Hossz| Mező |Leírás|
---|---|---|---|
|10| 2 bájt |Bővítmény mérete |A kiterjesztési terület mérete bájtban, mindig 495|
|11| 41 bájt| Szerző neve |A szerző neve. Ha nem használja, a bájtokat NULL-ra (\0) vagy szóközre kell állítani
|12| 324 bájt| Szerző megjegyzés| Négy sorba rendezett megjegyzés, mindegyik 80 karakterből és egy NULL|-ból áll
|13| 12 bájt| Dátum/időbélyeg |A kép létrehozásának dátuma és időpontja|
|14| 41 bájt| Munkaazonosító ||
|15| 6 bájt| Munkaidő| A fájl létrehozásával töltött órák, percek és másodpercek (számlázáshoz stb.)|
|16| 41 bájt| Szoftverazonosító |A fájlt létrehozó alkalmazás.|
|17| 3 bájt| Szoftver verzió||
|18| 4 bájt| Kulcs színe||
|19| 4 bájt| Pixel képarány||
|20| 4 bájt| Gamma érték||
|21| 4 bájt| Színkorrekciós eltolás |Bájtok száma a fájl elejétől a színkorrekciós táblázatig, ha van|
|22| 4 bájt| Postai bélyeg | A bájtok száma a fájl elejétől a bélyegképig, ha van|
|23| 4 bájt| Pásztázási vonal eltolás| Bájtok száma a fájl elejétől a vizsgálati sorok táblázatáig, ha van|
|24| 1 bájt| Attribútumok típusa| Megadja az alfa csatornát|

### Fájlláb (opcionális)

A fájl utolsó 26 bájtja a láblécet jelenti, amely, ha van, valószínűleg egy TGA 2-es verziójú fájlt jelent.

|Mezőszám| Hossz| Mező| Leírás|
---|---|---|---|
|28| 4 bájt| Kiterjesztés eltolás| Eltolás bájtban a fájl elejétől|
|29| 4 bájt| Fejlesztői terület eltolás| Eltolás bájtban a fájl elejétől|
|30| 16 bájt| Aláírás| Tartalmazza: "TRUEVISION-XFILE"|
|31| 1 bájt| | Tartalmaz "."|
|32| 1 bájt| | NULL|-t tartalmaz


## Hivatkozások

* [TGA 2.0 fájlformátum specifikációi](https://products.conholdate.app/viewer/view/rVqTeZPLAL/tga-file-format-specifications.pdf?default=view&preview = true.pdf)
* [TGA a Wikipedia-tól](https://en.wikipedia.org/wiki/Truevision_TGA)

