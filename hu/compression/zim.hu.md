{
  "date" : "2019-12-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ZIM fájlformátum - OpenZIM archív fájl",
  "description":"További információ a ZIM fájlformátumról és az API-król, amelyek ZIM fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "ZIM",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2019-12-09"
}

## Mi az a ZIM fájl? ##

A .zim kiterjesztésű fájlok a Wiki-tartalom offline tárolására létrehozott archívumok. Ez a legmegfelelőbb nyílt fájlformátum a Wikipédia USB-n való tárolására. A webhely tartalmát kompakt formátumban tárolja. A neve a "Zeno IMproved"-ből származik, amely a korábbi Zeno fájlformátum volt. A ZIM-et az [openZIM ](https://openzim.org/)projekt karbantartja, amelyet a Wikimedia CH szponzorál, és a Wikimedia Foundation támogat. A ZIM-fájlokat olyan alkalmazások nyithatják meg, mint a Kiwix és a ZIMReader. Az OpenZIM projekt a ZIM fájlformátum megvalósítását adta a [Github] (https://github.com/openzim) webhelyen az OpenSource közösség hozzájárulása érdekében.

## A ZIM fájlformátum specifikációi

A ZIM fájlformátumot a [Zeno fájlformátum] (https://openzim.org/wiki/Zeno_file_format) tetejére fejlesztették ki, és visszafelé nem kompatibilis. A ZIM fájlformátum formátumspecifikációi [elérhető online](https://openzim.org/wiki/ZIM_file_format) az openZIM-től, fejlesztői hivatkozásként. Az OpenZIM C++ nyílt forráskódú implementációt, [LibZim](https://openzim.org/wiki/Zimlib) biztosított a ZIM-fájlok olvasásához és írásához.

A ZIM fájlformátum LZMA2 tömörítést használ a tartalom tömörítéséhez.

{{< figure src="../ZIM_File_Format.jpeg" alt="ZIM fájlformátum" >}}


### ZIM fejléc

A ZIM fájl egy fejléccel kezdődik, amely 0 eltolású. Az összes összetevő a little-endian-on alapul, és minden egész előjel nélküli egész szám, azaz uint_16, uint_32, uint_64.

|Mező neve |Típus| Offset| Hossz| Leírás|
---|---|---|---|---|
|magicNumber| egész szám| 0| 4| A fájlformátum felismeréséhez szükséges mágikus számnak 72173914 (0x44D495A)|
|majorVersion| egész szám| 4| 2| A ZIM fájlformátum fő verziója (5 vagy 6)|
|minorVersion| egész szám| 6| 2| A ZIM fájlformátum kisebb változata|
|uuid| egész szám| 8| 16| ennek a zim-fájlnak az egyedi azonosítója|
|cikkszám| egész szám| 24| 4| cikkek teljes száma|
|clusterCount| egész szám| 28| 4| klaszterek teljes száma|
|urlPtrPos| egész szám| 32| 8| a címtármutatók listája URL| szerint rendezve
|titlePtrPos| egész szám| 40| 8| a címtármutató lista pozíciója a Title| szerint rendezve
|clusterPtrPos| egész szám| 48| 8| a fürtmutató lista helyzete|
|mimeListPos| egész szám| 56| 8| a MIME típuslista pozíciója (fejlécméret is)|
|főoldal| egész szám| 64| 4| főoldal vagy 0xffffffff, ha nincs főoldal|
|layoutPage| egész szám| 68| 4| elrendezési oldal vagy 0xffffffffff, ha nincs elrendezési oldal|
|checksumPos| egész szám| 72| 8| mutasson a fájl md5checksumára, maga az ellenőrzőösszeg nélkül. Ez mindig 16 bájttal a fájl vége előtt mutat.|

## Referenciák ##

* [OpenZIM](https://openzim.org/)
* [C++ LibZim](https://openzim.org/wiki/Zimlib)

