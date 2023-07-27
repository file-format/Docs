{
  "date" : "2019-12-12",
  "keywords" :[ "CBC", "extension", "file", "format", "Comic books", "Comic Books File Format", "eBook" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"További információ a CBC fájlformátumról és az API-król, amelyek CBC-fájlokat hozhatnak létre és nyithatnak meg.",
  "title" :"CBC - Képregénygyűjtemény fájlformátuma",
  "linktitle" : "CBC",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-03-03"
}

## Mi az a CBC fájl?

A .cbc kiterjesztésű fájl képregény-fájlok tömörített gyűjteménye e-könyvekhez, és [CBZ](/hu/ebook/cbz/) és [CBR](/hu/ebook/cbr/) fájlokat tartalmaz. A [Calibre](https://calibre-ebook.com/) e-könyv-konverziós alkalmazás használja, amely egy többplatformos nyílt forráskódú e-könyvkezelő, és lehetővé teszi az e-könyvek kezelését és azok különböző formátumokba való konvertálását. . A CBC-fájl egy .txt fájlt (comics.txt) tartalmaz, amely felsorolja az archívum részét képező egyéb fájlokat. Számos olyan alkalmazás érhető el online, amelyek CBC-fájlokat konvertálhatnak [AZW3](/hu/ebook/azw3/), [EPUB](/hu/ebook/epub/), [FB2](/hu/ebook/fb2/), [MOBI](/hu/ebook/) mobi/), [TXT](/hu/word-processing/txt/), [PDF](/hu/pdf/) és más népszerű fájlformátumok.

## CBC fájl formátum

A CBC fájlok tömörített archívumok, amelyek CBZ-t, CBR-t és egy szöveges fájlt tartalmaznak a tartalom felsorolásához. A comics.txt szövegfájl UTF8 kódolású, és tartalmazza azon CBC-fájlok listáját, amelyeket az olvasók használnak a gyűjteményük rendszerezéséhez. A CBC-fájlnak általában több olyan attribútuma van, amelyek lehetővé teszik a gyűjtemény szervezését, például képregény, kategória, kiadó, sorozat, kiadás és előadó.

A minta CBC-fájl tartalma a következő:

* comics.txt - Szöveges fájl, amely tartalmazza a CBR és CBZ fájlok listáját
* 1.cbz
* 2.cbz
* 3.cbz
* CBZ fájl(ok)

ahol a comics.txt fájl a következőképpen sorolja fel a tartalmat:

* 1.cbz: Első fejezet
* 2.cbz: Második fejezet
* 3.cbz: Harmadik fejezet

Az olvasók feldolgozzák a comics.txt fájlt, és a megadott adatok alapján elkészítik a tartalomjegyzéket.

## Hivatkozások

* [Calibre](https://calibre-ebook.com/)

