{
  "date": "2019-12-12",
  "keywords": [
"FBX",
"failu",
"pagarinājumu",
"formātā",
"3D faila formāts"
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

## Kas ir FBX fails?

FBX, FilmBox, ir populārs 3D failu formāts, ko sākotnēji izstrādāja Kaydara darbam ar MotionBuilder. Autodesk Inc to iegādājās 2006. gadā, un tagad tas ir viens no galvenajiem 3D apmaiņas formātiem, ko izmanto daudzi 3D rīki. FBX ir pieejams gan binārā, gan ASCII faila formātā. Formāts tika izveidots, lai nodrošinātu sadarbspēju starp digitālā satura veidošanas lietojumprogrammām. Ir pieejami daudzi rīki konvertēšanai no/uz FBX faila formātu.

## FBX faila formāts — vairāk informācijas

FBX ir patentēts formāts, un tā binārā faila formāta specifikācijas nav oficiāli pieejamas. Autodesk nodrošina C++ FBX SDK lasīšanai, rakstīšanai un konvertēšanai uz/no FBX faila. Python importēšanas un eksportēšanas skripts FBX ir pieejams arī Blender programmatūrā, kas neizmanto FBX SDK.

### Teksta faila struktūra

The text-based file structure is a tree-structured documented with clearly named identifiers. It consists of a nested list of nodes arranged in hierarchy where each node has:

* NodeType identifikators (klases nosaukums)

* Ar to saistīts rekvizītu virkne, kortedža elementi ir parastie primitīvie datu tipi: ##float, integer, string## utt.

* Saraksts, kurā ir mezgli tādā pašā formātā (rekursīvi).


Tos var loģiski attēlot šādi:

```
NodeType: SomeProperty0a, SomeProperty0b, ... , {

 NestedNodeType1 : SomeProperty1a, ...
 NestedNodeType2 : SomeProperty2a, ... , {
 ... Sub-scope
 }

 ...
}
```

Daži standarta mezgli ir definēti kā netiešs saraksts, kurā katrs vienums sastāv no ligzdota saraksta. Jebkurai lietojumprogrammai, kas vēlas piekļūt FBX ģeometrijai, šis saturs ir jāparsē un jāizveido tā lietderīga nozīme. Teksta FBX faila piemērs ir šāds:

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

## FBX failu bināro failu struktūra

Kā minēts iepriekš, FBX faila formāta specifikācijas nav publiski pieejamas FBX. Tā kā Blender Foundation ievieš FBX faila formātu, neizmantojot uzņēmuma nodrošināto SDK, daži dati par bināro faila formātu ir [available](https://code.blender.org/2013/08/fbx-binary-file-format-specification/) kā daļa no tā ieviešanas.

Bināro failu struktūra ir šāda:

* Virsraksts

* Objekta ieraksts

* Kājene


### FBX galvene

Faila galvenes informācija sastāv no 27 baitiem.

* 0–20 baiti: Kaydara FBX Binary \x00 (failu maģija, ar 2 atstarpēm beigās, pēc tam NULL terminators).

* 21.–22. baiti: [0x1A, 0x00]## (nezināms, bet visos novērotajos failos tiek rādīti šie baiti).

* 23.–26. baiti: neparakstīts int, versijas numurs. 7300, piemēram, versijai 7.3.


### Objekta ieraksts ###

Pēc galvenes seko objekta ieraksts, kas ir pilns mezgla ieraksts ar tukšu nosaukumu un tukšu rekvizītu sarakstu. Tas rekursīvi satur visu faila veidošanu.

### Kājene ###

FBX kājenes sadaļa atrodas faila beigās, kura saturs nav zināms.

## Ierakstu formāti ##

Ieraksti FBX failā tiek klasificēti kā:

* Mezglu ieraksti

* Īpašuma ieraksti


### Mezgla ieraksta formāts ###

Katrs mezgla ieraksta formāts ir nosaukts, un tam ir šāds atmiņas izkārtojums.


|Izmērs (baiti)|Datuma tips|Nosaukums
--- | ---|---|
|4|UInt32|EndOffset
|4|UInt32|NumProperties
|4|UInt32|PropertyListLen
|1|UInt8|VārdsLen
|NameLength|char|Vārds
|?|?|Īpašums[n], kur n = 0:PropertyListLen
|Izvēles| |
|?|?|NestedList
|13|uint8[]|Null-Record

kur:

* `EndOffset` ir attālums no faila sākuma līdz mezgla ieraksta beigām (ti, pirmais baits no tā, kas nāk pēc tam). To var izmantot, lai viegli izlaistu nezināmus vai nevajadzīgus ierakstus.

* "NumProperties" ir rekvizītu skaits vērtību virknē, kas saistīts ar mezglu. Ligzdots saraksts kā pēdējais elements netiek uzskatīts par īpašumu.

* `PropertyListLen` ir īpašumu saraksta garums. Šis ir ##NumProperties## rekvizītu glabāšanai nepieciešamais lielums, kas ir atkarīgs no rekvizītu datu veida.

* `NameLen` ir objekta nosaukuma garums rakstzīmēs. Šķiet, ka vienīgais gadījums, kad tas ir 0, ir saraksti augšējā līmenī.

* "Nosaukums" ir objekta nosaukums. Nulles izbeigšanas nav.

* Īpašums[n] ir n-tais īpašums. Informāciju par formātu skatiet sadaļā Rekvizīts Ieraksta formāts. Rekvizīti tiek rakstīti secīgi un bez polsterējuma.

* `NestedList` ir ligzdots saraksts, kura esamību norāda ar NULL ierakstu pašās beigās.


Ligzdota saraksta ieraksta esamību var noteikt, pārbaudot, vai ir atlikuši baiti, līdz tiek sasniegts EndOffset. Ja tā, nākamais objekta ieraksts ir jālasa tieši aiz pēdējā rekvizīta. Pēc tam objekta ieraksts seko 13 nulles baitiem, kas pēc tam tiek apvienoti ar EndOffset. NULL ieraksta mērķis vai prasība nav zināma un var norādīt uz kādu formāta līdzekli.

### Īpašuma ieraksta formāts ###

Īpašuma ierakstā ir ietverta informācija par rekvizītiem, kas ir daļa no Node. Rekvizīta ierakstam ir šāds atmiņas izkārtojums:


|Izmērs (baiti)|Datu tips|Nosaukums
--- | --- | ---
|1|char|Tila kods
|?|?|Dati

TypeCode apzīmē rakstzīmju kodus, kas ir sakārtoti grupās, kurām nepieciešama līdzīga apstrāde. TypeCodes var iedalīt šādos veidos, un TypeCode var būt viens no rakstzīmju kodiem starp šiem veidiem.

#### Primitīvie tipi ####

```
Y: 2 byte signed Integer
C: 1 bit boolean (1: true, 0: false) encoded as the LSB of a 1 Byte value.
I: 4 byte signed Integer
F: 4 byte single-precision IEEE 754 number
D: 8 byte double-precision IEEE 754 number
L: 8 byte signed Integer
```

Dati primitīvā skalārā tipa ierakstā ir tieši vērtības binārais attēlojums mazā baitu secībā.

#### Masīvu veidi ####

```
f: Array of 4 byte single-precision IEEE 754 number
d: Array of 8 byte double-precision IEEE 754 number
l: Array of 8 byte signed Integer
i: Array of 4 byte signed Integer
b: Array of 1 byte Booleans (always 0 or 1)
```

Masīva veida dati ir sarežģītāki, un tiem ir šāda struktūra.


|Izmērs (baiti)|Datu tips|Nosaukums
--- | --- | ---
|4|Uint32|ArrayLength
|4|Uint32|Kodējums
|4|Uint32|Saspiestais garums
|?|?|Saturs

### Īpašie veidi ###

Tālāk ir norādīti īpašo veidu tipa kodi.

```
S: String
R: raw binary data
```

Abi šie tipa kodi ir attēloti šādi:


|Izmērs (baiti)|Datu tips|Nosaukums
--- | --- | ---
|4|Uin32|Garums
|Garums| |

Virknei nav nulles beigu, un tajā var būt \0 rakstzīmes (tas faktiski tiek izmantots dažos FBX rekvizītos).

## Atsauces Nr.

* [FBX — The Autodesk SDK](https://help.autodesk.com/view/FBX/2017/ENU/)

* [FBX binārā faila formāta specifikācijas](https://code.blender.org/2013/08/fbx-binary-file-format-specification/)

* [FBX — Wikipedia](https://en.wikipedia.org/wiki/FBX#File_format)


