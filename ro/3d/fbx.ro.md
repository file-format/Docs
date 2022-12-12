{
  "date" : "2019-12-12",
  "keywords" :[ "FBX", "fișier", "extensie", "format", "Format fișier 3D"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Ghidul dvs. de format de fișier pentru a ști ce este un fișier FBX și API-urile care le pot crea și deschide.",
  "title" :"FBX - Format de fișier FilmBox 3D",
  "linktitle" : "FBX",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este un fișier FBX?

FBX, FilmBox, este un format de fișier 3D popular care a fost dezvoltat inițial de Kaydara pentru MotionBuilder. A fost achiziționat de Autodesk Inc în 2006 și este acum unul dintre principalele formate de schimb 3D, așa cum sunt utilizate de multe instrumente 3D. FBX este disponibil în format de fișier binar și ASCII. Formatul a fost stabilit pentru a oferi interoperabilitate între aplicațiile de creare de conținut digital. Există multe instrumente disponibile pentru conversia din/în formatul de fișier FBX.

## Format de fișier FBX - Mai multe informații

FBX este un format proprietar, iar specificațiile despre formatul său de fișier binar nu sunt disponibile oficial. Un C++ FBX SDK este furnizat de Autodesk pentru citirea, scrierea și conversia în/din fișierul FBX. Un script Python de import și export pentru FBX este disponibil și în software-ul Blender care nu utilizează SDK-ul FBX.

### Structura fișierului bazată pe text

Structura de fișiere bazată pe text este un arbore structurat documentat cu identificatori denumiți clar. Constă dintr-o listă imbricată de noduri aranjate în ierarhie în care fiecare nod are:

* Un identificator NodeType (numele clasei)
* Un tuplu de proprietăți asociat cu acesta, elementele tuplu sunt tipurile de date primitive obișnuite: ##float, integer, șir## etc.
* O listă care conține noduri în același format (recursiv).

Acestea pot fi reprezentate logic după cum urmează:

```
NodeType: SomeProperty0a, SomeProperty0b, ... , {

 NestedNodeType1 : SomeProperty1a, ...
 NestedNodeType2 : SomeProperty2a, ... , {
 ... Sub-scope
 }

 ...
}
```

Unele dintre nodurile standard sunt definite ca liste implicite în care fiecare articol constă dintr-o listă imbricată. Orice aplicație, care intenționează să acceseze geometria FBX, trebuie să analizeze acest conținut și să-i dea un sens util. Un exemplu de fișier FBX bazat pe text este prezentat mai jos:

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

## Structura fișierelor binare a fișierelor FBX

După cum sa menționat mai devreme, specificațiile de format de fișier FBX nu sunt disponibile public pentru FBX. Deoarece Blender Foundation implementează formatul de fișier FBX fără a utiliza SDK-ul furnizat de companie, unele dintre detaliile despre formatul de fișier binar sunt [disponibile](https://code.blender.org/2013/08/fbx-binary-file-format -specificația/) ca parte a implementării acesteia.

Structura fișierelor binare urmează următoarea ordine:

* Antet
* Înregistrare obiect
* Subsol

### Antet FBX

Informațiile din antetul fișierului sunt compuse din 27 de octeți.

* Octeți 0 - 20: Kaydara FBX Binary \x00 (fișier-magic, cu 2 spații la sfârșit, apoi un terminator NULL).
* Octeți 21 - 22: [0x1A, 0x00]## (necunoscut, dar toate fișierele observate arată acești octeți).
* Octeții 23 - 26: unsigned int, numărul versiunii. 7300 pentru versiunea 7.3, de exemplu.

### Înregistrare obiect ###

Antetul este urmat de o înregistrare de obiect care este o înregistrare de nod completă cu nume goale și listă de proprietăți goală. Conține în mod recursiv întreaga formare a fișierului.

### Subsol ###

Secțiunea FBX Footer se află la sfârșitul fișierului al cărui conținut este necunoscut.

## Formate de înregistrare ##

Înregistrările dintr-un fișier FBX sunt clasificate astfel:

* Înregistrări de noduri
* Înregistrări de proprietate

### Format înregistrare nod ###

Fiecare format de înregistrare a nodului este numit și are următorul aspect de memorie.


|Dimensiune (octeți)|Tip de dată|Nume
--- | ---|---|
|4|UInt32|EndOffset
|4|UInt32|NumProperties
|4|UInt32|PropertyListLen
|1|UInt8|NameLen
|NameLength|char|Nume
|?|?|Proprietate[n], unde n = 0:PropertyListLen
|Opțional| |
|?|?|NestedList
|13|uint8[]|Null-Record

Unde:

* `EndOffset` este distanța de la începutul fișierului până la sfârșitul înregistrării nodului (adică primul octet din orice urmează). Acest lucru poate fi folosit pentru a sări cu ușurință peste înregistrările necunoscute sau care nu sunt necesare.
* `NumProperties` este numărul de proprietăți din tuplul valoric asociat cu nodul. O listă imbricată ca ultim element nu este socotită ca proprietate.
* `PropertyListLen` este lungimea listei de proprietăți. Aceasta este dimensiunea necesară pentru stocarea proprietăților ##NumProperties##, care depinde de tipul de date al proprietăților.
* `NameLen` este lungimea numelui obiectului, în caractere. Singurul caz în care acesta este 0 pare să fie listele de nivel superior.
* `Nume` este numele obiectului. Nu există terminație zero.
* `Proprietatea[n]` este a n-a proprietate. Pentru format, consultați secțiunea Proprietatea Format de înregistrare. Proprietățile sunt scrise secvențial și fără umplutură.
* `NestedList` este lista imbricată, a cărei prezență este indicată de o înregistrare NULL la sfârșit.

Existența unei intrări de listă imbricată poate fi determinată verificând dacă au mai rămas octeți până la atingerea EndOffset. Dacă da, următoarea înregistrare a obiectului ar trebui citită direct după ultima proprietate. Înregistrarea obiectului urmează apoi 13 zero octeți, care apoi se combină cu EndOffset. Scopul sau cerința intrării NULL nu este cunoscută și poate indica anumite caracteristici de format.

### Format de înregistrare a proprietății ###

O înregistrare de proprietate conține detalii despre proprietățile care fac parte din Node. O înregistrare de proprietate are următorul aspect de memorie:


|Dimensiune (octeți)|Tip de date|Nume
--- | --- | ---
|1|char|TypeCode
|?|?|Date

TypeCode reprezintă coduri de caractere care sunt ordonate în grupuri care necesită o manipulare similară. TypeCodes poate fi clasificat în următoarele tipuri, iar TypeCode poate fi unul dintre codurile de caractere dintre aceste tipuri.

#### Tipuri primitive ####

```
Y: 2 byte signed Integer
C: 1 bit boolean (1: true, 0: false) encoded as the LSB of a 1 Byte value.
I: 4 byte signed Integer
F: 4 byte single-precision IEEE 754 number
D: 8 byte double-precision IEEE 754 number
L: 8 byte signed Integer
```

Datele din înregistrarea de tip scalar primitiv sunt exact reprezentarea binară a valorii, în ordinea octeților mici-endian.

#### Tipuri de matrice ####

```
f: Array of 4 byte single-precision IEEE 754 number
d: Array of 8 byte double-precision IEEE 754 number
l: Array of 8 byte signed Integer
i: Array of 4 byte signed Integer
b: Array of 1 byte Booleans (always 0 or 1)
```

Datele pentru tipul de matrice sunt mai complexe și sunt în următoarea structură.


|Dimensiune (octeți)|Tip de date|Nume
--- | --- | ---
|4|Uint32|ArrayLength
|4|Uint32|Codificare
|4|Uint32|CompressedLength
|?|?|Cuprins

### Tipuri speciale ###

Următoarele sunt tipurile speciale de coduri de tip.

```
S: String
R: raw binary data
```

Ambele aceste coduri de tip sunt reprezentate după cum urmează:


|Dimensiune (octeți)|Tip de date|Nume
--- | --- | ---
|4|Uin32|Lungime
|Lungime| |

Șirul nu este terminat cu zero și poate conține \0 caractere (aceasta este de fapt folosită în unele proprietăți FBX).

## Referințe ##

* [FBX - Autodesk SDK](http://help.autodesk.com/view/FBX/2017/ENU/?guid#__files_GUID_105ED19A_9A5A_425E_BFD7_C1BBADA67AAB_htm)
* [Specificații de format de fișier binar FBX](https://code.blender.org/2013/08/fbx-binary-file-format-specification/)
* [FBX - Wikipedia](https://en.wikipedia.org/wiki/FBX#File_format)

