{
  "date": "2019-12-12",
  "keywords": [
"FBX",
"fil",
"udvidelse",
"format",
"3D filformat"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Your file format guide to know what is an FBX file and APIs that can create and open them.",
  "title": "FBX - FilmBox 3D File Format",
  "linktitle": "FBX",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-fbx"
}
},
  "lastmod": "2019-09-10"
}

## Hvad er en FBX fil?

FBX, FilmBox, er et populært 3D-filformat, der oprindeligt blev udviklet af Kaydara til MotionBuilder. Det blev erhvervet af Autodesk Inc i 2006 og er nu et af de vigtigste 3D-udvekslingsformater, som bruges af mange 3D-værktøjer. FBX er tilgængelig i både binært og ASCII-filformat. Formatet blev etableret for at give interoperabilitet mellem applikationer til oprettelse af digitalt indhold. Der er mange værktøjer tilgængelige til konvertering fra/til FBX-filformat.

## FBX-filformat - flere oplysninger

FBX er et proprietært format, og specifikationer om dets binære filformat er ikke officielt tilgængelige. En C++ FBX SDK leveres af Autodesk til læsning, skrivning og konvertering til/fra FBX-fil. Et Python-import- og eksportscript til FBX er også tilgængeligt i Blender-software, der ikke bruger FBX SDK.

### Tekstbaseret filstruktur

The text-based file structure is a tree-structured documented with clearly named identifiers. It consists of a nested list of nodes arranged in hierarchy where each node has:

* En NodeType identifikator (klassenavn)

* En tuple af egenskaber forbundet med det, tuple-elementerne er de sædvanlige primitive datatyper: ##float, integer, string## osv.

* En liste, der indeholder noder i samme format (rekursivt).


Disse kan repræsenteres logisk som følger:

```
NodeType: SomeProperty0a, SomeProperty0b, ... , {

 NestedNodeType1 : SomeProperty1a, ...
 NestedNodeType2 : SomeProperty2a, ... , {
 ... Sub-scope
 }

 ...
}
```

Nogle af standardknuderne er defineret som implicit liste, hvor hvert element består af en indlejret liste. Enhver applikation, der har til hensigt at få adgang til FBX-geometri, skal analysere dette indhold og gøre brugbar mening med det. Et eksempel på tekstbaseret FBX-fil er som angivet nedenfor:

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

## Binær filstruktur af FBX-filer

