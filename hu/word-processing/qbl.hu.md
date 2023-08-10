{
  "date" : "2021-07-28",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"QBL - QuickBooks License File",
  "description":"További információ a QBL fájlformátumról és az API-król, amelyek QBL fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "QBL",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2021-07-28"
}

## Mi az a QBL fájl?

A .qbl kiterjesztésű fájl egy QuickBooks licencfájl, amely a felhasználó által megvásárolt példány licencinformációit tartalmazza. Általában a helyi rendszerben tárolják "license.qbl" néven a QuickBooks telepítése után, és a felhasználó megadja a licencinformációkat a szoftverben, amikor a szoftvert első alkalommal futtatják. A QBL volt a QuickBooks licencinformációinak tárolására használt korábbi fájlformátum. Ezt most a QuickBooks `qbregisteration.dat' fájlja váltotta fel, és a felhasználó megerősítő e-mailjéből, a vásárolt DVD-ből vagy más vásárlási módból származó információkkal van feltöltve. A QBL fájlok bármely szövegszerkesztőben megnyithatók, például a Windows Notepad, az Apple TextEdit, a Notepad++, a Github Atom szerkesztő és még sok más programban.

## QBL fájlformátum - További információ

A QBL fájlok egyszerű szöveges fájlként jönnek létre és tárolódnak. Az ezekben a fájlokban lévő információk ember által olvashatók, és szerkeszthetők/frissíthetők, amikor ezeket a fájlokat szövegszerkesztőben megnyitják. A licencelési és felhasználói regisztrációs információk ezután átmásolhatók ebbe a fájlba a QuickBooks szoftver használatának megkezdéséhez. A QBL fájlokat általában a Program Files\Intuit\QuickBooks\INET könyvtárban tárolják a Windows operációs rendszeren.

A QBL fájl kétféle információt tartalmaz.

* `QuickBooks Version Information:` A QuickBooks telepített verziójára utal, és a következő formátumban van: xx.x
* `Licenckulcs:` 000-000 0000-0000-0000-000 000073adbf3f formátumú szöveg, ahol a 000-000 0000-0000-0000-000 helyére a felhasználó qbregisteration kulcsa kerül

## Hivatkozások

* [QuickBooks by Intuit](https://quickbooks.intuit.com/)
* [QuickBooks – A qbregistration.dat fájl létrehozása](https://quickbooks.intuit.com/learn-support/en-us/help-article/license-information/create-create-qbregistration-dat-file/L7S5BwSst_US_en_US)

