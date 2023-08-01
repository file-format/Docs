{
  "date" : "2021-08-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ADF – ESRI ArcInfo bináris rácsformátum",
  "description":"További információ az ADF fájlformátumról és az API-król, amelyek ADF-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "ADF",
  "menu" : {
    "docs" : {
      "identifier": "gis-adf",
      "parent" : "gis"
}
},
  "lastmod" : "2021-08-26"
}

## Mi az ADF fájl?

Az .adf kiterjesztésű fájl egy raszteres adatfájlformátum, amelyet az ESRI szoftveralkalmazások, például az ArcGIS, az ArcView és az ArcInfo használnak. A térbeli adatokat az ESRI natív bináris rácsként tárolja. A rács cellák soraiból és oszlopaiból áll, amelyek lehetnek egész számok és lebegőpontosak is. Az ADF fájlban lévő egész rácsok diszkrét adatokat, a lebegőpontos rácsok pedig folyamatos adatokat jelentenek. Egy másik népszerű ESRI-fájlformátum az [SHP](/hu/gis/shp/) fájl, amely a térinformatikai információkat vektoradatok formájában jeleníti meg, amelyeket a földrajzi információs rendszerek (GIS) alkalmazásai használnak.

## ADF fájlformátum - További információ

Az ADF-fájlok bináris fájlként kerülnek mentésre a lemezre egy bináris rácsban. Az egész rácsoknak vannak attribútumai, amelyeket a rendszer egy értékattribútumtáblázatban (VAT) tárol. A rács minden egyedi értékéhez tartozik egy áfa-rekord, ahol a rekord tárolja az egyedi értéket, és a rács celláinak számát ez az érték képviseli.

A lebegőpontos rácsoknak nincs áfa.

### Rácsszerkezet

Az ADF-fájlon belül a rácsok csempézett raszteres adatszerkezettel vannak megvalósítva. A raszteres adatstruktúra alapegysége egy négyszögletes cellatömb. Minden blokk a lemezen van tárolva, és egy változó hosszúságú fájlszerkezetben, úgynevezett csempében tömörítve van. Minden blokk egy változó hosszúságú rekordként kerül tárolásra.

A GRID rasztereket munkaterületeken tárolják, ahol egy munkaterület minden GRID-hez egy információs alkönyvtárat és egy alkönyvtárat tartalmaz. Számos fájl létezik, amelyek földrajzi elhelyezkedést és attribútumadatokat rendelnek hozzá a megfelelő rácshoz. Az Info alkönyvtár több olyan fájlt tartalmaz, amelyek bizonyos információkat tárolnak a GRID-ről és más adatkészletekről, például a lefedettségekről a munkaterületen.

## Hivatkozások ##

* [ESRI Grid Format](https://desktop.arcgis.com/en/arcmap/latest/manage-data/raster-and-images/esri-grid-format.htm)
