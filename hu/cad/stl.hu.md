{
  "date" : "2020-03-16",
  "keywords" :[ "STL fájl", "Formátum", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"További információ az STL fájlformátumról és az STL-fájlok létrehozására és megnyitására alkalmas API-król.",
  "title" :"STL fájlformátum",
  "linktitle" : "STL",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az STL fájl?

Az STL, a sztereolitrográfia rövidítése, egy felcserélhető fájlformátum, amely háromdimenziós felületi geometriát képvisel. A fájlformátumot számos területen használják, mint például a gyors prototípuskészítés, a 3D nyomtatás és a számítógéppel segített gyártás. A felületet kis háromszögek sorozataként ábrázolja, amelyeket lapoknak nevezünk, ahol minden oldalt egy merőleges irány és három pont ír le, amelyek a háromszög csúcsait képviselik. A kapott adatokat az alkalmazások arra használják, hogy meghatározzák a gyártó által megépítendő 3D alakzat keresztmetszetét. Az STL fájlformátumban nem áll rendelkezésre információ a színek, textúrák vagy más általános [CAD](/hu/cad/) modellattribútumok megjelenítéséhez.

## Rövid története ##

Az STL fájlformátum kifejlesztése 1987-ig nyúlik vissza. A 3D Systems fejlesztette ki kereskedelmi 3D nyomtatókban való használatra. 2009-ben javasolták az STL fájlformátum átdolgozott változatát, az STL 2.0-t, a fájlformátum frissítésével.

## Fájlformátum specifikációi ##

Az STL-fájl egy felületgeometriát ábrázol fazettákat használva. A lapok egy 3D-s objektum felületét határozzák meg, és egyedileg azonosítják őket egy normálegység, amely egy 1,0 hosszúságú háromszögre merőleges egyenes, valamint három csúcs. Összesen 12 szám van tárolva minden oldalhoz, mivel a Normál és minden csúcsot három-három koordináta határoz meg. Az StL fájl nem tartalmaz léptékinformációkat; a koordináták tetszőleges mértékegységben vannak megadva.

Az STL fájlformátum specifikációit a következő két szempontból lehet vizsgálni.

### Szempontok orientációja ###

A fazetta tájolását az egységnormál iránya és a csúcsok felsorolásának sorrendje határozza meg. A lapok tájolása kétféleképpen van megadva, az alábbiak szerint:

* A normál iránya kifelé mutat
* A csúcsok az óramutató járásával ellentétes sorrendben vannak felsorolva kívülről, a jobbkéz szabályának megfelelően.

### Csúcstól csúcsig szabály ###

E szabály szerint minden háromszögnek két csúcsa van a szomszédos háromszögeivel. Így az egyik háromszög csúcsa nem feküdhet egy másik háromszög oldalán.

## Fájlformátumok ##

Az STL ASCII-ben és bináris formában is elérhető a kompakt fájlformátumhoz.

### STL ASCII formátum ###

Az STL fájlformátum ASCII verziója sima ASCII-ben van írva. A nagy mérete miatt azonban a fájlformátumot nem választották előnyben részesített formátumként. Az ASCII STL fájl szintaxisa a következő:
```
solid name
     facet normal ni nj nk
         outer loop
             vertex v1x v1y v1z
             vertex v2x v2y v2z
             vertex v3x v3y v3z
         endloop
     endfacet
endsolid name
```
A félkövér szavak olyan kulcsszavakat jelölnek, amelyeknek mindig kisbetűsnek kell lenniük. A dőlt betűs szimbólumok olyan változók, amelyeket a felhasználó által megadott értékekkel kell helyettesíteni. A **facet normal** és **vertex** vonalak numerikus adatai egyszeri precíziós lebegtetések, például 1.23456E+789. A **szét normál** koordinátának lehet egy vezető mínusz jele; egy **csúcs** koordináta nem feltétlenül.

### STL bináris formátum ###

A bináris formátum az IEEE egész és lebegőpontos numerikus ábrázolását használja. A fájlformátum a következőképpen jelenik meg:

|Mező|Infó|
---|---|
|Fejléc|80 karakter|
|Háromszögek száma|4 bájtos kis endian előjel nélküli egész szám|
|Adatok minden háromszöghez|12 32 bites lebegőpontos szám|

A fájlformátum részletesebb nézete az alábbiak szerint látható.

```
UINT8[80] – Header
UINT32 – Number of triangles


foreach triangle
REAL32[3] – Normal vector
REAL32[3] – Vertex 1
REAL32[3] – Vertex 2
REAL32[3] – Vertex 3
UINT16 – Attribute byte count
end
```

## Hivatkozások ##

* [Az STL formátum](http://www.fabbers.com/tech/STL_Format)
* [STL – a Wikipedia által](https://en.wikipedia.org/wiki/STL_(file_format))

