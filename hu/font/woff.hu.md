{
  "date" : "2020-08-20",
  "keywords" :[ "woff fájl", "woff fájl formátum", "mi az a woff fájl", "fájl", "woff példa", "woff fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"WOFF - Web Open File Format",
  "description":"A WOFF fájl egy nyílt betűtípus formátum, amelyet a Web Open Font Format formátumban hoztak létre.",
  "linktitle" : "WOFF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-09-30"
}

## Mi az a WOFF fájl?

A .woff kiterjesztésű fájl egy webes betűtípusfájl, amely a Web Open Font Format (WOFF) formátumon alapul. Formátumspecifikus tömörített tárolóval rendelkezik, amely TrueType (.TTF) vagy OpenType (.OTT) betűtípusokon alapul. A WOFF-ot azzal a céllal vezették be, hogy a webes betűtípusokat megkülönböztessék az asztali alkalmazásokban használt betűtípusfájloktól. Ezenkívül a formátum a kiszolgálóról az ügyfél számítógépére a hálózaton keresztül történő betűtípusok átvitelének késleltetésének csökkentését célozza. Számos eszköz áll rendelkezésre, amelyek a WOFF-fájlokat TTF-re és más betűtípus-fájlformátumokra konvertálhatják.

## **WOFF fájlformátum**

A WOFF betűtípus formátum tömöríti a táblázat alapú sfnt struktúrák betűtípus-adattáblázatait, amelyeket különböző betűtípusokban, például TrueType, OpenType és Open Font Format használnak. Ez olyan, mint egy tároló ezeknek a betűtípusoknak, és van helye a betűtípus metaadatainak és a tárolóba beillesztendő magáncélú adatoknak. A konverterek az sfnt fájlokat WOFF formátumú fájllá használják, a felhasználói ügynökök pedig visszaállítják a kódolt fájlt a webdokumentumhoz való használatra. Megjegyzendő, hogy a visszaállított betűtípusadatok minden szempontból pontosan megegyeznek a bemeneti betűtípus formátumával.

A WOFF fájl segédprogramok gyakran tartalmaznak további szolgáltatásokat, például karakterjel-alkészletet, érvényesítést vagy betűtípus-jellemzőket, de ez nem szükséges. Mind az alkotónak, mind a felhasználói ügynöknek gondoskodnia kell az alapul szolgáló betűtípusadatok érvényességének megőrzéséről.

### WOFF fájlstruktúra

A WOFF fájl szerkezete hasonló az sfnt betűtípusokhoz. Egy táblakönyvtáron alapul, amely tartalmazza az egyes betűtípus-adattáblázatok hosszát és eltolásait. Az összes táblázatot követjük ezen kezdeti információk után. A fájl olyan betűkészlet-adatbázist tartalmaz, amely megegyezik az eredeti betűtípusokkal. A táblázatok sorrendje is azonos, de mindegyik tömöríthető. A WOFF táblakönyvtár azonban lecseréli az eredeti táblakönyvtárat.

A WOFF fájl a következőkből áll:

* WOFFHeader - Fájlfejléc alapvető betűtípussal és -verzióval, valamint metaadatok és privát adatblokkok eltolásai.
* TableDirectory - Betűtáblák könyvtára, amely jelzi az eredeti méretét, tömörített méretét és az egyes táblák helyét a WOFF-fájlban.
* FontTables – A bemeneti sfnt font betűtípus-adattáblázatai, tömörítve a sávszélesség-szükséglet csökkentése érdekében.
* ExtendedMetadata – A kiterjesztett metaadatok opcionális blokkja, amely XML formátumban jelenik meg, és a WOFF fájlban való tároláshoz tömörítve van.
* PrivateData – A privát adatok opcionális blokkja a betűtípustervező, öntöde vagy szállító számára.

### WOFF fejléc
A WOFF fejléc egy azonosító aláírást tartalmaz, amely jelzi, hogy a fájl milyen típusú adatokat tartalmaz. A WOFF fejléc a mezőivel együtt a következő.

|Típus|Mezőnév|Leírás|
---|---|---|
|UInt32|aláírás |0x774F4646 'wOFF' |
|UInt32| flavor |A beviteli betűtípus "sfnt verziója".|
|UInt32| hossz |A WOFF fájl teljes mérete.|
|UInt16| numTables |Bejegyzések száma a betűtípustáblázatok könyvtárában.|
|UInt16| fenntartva |Fenntartva; nullára állítva.|
|UInt32| totalSfntSize |A tömörítetlen betűtípusadatokhoz szükséges teljes méret, beleértve az sfnt fejlécet, a könyvtárat és a betűtípustáblázatokat (beleértve a kitöltést is).|
|UInt16| majorVersion |A WOFF fájl fő verziója.|
|UInt16| minorVersion |A WOFF fájl kisebb verziója.|
|UInt32| metaOffset |Eltolás a metaadatblokkhoz, a WOFF fájl elejétől.|
|UInt32| metaLength |Tömörített metaadatblokk hossza.|
|UInt32| metaOrigLength |A metaadatblokk tömörítetlen mérete.|
|UInt32| privOffset |Eltolás a privát adatblokkhoz, a WOFF fájl elejétől.|
|UInt32| privLength |Privát adatblokk hossza.|


## **Referenciák**
* [w3 WOFF fájlformátum](https://www.w3.org/TR/WOFF/)

