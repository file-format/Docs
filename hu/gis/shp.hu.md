{
  "date" : "2019-10-11",
  "keywords" :[ "shp fájl", "shp fájlformátum", "mi az shp fájl", "fájl", "shp példa", "shp fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SHP - ESRI Shapefile",
  "description":"További információ az SHP fájlformátumról és az SHP-fájlok létrehozására és megnyitására alkalmas API-król.",
  "linktitle" : "SHP",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az SHP fájl?

Az SHP az ESRI Shapefile ábrázolására használt egyik elsődleges fájltípus fájlkiterjesztése. A térinformatikai információkat vektoradatok formájában képviseli, amelyeket a földrajzi információs rendszerek (GIS) alkalmazásai használnak. A formátumot nyílt specifikációként fejlesztették ki, hogy megkönnyítsék az ESRI és más szoftvertermékek közötti együttműködést.

## Adatábrázolás

Amint már említettük, a shapefile formátum vektoros jellemzőkként írja le az adatkészlet térinformációit. Ezek a vektor jellemzők a következők:

* pont
* sorok
* sokszögek

Ezek a jellemzők kombinálva szinte bármilyen típusú alakzatot képviselhetnek, például vízkutak, országhatárok, térbeli pontok, folyók áramlása, tavak stb. Minden vektoros jellemzőnek lehetnek olyan attribútumai, amelyek ténylegesen meghatározzák az adott elem célját. Például egy Los Angeles-i városokat tartalmazó alakfájl rendelkezhet városnévvel és hőmérséklettel attribútumként, amely értelmes ábrázolást ad a térbeli adatoknak.

## Kapcsolódó fájlok

Az önálló shp-fájlt szoftveralkalmazások nem használhatják a benne lévő adatok értelmezésére. Az ilyen fájlokban található információk megértése érdekében a shapefile a következő további kötelező fájlokat használja fel.

* shx fájl - indexfájl
* dbf fájl – egy dBASE fájl, amely a fő fájlban lévő alakzatok összes attribútumait tárolja
* prj fájl – a fájl projektinformációit tárolja

Más opcionális fájlok is lehetnek, amelyek ugyanazt a nevet viselik, mint a fő fájl.

## Az SHP fájlformátum specifikációi

A shapefile nyílt specifikációi online elérhetők az ESRI-től [Technical Description](https://www.esri.com/content/dam/esrisites/sitecore-archive/Files/Pdfs/library/whitepapers/pdfs/shapefile.pdf) formájában, és részletesen kidolgozzák a fájl általános szerkezetét. A fő .shp fájl információi fejlécekből és rekordokból állnak. A rögzített hosszúságú fájlfejlécet változó hosszúságú rekordok követik, ahol minden rekord egy rögzített hosszúságú rekord fejlécből áll, amelyet változó hosszúságú rekordtartalom követ.

### Fő SHP-fájl fejléc

A fő fájlfejléc a fájl elejétől kezdődik, és 100 bájt hosszúságú. A fő fájl fejlécének felépítése a bájtpozícióval, értékkel, típussal és bájtok sorrendjével együtt a következő táblázatban látható.


|Bájtok|Mező|Érték|Típus|Bájtsorrend
---|---|---|---|---|
|0-3|Fájlkód|9994|Integer|Big Endian
|4-23|Unused|0|Integer|Big Endian
|24-27|Fájl hossza|Fájl hossza|Egész szám|Big Endian
|28-31|Verzió|1000|Integer|Little Endian
|32-35|Alaktípus|Alaktípus|Egész szám|Little Endian
|36-67|Minimális határoló téglalap|Xmin, Ymin, Xmax és Ymax|dupla|Little Endian
|68-83|Határdoboz|Zmin, Zmax|dupla|Little Endian
|84-99|Határdoboz|Mmin, Mmax|dupla|

Megjegyzendő, hogy a fájl hosszának értéke a fájl teljes hossza 16 bites szavakban, amely magában foglalja a fejlécet alkotó ötven 16 bites szót is.

#### Alaktípusok

Az alaktípusok mező értékei a fenti táblázatban a következők:


|Érték|Alaktípus
---|---|
|0|Null Shape
|1|Pont
|3|Vonallánc
|5|Sokszög
|8|Többpontos
|11|PontZ
|13|PolyLineZ
|15|SokszögZ
|18|MultiPointZ
|21|PontM
|23|PolyLineM
|25|SokszögM
|28|MultiPointM
|31|MultiPatch

### Adatrekordok ###

A fő fájl fejlécet változó hosszúságú rekordok követik, ahol minden rekord egy rögzített hosszúságú rekordfejlécből áll, amelyet változó hosszúságú rekordtartalom követ.

#### Rekordfejléc ####

A rekord fejléce a rekord számáról és a rekord tartalmi hosszáról tartalmaz információkat, rögzített 8 bájt hosszúságban. A rekord fejlécének felépítése a következő:


|Bájtok|Mező|Érték|Típus|Bájtsorrend
---|---|---|---|---|
|0-3|Rekordszám|Rekordszám|Egész szám|Nagy
|4-7|Rekord hossza|Rekord hossza|Egész szám|Nagy

#### Tartalom felvétele ####

A shapefile rekord tartalma egy alakzattípusból, majd az adott alakzat geometriai adataiból áll. A 0-s alakzat olyan nullalakzatot jelöl, amely nem rendelkezik geometriai adatokkal az alakzathoz. A rekord tartalmának hossza tükrözi az alakzatrészeket és csúcsokat. Vegyünk egy példát a Point Shape típusra annak kidolgozásához, hogy egy rekord hogyan tartalmaz információt egy ilyen alakzattípusról.

Egy pont egy adott földrajzi helyet jelent X,Y sorrendben, ahol minden koordinátát dupla pontosságú érték képvisel. A következő táblázat egy pontforma típus elrendezését mutatja be.


|Bájtok|Alakzattípus|Érték|Típus|Szám|Bájtsorrend
---|---|---|---|---|---|
|0-3|Alaktípus|1|Egész szám|1|Kicsi
|4-11|X|X|dupla|1|Kevés
|12-19|I|I|dupla|1|Kevés

Más alaktípusokra példákat találhat az ESRI műszaki leírásában.

## Hivatkozások ##

* [ESRI Shapefile műszaki leírás](https://www.esri.com/content/dam/esrisites/sitecore-archive/Files/Pdfs/library/whitepapers/pdfs/shapefile.pdf) az ESRI által

