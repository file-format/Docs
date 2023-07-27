{
  "date" : "2019-10-11",
  "keywords" :[ "bmp fájl", "bmp fájl formátum", "mi az a bmp fájl", "fájl", "bmp példa", "bmp fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"BMP - Képfájl formátum",
  "description":"További információ a BMP fájlformátumról és az API-król, amelyek BMP fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "BMP",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

# Mi az a BMP fájl? #

A .BMP kiterjesztésű fájlok olyan bittérképes képfájlokat képviselnek, amelyeket bittérképes digitális képek tárolására használnak. Ezek a képek függetlenek a grafikus adaptertől, és eszközfüggetlen bittérkép (DIB) fájlformátumnak is nevezik őket. Ez a függetlenség azt a célt szolgálja, hogy a fájlt több platformon, például Microsoft Windowson és Macen is megnyissa. A BMP fájlformátum kétdimenziós digitális képként képes tárolni az adatokat mind monokróm, mind színes formátumban, különböző színmélységgel.

## BMP fájlformátum specifikációi ##

Az eszközfüggetlen bittérképek segítik az eszközök és alkalmazások közötti bittérképek cseréjét. A fájlformátum folyamatos fejlődése miatt a fejlécekben található információk a Bitmap verziójától függően eltérőek lehetnek. Egyetlen bittérképes fájl meghatározott sorrendben rögzített és változó méretű struktúrákból áll.

A Bitmap fájl struktúrái a következő sorrendben vannak elrendezve:


|Struktúra|Opcionális|Méret|Cél
---|---|---|---|
|Fájlfejléc|Nem|14|Általános információk tárolására a bittérképes képfájlról
|DIB fejléc|Nem|Rögzített méretű|Részletes információk tárolása a bittérképes képről és a pixelformátum meghatározása
|Extra bitmaszkok|Igen|12 vagy 16 bájt|A pixelformátum meghatározása
|Színpaletta|Félig választható|Változó méretű|A bittérképes képadatok által használt színek meghatározása
|Gap1|Igen|Változó méretű|Struktúra-igazítás
|Pixel Array|No|Variable-size|A pixelformátumot a DIB fejléc vagy az Extra bitmaszkok határozzák meg.
|Gap2|Igen|Változó méretű|Struktúra-igazítás
|ICC Color profile|Yes|Variable-size|A színprofil meghatározása a színkezeléshez

Amikor egy bittérképes kép betöltődik a memóriába, az DIB-struktúrává válik, amelyet a Windows a GDI API-ján keresztül használ. A Fájl fejléc nem része ennek az adatstruktúrának. A szín 16 bites bejegyzésekből is állhat, amelyek explicit RGB színdefiníciók helyett indexeket alkotnak az éppen hivatkozott palettához. Nézzünk meg néhányat ezek közül részletesen, különösen a fejléceket.

### Bittérképes fájl fejléce ###

A bittérképes fájlfejléc hasonló a fájl azonosítására használt többi fájlfejléchez. Mivel a BMP fájlformátumnak különböző változatai léteznek, a BMP fájlformátum első 2 bájtja a „B” karakter, majd az „M” karakter ASCII kódolásban. Minden egész érték kis-végi formátumban van tárolva.

|Eltolás hatszög|Eltolás dec|Méret|Cél
---|---|---|---|
|00|0|2 bájt|A BMP és DIB fájl azonosítására használt fejléc mező 0x42 0x4D hexadecimális formában, ugyanaz, mint a BM az ASCII-ben. Követheti a lehetséges értékeket.* **BM** – Windows 3.1x, 95, NT, ... stb. * **BA** – OS/2 struct bitmap tömb * **CI** – OS/2 struct színes ikon * **CP** – OS/2 állandó színmutató * **IC** – OS/2 struktúra ikon * **PT** – OS/2 mutató
|02|2|4 bájt|A BMP fájl mérete bájtban
|06|6|2 bájt|Fenntartva; A tényleges érték a képet létrehozó alkalmazástól függ
|08|8|2 bájt|Fenntartva; A tényleges érték a képet létrehozó alkalmazástól függ
|0A|10|4 bájt|Annak a bájtnak az eltolása, azaz kezdőcíme, ahol a bittérképes képadatok (pixeltömb) találhatók.

#### DIB fejléc (bittérképes információs fejléc) ####

A képre vonatkozó részletes információkat ez a fejléc képviseli. Ezen információk alapján a rendszer meghatározza azt az alkalmazást, amely a kép képernyőn való megjelenítésére szolgál. Minden ilyen fejléc tartalmaz egy DWORD (32 bites) mezőt, amely megadja a méretüket, így az alkalmazás könnyen meghatározhatja a képben használt fejlécet. Ez alapvetően annak tudható be, hogy a DIB formátum több kiterjesztésen esett át. Az alábbiakban látható a DIB fejléc felsorolt mezőkkel.

#### Szín paletta ####

A BMP színpaletta olyan struktúrák tömbje, amelyek meghatározzák a megjelenítő eszköz színpalettáján szereplő egyes színek RGB intenzitásértékeit. A bittérképes adatok minden képpontja egyetlen, indexként használt értéket tárol a színpalettán. Az adott indexen lévő elemben tárolt színinformáció határozza meg az adott pixel színét. A bittérképes fájlok színének elérhetősége az alábbiak szerint változik:

* Egy, 4 és 8 bites – várhatóan mindig tartalmaz egy színpalettát
* Tizenhat, 24 és 32 bites – soha nem tartalmaz színpalettát
* Tizenhat és 32 bites BMP-fájlok – a színpaletta helyett bitmezőmaszkértékeket tartalmaznak

#### Pixel tárhely ####

A bittérképes pixeleket a rendszer sorokba csomagolt bitekként tárolja, ahol az egyes sorok méretét kitöltéssel felfelé kerekítik 4 bájt többszörösére (32 bites duplaszó). A kép pixeleinek tárolásához szükséges bájtok teljes mennyisége nem számítható ki közvetlenül a bitek megszámlálásával. Mivel kitöltésről van szó, az egyes sorok méretét 4 bájt többszörösére kell kerekíteni. Kitöltő bájtokat (nem feltétlenül 0-t) kell a sorok végéhez hozzáfűzni, hogy a sorok hossza négy bájt többszörösére nőjön. Amikor a pixeltömb betöltődik a memóriába, minden sornak egy olyan memóriacímen kell kezdődnie, amely 4 többszöröse.

A képet valójában a pixeltömb 32 bites duplaszó-ábrázolása írja le. A pixelek tárolása általában "alulról felfelé", a bal alsó sarokban kezdődik, balról jobbra haladva, majd soronként alulról felfelé haladva a képen. A pixelformátumok és következményeik az alábbiak:

* Az 1 bit/pixel (1 bpp) formátum 2 különböző színt támogat (például: fekete és fehér).
* A 2 bit/pixel (2bpp) formátum 4 különböző színt támogat, és 1 bájtonként 4 pixelt tárol, a bal szélső pixel pedig a két legjelentősebb bitben található. Minden pixelérték egy 2 bites index egy legfeljebb 4 színből álló táblázatba.
* A 4 bit/pixel (4bpp) formátum 16 különböző színt támogat, és 2 képpontot tárol 1 bájtonként, a bal szélső pixel pedig a jelentősebb nibble-ben van. Minden pixelérték egy 4 bites index egy legfeljebb 16 színt tartalmazó táblázatba.
* A 8 bit/pixel (8bpp) formátum 256 különböző színt támogat, és 1 bájtonként 1 pixelt tárol. Minden bájt egy index egy legfeljebb 256 színt tartalmazó táblázatba.
* A 16 bit/pixel (16 bpp) formátum 65536 különböző színt támogat, és 1 képpontot tárol 2 bájtos WORD-onként. Minden WORD meghatározhatja a pixel alfa, piros, zöld és kék mintáját.
* A 24 bites pixel (24 bpp) formátum 16 777 216 különböző színt támogat, és 3 bájtonként 1 pixel értéket tárol. Minden pixelérték meghatározza a pixel vörös, zöld és kék mintáját (RGAX jelöléssel 8.8.8.0.0). Pontosabban a következő sorrendben: kék, zöld és piros (mintánként 8 bit).
* A 32 bites képpontonkénti (32 bpp) formátum 4 294 967 296 különböző színt támogat, és 1 pixelt tárol 4 bájtos duplaszónként. Mindegyik duplaszó meghatározhatja a pixel alfa, piros, zöld és kék mintáját.

## Referenciák ##

* [Windows MetaFile formátum](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-wmf/4813e7fd-52d0-4f42-965f-228c8b7488d2)
* [BMP fájlformátum](https://en.wikipedia.org/wiki/BMP_file_format)

