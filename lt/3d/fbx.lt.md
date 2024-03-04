{
  "date": "2019-12-12",
  "keywords": [
"FBX",
"failą",
"pratęsimas",
"formatu",
"3D failo formatas"
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

## Kas yra FBX failas?

FBX, FilmBox, yra populiarus 3D failo formatas, kurį iš pradžių sukūrė Kaydara, skirtą MotionBuilder. 2006 m. jį įsigijo Autodesk Inc. ir dabar yra vienas iš pagrindinių 3D mainų formatų, naudojamų daugelyje 3D įrankių. FBX galima tiek dvejetainiu, tiek ASCII failo formatu. Formatas buvo sukurtas siekiant užtikrinti skaitmeninio turinio kūrimo programų sąveiką. Yra daug įrankių, skirtų konvertuoti iš/į FBX failo formatą.

## FBX failo formatas – daugiau informacijos

FBX yra patentuotas formatas, o jo dvejetainio failo formato specifikacijos nėra oficialiai prieinamos. Autodesk teikia C++ FBX SDK, skirtą skaityti, rašyti ir konvertuoti į FBX failą arba iš jo. Python importavimo ir eksportavimo scenarijus, skirtas FBX, taip pat galimas Blender programinėje įrangoje, kuri nenaudoja FBX SDK.

### Teksto failo struktūra

The text-based file structure is a tree-structured documented with clearly named identifiers. It consists of a nested list of nodes arranged in hierarchy where each node has:

* NodeType identifikatorius (klasės pavadinimas)

* Su juo susieta ypatybių rinkinys, eilės elementai yra įprasti primityvūs duomenų tipai: ##float, integer, string## ir kt.

* Sąrašas, kuriame yra to paties formato mazgų (rekursyviai).


Logiškai juos galima pavaizduoti taip:

```
NodeType: SomeProperty0a, SomeProperty0b, ... , {

 NestedNodeType1 : SomeProperty1a, ...
 NestedNodeType2 : SomeProperty2a, ... , {
 ... Sub-scope
 }

 ...
}
```

Kai kurie standartiniai mazgai apibrėžiami kaip numanomas sąrašas, kuriame kiekvienas elementas susideda iš įdėto sąrašo. Bet kuri programa, ketinanti pasiekti FBX geometriją, turi išanalizuoti šį turinį ir suteikti naudingą reikšmę. Toliau pateikiamas tekstinio FBX failo pavyzdys:

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

## Dvejetainė FBX failų struktūra

Kaip minėta anksčiau, FBX failo formato specifikacijos nėra viešai prieinamos FBX. Kadangi Blender Foundation įgyvendina FBX failo formatą nenaudodama įmonės pateikto SDK, dalis informacijos apie dvejetainį failo formatą yra [available](https://code.blender.org/2013/08/fbx-binary-file-format-specification/) kaip jo įgyvendinimo dalis.

Dvejetainių failų struktūra yra tokia:

* Antraštė

* Objekto įrašas

* Poraštė


### FBX antraštė

Failo antraštės informaciją sudaro 27 baitai.

* 0–20 baitai: „Kaydara FBX Binary“ \x00 (magiškas failas, 2 tarpai pabaigoje, tada NULL terminatorius).

* 21–22 baitai: [0x1A, 0x00]## (nežinoma, bet visi stebimi failai rodo šiuos baitus).

* 23–26 baitai: nepasirašytas int, versijos numeris. 7300, pavyzdžiui, 7.3 versijai.


### Objekto įrašas ###

Po antraštės yra objekto įrašas, kuris yra visas mazgo įrašas su tuščiu pavadinimu ir tuščiu ypatybių sąrašu. Jame rekursyviai yra visas failo formavimas.

### Poraštė ###

FBX poraštės skyrius yra failo, kurio turinys nežinomas, pabaigoje.

## Įrašų formatai ##

FBX failo įrašai skirstomi į:

* Mazgo įrašai

* Nuosavybės įrašai


### Mazgo įrašo formatas ###

Kiekvienas mazgo įrašo formatas yra pavadintas ir turi tokį atminties išdėstymą.


|Dydis (baitai)|Datos tipas|Vardas
--- | ---|---|
|4|UInt32|EndOffset
|4|UInt32|NumProperties
|4|UInt32|PropertyListLen
|1|UInt8|VardasLen
|VardasIlgis|char|Vardas
|?|?|Ypatybė[n], kur n = 0:PropertyListLen
|Neprivaloma| |
|?|?|NestedList
|13|uint8[]|Nulinis įrašas

kur:

* „EndOffset“ yra atstumas nuo failo pradžios iki mazgo įrašo pabaigos (ty pirmojo baito to, kas ateina). Tai gali būti naudojama norint lengvai praleisti nežinomus ar nereikalingus įrašus.

* „NumProperties“ yra ypatybių skaičius verčių eilutėje, susietoje su mazgu. Įdėtas sąrašas kaip paskutinis elementas nėra skaičiuojamas kaip nuosavybė.

* „PropertyListLen“ yra nuosavybės sąrašo ilgis. Tai dydis, reikalingas ##NumProperties## ypatybėms saugoti, kuris priklauso nuo ypatybių duomenų tipo.

* „NameLen“ yra objekto pavadinimo ilgis simboliais. Atrodo, kad vienintelis atvejis, kai tai yra 0, yra aukščiausio lygio sąrašai.

* "Vardas" yra objekto pavadinimas. Nulinio nutraukimo nėra.

* „Nuosavybė[n]“ yra n-oji nuosavybė. Norėdami sužinoti apie formatą, žr. skyrių ypatybė Įrašo formatas. Savybės rašomos nuosekliai ir be užpildymo.

* „NestedList“ yra įdėtas sąrašas, kurio buvimas rodomas NULL įrašu pačioje pabaigoje.


Įdėto sąrašo įrašo buvimą galima nustatyti patikrinus, ar liko baitų, kol pasiekiamas EndOffset. Jei taip, kitas objekto įrašas turėtų būti skaitomas iškart po paskutinės savybės. Tada objekto įrašas seka 13 nulinių baitų, kurie vėliau sujungiami su EndOffset. NULL įrašo tikslas ar reikalavimas nežinomas ir gali nurodyti tam tikrą formato funkciją.

### Nuosavybės įrašo formatas ###

Ypatybės įraše yra informacijos apie ypatybes, kurios yra mazgo dalis. Nuosavybės įrašas turi tokį atminties išdėstymą:


|Dydis (baitai)|Duomenų tipas|Vardas
--- | --- | ---
|1|char|Tipo kodas
|?|?|Duomenys

TypeCode reiškia simbolių kodus, kurie suskirstyti į grupes, kurias reikia tvarkyti panašiai. TypeCodes galima suskirstyti į šiuos tipus, o TypeCode gali būti vienas iš šių tipų simbolių kodų.

#### Primityvūs tipai ####

```
Y: 2 byte signed Integer
C: 1 bit boolean (1: true, 0: false) encoded as the LSB of a 1 Byte value.
I: 4 byte signed Integer
F: 4 byte single-precision IEEE 754 number
D: 8 byte double-precision IEEE 754 number
L: 8 byte signed Integer
```

Duomenys primityvaus skaliarinio tipo įraše yra tiksliai dvejetainis reikšmės atvaizdas, mažos baigties baitų tvarka.

#### Masyvo tipai ####

```
f: Array of 4 byte single-precision IEEE 754 number
d: Array of 8 byte double-precision IEEE 754 number
l: Array of 8 byte signed Integer
i: Array of 4 byte signed Integer
b: Array of 1 byte Booleans (always 0 or 1)
```

Masyvo tipo duomenys yra sudėtingesni ir yra tokios struktūros.


|Dydis (baitai)|Duomenų tipas|Vardas
--- | --- | ---
|4|Uint32|Masyvo ilgis
|4|Uint32|Kodavimas
|4|Uint32|Suspaustas ilgis
|?|?|Turinys

### Specialūs tipai ###

Toliau pateikiami specialiųjų tipų tipo kodai.

```
S: String
R: raw binary data
```

Abu šie tipo kodai pateikiami taip:


|Dydis (baitai)|Duomenų tipas|Vardas
--- | --- | ---
|4|Uin32|Ilgis
|Ilgis| |

Eilutė nėra baigta nuliu, joje gali būti \0 simbolių (tai iš tikrųjų naudojama kai kuriose FBX ypatybėse).

## Nuorodos Nr.

* [FBX – The Autodesk SDK](https://help.autodesk.com/view/FBX/2017/ENU/)

* [FBX dvejetainio failo formato specifikacijos](https://code.blender.org/2013/08/fbx-binary-file-format-specification/)

* [FBX – Vikipedija](https://en.wikipedia.org/wiki/FBX#File_format)


