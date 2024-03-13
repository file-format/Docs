{
  "date": "2019-12-12",
  "keywords": [
"FBX",
"fayl",
"uzadılması",
"format",
"3D fayl formatı"
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

## FBX faylı nədir?

FBX, FilmBox, ilk olaraq Kaydara tərəfindən MotionBuilder üçün hazırlanmış məşhur 3D fayl formatıdır. O, 2006-cı ildə Autodesk Inc tərəfindən alınıb və indi bir çox 3D alətləri tərəfindən istifadə edilən əsas 3D mübadilə formatlarından biridir. FBX həm ikili, həm də ASCII fayl formatında mövcuddur. Format rəqəmsal məzmun yaratma proqramları arasında qarşılıqlı əlaqəni təmin etmək üçün yaradılmışdır. FBX fayl formatından / formatına çevirmək üçün çoxlu alətlər mövcuddur.

## FBX Fayl Format - Ətraflı Məlumat

FBX mülkiyyət formatıdır və onun ikili fayl formatı ilə bağlı spesifikasiyalar rəsmi olaraq mövcud deyil. C++ FBX SDK oxumaq, yazmaq və FBX faylına/faylına çevirmək üçün Autodesk tərəfindən təmin edilir. FBX üçün Python idxal və ixrac skripti FBX SDK-dan istifadə etməyən Blender proqramında da mövcuddur.

### Mətnə əsaslanan fayl strukturu

The text-based file structure is a tree-structured documented with clearly named identifiers. It consists of a nested list of nodes arranged in hierarchy where each node has:

* NodeType identifikatoru (sinif adı)

* Onunla əlaqəli xassələr dəsti, dəst elementləri adi primitiv məlumat növləridir: ##float, tam, string## və s.

* Eyni formatda qovşaqları ehtiva edən siyahı (rekursiv).


Bunları məntiqi olaraq aşağıdakı kimi təqdim etmək olar:

```
NodeType: SomeProperty0a, SomeProperty0b, ... , {

 NestedNodeType1 : SomeProperty1a, ...
 NestedNodeType2 : SomeProperty2a, ... , {
 ... Sub-scope
 }

 ...
}
```

Standart qovşaqlardan bəziləri gizli siyahı kimi müəyyən edilir, burada hər bir element daxili siyahıdan ibarətdir. FBX həndəsəsinə daxil olmaq niyyətində olan hər hansı proqram bu məzmunu təhlil etməli və onun faydalı mənasını verməlidir. Mətn əsaslı FBX faylının nümunəsi aşağıda verilmişdir:

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

## FBX Fayllarının Binar Fayl Strukturu

Daha əvvəl qeyd edildiyi kimi, FBX fayl formatının spesifikasiyası FBX üçün açıq şəkildə mövcud deyil. Blender Foundation şirkətin təqdim etdiyi SDK-dan istifadə etmədən FBX fayl formatını tətbiq etdiyinə görə, ikili fayl formatı ilə bağlı bəzi təfərrüatlar onun həyata keçirilməsinin bir hissəsi kimi [available](https://code.blender.org/2013/08/fbx-binary-file-format-specification/)-dir.

İkili fayl strukturu aşağıdakı ardıcıllıqla əmələ gəlir:

* Başlıq

* Obyekt qeydi

* Altbilgi


### FBX Başlığı

Fayl başlığı məlumatı 27 baytdan ibarətdir.

* Bayt 0 - 20: Kaydara FBX Binary \x00 (fayl sehri, sonunda 2 boşluq, sonra NULL terminatoru).

* Bayt 21 - 22: [0x1A, 0x00]## (naməlum, lakin müşahidə edilən bütün fayllar bu baytları göstərir).

* Bayt 23 - 26: imzasız int, versiya nömrəsi. Məsələn, 7.3 versiyası üçün 7300.


### Obyekt qeydi ###

Başlıqdan sonra boş ad və boş əmlak siyahısı olan tam node qeydi olan obyekt qeydi gəlir. O, rekursiv olaraq bütün fayl formalaşmasını ehtiva edir.

### Altbilgi ###

FBX Footer bölməsi məzmunu bilinməyən faylın sonunda yerləşir.

## Qeyd Formatları ##

FBX faylındakı qeydlər aşağıdakı kimi təsnif edilir:

* Düyün qeydləri

* Əmlak qeydləri


### Node Record Format ###

Hər Node Record Format adlanır və aşağıdakı yaddaş quruluşuna malikdir.


|Ölçü (bayt)|Tarix Növü|Ad
--- | ---|---|
|4|UInt32|EndOffset
|4|UInt32|NumProperties
|4|UInt32|PropertyListLen
|1|UInt8|AdLen
|NameLength|char|Ad
|?|?|Property[n], burada n = 0:PropertyListLen
|Könüllü| |
|?|?|NestedList
|13|uint8[]|Null-Record

harada:

* `EndOffset` faylın əvvəlindən qovşaq qeydinin sonuna qədər olan məsafədir (yəni sonrakı gələn hər şeyin ilk baytı). Bu, naməlum və ya tələb olunmayan qeydləri asanlıqla keçmək üçün istifadə edilə bilər.

* `NumProperties` qovşaqla əlaqəli dəyər dəstindəki xassələrin sayıdır. Son element kimi iç-içə yerləşdirilmiş siyahı mülkiyyət kimi sayılmır.

* `PropertyListLen` əmlak siyahısının uzunluğudur. Bu, ##NumProperties## xassələrinin saxlanması üçün tələb olunan ölçüdür, xassələrin məlumat növündən asılıdır.

* `NameLen` obyekt adının simvollarla uzunluğudur. Bunun 0 olduğu yeganə hal siyahıların yuxarı səviyyəli olduğu görünür.

* `Ad` obyektin adıdır. Sıfır xitam yoxdur.

* `Əmlak[n]` n-ci xüsusiyyətdir. Format üçün Record Format bölməsinə baxın. Xüsusiyyətlər ardıcıllıqla və doldurulmadan yazılır.

* `NestedList` iç-içə siyahıdır, onun mövcudluğu ən sonunda NULL qeydi ilə göstərilir.


İç-içə siyahı girişinin mövcudluğu EndOffset-ə çatana qədər baytların qalıb-qalmadığını yoxlamaqla müəyyən edilə bilər. Əgər belədirsə, növbəti obyekt qeydi birbaşa sonuncu xüsusiyyətdən sonra oxunmalıdır. Obyekt qeydi daha sonra EndOffset ilə birləşən 13 sıfır baytı izləyir. NULL girişinin məqsədi və ya tələbi məlum deyil və bəzi format xüsusiyyətinə işarə edə bilər.

### Mülkiyyət Qeydi Format ###

Əmlak Qeydində Node-un bir hissəsi olan xüsusiyyətlər haqqında təfərrüatlar var. Mülk qeydi aşağıdakı yaddaş quruluşuna malikdir:


|Ölçü (bayt)|Məlumat növü|Ad
--- | --- | ---
|1|char|TypeCode
|?|?|Məlumat

TypeCode oxşar işləmə tələb edən qruplarda sifariş edilən simvol kodlarını təmsil edir. TypeCodeları aşağıdakı növlərə bölmək olar və TypeCode bu tiplər arasında simvol kodlarından biri ola bilər.

#### İbtidai Növlər ####

```
Y: 2 byte signed Integer
C: 1 bit boolean (1: true, 0: false) encoded as the LSB of a 1 Byte value.
I: 4 byte signed Integer
F: 4 byte single-precision IEEE 754 number
D: 8 byte double-precision IEEE 754 number
L: 8 byte signed Integer
```

İbtidai skalyar tipli qeyddəki məlumatlar tam olaraq kiçik endian bayt sırası ilə dəyərin ikili təsviridir.

#### Massiv növləri ####

```
f: Array of 4 byte single-precision IEEE 754 number
d: Array of 8 byte double-precision IEEE 754 number
l: Array of 8 byte signed Integer
i: Array of 4 byte signed Integer
b: Array of 1 byte Booleans (always 0 or 1)
```

Massiv Tipi üçün verilənlər daha mürəkkəbdir və aşağıdakı strukturdadır.


|Ölçü (bayt)|Məlumat növü|Ad
--- | --- | ---
|4|Uint32|ArrayLength
|4|Uint32|Kodlaşdırma
|4|Uint32|Sıxılmış Uzunluq
|?|?|Mündərici

### Xüsusi Növlər ###

Aşağıda Xüsusi Növlər Tip Kodları verilmişdir.

```
S: String
R: raw binary data
```

Bu TipKodların hər ikisi aşağıdakı kimi təmsil olunur:


|Ölçü (bayt)|Məlumat növü|Ad
--- | --- | ---
|4|Uin32|Uzunluq
|Uzunluq| |

Sətir sıfırla dayandırılmır və \0 simvoldan ibarət ola bilər (bu, əslində bəzi FBX xassələrində istifadə olunur).

## İstinadlar ##

* [FBX - Autodesk SDK](https://help.autodesk.com/view/FBX/2017/ENU/)

* [FBX Binary File Format Spesifikasiyaları](https://code.blender.org/2013/08/fbx-binary-file-format-specification/)

* [FBX - Wikipedia](https://en.wikipedia.org/wiki/FBX#File_format)


