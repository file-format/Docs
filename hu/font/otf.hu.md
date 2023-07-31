{
  "date" : "2020-08-20",
  "keywords" :[ "otf fájl", "otf fájl formátum", "mi az otf fájl", "fájl", "otf példa", "otf fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OTF - TrueType Font File Format",
  "description":"További információ az OTF fájlformátumról és az API-król, amelyek OTF-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "OTF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-09-21"
}

## Mi az az OTF fájl?

Az .otf kiterjesztésű fájl OpenType betűtípus formátumra utal. Az OTF betűtípus skálázhatóbb, és kiterjeszti a [TTF](/hu/font/ttf/) formátumok meglévő szolgáltatásait a digitális tipográfia számára. A Microsoft és az Adobe által kifejlesztett OTF egyesíti a PostScript és a TrueType betűtípusok jellemzőit. Ez teszi az OTF formátumot a többségi írási rendszerek befogadására, és ezért egységesen használják a főbb számítógépes platformokon. Az OpenType betűtípus formátumot a Mac OS X és a Windows 2000 és újabb verziók támogatják.

## Rövid története

Az OpenType betűtípusok követelménye egy kifejezőbb betűformátum követelményeként keletkezett, amely képes kezelni a finom tipográfiát. Ezenkívül az volt a cél, hogy megfeleljen a világ számos írásrendszerének összetett viselkedési követelményeinek. A Microsoft az 1990-es évek elején megkísérelte licencelni az Apple fejlett tipográfiai technológiáját, amely GX Typography néven ismert. Ez nem ment jól, ennek eredményeként a Microsoft 1994-ben megkezdte saját TrueType betűtípus-technológiájának továbbfejlesztését. A módosítások között szerepelt egy megfelelőbb betűformátum bevezetése is, amely megfelel az Adobe Type 1 (PostScript) betűformátumainak jellemzőinek is.

Az Adobe 1996-ban csatlakozott a Microsofthoz az Apple TrueType és a saját Type 1 betűtípusok felülírására irányuló erőfeszítéseihez. Ennek eredményeként a két mögöttes betűformátum kombinációját sikerült leküzdeni a korlátokon és új kiterjesztéseket adni. Ezt az új technológiát ugyanabban az évben mutatták be **OpenType** néven.

## Az OTF fájlformátum specifikációi

Az OTF-specifikációk a Microsoft által nyilvánosan elérhetők, és a fejlesztők szemszögéből is hivatkozhatnak rájuk. A TTF-hez hasonlóan ugyanazt az „sfnt” tárolószerkezetet használja, és kompatibilis a TrueType specifikációival. Az OpenType betűtípusfájlon belüli adatokat különböző célokra használják fel, például a szövegelrendezés kiszámítására, a karakterjelek TrueType vagy Compact Font Format (CFF) körvonalaként történő meghatározására, monokromatikus vagy színes bittérképek vagy SVG-dokumentumok alternatív karakterjel-leírások biztosítására, valamint metaadat-információkra.

### OTF adattípusok
Az OTF-fájlok a következő adattípusokat használják, amelyek mindegyike a Big Endianban található.

|Adattípus| Leírás|
---|---|
|uint8| 8 bites előjel nélküli egész.|
|int8| 8 bites előjeles egész szám.|
|uint16| 16 bites előjel nélküli egész.|
|int16| 16 bites előjeles egész szám.|
|uint24| 24 bites előjel nélküli egész.|
|uint32| 32 bites előjel nélküli egész.|
|int32| 32 bites előjeles egész szám.|
|Rögzített| 32 bites előjeles fixpontos szám (16.16)|
|FWORD| int16, amely egy mennyiséget ír le font tervezési egységekben.|
|UFWORD| uint16, amely egy mennyiséget ír le font tervezési egységekben.|
|F2DOT14| 16 bites előjelű fix szám alacsony 14 bites törttel (2.14).|
|LONGDATETIME| A dátum és az idő másodpercek számában kifejezve 1904. január 1., UTC 12:00 éjfél óta. Az érték előjeles 64 bites egész számként jelenik meg.|
|Címke| Négy uint8-ból álló tömb (hossz = 32 bit), amely egy táblázat, tervezési variációs tengely, szkript, nyelvi rendszer, szolgáltatás vagy alapvonal azonosítására szolgál|
|Eltolás16| Rövid eltolás egy táblázathoz, ugyanaz, mint az uint16, NULL eltolás = 0x0000|
|Eltolás32| Hosszú eltolás egy táblázathoz, ugyanaz, mint az uint32, NULL eltolás = 0x00000000|
|Verzió16Dot16| Csomagolt 32 bites érték fő- és mellékverziószámokkal. (Lásd a táblázat verziószámait.)|

### OTF Tables Directory

Az OTF fájl egy táblakönyvtárral kezdődik. Ez a könyvtár a betűtípusfájl tábláinak legfelső szintű gyűjteménye. A fájlban lévő betűtípusok számától függően a táblázat könyvtára a fájl különböző helyein lehet. Például abban az esetben, ha a fontfájlnak csak egy betűtípusa van, a táblakönyvtár a fájl 0. bájtjával kezdődik. Több OpenType Fonts gyűjtemény esetén
a táblakönyvtár kezdetét a TTCHader jelzi.

|Típus |Név |Leírás|
---|---|---|
|uint32 |sfntVersion| 0x00010000 vagy 0x4F54544F ('OTTO')|
|uint16| numTables |Táblázatok száma.|
|uint16| searchRange |A 2 maximális hatványa kisebb vagy egyenlő, mint a numTables, szorozva 16-tal ((2\**floor(log2(numTables))) * 16, ahol a „**” egy hatványozási operátor).|
|uint16 |entrySelector Log2, amelynek maximális teljesítménye 2 kisebb vagy egyenlő, mint a numTables (log2(searchRange/16), ami egyenlő a floor(log2(numTables))).|
|uint16 |rangeShift |numTables szor 16, mínusz searchRange ((numTables * 16) - searchRange).|
|tableRecord| tableRecords[numTables] |Táblázatrekordok tömbje – egy a betűtípus minden legfelső szintű táblájához|


### Táblázat rekord

A betűtípus minden legfelső szintű táblázatához tartozik egy táblázatrekord, amely a következő mezőkből áll.

|Típus| Név| Leírás|
---|---|---|
|Címke| tableTag| Táblaazonosító.|
|uint32| ellenőrző összeg| Ellenőrző összeg ehhez a táblázathoz.|
|Eltolás32| eltolás| Eltolás a betűtípusfájl elejétől.|
|uint32| hossz E táblázat hossza.|

Az OpenType betűtípusfájlban minden táblát táblázatcímkékként ismert nevek képviselnek. A tömbben lévő összes rekordot kötelező címkénként növekvő sorrendbe rendezni.

## Hivatkozások
* [A Microsoft OpenType betűtípus-specifikációi](https://learn.microsoft.com/en-us/typography/opentype/spec/overview)
* [TrueType áttekintése](https://learn.microsoft.com/en-us/typography/truetype/)

