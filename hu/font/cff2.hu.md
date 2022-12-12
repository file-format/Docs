{
  "date" : "2020-08-20",
  "keywords" :[ "cff2 fájl", "cff2 fájlformátum", "mi az a cff2 fájl", "fájl", "cff2 példa", "cff2 fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CFF2 - Compact Font File Format version 2",
  "description":"További információ a CFF2 fájlformátumról és az API-król a CFF2 fájlok létrehozásához és megnyitásához.",
  "linktitle" : "CFF2",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-21"
}

## Mi az a CFF2 fájl?

A CFF2 fájlformátum a CFF fájlformátum 2.0-s verziója, és lehetővé teszi a karakterjelek körvonalainak és a CFF fájlformátumhoz hasonló metaadatok hatékony tárolását. A CFF2 abban különbözik a CFF-től, hogy egy OpenType betűtípussal összefüggésben CFF2 címkével ellátott „sfnt” táblaként használható. Nem használható önálló programként, és más OpenType táblák adataitól függ.

## CFF2 fájlformátum

A [CFF2 fájlformátum specifikációi](https://docs.microsoft.com/en-us/typography/opentype/spec/cff2) részleteket tartalmaz a belső adatelrendezésről, adattípusokról, táblázatokról és a fájlformátummal kapcsolatos egyéb belső információkról. Fejlesztői referenciaként hivatkozhat rá. Néhány részlet ezekről a következők.

### Adatelrendezés

A CFF2 fájlformátum bináris adatai logikailag több különálló adatstruktúraként vannak elrendezve. A bináris adatokon belüli elrendezés a következő táblázatban látható.

|Bejegyzés |Megjegyzések|
---|---|
|Fejléc |Rögzített hely|
|Top DICT| Fix hely|
|Global Subr INDEX| Fix hely|
|Változat |Üzlet|
|FDSelect |Csak akkor jelenjen meg, ha egynél több Font DICT van a Font DICT INDEX-ben.|
|Betűtípus DICT INDEX ||
|A DICT betűtípus tömbje| A Font DICT INDEX.|
|Privát DICT| Egy betűtípusonként DICT.|

Csak az első három struktúra fix helyeken alapul. A fennmaradó részeket eltolásokkal érik el, és ezek sorrendje módosítható.

### Adattípusok

A CFF2 fájlformátum a következő adattípusokat használja.

|Név |Tartomány |Leírás|
---|---|---|
|uint8 |0-tól 255-ig |8 bites előjel nélküli szám|
|uint16 |0-tól 65535-ig| 16 bites előjel nélküli szám|
|uint32 |0–4294967295| 32 bites előjel nélküli szám|
|Eltolás |változó| 1, 2, 3 vagy 4 bájtos eltolások (az Index táblázat OffSize mezőjében megadva)|
|OffSize |1-től 4-ig| Az 1 bájtos előjel nélküli szám az Eltolás mező vagy mezők méretét határozza meg|

Az összes többbájtos numerikus adatot és eltolási mezőt nagyméretű bájt sorrendben tárolja. A CFF2 formátum mentes a kitöltési bájtoktól, mivel nem tartja be az igazítási korlátozásokat.

### DICT adatok

A CFF2 fájlok a betűtípusszótár adatait kulcs-érték párokként tartalmazzák, kompakt tokenizált formátumban. A szótárkulcsok 1 vagy 2 bájtos operátorként, a szótárértékek pedig változó méretű numerikus operandusokként vannak kódolva. Három struktúra használja a DICT adatformátumot: "Top DICT", "Font DICT" és "Privát DICT". Számos, változó méretű egész szám típusú operandus van meghatározva és kódolva a következő táblázat szerint (az operandus első bájtja b0, második b1 és így tovább).

|Méret |b0 tartomány |Értéktartomány |Értékszámítás|
---|---|---|---|
|1 |32–246| -107 - +107 |b0 - 139|
|2 |247–250| +108 - +1131 |(b0 - 247) * 256 + b1 + 108|
|2 |251–254| -1131 - -108| -(b0 - 251) * 256 - b1 - 108|
|3 |28| -32768 - +32767| b1 << 8 | b2|
|5 |29| -(2^31) - +(2^31 - 1)| b1 << 24 \| b2 << 16 \| b3 << 8 \| b4|

### Fejléc

A bináris adat egy fejléccel kezdődik, amelynek formátuma az alábbi táblázatban látható.

|Típus |Név |Leírás|
---|---|---|
|uint8| főVerzió| Formázza a fő verziót. 2.|
|uint8| minorVersion| Formázza a kisebb verziót. Állítsa nullára.|
|uint8| headerSize| Fejléc mérete (byte).|
|uint16| topDictLength| A Top DICT struktúra hossza bájtban.|

## Hivatkozások

* [CFF2 fájlformátum](https://docs.microsoft.com/en-us/typography/opentype/spec/cff2)

