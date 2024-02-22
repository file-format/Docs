{
  "date" : "2022-12-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "ZST fájl – Zstandard tömörített fájlformátum",
  "description":"Ismerje meg a ZST fájlformátumot és az API-kat, amelyekkel ZST fájlokat hozhat létre és nyithat meg.",
  "linktitle" : "ZST",
  "menu" : {
    "docs" : {
      "identifier":"compression-zst-hu",
      "parent" : "compression"
}
},
  "lastmod" : "2022-12-26"
}

## Mi az a ZST fájl?

A ZST-fájl egy tömörített fájl, amelyet a Zstandard (zstd) tömörítési algoritmussal állítanak elő. Ez egy tömörített fájl, amelyet veszteségmentes tömörítéssel hoz létre az algoritmus. A ZST fájlok különféle típusú fájlok, például adatbázisok, fájlrendszerek, hálózatok és játékok tömörítésére használhatók. A Zstandardot a [RFC 8878](https://www.rfc-editor.org/rfc/rfc8878) szabályozza, amely leírja az általános tömörítési mechanizmust, a médiatípust és a tartalomkódolást.

## ZST fájlformátum

A ZST fájlok tömörített fájlformátumban kerülnek a lemezre. A tömörítési mechanizmust az RFC 8878 írja le, amely elavult RFC 8478-at.

## ZST keretek

A ZST-fájl egy vagy több keretből áll. Mindegyik keret lehet Zstandard keret vagy átugorható keret. A Zstandard keret tömörített adatokat tartalmaz, míg az átugorható keret egyéni felhasználói metaadatokat tartalmaz.

### Zstandard keret

A Zstandard keret a következő szerkezettel rendelkezik.

|Mező|Méret bájtban|
---|---|
|Magic_Number |4 byte|
|Frame_Header |2-14 byte|
|Data_Block |n byte|
|[További adatblokkok] ||
|[Content_Checksum] |4 bájt|

### Átugorható keret

Az átugorható keret lehetővé teszi a felhasználó által meghatározott metaadatok beillesztését az összefűzött keretek folyamába. Az átugorható keret felépítése a következő.

|Mágikus_Szám |Keret_méret |Felhasználói_adatok|
---|---|---|
|4 bájt |4 bájt |n bájt|

## Hivatkozások ##

* [RFC 8878 Zstandard Compression](https://www.rfc-editor.org/rfc/rfc8878)


