{
  "date" : "2021-08-29",
  "keywords" :[ "ade", "extension", "file", "file format", "Database File Type", "Database File Format", "Microsoft Access" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"További információ az ADE fájlformátumról és az API-król, amelyek ADE fájlokat hozhatnak létre és nyithatnak meg.",
  "title" :"ADE - Access Project Extension File",
  "linktitle" : "ADE",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-08-29"
}

## Mi az ADE fájl?

Az .ade kiterjesztésű fájl egy Microsoft Access Project fájl, amely tartalmazza a Microsoft Access ADP projektfájlban található információk összeállított kimenetét. Az Access-projektfájlban található információk – a Visual Basic for Applications (VBA) kivételével – ADE-fájlokban összeállított formában állnak rendelkezésre. Ezekben a fájlokban az adatokat tömörített formátumban tárolják a fájlméret csökkentése és az Access teljesítményének javítása érdekében. Mivel az ADE az Access projektfájl lefordított kimenete, a projekt részét képező VBA-forráskódok védettek maradnak, mivel nem engedik, hogy a kimenet része legyen. Az ADE-fájlok a Microsoft Access 365-ben nyithatók meg.

## ADE fájlformátum - További információ

Az ADE lefordított Access Database fájlok, amelyek bináris fájlként kerülnek a lemezre. Ezeknek a fájloknak a belső fájlszerkezete nem ismert.

Az ADE-fájlok megnyitási problémákat okozhatnak a fájlok létrehozásához használt Microsoft Access verziója alapján. A Microsoft Access 2010 64 bites verzióját használó hozzáférési adatbázisokat, amelyek MDE-, [ACCDE](/hu/database/accde/) vagy ADE-fájlokként vannak lefordítva, újra kell fordítani a Microsoft Access 2021 Service Pack 1 (SP1) szolgáltatásban. megfelelően működik az Access 2010 SP1 szervizcsomaggal. Ez a probléma azért jelentkezik, mert az Access 2010 SP1 a VBE7.dll fájl újabb verzióját (7.00.1619-es verzió) használja.

## Hivatkozások

* [Probléma az Access ADE fájlokkal](https://docs.microsoft.com/en-us/office/troubleshoot/access/error-run-compiled-mde-accde-ade)
* [Melyik hozzáférési fájlformátumok használhatók](https://support.microsoft.com/en-us/office/which-access-file-format-should-i-use-012d9ab3-d14c-479e-b617-be66f9070b41)

