{
  "date" : "2023-06-18",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"További információ az ABS fájlformátumról és az API-król, amelyek ABS-fájlokat hozhatnak létre és nyithatnak meg.",
  "title" :"ABS fájlkiterjesztés - Delphi abszolút adatbázis-fájlformátum",
  "linktitle" : "ABS",
  "menu" : {
    "docs" : {
      "identifier":"database-abs",
      "parent" : "database"
}
},
  "lastmod" : "2023-06-18"
}

## Mi az ABS fájl?

Az .abs kiterjesztésű fájl az Absolute adatbázis által generált és használt adatbázis, amely a Delphi szoftverfejlesztő IDE adatbázismotorja. Leváltotta a Borland Database Engine-t (DBE), és kompaktabb, nagyobb sebességű, robusztusabb és könnyen használható. Az ABS-adatbázis az alkalmazás EXE-fájl részeként fordítható le, így az alkalmazás gyorsabbá és kisebbé válik. Az adatok ABS-fájlban tárolódnak strukturált, relációs formátumban.

## ABS fájlformátum - További információ

Az ABS-fájlok az alkalmazás [EXE-fájlja] (/hu/executable/exe/) részeként jelennek meg, amelyet általában bináris fájlként tárolnak. A bináris fájlok egyetlen szövegszerkesztőben sem nyithatók meg, és gyors hozzáférést biztosítanak az adatbázisfájl tartalmához.

### Az ABS fájlformátum főbb jellemzői

Az ABS fájlok meglehetősen egyszerűek, és beágyazódnak az alkalmazás végrehajtható fájljába. A következő tulajdonságokkal rendelkezik:

* Nincs BDE; nincsenek DLL-ek
* Egyfájlos adatbázis
* SQL'92 (DDL és DML) támogatás
* Kompatibilis a szabványos és harmadik féltől származó adatbázis-vezérlőkkel
* Egyfelhasználós és többfelhasználós mód (fájlszerver)
* Kiválóan működik a Windows összes verzióján – 98-tól a legújabbig, nem igényel frissítést vagy szervizcsomagot
* Ultragyors memóriatáblák
* Páratlan egyszerű használat
* Erős titkosítás
* BLOB tömörítés
* Személyes használatra ingyenes
* Teljes forráskód elérhető
* Jogdíjmentes terjesztés

## Hivatkozások

 * [Delphi Absolute Database File Format](https://www.componentace.com/bde_replacement_database_delphi_absolute_database.htm)
