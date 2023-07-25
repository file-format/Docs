{
  "date" : "2019-12-12",
  "keywords" :[ "FBX", "fájl", "kiterjesztés", "formátum", "3D fájlformátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"A fájlformátum útmutatója, hogy megtudja, mi az FBX fájl és API-k, amelyek létrehozhatják és megnyithatják azokat.",
  "title" :"FBX - FilmBox 3D fájlformátum",
  "linktitle" : "FBX",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az FBX fájl?

Az FBX, a FilmBox egy népszerű 3D-s fájlformátum, amelyet eredetileg a Kaydara fejlesztett ki a MotionBuilder számára. Az Autodesk Inc 2006-ban vásárolta meg, és jelenleg az egyik fő 3D-s csereformátum, amelyet számos 3D-eszköz használ. Az FBX bináris és ASCII fájlformátumban is elérhető. A formátumot azért hozták létre, hogy interoperabilitást biztosítson a digitális tartalomkészítő alkalmazások között. Számos eszköz áll rendelkezésre az FBX fájlformátumból/FBX fájlformátumba való konvertáláshoz.

## FBX fájlformátum - További információ

Az FBX egy szabadalmaztatott formátum, és a bináris fájlformátumra vonatkozó specifikációk hivatalosan nem érhetők el. Az Autodesk egy C++ FBX SDK-t biztosít az olvasáshoz, íráshoz és FBX-fájlba való konvertáláshoz. Az FBX-hez készült Python-importálási és -exportálási szkript a Blender szoftverben is elérhető, amely nem használja az FBX SDK-t.

### Szöveg alapú fájlstruktúra

A szöveg alapú fájlstruktúra egy fa szerkezetű, egyértelműen megnevezett azonosítókkal dokumentált. A csomópontok beágyazott listájából áll, amelyek hierarchiában vannak elrendezve, ahol minden csomópont rendelkezik:

* Egy NodeType azonosító (osztálynév)
* A hozzá tartozó tulajdonságok sora, a sorelemek a szokásos primitív adattípusok: ##float, integer, string## stb.
* Egy lista, amely azonos formátumú (rekurzív) csomópontokat tartalmaz.

Ezeket logikusan a következőképpen ábrázolhatjuk:

```
NodeType: SomeProperty0a, SomeProperty0b, ... , {

 NestedNodeType1 : SomeProperty1a, ...
 NestedNodeType2 : SomeProperty2a, ... , {
 ... Sub-scope
 }

 ...
}
```

Néhány szabványos csomópont implicit listaként van definiálva, ahol minden elem egy beágyazott listából áll. Minden alkalmazásnak, amely hozzá kíván férni az FBX geometriához, elemeznie kell ezeket a tartalmakat, és hasznos jelentést kell adnia. Az alábbiakban látható egy példa a szöveges FBX-fájlra:

```
; FBX ...
; Copyright (C) 1997-2008 ...
; All rights reserved.
; ----------------------------------------------------
FBXHeaderExtension: {
    FBXHeaderVersion: 1003
    FBXVersion: 6000
    CurrentCameraResolution: {
        CameraName: "Model::Producer Perspective"
        CameraResolutionMode: "Window Size"
        CameraResolutionW: 1
        CameraResolutionH: 1
}
    CreationTimeStamp: {
    ...
}
}
;Object definitions
;------------------------------------------------------------------
Definitions: {
    Count: 2
    ObjectType: "Model" {
    Count: 2
}
}
...
```

## FBX fájlok bináris fájlstruktúrája

Amint azt korábban említettük, az FBX fájlformátum specifikációi nem érhetők el nyilvánosan az FBX számára. Mivel a Blender Foundation az FBX fájlformátumot a vállalat által biztosított SDK használata nélkül valósítja meg, a bináris fájlformátumról néhány részlet [elérhető](https://code.blender.org/2013/08/fbx-binary-file-format -specifikáció/) megvalósításának részeként.

A bináris fájlok szerkezete a következő sorrendet követi:

* Fejléc
* Objektum rekord
* Lábléc

### FBX fejléc

A fájlfejléc információ 27 bájtból áll.

* 0-20 bájtok: Kaydara FBX Binary \x00 (fájlvarázslat, 2 szóközzel a végén, majd NULL lezáró).
* 21–22 bájtok: [0x1A, 0x00]## (ismeretlen, de minden megfigyelt fájl ezeket a bájtokat mutatja).
* 23-26 bájt: unsigned int, a verziószám. 7300 például a 7.3-as verzióhoz.

### Tárgyrekord ###

A fejlécet egy objektumrekord követi, amely egy teljes csomópontrekord üres névvel és üres tulajdonságlistával. Rekurzívan tartalmazza a teljes fájlképzést.

### Lábléc ###

Az FBX Footer szakasz olyan fájl végén található, amelynek tartalma ismeretlen.

## Felvételi formátumok ##

Az FBX-fájlban lévő rekordok a következő kategóriákba sorolhatók:

* Node Records
* Property Records

### Node Record Format ###

Minden csomóponti rekordformátum el van nevezve, és a következő memóriaelrendezéssel rendelkezik.


|Méret (Bájt)|Dátum típusa|Név
--- | ---|---|
|4|UInt32|EndOffset
|4|UInt32|NumProperties
|4|UInt32|PropertyListLen
|1|UInt8|NévLen
|NameLength|char|Név
|?|?|Tulajdonság[n], ahol n = 0:PropertyListLen
|Opcionális| |
|?|?|NestedList
|13|uint8[]|Null-Rekord

ahol:

* Az `EndOffset` a fájl eleje és a csomópontrekord vége közötti távolság (azaz a következő lépés első bájtja). Ezzel könnyen átugorhat az ismeretlen vagy nem kötelező rekordok között.
* A `NumProperties` a csomóponthoz társított értéksor tulajdonságainak száma. A beágyazott lista utolsó elemként nem számít tulajdonságnak.
* A `PropertyListLen` a tulajdonságlista hossza. Ez a ##NumProperties## tulajdonságok tárolásához szükséges méret, amely a tulajdonságok adattípusától függ.
* A `NameLen` az objektum nevének hossza karakterekben. Úgy tűnik, az egyetlen eset, amikor ez 0, a legfelső szintű listák.
* A "Név" az objektum neve. Nincs nulla leállás.
* A `Tulajdon[n]` az n-edik tulajdonság. A formátumot lásd a Rekordformátum tulajdonsága szakaszban. A tulajdonságok szekvenciálisan íródnak, kitöltés nélkül.
* A "NestedList" egy beágyazott lista, amelynek jelenlétét egy NULL-rekord jelzi a legvégén.

Egy beágyazott listabejegyzés megléte úgy határozható meg, hogy ellenőrizzük, hogy van-e még bájt az EndOffset eléréséig. Ha igen, akkor a következő objektumrekordot közvetlenül az utolsó tulajdonság után kell beolvasni. Az objektumrekord ezután 13 nulla bájtot követ, amelyek azután kombinálódnak az EndOffset-tel. A NULL bejegyzés célja vagy követelménye nem ismert, és bizonyos formátum jellemzőkre utalhat.

### Tulajdon nyilvántartási formátum ###

A tulajdonságrekord részleteket tartalmaz a csomópont részét képező tulajdonságokról. A tulajdonságrekord a következő memóriaelrendezéssel rendelkezik:


|Méret (Bájt)|Adattípus|Név
--- | --- | ---
|1|karakter|Típuskód
|?|?|Adatok

A TypeCode olyan karakterkódokat jelent, amelyek csoportokba vannak rendezve, amelyek hasonló kezelést igényelnek. A TypeCode a következő típusokba sorolható, és a TypeCode lehet az egyik karakterkód ezen típusok között.

#### Primitív típusok ####

```
Y: 2 byte signed Integer
C: 1 bit boolean (1: true, 0: false) encoded as the LSB of a 1 Byte value.
I: 4 byte signed Integer
F: 4 byte single-precision IEEE 754 number
D: 8 byte double-precision IEEE 754 number
L: 8 byte signed Integer
```

A primitív skalár típusú rekordban lévő adatok pontosan az érték bináris reprezentációi, kis-végi bájt sorrendben.

#### Tömbtípusok ####

```
f: Array of 4 byte single-precision IEEE 754 number
d: Array of 8 byte double-precision IEEE 754 number
l: Array of 8 byte signed Integer
i: Array of 4 byte signed Integer
b: Array of 1 byte Booleans (always 0 or 1)
```

A tömbtípus adatai összetettebbek, és a következő szerkezetben találhatók.


|Méret (Bájt)|Adattípus|Név
--- | --- | ---
|4|Uint32|ArrayLength
|4|Uint32|Kódolás
|4|Uint32|CompressedLength
|?|?|Tartalom

### Különleges típusok ###

Az alábbiakban a speciális típuskódok találhatók.

```
S: String
R: raw binary data
```

Mindkét típuskód a következőképpen jelenik meg:


|Méret (Bájt)|Adattípus|Név
--- | --- | ---
|4|Uin32|Hossz
|Hosszú| |

A karakterlánc nem nulla végű, és \0 karaktert is tartalmazhat (ezt bizonyos FBX tulajdonságok használják).

## Hivatkozások ##

* [FBX – Az Autodesk SDK](https://help.autodesk.com/view/FBX/2017/ENU/)
* [FBX bináris fájlformátum specifikációi](https://code.blender.org/2013/08/fbx-binary-file-format-specification/)
* [FBX – Wikipédia](https://en.wikipedia.org/wiki/FBX#File_format)

