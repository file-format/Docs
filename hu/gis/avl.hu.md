{
  "date" : "2022-11-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "AVL – ArcView jelmagyarázat fájl",
  "description":"Ismerje meg az AVL fájlformátumot és az API-kat, amelyek AVL fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "AVL",
  "menu" : {
    "docs" : {
      "identifier":"gis-avl-hu",
      "parent" : "gis"
}
},
  "lastmod" : "2022-11-30"
}

## Mi az AVL fájl?

Az AVL fájl egy jelmagyarázat fájl, amely az ESRI ArcView GIS (Geographic Information System) szoftverrel generált térkép kulcsát tartalmazza. Tartalmazza a hozzáféréshez a megfelelő térképen használt hivatkozási szimbolikus információkat. Az AVL-fájl a típustól függően további információkat tartalmazhat, például szimbológiát, megjelenítési beállításokat, például átlátszóságot, léptéktől függő megjelenítési tulajdonságokat, egyesített táblára/kapcsolódó táblázatra vonatkozó információkat, definíciós lekérdezést, címkézési tulajdonságokat a jellemzőrétegekhez és megjegyzés megjelenítési tulajdonságait a kommentárrétegekhez. fajta réteg.

Egy AVL fájlra hivatkozhat az ArcView projekt [.APR](/gis/apr/) fájlja.

## AVL fájlformátum - További információ

Az AVL fájlok egyszerű szöveges fájlformátumban kerülnek mentésre. Ez azt jelenti, hogy az AVL fájlokat bármilyen szövegszerkesztőben megnyithatja, például a Notepad, Notepad++ és Apple TextEdit segítségével. Megnyitás után nem csak megtekintheti a fájl tartalmát, hanem módosíthatja is azokat.

### A .LYR és az .AVL fájlok közötti különbség

 * **Fájlformátum-különbség** - A .lyr egy bináris fájl, míg az .avl egy szövegfájl
 * **Tartalombeli különbség** – A .lyr fájl több információt tartalmaz, mint az .avl fájl. Az AVL-fájlok csak szimbolikus információkat tárolnak, míg a LYR-fájlok az ArcMap rétegtulajdonságok párbeszédpanelében elérhető összes információt.

## Hivatkozások

* [Különbség a .lyr és .avl fájlok között](https://support.esri.com/en/technical-article/000005936)


