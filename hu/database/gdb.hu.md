{
  "date" : "2022-05-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GDB fájlformátum - ESRI fájl geoadatbázis-fájl",
  "description":"További információ a GDB fájlformátumról és az API-król, amelyek GDB fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "GDB",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2022-05-08"
}

## Mi az a GDB fájl?

Az ESRI fájl geoadatbázis (FileGDB) a lemezen lévő mappában lévő fájlok gyűjteménye, amelyek kapcsolódó térinformatikai adatokat, például jellemző adatkészleteket, jellemzőosztályokat és kapcsolódó táblázatokat tartalmaznak. A működéshez bizonyos más fájlokat a .gdb fájl mellett ugyanabban a könyvtárban kell tartani. Lekérdezések hajthatók végre a .gdb fájlon a térbeli és nem térbeli adatok kezelésére.

## GDB fájlformátum - További információ

A fájl geoadatbázisok hét rendszertáblából és felhasználói adatokból állnak. A felhasználói adatok a következő típusú adatkészletekben tárolhatók:

* Funkcióosztály
* Funkció adatkészlet
* Mozaik adatkészlet
* Raszteres katalógus
* Raszteres adatkészlet
* Sematikus adatkészlet
* Táblázat (nem térbeli)
* Eszköztárak

A szolgáltatásadatkészletek jellemzőosztályokat, valamint a következő típusú adatkészleteket tartalmazhatnak:

* Mellékletek
* Funkcióhoz kapcsolódó megjegyzés
* Geometriai hálózatok
* Hálózati adatkészletek
* Csomag szövetek
* Kapcsolati osztályok
* Terepek
* Topológiák

Az adatkészletek alapértelmezett maximális mérete a fájl geoadatbázisokban 1 TB. A maximális méret 256 TB-ra növelhető nagy adatkészletek (általában raszteres) esetén. Ezt egy konfigurációs kulcsszó vezérli. További információért lásd: Konfigurációs kulcsszavak fájlok geoadatbázisaihoz.

A fájlok geoadatbázisai altípusokat és tartományokat is tartalmazhatnak, és részt vehetnek a checkout/check-in replikációban és az egyirányú replikákban.

Egy fájl geoadatbázishoz egyszerre több felhasználó is hozzáférhet. Ha a felhasználók szerkesztenek, akkor különböző adatkészleteket kell szerkeszteniük.

## GDB fájlformátum specifikációi ##

A GDB fájl az ESRI saját formátuma, és specifikációi nem érhetők el nyilvánosan. Emiatt a FIle GDB fájlformátum részleteit nem tudták máshol dokumentálni, csak néhány forrásból, akik ezt [részben](https://github.com/rouault/dump_gdbtable/wiki/FGDB-Spec) tették visszafejtéssel. .

## Referenciák ##

* [FGDB-specifikációk](https://github.com/rouault/dump_gdbtable/wiki/FGDB-Spec)

