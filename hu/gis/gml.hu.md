{
  "date" : "2019-10-11",
  "keywords" :[ "gml fájl", "mi az a gml fájl", "fájl", "gml példa", "gml fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GML – Geography Markup Language File Format",
  "description":"További információ a GML-fájlformátumról és az API-król, amelyek GML-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "GML",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az a GML fájl?

A GML a Geography Markup Language rövidítése, amely az Open Geospatial Consortium (OGC) által kifejlesztett XML specifikációkon alapul. A formátumot földrajzi adatok tárolására használják a különböző fájlformátumok közötti csere érdekében. Modellező nyelvként szolgál a földrajzi rendszerek számára, valamint nyílt adatcsere-formátumként az internetes földrajzi tranzakciókhoz.

## GML fájlformátum ##

A legtöbb XML-alapú nyelvtanhoz hasonlóan a nyelvtannak két része van: a dokumentumot leíró séma és a tényleges adatokat tartalmazó példánydokumentum. A GML-dokumentum leírása GML-séma használatával történik. Ez lehetővé teszi a felhasználók és a fejlesztők számára, hogy olyan általános földrajzi adatkészleteket írjanak le, amelyek pontokat, vonalakat és sokszögeket tartalmaznak. Az alkalmazássémák használatával a felhasználók pontok, vonalak és sokszögek helyett utakra, autópályákra és hidakra hivatkozhatnak.

Érdemes megjegyezni, hogy a GML-t nem szabad térbeli adatok térképeken való megjelenítésére értelmezni. A GML-tartalom megjelenítése eltér attól a céltól, amelyre a GML-t létrehozták. Röviden, a GML abban hasonlít az XML-hez, hogy csak olyan térbeli tartalmak tárolására szolgál, amelyeket megjelenítési célú leképezési alkalmazások használhatnak.

### Tartalomképzés a GML-ben ###

A GML a térbeli adatokat a tulajdonságok és geometriák listáját tartalmazó szolgáltatások segítségével reprezentálja. A tulajdonságnak van neve, típusa és értékleírása. A geometriák alapvető geometriai építőelemekből állnak, mint például:

* pont
* vonalak
* görbék
* felületeket és
* sokszögek

A GML jövőbeli verziói a tervek szerint támogatni fogják a 3D geometriát, valamint a jellemzők közötti topológiai kapcsolatokat.

A GML kódolás már meglehetősen összetett funkciókat tesz lehetővé. Egy jellemző például más jellemzőkből is állhat. Egyetlen elem, mint például egy repülőtér, más jellemzőkből is állhat, például taxipályákból, kifutópályákból, akasztókból és légi terminálokból. Egy földrajzi jellemző geometriája sok geometriai elemből is összeállítható. A geometriailag összetett jellemzők így geometriatípusok keverékéből állhatnak, beleértve a pontokat, vonalláncokat és sokszögeket.

### Példák ###

A GML 1.0 és 2.0 a poligonokat, pontokat és vonallánc objektumokat a következők szerint kódolja:

```
<gml:Polygon>
         <gml:outerBoundaryIs>
                 <gml:LinearRing>
                         <gml:coordinates>0,0 100,0 100,100 0,100 0,0</gml:coordinates>
                 </gml:LinearRing>
        </gml:outerBoundaryIs>
     </gml:Polygon>
     <gml:Point>
        <gml:coordinates>100,200</gml:coordinates>
     </gml:Point>
     <gml:LineString>
        <gml:coordinates>100,200 150,300</gml:coordinates>
     </gml:LineString>
```

## Referenciák ##

* [GML-specifikációk](http://www.opengeospatial.org/standards/gml)
* [GML – a Wikipedia által](https://en.wikipedia.org/wiki/Geography_Markup_Language)

