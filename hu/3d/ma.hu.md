{
  "date" : "2019-10-11",
  "keywords" :[ "ma", "ma fájl", "ma fájlformátum", "fájlformátum", "3d", "ma fájl letöltése", ".ma fájl", ".ma"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"További információ az MA fájlformátumról és az API-król, amelyek MA-fájlokat nyithatnak meg és hozhatnak létre.",
  "title" :"MA fájlformátum",
  "linktitle" : "MA",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-06-04"
}

## Mi az a MA fájl?

A .ma kiterjesztésű fájl egy Autodesk Maya alkalmazással létrehozott 3D projektfájl. A szöveges parancsok nagy listáját tartalmazza a fájl információinak megadásához. A **.ma fájl** bármely szövegszerkesztőben megnyitható és szerkeszthető a parancsokkal kapcsolatos problémák megoldása érdekében, ha egy fájl megsérül. Ezek a fájlok tartalmazzák a 3D jelenet meghatározásához szükséges információkat, például geometriát, világítást, animációt és renderelést.

## MA Fájlformátum

Az MA fájlok ASCII szöveges formátumban kerülnek a lemezre, ellentétben a bináris fájlformátumban lemezre mentett MB fájlokkal. Az MA fájlformátumra vonatkozó részletes hivatkozás az [Autodesk Maya dokumentációjában] (https://download.autodesk.com/us/maya/2010help/index.html?url=Glossary_M_ma_file_format.htm,topicNumber=d0e192001) érhető el. fejlesztői tájékoztatásul.

### MA fájl fejléc

Az MA fájl fejléce megjegyzések részével kezdődik, amely megadja a fájl létrehozási adatait és a módosítás dátumát. A Maya fájlolvasók figyelmen kívül hagyják ezt a blokkot, mivel csak információs célokra használják. A fejlécnek azonban az első hat karakterrel "//Maya"-val kell kezdődnie.

Az ASCII fájl fejléce a következőképpen néz ki.

```
//Maya ASCII 1.0 scene
//Name: solstice.ma
//Last modified: Sun, Dec 21, 97 10:18:26 AM
```
### Fájlhivatkozások

A .ma fájl fájlhivatkozások szakasza információkat tartalmaz az összes többi Maya fájlról, amelyre ebben a fájlban hivatkoznak. Minden hivatkozott fájl egyetlen fájl paranccsal olvasható, amely ugyanabban a fájlban található. A fájlparancs szintaxisa hivatkozáskor a következő:

```
file -r -rpr prefixString fileName;
```
vagy

```
file -r -ns nameSpace fileName
```
Itt van egy példa karakterlánc.

```
file -r -rpr "solar" "/u/sally/work/solar.ma";
```
Ez a példa azt mutatja, hogy a `solar` fájlban található Sun objektum a "solar_sun" néven érhető el ebben a fájlban.

### Követelmények

A .ma fájl Követelmények szakasza egy sor kötelező parancsból áll, és a fájlok olvasásához szükséges May-információkat, például verzió- és bővítményinformációkat közöl. A követelmények szakasz példája a következő.

```
requires maya "2.0";
requires specialPlugIn "1.2";
```


A következő szakasz a követelményeket határozza meg. Ez a szükséges parancsok sorozatából áll. A fájl ezen része megmondja Mayának, hogy milyen szoftverre van szükség a fájl megfelelő betöltéséhez. Pontosabban, hogy a Maya melyik verziója, és milyen beépülő modulokkal.

## MA fájl letöltése
Kicsit nehéz megtalálni és letölteni egy 3d modell MA fájlját. Ezért letölthet egy MA-fájl mintát innen:

- [Sample.ma](../sample.ma)


## Hivatkozások

* [A Maya ASCII-fájlok szervezése – Autodesk](https://download.autodesk.com/us/maya/2010help/index.html?url=Glossary_M_ma_file_format.htm,topicNumber=d0e192001)

