{
  "date" : "2022-05-25",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"További információ az FMPSL fájlformátumról és az FMPSL-fájlok létrehozására és megnyitására alkalmas API-król.",
  "title" :"FMPSL fájlformátum – FileMaker Pro 12 pillanatkép hivatkozási fájl",
  "linktitle" : "FMPSL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2022-05-25"
}

## Mi az FMPSL fájl?

Az FMPSL-fájl a FileMaker Pro 12-vel létrehozott adatbázis pillanatkép-fájlja. Tárolja az adatbázisból a lekérdezett eredményeket egyéb információkkal, például a vizuális elrendezéssel és a látható információkkal együtt. Az FMPSL fájl felhasználható ezen adatok visszaállítására a FileMaker Pro adatbázis egy másik példányában. Ezt a fájlformátumot a FileMaker Pro v 12 elindításával vezették be. Ezt a verziót megelőzően a pillanatkép hivatkozásokat FPSL fájlformátumként vezették be a FileMaker Pro v 11-ben. Az FMPSL fájlok a FileMaker Pro Advanced szoftverrel nyithatók meg. A FileMaker Pro által támogatott egyéb fájlformátumok közé tartozik az [FP5](/hu/database/fp5/), az [FP7](/hu/database/fp7/) és az [FMP12](/hu/database/fmp12/).

## FMPSL fájlformátum

Az FMPSL-fájlok belső fájlformátumának részletei nem érhetők el nyilvánosan a fejlesztők számára.

### Hogyan lehet rekordokat menteni FMPSL fájlként?

A FileMaker Pro adatbázisból származó adatok pillanatfelvétel hivatkozásfájlként menthetők a következő lépésekkel.

1. Keresse meg azokat a rekordokat az adatbázisban, amelyeket pillanatfelvétel hivatkozásfájlként kell menteni.
1. Mentse el a fájlt a menü Send Record as Snapshot Link opciójával a fájlnév megadásával.
1. Használja a böngészés alatt álló rekordokat a teljes talált rekordkészlet mentéséhez.

Az előállított pillanatkép fájl a megadott néven a lemezre kerül.

## Hivatkozások

* [A FileMaker Pro fájlformátumok korábbi verzióinak konvertálása FMP12 fájlformátumra](https://fmhelp.filemaker.com/help/16/fmp/en/index.html#page/FMP_Help/converting-files.html)
* [Rekordok mentése pillanatfelvétel linkfájlként](https://fmhelp.filemaker.com/help/12/fmp/en/html/import_export.17.5.html)

