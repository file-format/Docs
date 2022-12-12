{
  "date" : "2019-10-11",
  "keywords" :[ "obj fájl", "obj fájl formátum", "mi az obj fájl", "fájl", "obj példa", "obj fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OBJ fájl formátum",
  "description":"További információ az OBJ fájlformátumról és az API-król, amelyek megnyithatnak és létrehozhatnak OBJ fájlokat.",
  "linktitle" : "OBJ",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az OBJ fájl?

Az **OBJ** fájlokat a Wavefront Advanced Visualizer alkalmazása használja a geometriai objektumok meghatározására és tárolására. A geometriai adatok vissza- és előre továbbítása OBJ-fájlokon keresztül lehetséges. Az OBJ formátum támogatja mind a sokszögű geometriát, mint a pontok, vonalak, textúra csúcsok, lapok és a szabad formájú geometria (görbék és felületek). Ez a formátum nem támogatja az animációt vagy a fényre és a jelenetek helyzetére vonatkozó információkat.

Az OBJ fájl általában a CAD (Computer Aided Design) által generált 3D modellezési folyamat végterméke. A csúcsok tárolásának alapértelmezett sorrendje az óramutató járásával ellentétes, elkerülve az arcnormálok kifejezett deklarálását. Noha az OBJ-fájlok megjegyzéssorban deklarálják a léptékinformációkat, az OBJ-koordinátákhoz még nincsenek deklarálva mértékegységek.

## A 3D OBJ formátum története

A Wavefront Technologies OBJ fájlformátumot hozott létre Advanced Visualizer alkalmazásához geometriai objektumok és 3D adatok tárolására. A 2.11-es verzióját egy újonnan dokumentált 3-as verzió váltja fel. A fájlformátum nyitott, és más gyártók implementálták 3D grafikus alkalmazásaikhoz. A Wavefront Technologies ezt a fájlformátumot nyílt forráskódúnak és semlegesnek tartotta.

## OBJ fájl formátum

A 3D objektumokban a felületi geometria kódolása kihívást jelentő feladat, amelyet az OBJ fájlformátum nagyon jól teljesített. Ez a formátum meglehetősen sokoldalú, mivel számos lehetőséget kínál a felületi geometria kódolására. Az alábbiakban három engedélyezett formátumot mutatunk be, amelyeknek megvannak a maga előnyei és hiányosságai:

### Tesszeláció sokszögű felületekkel

Az OBJ fájlformátum lehetővé teszi a felhasználó számára, hogy egyszerű vagy összetett geometriai alakzatok segítségével tesszellázza a 3D modell felületét. Egy modell felületgeometriai kódolásához egy fájl tárolja az egyes sokszögek csúcsait és normálisait. Bár a tesszelláció növeli a modell durvaságát, mégis meg kell találni a megfelelő egyensúlyt a fájl mérete és a nyomtatási minőség között.

### Szabad formájú görbe

Az OBJ fájlformátum lehetővé teszi, hogy a felhasználó által definiált szabad formájú felületi görbék meghatározzák a modell felületi geometriáját. Mivel a szabad formájú görbék összetettebbek, mint a sokszögű lapok, mivel kevés matematikai paraméterrel az íves vonalak legjobban szabad formájú görbékkel határozhatók meg. Ezért a sokszögű tesszellációkhoz képest kevesebb adattal a szabad formájú görbék bármely 3D modell kiváló minőségű kódolását generálják a fájlméret növelése nélkül.

### Szabad formájú felületek

Az OBJ fájlformátum a felületi geometria csempézését is meghatározza szabad formájú felületfoltokkal. Ez a fajta szabad formájú felületfolt (NURBS) kiválóan alkalmas merev radiális méretekkel nem rendelkező felületekre, mint például teherautó karosszériája, helikopter szárnyai vagy hajótörzs. A szabad formájú felületek használata nagyon előnyös, mivel precízebb a fájlméretek kisebb tartása nagyobb pontosság mellett. Ezek a felületek elengedhetetlen részét képezik a repülőgépiparnak és az autóiparnak, ahol az alacsony pontosság megbocsáthatatlan.

A következő kulcsszavak adattípus szerint vannak elrendezve a felület geometriájának meghatározásához.


|Elemek|Szabad formájú görbe/felületi test nyilatkozatok|Szabad formájú görbe/felület attribútumok
---|---|---|
|p|Pont|parm|Paraméterértékek|deg|Fok
|l|Vonal|trim|Külső vágóhurok|bmat|Alapmátrix
|f|Arc|lyuk|Belső vágóhurok|lépcső|Lépésméret
|görbe|Görbe|scrv|Speciális görbe|cstype|Görbe vagy felülettípus
|görbe2|2D görbe|sp|Speciális pont|**Kapcsolatosság és felületek csoportosítása**
|surf|Surface|end|End utasítás|con|connect
|**Megjelenítési/megjelenítési attribútumok**|g|Csoportnév
|ferde|ferde interpoláció|shadow_obj|Shadow casting|s|Simító csoport
|lod|Részletezési szint|trace_obj|Ray tracing|mg|Csoport egyesítése
|d_interp|Interpoláció feloldása|ctech|Görbe közelítési technika|o|Objektumnév
|c_interp|Színinterpoláció|stech|Felületi közelítési technika|
|usemtl|Anyag neve|mtllib|Anyagtár|
|**Geometriai csúcsok**|
|v|Geometriai csúcsok|vn|Csúcsnormálok|
|vt|Textúra csúcsai|vp|Paramétertércsúcsok|

### Szín és textúra

Az OBJ fájl lehetővé teszi a szín- és textúrainformációk tárolását egy társított fájlformátumban, az úgynevezett Material Template Library (MTL). A többszínű geometriai modellek e két fájl együttes használatával jelennek meg. Az MTL fájlok ASCII alapúak, és megkönnyítik a számítógépes renderelést azáltal, hogy a Phong-reflexiós modell segítségével leírják a felület fényvisszaverő tulajdonságait. A szabványt számos szoftvergyártó vette át, akik kihasználják az anyagcserére vonatkozó előnyöket. Az MTL formátum kissé elavult, mivel nem támogatja a legújabb technológiákat, például a tükör- és parallaxis térképeket.

## Hivatkozások

* [Wavefront .obj fájl](https://en.wikipedia.org/wiki/Wavefront_.obj_file)

