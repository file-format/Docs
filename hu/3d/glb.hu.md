{
  "date" : "2019-12-03",
  "keywords" :[ "GLB", "fájl", "formátum", "fájl típusa", "kiterjesztés", "mi az a GLB fájl?" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GLB",
  "description":"További információ a GLB fájlformátumról és az API-król, amelyek megnyithatnak és létrehozhatnak GLB fájlokat.",
  "linktitle" : "GLB",
  "menu" : {
    "docs" : {
      "identifier":"3d-glb",
      "parent" : "3d"
}
},
  "lastmod" : "2020-09-01"
}

## Mi az a GLB fájl?

A GLB a GL átviteli formátumban ([glTF](/hu/3d/gltf/)) mentett 3D modellek bináris fájlformátumú reprezentációja. Információk a 3D modellekről, például csomóponti hierarchiáról, kamerákról, anyagokról, animációkról és hálókról bináris formátumban. Ez a bináris formátum a glTF-eszközt (JSON, .bin és képek) egy bináris blobban tárolja. Ezzel elkerülhető a fájlméret növekedésének problémája is, ami a glTF esetén fordul elő. A GLB fájlformátum kompakt fájlméreteket, gyors betöltést, teljes 3D-s jelenetábrázolást és bővíthetőséget eredményez a további fejlesztéshez. A formátum a model/gltf-binárist használja MIME-típusként.

## GLB fájlformátum – További információ

A glTF által használt tartalomszolgáltatási módszerek extra feldolgozást eredményeznek a base-64 kódolású bináris adatok dekódolásához, és 33%-kal növelik a fájlméretet. Ezek a kézbesítési módszerek, amelyek hozzájárultak a GLB fájlformátum kialakulásához, a következők:

* A glTF JSON külső bináris adatokra (geometria, kulcskeretek, felszínek) és képekre mutat.
* A glTF JSON base64 kódolású bináris adatokat és képeket ágyaz be, adat-URI-k használatával.

A GLB-t mint tárolóformátumot bináris fájlformátumként vezették be a glTF-eszköz bináris blob-ban való megjelenítéséhez, hogy elkerüljék a glTF által okozott problémákat. A GLB fájlformátum [specifikációja] (https://github.com/KhronosGroup/glTF/tree/master/specification/2.0#glb-file-format-specification) hivatkozni kell az alkalmazásfejlesztéshez használt olvasó/író megvalósítására. .

## GLB fájlszerkezet

A GLB fájlformátum a little endianon alapul, és szerkezete azt mutatja, hogy a következőket tartalmazza:

* Egy 12 bájtos preambulum, melynek címe a fejléc.
* Egy vagy több darab, amely JSON-tartalmat és bináris adatokat tartalmaz.

#### GLB fejléc

A GLB fájlformátum fejléce három 4 bájtos bejegyzésből áll:

* uint32 magic - magic egyenlő 0x46546C67. Ez egy glTF ASCII karakterlánc, és az adatok bináris glTF-ként történő azonosítására használható
* uint32 verzió – a bináris glTF tároló formátum verzióját jelzi
* uin32 hossz - a bináris glTF teljes hossza, beleértve a fejlécet és az összes darabot bájtban

#### Darabok

A GLB-fájlban minden egyes darab a következő szerkezettel rendelkezik:

|uint32|uint32|ubyte[]
---|---|---|
|chunkLength|chunkType|chunkData

* "chunkLength" - a chunkData hossza bájtokban
* `chunkType` – jelzi a darab típusát
* `chunkData` – a darab bináris hasznos terhelése

ahol a darab típusok vannak:

|# |Részlettípus|ASCII|Leírás|Előfordulások
---|---|---|---|---|
|1.|0x4E4F534A|JSON|Strukturált JSON-tartalom|1
|2.|0x004E4942|BIN|Bináris puffer|0 vagy 1

Az egyes darabok elejét és végét 4 bájtos határvonalhoz kell igazítani, és erre a célra kitöltést kell használni.

##### Strukturált JSON-tartalom

Ennek a bináris glTF-eszköz legelső darabjának kell lennie, és lehetővé teszi a megvalósítás számára, hogy fokozatosan lekérje az erőforrásokat a következő darabokból. Ez azt is lehetővé teszi, hogy egy bináris glTF-eszközből csak az erőforrások kiválasztott részhalmazát olvassa be, például egy háló legdurvább LOD-ját. Az igazítási követelmények teljesítése érdekében ezt a darabot ki kell tölteni a záró szóköz karakterekkel (0x20).

##### Bináris puffer #####

Ez a darab tartalmazza a geometria, az animációs kulcskockák, a felszínek és a képek bináris hasznos adatát. Ennek a bináris glTF-eszköz második darabjának kell lennie, és az igazítási követelmények teljesítése érdekében a végén nullákkal (0x00) kell kitölteni.

## Referenciák ##

* [GLB fájlformátum specifikációi – Khronos](/hu/3D/GLTF/)

