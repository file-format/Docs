{
  "date" : "2019-12-12",
  "keywords" :[ "FBX", "fil", "tillägg", "format", "3D-filformat" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Din filformatguide för att veta vad en FBX-fil och API:er är som kan skapa och öppna dem.",
  "title" :"FBX - FilmBox 3D-filformat",
  "linktitle" : "FBX",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är en FBX fil?

FBX, FilmBox, är ett populärt 3D-filformat som ursprungligen utvecklades av Kaydara för MotionBuilder. Det förvärvades av Autodesk Inc 2006 och är nu ett av de viktigaste 3D-utbytesformaten som används av många 3D-verktyg. FBX är tillgängligt i både binärt och ASCII-filformat. Formatet skapades för att tillhandahålla interoperabilitet mellan applikationer för skapande av digitalt innehåll. Det finns många verktyg tillgängliga för konvertering från/till FBX-filformat.

## FBX-filformat - Mer information

FBX är ett proprietärt format och specifikationer om dess binära filformat är inte tillgängliga officiellt. En C++ FBX SDK tillhandahålls av Autodesk för läsning, skrivning och konvertering till/från FBX-fil. Ett Python-import- och exportskript för FBX är också tillgängligt i Blender-programvara som inte använder FBX SDK.

### Textbaserad filstruktur

Den textbaserade filstrukturen är en trädstrukturerad dokumenterad med tydligt namngivna identifierare. Den består av en kapslad lista med noder ordnade i hierarki där varje nod har:

* En NodeType-identifierare (klassnamn)
* En tupel av egenskaper associerade med den, tupelelementen är de vanliga primitiva datatyperna: ##float, integer, string## etc.
* En lista som innehåller noder i samma format (rekursivt).

Dessa kan representeras logiskt enligt följande:

```
NodeType: SomeProperty0a, SomeProperty0b, ... , {

 NestedNodeType1 : SomeProperty1a, ...
 NestedNodeType2 : SomeProperty2a, ... , {
 ... Sub-scope
 }

 ...
}
```

Vissa av standardnoderna definieras som implicit lista där varje objekt består av en kapslad lista. Varje applikation som har för avsikt att komma åt FBX-geometri måste analysera detta innehåll och göra en användbar mening med det. Ett exempel på textbaserad FBX-fil är enligt nedan:

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

## Binär filstruktur för FBX-filer

Som nämnts tidigare är FBX-filformatspecifikationer inte tillgängliga offentligt för FBX. Eftersom Blender Foundation implementerar FBX-filformatet utan att använda företagets tillhandahållna SDK, är några av detaljerna om binärt filformat [tillgängliga](https://code.blender.org/2013/08/fbx-binary-file-format-specification/) som en del av implementeringen.

Den binära filstrukturen följer följande ordning:

* Header
* Objekt Record
* Sidfot

### FBX Header

Filhuvudinformationen består av 27 byte.

* Byte 0 - 20: Kaydara FBX Binary \x00 (filmagi, med 2 mellanslag i slutet, sedan en NULL-terminator).
* Byte 21 - 22: [0x1A, 0x00]## (okänt men alla observerade filer visar dessa byte).
* Byte 23 - 26: osignerad int, versionsnumret. 7300 för version 7.3 till exempel.

### Objektpost ###

Rubriken följs av en objektpost som är en fullständig nodpost med tomt namn och tom egenskapslista. Den innehåller rekursivt hela filformationen.

### Sidfot ###

FBX Footer-sektionen ligger i slutet av filen vars innehåll är okänt.

## Record Format ##

Poster i en FBX-fil kategoriseras som:

* Nodposter
* Fastighetsregister

### Nodpostformat ###

Varje nodpostformat heter och har följande minneslayout.


|Storlek (Bytes)|Datumtyp|Namn
--- | ---|---|
|4|UInt32|EndOffset
|4|UInt32|NumProperties
|4|UInt32|PropertyListLen
|1|UInt8|NamnLen
|NamnLängd|char|Namn
|?|?|Egenskap[n], där n = 0:PropertyListLen
|Valfritt| |
|?|?|NestedList
|13|uint8[]|Null-Record

var:

* `EndOffset` är avståndet från början av filen till slutet av nodposten (dvs den första byten av det som kommer härnäst). Detta kan användas för att enkelt hoppa över okända eller ej nödvändiga poster.
* `NumProperties` är antalet egenskaper i värdetuplen som är associerad med noden. En kapslad lista som sista element räknas inte som egenskap.
* `PropertyListLen` är längden på egenskapslistan. Detta är storleken som krävs för att lagra ##NumProperties## egenskaper, vilket beror på egenskapernas datatyp.
* `NameLen` är längden på objektnamnet, i tecken. Det enda fallet där detta är 0 verkar vara listornas översta nivå.
* `Namn` är namnet på objektet. Det finns ingen nollterminering.
* 'Egenskap[n]' är den n:e egenskapen. För formatet, se avsnittet egenskap Postformat. Egenskaper skrivs sekventiellt och utan utfyllnad.
* `NestedList` är den kapslade listan, vars närvaro indikeras av en NULL-post i slutet.

Förekomsten av en kapslad listpost kan fastställas genom att kontrollera om det finns byte kvar tills EndOffset nås. Om så är fallet bör nästa objektpost läsas direkt efter den sista egenskapen. Objektposten följer sedan 13 nollbyte, som sedan kombineras med EndOffset. Syftet med eller kravet för NULL-posten är inte känt och kan peka på någon formatfunktion.

### Fastighetspostformat ###

En egenskapspost innehåller detaljer om egenskaper som är en del av Node. En egenskapspost har följande minneslayout:


|Storlek (Bytes)|Datatyp|Namn
--- | --- | ---
|1|char|Typkod
|?|?|Data

TypeCode representerar teckenkoder som är ordnade i grupper som kräver liknande hantering. Typkoder kan kategoriseras i följande typer och TypeCode kan vara en av teckenkoderna bland dessa typer.

#### Primitiva typer ####

```
Y: 2 byte signed Integer
C: 1 bit boolean (1: true, 0: false) encoded as the LSB of a 1 Byte value.
I: 4 byte signed Integer
F: 4 byte single-precision IEEE 754 number
D: 8 byte double-precision IEEE 754 number
L: 8 byte signed Integer
```

Data i den primitiva skalärtypsposten är exakt den binära representationen av värdet, i little-endian byteordning.

#### Arraytyper ####

```
f: Array of 4 byte single-precision IEEE 754 number
d: Array of 8 byte double-precision IEEE 754 number
l: Array of 8 byte signed Integer
i: Array of 4 byte signed Integer
b: Array of 1 byte Booleans (always 0 or 1)
```

Data för matristyp är mer komplex och har följande struktur.


|Storlek (Bytes)|Datatyp|Namn
--- | --- | ---
|4|Uint32|ArrayLength
|4|Uint32|Kodning
|4|Uint32|Komprimerad längd
|?|?|Innehåll

### Specialtyper ###

Följande är typkoderna för specialtyper.

```
S: String
R: raw binary data
```

Båda dessa typkoder representeras enligt följande:


|Storlek (Bytes)|Datatyp|Namn
--- | --- | ---
|4|Uin32|Längd
|Längd| |

Strängen är inte nollterminerad och kan mycket väl innehålla \0 tecken (detta används faktiskt i vissa FBX-egenskaper).

## Referenser ##

* [FBX - Autodesk SDK](https://help.autodesk.com/view/FBX/2017/ENU/)
* [FBX binära filformatspecifikationer](https://code.blender.org/2013/08/fbx-binary-file-format-specification/)
* [FBX - Wikipedia](https://en.wikipedia.org/wiki/FBX#File_format)

