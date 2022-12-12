{
  "date" : "2019-12-12",
  "keywords" :[ "PLY", "file", "extension", "format", "3D file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"További információ a PLY fájlformátumról és az API-król, amelyek PLY fájlokat hozhatnak létre és nyithatnak meg.",
  "title" :"PLY - Polygon 3D File Format",
  "linktitle" : "PLY",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az a PLY fájl?

A PLY, a Polygon File Format egy 3D fájlformátum, amely sokszögek gyűjteményeként leírt grafikus objektumokat tárol. Ennek a fájlformátumnak az volt a célja, hogy egy egyszerű és egyszerű fájltípust hozzon létre, amely elég általános ahhoz, hogy a modellek széles skálájához használható legyen. A PLY fájlformátum ASCII és bináris formátumban is elérhető a kompakt tároláshoz, valamint a gyors mentéshez és betöltéshez. A fájlformátumot különböző alkalmazások használják, amelyek támogatják a 3D-s fájlok olvasását.

A PLY formátumú objektumokat csúcsok, lapok és egyéb elemek gyűjteménye írja le, valamint olyan tulajdonságok, mint a szín és a normál irány, amelyek ezekhez az elemekhez kapcsolhatók. Az objektummal együtt tárolható egyéb tulajdonságok is:

* Normál felület
* textúra koordináták
* átláthatóság
* tartomány adatok megbízhatósága
* tulajdonságok egy sokszög elejére és hátuljára

A PLY formátum által képviselt objektumok különféle forrásokból származhatnak, például kézzel digitalizált objektumok, modellező alkalmazásokból származó sokszög objektumok, tartományadatok, menetkockákból származó háromszögek, terepadatok és radiozitásmodellek.

## Rövid története

A PLY formátumot az 1990-es években fejlesztették ki Greg Turk és mások a stanfordi grafikus laborban, ezért Stanford Triangle Format néven is ismerték. A fájlformátum azóta 1.0-s verzióval rendelkezik, és nem történt további módosítás.

## PLY fájlformátum

Egy egyszerű PLY objektum elemek gyűjteményéből áll az objektum ábrázolására. Ez egy csúcsok (x,y,z) hármasainak listájából és azon lapok listájából áll, amelyek valójában indexek a csúcsok listájában. A csúcsok és a lapok két példa az elemekre, és a PLY fájl nagy része ebből a két elemből áll. Új tulajdonságok is létrehozhatók és az objektum elemeihez csatolhatók, de ezeket úgy kell hozzáadni, hogy a régi programok ne törjenek össze, amikor ezekkel az új tulajdonságokkal találkozunk. Az ilyen tulajdonságokat az alkalmazások olvasásával is el lehet vetni. Sőt, ezzel az elemmel új elemek is létrehozhatók, tulajdonságok definiálhatók.

### Fájlszerkezet

A PLY fájlformátum fájlszerkezete a következő:

|Mező
---|
|Fájlfejléc
|Csúcslista
|Arclista
|Egyéb elemek listája

#### Példastruktúra

Az alábbi példát a következő tárgyalásunkban a PLY fájlformátum különböző részeihez fogjuk használni.

```
ply
format ascii 1.0           { ascii/binary, format version number }
comment made by Greg Turk  { comments keyword specified, like all lines }
comment this file is a cube
element vertex 8           { define "vertex" element, 8 of them in file }
property float x           { vertex contains float "x" coordinate }
property float y           { y coordinate is also a vertex property }
property float z           { z coordinate, too }
element face 6             { there are 6 "face" elements in the file }
property list uchar int vertex_index { "vertex_indices" is a list of ints }
end_header                 { delimits the end of the header }
0 0 0                      { start of vertex list }
0 0 1
0 1 1
0 1 0
1 0 0
1 0 1
1 1 1
1 1 0
4 0 1 2 3                  { start of face list }
4 7 6 5 4
4 0 4 5 1
4 1 5 6 2
4 2 6 7 3
4 3 7 4 0
```

#### Fájlfejléc

A PLY fájlformátum fejléce ASCII szöveget tartalmaz mind az ASCII, mind a bináris formátumhoz. A fejlécszakasz elejét és végét a ply és end-header kulcsszavak azonosítják. A fejléc elején található a ply varázsszó, amelyet a PLY fájlformátum felismerésére használnak az olvasók. A következő sor a fájl verziószámát mutatja. A PLY fájlformátumú megjegyzések a megjegyzés kulcsszóval kezdődnek az egyes megjegyzéssorok elején.

#### Elem kulcsszó

Az elem kulcsszó ezután megmondja, hogy mi van a fájlban. Ezt követik az adott elemtípus tulajdonságai, ahol minden tulajdonságnak megvan a maga tulajdonságtípusa és sorrendje az alábbiak szerint:

```
element vertex 8           { define "vertex" element, 8 of them in file }
property float x           { vertex contains float "x" coordinate }
property float y           { y coordinate is also a vertex property }
property float z           { z coordinate, too }
```

Ebben a konkrét példában az adott csúcselemnek 3 float típusú tulajdonsága van a sorrendjükkel.

#### Adattípusok típusai

Egy tulajdonságnak kétféle adattípusa lehet.

"Skalár": A skaláris adattípusok az alábbiak:

|#Név|#Típus|#Bájtok száma
|karakter|karakter|1
|uchar|előjel nélküli karakter|1
|rövid|rövid egész|2
|ushort|előjel nélküli rövid egész szám|2
|int|Egész szám|4
|uint|előjel nélküli egész szám|4
|úszó|egyes pontosságú úszó|4
|dupla|dupla pontosságú úszó|8

`Lista`: A tulajdonságdefinícióknak van egy speciális formája, amely a lista adattípust használja. Példa erre a fenti kockafájlból:

`tulajdonságlista uchar int vertex_index`

Ez azt jelenti, hogy a "vertex_index" tulajdonság először egy előjel nélküli karaktert tartalmaz, amely megmondja, hogy a tulajdonság hány indexet tartalmaz, majd egy listát, amely ennyi egész számot tartalmaz. Ebben a változó hosszúságú listában minden egész szám egy csúcs indexe.

## Hivatkozások ##

* [PLY fájlformátum](http://paulbourke.net/dataformats/ply/)
* [PLY – a Wikipedia által](https://en.wikipedia.org/wiki/PLY_(file_format))

