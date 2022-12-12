{
  "date" : "2022-06-06",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TPSR fájlformátum - TeamViewer kísérleti munkamenet jelentésfájl",
  "description":"További információ a TPSR fájlformátumról és az API-król, amelyek létrehozhatnak és megnyithatnak TPSR fájlokat.",
  "linktitle" : "TPSR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-06"
}

## Mi az a TPSR fájl?

A TPSR a TeamViewer Assist AR (korábbi nevén TeamViewer Pilot) által használt kapcsolati protokollfájl. A TPSR-fájlban tárolt információk tömörített [ZIP](/hu/compression/zip/) fájlformátumban kerülnek tárolásra. A TPSR részletes előzményeket tartalmaz a TeamViewer kapcsolatáról a szakértő és a technikus között a probléma megoldásához és a felülvizsgálati célhoz. A TPSR-fájlban található információk közé tartozik az eszköz típusa, neve, Assist AR azonosítója, szakértői azonosítója, dátuma és időpontja, valamint a kapcsolat időtartama. Ezeket az adatokat a [JSON](/hu/web/json/) fájl tárolja a tömörített TPSR archívumban.

## TPSR fájlformátum

A TPSR-fájl ZIP-archívum-fájlformátumban kerül tárolásra a lemezen, ahol a tartalom egy JSON-fájlban van tárolva. Az Assist AR kapcsolat befejezése után automatikusan létrejön, feltéve, hogy a TeamViewerben engedélyezve van a Kapcsolati jelentés lehetőség.

A TeamViewer Assist AR segítségével a szakértők kapcsolódhatnak a technikusokhoz, hogy a mobil kamerán keresztül ÉLŐ adást kapjanak a távoli végről. Telefonon segíthetnek a technikusoknak a probléma megoldásában.

## Nyissa meg a TPSR fájlokat

A TPSR fájlokat a TeamViewer szoftver asztali verziójával nyithatja meg. Ha telepítve van a számítógépére, a TPSR fájl kétszeri kattintása megnyílik a TeamViewer szoftverben. A TPSR-fájlok exportálhatók [PDF](/hu/pdf/) fájlokba is, vagy kinyomtathatók a protokollfájl nyomtatott másolata céljából.

## Referenciák ##

* [TPSR](https://community.teamviewer.com/English/kb/articles/46456-using-teamviewer-assist-ar)

