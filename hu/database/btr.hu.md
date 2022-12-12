{
  "date" : "2021-09-06",
  "keywords" :[ "btr", "extension", "file", "file format", "Database File Type", "Database File Format", "Btrieve Database" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"További információ a BTR fájlformátumról és az API-król, amelyek BTR fájlokat hozhatnak létre és nyithatnak meg.",
  "title" :"BTR - Btrieve adatbázisfájl",
  "linktitle" : "BTR",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-09-06"
}

## Mi az a BTR fájl?

A .btr kiterjesztésű fájl a [Btrieve](https://www.actian.com/) tranzakciós adatbázis-alkalmazás által létrehozott adatbázisfájl. A relációs adatbázis-kezelő rendszerekkel (RBMS) ellentétben a Btrieve az Indexed Sequential Access Method (ISAM) módszeren alapul, amely az adatok tárolásának egyik módja a gyors visszakeresés érdekében. A BTR fájl rekordok gyűjteményét tárolja, és a követelményeknek megfelelő jelentések készítésére szolgál. A BTR fájlok a Pervasive Btrieve Database Manager, a Pervasive PSQL Maintenance Utility és a Legend Software BTRIEVE Viewer segítségével nyithatók meg.

## BTR fájlszerkezet - További információ

A BTR-fájl szerkezetében lévő egyes bájtok belső adatstruktúrája és igazítása nem nyilvánosan elérhető. Azonban Btrieve
biztosítja a [Btrieve API-t] (https://docs.actian.com/psql/PSQLv13/index.html#page/btrieveapi%2Fbtrintro.htm), amely a BTR-fájlokból származó információk kiolvasására használható. A következő programozási nyelvekkel és fejlesztői környezetekkel kompatibilis.

* Embarcadero C/C++
* Embarcadero Delphi
* GNU C/C++
* Micro Focus COBOL
* Microsoft Visual Basic
* Microsoft Visual C++
* Watcom C/C++

Az adatok lekérése egy BTR-fájlból a hozzá tartozó DDF-fájltól függ. A DDF nélkül nem lesz könnyű lekérni az információkat egy ilyen fájlból.

## Hivatkozások

* [Btrieve – Wikipédia](https://en.wikipedia.org/wiki/Btrieve)
* [Bevezetés a Btreive API-kba](https://docs.actian.com/psql/PSQLv13/index.html#page/btrieveapi%2Fbtrintro.htm)

