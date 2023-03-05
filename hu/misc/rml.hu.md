{
  "date" : "2022-01-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RML – Elixir jelentéssablon fájl",
  "description":"További információ az RML-fájlokról és az RML-fájlok létrehozására és megnyitására alkalmas API-król.",
  "linktitle" : "RML",
  "menu" : {
    "docs" : {
      "identifier":"misc-rml",
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-12"
}

## Mi az RML fájl?

Az RML-fájl egy jelentéssablonfájl az [Elixir Repertoire](https://elixirtech.com/repertoire-2/) jelentéskészítő motorral. A sablonfájl jelentések létrehozására szolgál az Elixir fájlrendszerhez csatlakoztatott adatforrással. Az adatok beolvasása és feltöltése az RML-sablonfájlban történik, és számos különböző fájlformátumba exportálhatók, például [PDF](/hu/pdf/), [RTF](/hu/word-processing/rtf/) és táblázatba [XLS](/hu/spreadsheet/xls/). Az Elixir Repertoár jelentéskészítő motor számos JDBC adatforráshoz csatlakoztatható.

## RML fájl formátum

Az RML fájlformátum belső fájlszerkezetének részletei nem érhetők el nyilvánosan. A fájlokat az Elixir Repertoár alkalmazás belsőleg állítja elő és menti, hogy jelentéseket hozzon létre a csatlakoztatott adatforrásokból feltöltött adatokkal. Az RML-sablonfájl tartalmazza az adatokból generálandó zárójelentés általános elrendezését és helyőrzőit.

## Hogyan készítsünk RML sablonfájlt?

Az RML sablon létrehozásához az Elixir Repertoárban a következő lépéseket kell követni.

1. Csatlakoztasson egy JDBC adatforrást a fájlrendszerhez.
1. Indítsa el a Jelentéssablon varázslót
1. A szoftver segítségével keresse meg az adatforrás .ds fájlt
1. Válassza a táblázatos jelentést exportálási lehetőségként
1. Válassza ki a jelentéssablonba felvenni kívánt mezőket
1. Végül a Befejezés gombra kattintva a First report.rml hozzáadódik a tárhoz, és megnyílik az Elrendezés lap megjelenítéséhez.

## Hivatkozások

* [Elixir repertoár](https://elixirtech.com/repertoire-2/)

