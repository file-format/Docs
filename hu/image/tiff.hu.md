{
  "date" : "2019-10-11",
  "keywords" :[ "tiff fájl", "tiff fájl formátum", "mi az a tiff fájl", "fájl", "tiff példa", "tiff fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TIFF - Képfájl formátum",
  "description":"További információ a TIFF fájlformátumról és az API-król, amelyek TIFF-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "TIFF",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az a TIFF fájl?

A TIFF vagy TIF, Tagged Image File Format, olyan raszterképeket jelöl, amelyeket különféle eszközökön való használatra terveztek, amelyek megfelelnek ennek a fájlformátum-szabványnak. Több színtérben képes kétszintes, szürkeárnyalatos, palettaszínes és színes képadatok leírására. Támogatja a veszteséges és a veszteségmentes tömörítési sémákat, hogy válasszon a tér és az idő között a formátumot használó alkalmazások számára. A formátum nem gépfüggő, és olyan korlátoktól mentes, mint a processzor, az operációs rendszer vagy a fájlrendszer.

## A TIFF fájlformátum rövid története

A TIFF fájlformátumot eredetileg az Aldus Corporation hozta létre 1986 őszén, a különböző szkennergyártókkal és szoftverfejlesztőkkel folytatott megbeszéléseket követően. A TIFF fájlformátum elsődleges célja az volt, hogy közös beolvasott képfájlformátumot biztosítson az összes asztali szkennergyártó számára. A csak bináris képformátum támogatásától kezdve a formátum az idő múlásával a szürkeárnyalatos és színes képek támogatására fejlődött. A TIFF fájlformátum-specifikációk kezdeti verziója Reivision 3.0-nak nevezhető, mivel két korábbi vázlatos kiadás volt. 1988-ban jelent meg egy jelentős 5.0-s verzió, amely támogatta a paletta színes képeket és az LZW tömörítést. Ezt követően 1992-ben tették közzé a TIFF fájlformátumok 6.0-s verzióját. 1994-ben az Adobe Systems felvásárolta az Aldust, és a specifikációk már elérhetőek és az Adobe Systems által karbantarthatók.

## A TIFF fájlformátum specifikációi

A TIFF fájlformátum bővíthető, és számos olyan felülvizsgálaton ment keresztül, amely lehetővé teszi korlátlan mennyiségű személyes vagy speciális célú információ felvételét. A TIFF-fájl egy 8 bájtos fejléccel kezdődik, ahol a bájtok száma 0-tól N-ig terjed. A lehetséges legnagyobb TIFF-fájl 2**32 bájt hosszú. A fájl egy 8 bájtos képfájl fejléccel kezdődik, amely közvetlenül egy képfájlra (IFD) mutat. Az IFD információkat tartalmaz a képről, valamint a tényleges képadatokra mutató mutatókat.

### TIFF-fájl fejléce

A 8 bájtos TIFF fájl fejléce a következő információkat tartalmazza:

**Bájtok 0-1:** A fájlban használt bájtsorrend. A törvényes értékek: „II”(4949.H)„MM” (4D4D.H).

A „II” formátumban a bájtok sorrendje mindig a legkisebb jelentőségű bájttól a legjelentősebb bájtig terjed mind a 16 bites, mind a 32 bites egész számok esetében. Ezt nevezzük little-endian byte ordernek. Az „MM” formátumban a bájtok sorrendje mindig a legjelentősebbtől a legkevésbé jelentősig terjed, mind a 16 bites, mind a 32 bites egész számok esetében. Ezt nevezik big-endian byte ordernek.

**2-3 bájt:** Tetszőleges, de gondosan kiválasztott szám (42), amely a fájlt TIFF-fájlként azonosítja. A bájtok sorrendje a 0-1 bájtok értékétől függ.

**4-7 bájt:** Az első IFD eltolása (byte-ban). A könyvtár a fejléc után bárhol lehet a fájlban, de szóhatáron kell kezdődnie. Az Image File Directory különösen követheti az általa leírt képadatokat. Az olvasóknak követniük kell a mutatókat, bárhová is vezetnek. A bájteltolás kifejezést ebben a dokumentumban mindig a TIFF-fájl elejéhez viszonyított helyre utaljuk. A fájl első bájtjának eltolása 0.

### Képfájl könyvtár

Az IFD információkat tartalmaz a képről, valamint a tényleges képadatokra mutató mutatókat. Ez a címtárbejegyzések számának (azaz a mezők számának) 2 bájtos számlálójából áll, amelyet 12 bájtos mezőbejegyzések sorozata követ. , amelyet a következő IFD 4 bájtos eltolása követ (vagy 0, ha nincs). Egy TIFF-fájlban legalább 1 IFD-nek kell lennie, és minden IFD-nek tartalmaznia kell legalább egy bejegyzést.

#### IFD Belépés

Minden 12 bájtos IFD bejegyzés a következő formátumú.


|Bájtok|Leírás
---|---|
|0-1|A mezőt azonosító címke
|2-3|A mező típusa
|4-7|A jelzett típus száma
|8-11|Az Értékeltolás, a mező értékének fájleltolása (bájtban). Az érték várhatóan szóhatáron kezdődik; a megfelelő Értékeltolás így páros szám lesz. Ez a fájleltolás bárhová mutathat a fájlban, még a képadatok után is

A TIFF mező egy logikai entitás, amely TIFF címkéből és annak értékéből áll. Ez a logikai koncepció IFD bejegyzésként valósul meg, plusz a tényleges érték, ha nem fér bele az érték/eltolás részbe, az IFD bejegyzés utolsó 4 bájtja. A TIFF mező és az IFD bejegyzés kifejezések a legtöbb kontextusban felcserélhetők.

### Alapvonal TIFF ###

Az alapszintű TIFF a TIFF magja, amely alapvető fontosságú, amelyet minden mainstream TIFF-fejlesztőnek támogatnia kell termékeiben. A TIFF formátumnak való megfelelés feltétele a TIFF alapkövetelményeinek betartása. Ezek a követelmények jól dokumentáltak a 6.0 specifikációs dokumentumban.

#### Több kép fájlonként ####

Egy TIFF-fájlban több IFD is lehet. Minden IFD meghatároz egy alfájlt. Az alfájlok egyik lehetséges felhasználási módja a kapcsolódó képek leírása, például egy faxküldés oldalai. Az alapszintű TIFF-olvasónak nincs szüksége az IFD-k olvasásához az elsőn kívül.

#### Képtípusok ####

Az alapvonal TIFF-képének típusai a következők:

**Kétszintű:** A kétszintű kép két színt tartalmaz – fekete és fehér. A TIFF lehetővé teszi az alkalmazások számára, hogy kétszintű adatokat írjanak ki a fehér nulla vagy a fekete nulla formátumban. Az információkat rögzítő mező neve **PhotometricInterpretation**.

* RGB színes

A kétszintű képek fotometriai értelmezési információi a következők:

Címke = 262 (106.H)
Típus = RÖVID
**Értékek**

|Érték|Leírás|
---|---|
|0|Kétszintű és szürkeárnyalatos képek esetén: a 0 fehérként jelenik meg. A maximális érték fekete színű. Ez a Compression#2| normál értéke
|1|BlackIsZero. Kétszintű és szürkeárnyalatos képek esetén: a 0 feketeként jelenik meg. A maximális érték fehérként jelenik meg. Ha ez az érték meg van adva a Compression#2-hez, akkor a képnek fordítva kell megjelennie és kinyomtatnia.|

**Szürkeárnyalatos:** A szürkeárnyalatos képek a kétszintű képek általánosítása. A kétszintű képek csak fekete-fehér képadatokat tárolhatnak, de a szürkeárnyalatos képek a szürke árnyalatait is tárolhatják. Az ilyen képek leírásához fel kell vennie vagy módosítania kell a következő mezőket. A többi kötelező mező megegyezik a kétszintű képekhez szükséges mezőkkel. Szürkeárnyalatos képek esetén Compression # 1 vagy 32773 (PackBits). A Baseline TIFF-ben a szürkeárnyalatos képek vagy tömörítetlen adatként tárolhatók, vagy a PackBits algoritmussal tömöríthetők.

A szürkeárnyalatos képek **BitsPerSample** információi a következők:

Címke = 258 (102.H)
Típus = RÖVID

Az összetevőnkénti bitek száma. A Baseline TIFF szürkeárnyalatos képek megengedett értéke 4 és 8, ami 16 vagy 256 különböző szürkeárnyalatot tesz lehetővé.

**Palet-Color:** A paletta színű képek hasonlóak a szürkeárnyalatos képekhez. Továbbra is van egy komponensük pixelenként, de a komponensértéket a rendszer indexként használja a teljes RGB-keresési táblázatban. Az ilyen képek leírásához hozzá kell adni vagy módosítani kell a következő mezőket. A többi kötelező mező ugyanaz, mint a szürkeárnyalatos képeknél.
A Palette-Color kép fotometriai értelmezési információi a következők:

Fotometriai értelmezés = 3 (Paletta színe).
ColorMapTag = 320 (140,H)
Típus = RÖVID
N = 3 * (2 BitsPerSample)

Ez a mező egy piros-zöld-kék színtérképet határoz meg (gyakran keresési táblázatnak nevezik) a palettaszínképekhez. A palettaszínű képeken egy pixelértéket használnak az RGB-keresési táblázatba való indexeléshez. Például egy 0 értékű palettaszín pixel a 0. Piros, Zöld, Kék hármas szerint jelenik meg. A TIFF ColorMap-ben az összes piros érték az első, ezt követik a zöld, majd a kék értékek. A ColorMap-ben a fekete színt 0,0,0, a fehéret pedig a 65535, 65535, 65535 jelek jelölik.

**RGB színes:** Az RGB-képen minden képpont három összetevőből áll: piros, zöld és kék. Nincs ColorMap. Az RGB-kép leírásához a következő mezőket és értékeket kell hozzáadnia vagy módosítania. A többi kötelező mező megegyezik a palettaszínes képekhez szükséges mezőkkel.

BitsPerSample = 8,8,8. Az alapvonal TIFF RGB képen minden komponens 8 bit mélységű.

PhotometricInterpretation = 2 (RGB), és nincs ColorMap.

Címke = 277 (115.H)
Típus = RÖVID
Az összetevők száma pixelenként. Ez a szám 3 RGB-képeknél, hacsak nincsenek jelen extra minták.

## Hivatkozások ##

* [TIFF fájlformátum – Wikipédia](https://en.wikipedia.org/wiki/TIFF)

