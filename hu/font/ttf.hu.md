{
  "date" : "2020-08-20",
  "keywords" :[ "ttf fájl", "ttf fájl formátum", "mi az a ttf fájl", "fájl", "ttf példa", "ttf fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TTF - TrueType Font File Format",
  "description":"A TrueType betűtípusok (TTF) az eredetileg az Apple, Inc. által tervezett digitális betűtípus-technológián alapulnak. Mind az Apple, mind a Microsoft TTF-et használt Mac és Windows operációs rendszereken.",
  "linktitle" : "TTF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-09-21"
}

## Mi az a TTF fájl?

A .ttf kiterjesztésű fájl a TrueType specifikációjú betűtípus-technológián alapuló betűtípus-fájlokat képvisel. Eredetileg az Apple Computer, Inc tervezte és dobta piacra Mac OS-hez, majd később a Microsoft is átvette a Windows operációs rendszerhez. A TrueType betűtípusok a legjobb minőségű megjelenítést biztosítják a számítógép képernyőjén és a nyomtatókon anélkül, hogy a felbontástól függnének. Minden modern, betűtípust használó alkalmazás képes TTF fájlokkal dolgozni. A TTF-betűkészlet-fájlok szabadon elérhetők az interneten, és más betűtípus-fájlformátumokká is konvertálhatók, például OTF és WOFF.

## Rövid története

Az Apply Computer, Inc. által az 1980-as években MacOS rendszerre tervezett TTF betűformátumot az Adobe Type 1 formátum néhány technikai korlátja volt. Az Apple 1991-ben támogatta a TrueType betűtípusokat Mac rendszerben. A TTF betűtípusok mögött meghúzódó tervezési cél a tárolás és a feldolgozás hatékonysága, valamint a bővíthetőség volt. E bővíthetőség alapján a meglévő betűtípusok átalakíthatók TrueType formátumba.

A Microsoft először 1992 áprilisában használta a TrueType betűtípusokat a Windows 3.1-ben, miután az Apple beleegyezett a TrueType licencébe a Microsoft számára. Javította a raszterezési mechanizmust, javította a hatékonyságát és teljesítményét.

## A True Type fájlformátum specifikációi

A TrueType betűtípusfájl egy bináris fájl, amely összefűzött táblák sorozatából áll. Minden táblázat egy szósorozat, és van egy neve, mint "Címke". Minden címke uint32 adattípusú, és négy karakterből áll. A fájl első táblázata a font könyvtár, amely hozzáférést biztosít a betűtípusfájl többi táblájához. A betűtípusadatokat a betűtípuskönyvtár-tábla után következő táblázatok tartalmazzák. Mivel minden tábla elérhető a címkéjével, a táblázatok bármilyen sorrendben megjelenhetnek a fájlban.

A szükséges táblák és címkeneveik a következő táblázatban láthatók.

|**Címke**|**Táblázat**|
---|---|
|'cmap'| karakter-jelkép leképezés|
|'glyf'| glyph data|
|'fej'| betűtípus fejléc|
|'hhea'| vízszintes fejléc|
|'hmtx'| vízszintes mérőszámok|
|'loca'| index a helyre|
|'maxp'| maximális profil|
|'név'| névadás|
|'post'| PostScript|

### Adattípusok
A TrueType betűtípusok az alábbi táblázatban felsorolt szabványos egész számokat és további adattípusokat használják.

|**Adattípus** | **Leírás** |
---|---|
|shortFrac| 16 bites előjeles tört|
|Rögzített| 16,16 bites előjeles fixpontos szám|
|FWord| 16 bites előjelű egész szám, amely egy mennyiséget ír le FU-egységben, a legkisebb mérhető távolság em térben.|
|uFWord| 16 bites előjel nélküli egész szám, amely egy mennyiséget ír le FU-egységben, a legkisebb mérhető távolság em térben.|
|F2Dot14| 16 bites előjelű fix szám, az alacsony 14 bit pedig törtet jelent.|
|longDateTime| Egy dátum hosszú belső formátuma másodpercekben 1904. január 1., 12:00 éjfél óta. Előjeles, 64 bites egész számként jelenik meg.|

### Betűtípuskönyvtár

A TrueType betűtípus első táblája az a betűtípus-könyvtár, amely hozzáférést biztosít a más táblákban lévő adatok eléréséhez szükséges információkhoz. A következőkből áll továbbá:

* `Eltolási altábla` - rögzíti a betűtípusban lévő táblázatokat, és eltolási információkat biztosít a könyvtár minden táblájának eléréséhez
* "Táblázatkönyvtár" - A betűtípus minden táblájához bejegyzést tartalmaz

#### Eltolás résztáblázat
Az eltolási résztáblázat az alábbiakban látható.

|**Típus**|**Név**|**Leírás**|
---|---|---|
|uint32| pikkelyes típus| A betűtípus raszterezéséhez használandó OFA-skálázót jelző címke; további információért lásd az alábbi megjegyzést a skálázó típusáról.|
|uint16| numTables| táblázatok száma|
|uint16| keresésTartomány| (2 maximális teljesítménye <= numTables)*16|
|uint16| entrySelector| log2(maximális hatványa 2 <= numTables)|
|uint16| rangeShift| numTables*16-searchRange|

#### Táblázatkönyvtár
A táblakönyvtár közvetlenül az eltolási altábla után található. Szerkezete a következő táblázatban látható.

|**Típus**|**Név**|**Leírás**|
---|---|---|
|uint32| tag| 4 bájtos azonosító|
|uint32| checkSum| ellenőrző összeg ehhez a táblázathoz|
|uint32| eltolás| eltolás az sfnt| elejétől
|uint32| hossza| ennek a táblázatnak a hossza bájtban (tényleges hossz nem kitöltött hossz)|

A betűtípusfájl minden táblájának saját táblakönyvtár-bejegyzéssel kell rendelkeznie. A táblázat bejegyzéseit címkék szerint növekvő sorrendbe kell rendezni.


## Hivatkozások
* [TrueType Font Reference Manual](https://developer.apple.com/fonts/TrueType-Reference-Manual/)
* [TrueType áttekintése](https://docs.microsoft.com/en-us/typography/truetype/)

