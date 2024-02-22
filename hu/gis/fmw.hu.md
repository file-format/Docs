{
  "date" : "2022-05-06",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "FMW fájl - FME Workbench fájlformátum",
  "description":"Ismerje meg az FMW fájlformátumot és az API-kat, amelyek FMW fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "FMW",
  "menu" : {
    "docs" : {
      "identifier":"gis-fmw-hu",
      "parent" : "gis"
}
},
  "lastmod" : "2022-05-06"
}

## Mi az FMW fájl?

Az FMW fájl egy FME Workbench szoftverrel létrehozott projektfájl (az FME Desktop programcsomag része), amelyet téradatok átalakítására használnak. Tartalmazza a felhasználó által meghatározott beállításokat, amelyeket a téradatok kezeléséhez használnak, például bemeneti adatkészleteket, fordítási tulajdonságokat, vetítéseket és kimeneti beállításokat. A téradat-kezelési beállítások vizuális elrendezésként tárolódnak, és könnyen szerkeszthetők és újra elmenthetők.

Az FMW fájlokat a [Safe Software FME Desktop](https://www.safe.com/fme/fme-desktop/) használatával nyithatja meg.

## FMW fájlformátum - További információ

Az FMW fájlok bináris fájlként kerülnek a lemezre, és csak az FME Desktop szoftverrel olvashatók. A szoftver számos relációs adatbázis-formátumból is képes adatokat olvasni, és számos adatformátumot is támogat.

### FMW gyors tények

|Tény|Érték|
---|---|
|Olvasó/Író|Olvasó|
|Engedélyezési szint|Alap|
|Függőségek|Nincs|
|Adatkészlet típusa|Fájl|
|Funkció típusa|Rögzített|
|Tipikus fájlkiterjesztések|.fmw|
|Automatikus fordítás támogatása|Igen|
|Felhasználó által meghatározott attribútumok|Nem|
|Koordinátarendszer támogatása|Nem|
|Általános színtámogatás|Nem|
|Térbeli index|Szám|
|Séma szükséges|Nem|
|Tranzakciótámogatás|Nem|
|Geometry Type Attribútum|Nincs|
|Kódolás támogatása|Nem|

### FMW geometria támogatás

|Geometria|Támogatott?|
---|---|
|aggregátum|nem|
|körök|nem|
|körív|nem|
|fánk sokszög|nem|
|elliptikus ív|nem|
|ellipszisek|nem|
|sor|nem|
|nincs|igen|
|pont|nem|
|sokszög|nem|
|raszteres|nem|
|szilárd|nem|
|felszín|nem|
|szöveg|nem|
|z értékek|nem|


## Hivatkozások

* [Safe Software FME Desktop](https://www.safe.com/fme/fme-desktop/)

* [FMW Quick Facts](https://docs.safe.com/fme/html/FME_Desktop_Documentation/FME_ReadersWriters/fmw/quick_facts_fmw.htm)