Som nævnt tidligere er FBX-filformatspecifikationer ikke tilgængelige offentligt for FBX. Da Blender Foundation implementerer FBX-filformatet uden at bruge virksomhedens SDK, er nogle af detaljerne om binært filformat [available](https://code.blender.org/2013/08/fbx-binary-file-format-specification/) som en del af implementeringen.

Den binære filstruktur følger følgende rækkefølge:

* Header

* Objekt Record

* Sidefod


### FBX Header

Filhovedinformationen består af 27 bytes.

* Bytes 0 - 20: Kaydara FBX Binær \x00 (filmagi, med 2 mellemrum i slutningen, derefter en NULL-terminator).

* Byte 21 - 22: [0x1A, 0x00]## (ukendt, men alle observerede filer viser disse bytes).

* Bytes 23 - 26: usigneret int, versionsnummeret. 7300 for version 7.3 for eksempel.


### Objektpost ###

Headeren efterfølges af en objektpost, der er en fuld nodepost med tomt navn og tom egenskabsliste. Den indeholder rekursivt hele filformationen.

### Sidefod ###

FBX Footer sektionen ligger i slutningen af filen, hvis indhold er ukendt.

## Optageformater ##

Poster i en FBX-fil er kategoriseret som:

* Node Records

* Ejendomsregistre


### Node Record Format ###

Hvert Node Record Format er navngivet og har følgende hukommelseslayout.


|Størrelse (Bytes)|Datotype|Navn
--- | ---|---|
|4|UInt32|EndOffset
|4|UInt32|NumProperties
|4|UInt32|PropertyListLen
|1|UInt8|NavnLen
|NavnLængde|tegn|Navn
|?|?|Ejendom[n], hvor n = 0:PropertyListLen
|Valgfrit| |
|?|?|NestedList
|13|uint8[]|Nul-Record

hvor:

* 'EndOffset' er afstanden fra begyndelsen af filen til slutningen af nodeposten (dvs. den første byte af det næste). Dette kan bruges til nemt at springe over ukendte eller ikke nødvendige poster.

* 'NumProperties' er antallet af egenskaber i værdituplen, der er knyttet til noden. En indlejret liste som sidste element tælles ikke som egenskab.

* `PropertyListLen` er længden af ejendomslisten. Dette er den størrelse, der kræves for at gemme ##NumProperties## egenskaber, hvilket afhænger af egenskabernes datatype.

* `NameLen` er længden af objektnavnet i tegn. Det eneste tilfælde, hvor dette er 0, ser ud til at være listernes øverste niveau.

* `Navn` er navnet på objektet. Der er ingen nul-terminering.

* "Ejendom[n]" er den n'te egenskab. For formatet, se afsnittet egenskab Record Format. Egenskaber skrives sekventielt og uden udfyldning.

* `NestedList` er den indlejrede liste, hvis tilstedeværelse er angivet med en NULL-record til allersidst.


Eksistensen af en indlejret listepost kan bestemmes ved at kontrollere, om der er bytes tilbage, indtil EndOffset er nået. Hvis det er tilfældet, skal den næste objektpost læses direkte efter den sidste egenskab. Objektposten følger derefter 13 nul bytes, som derefter kombineres med EndOffset. Formålet med eller kravet til NULL-indtastningen er ikke kendt og kan pege på en eller anden formatfunktion.

### Ejendomspostformat ###

En ejendomspost indeholder detaljer om egenskaber, der er en del af Node. En ejendomspost har følgende hukommelseslayout:


|Størrelse (Bytes)|Datatype|Navn
--- | --- | ---
|1|char|TypeCode
|?|?|Data

TypeCode repræsenterer tegnkoder, som er ordnet i grupper, der kræver lignende håndtering. TypeCodes kan kategoriseres i følgende typer, og TypeCode kan være en af tegnkoderne blandt disse typer.

#### Primitive typer ####

```
Y: 2 byte signed Integer
C: 1 bit boolean (1: true, 0: false) encoded as the LSB of a 1 Byte value.
I: 4 byte signed Integer
F: 4 byte single-precision IEEE 754 number
D: 8 byte double-precision IEEE 754 number
L: 8 byte signed Integer
```

Data i den primitive skalartype-record er nøjagtig den binære repræsentation af værdien i little-endian byte-rækkefølge.

#### Arraytyper ####

```
f: Array of 4 byte single-precision IEEE 754 number
d: Array of 8 byte double-precision IEEE 754 number
l: Array of 8 byte signed Integer
i: Array of 4 byte signed Integer
b: Array of 1 byte Booleans (always 0 or 1)
```

Data for Array Type er mere kompleks og er i følgende struktur.


|Størrelse (Bytes)|Datatype|Navn
--- | --- | ---
|4|Uint32|ArrayLength
|4|Uint32|Kodning
|4|Uint32|Komprimeret længde
|?|?|Indhold

### Specielle typer ###

Følgende er de særlige typer typekoder.

```
S: String
R: raw binary data
```

Begge disse TypeCodes er repræsenteret som følger:


|Størrelse (Bytes)|Datatype|Navn
--- | --- | ---
|4|Uin32|Længde
|Længde| |

Strengen er ikke nultermineret og kan godt indeholde \0 tegn (dette bruges faktisk i nogle FBX-egenskaber).

## Referencer ##

* [FBX - Autodesk SDK](https://help.autodesk.com/view/FBX/2017/ENU/)

* [FBX binære filformatspecifikationer](https://code.blender.org/2013/08/fbx-binary-file-format-specification/)

* [FBX - Wikipedia](https://en.wikipedia.org/wiki/FBX#File_format)


