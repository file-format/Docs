{
  "date": "2019-12-12",
  "keywords": [
"FBX",
"comhad",
"síneadh",
"formáid",
"Formáid Comhaid 3D"
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

## Cad is comhad FBX ann?

Is formáid comhaid 3D a bhfuil an-tóir uirthi é FBX, FilmBox, a d’fhorbair Kaydara do MotionBuilder ar dtús. Fuair Autodesk Inc é in 2006 agus tá sé anois ar cheann de na príomh-formáidí malartaithe 3D mar a úsáideann go leor uirlisí 3D é. Tá FBX ar fáil i bhformáid dhénártha agus i bhformáid comhaid ASCII. Bunaíodh an fhormáid chun idir-inoibritheacht a sholáthar idir feidhmchláir chruthaithe ábhair dhigitigh. Tá go leor uirlisí ar fáil le comhshó ó/go formáid comhaid FBX.

## Formáid Chomhaid FBX - Tuilleadh Eolais

Is formáid dhílsithe é FBX agus níl sonraíochtaí faoina bhformáid dhénártha comhaid ar fáil go hoifigiúil. Soláthraíonn Autodesk C++ FBX SDK le léamh, scríobh agus comhshó go/ó chomhad FBX. Tá script iompórtála agus easpórtála Python le haghaidh FBX ar fáil freisin i mbogearraí Cumascóra nach n-úsáideann an FBX SDK.

### Struchtúr Comhaid Téacsbhunaithe

The text-based file structure is a tree-structured documented with clearly named identifiers. It consists of a nested list of nodes arranged in hierarchy where each node has:

* Aitheantóir NodeType (ainm ranga)

* Tuple airíonna a bhaineann leis, is iad na heilimintí tuple na gnáthchineálacha sonraí primitive: ## snámh, slánuimhir, teaghrán## etc.

* Liosta ina bhfuil nóid san fhormáid chéanna (go hathchúrsach).


Is féidir iad seo a léiriú go loighciúil mar seo a leanas:

```
NodeType: SomeProperty0a, SomeProperty0b, ... , {

 NestedNodeType1 : SomeProperty1a, ...
 NestedNodeType2 : SomeProperty2a, ... , {
 ... Sub-scope
 }

 ...
}
```

Sainmhínítear cuid de na nóid chaighdeánacha mar liosta intuigthe ina bhfuil liosta neadaithe i ngach mír. Caithfidh aon fheidhmchlár, a bhfuil sé ar intinn aige rochtain a fháil ar chéimseata FBX, na hábhair seo a pharsáil agus brí úsáideach a bhaint as. Tá sampla de chomhad FBX téacsbhunaithe mar a thugtar thíos:

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

## Struchtúr Comhad Dénártha de Chomhaid FBX

Mar a dúradh roimhe seo, níl sonraíochtaí formáid comhaid FBX ar fáil go poiblí le haghaidh FBX. Ós rud é go gcuireann Fondúireacht Blender formáid comhaid FBX i bhfeidhm gan an chuideachta a sholáthraíonn SDK a úsáid, tá cuid de na sonraí maidir le formáid comhaid dhénártha [available](https://code.blender.org/2013/08/fbx-binary-file-format-specification/) mar chuid dá chur i bhfeidhm.

Leanann an struchtúr comhaid dhénártha an t-ordú seo a leanas:

* Ceanntásc

* Taifead Cuspóir

* Buntásc


### Ceanntásc FBX

Tá 27 beart san fhaisnéis ceannteidil comhaid.

* Bearta 0 - 20: Dénártha Kaydara FBX \x00 (draíocht chomhad, le 2 spás ag an deireadh, ansin Críochnaitheoir NULLComment).

* Bearta 21 - 22: [0x1A, 0x00]## (anaithnid ach léiríonn gach comhad breathnaithe na bearta seo).

* Bearta 23 - 26: slánuimhir gan síniú, uimhir an leagain. 7300 le haghaidh leagan 7.3 mar shampla.


### Taifead Oibiachta ###

Tar éis an Ceanntásc tá taifead oibiachta ar taifead iomlán nóid é le hainm folamh agus liosta réadmhaoine folamh. Tá an foirmiú comhad iomlán ann go hathchúrsach.

### Buntásc ###

Tá an chuid FBX Footer suite ag deireadh comhaid nach bhfuil a bhfuil ann.

## Formáidí Taifead ##

Déantar taifid i gcomhad FBX a chatagóiriú mar:

Taifid Nód *

Taifid Maoine *


### Formáid Taifead Nód ###

Tá gach Formáid Taifead Nód ainmnithe agus tá an leagan amach cuimhne seo a leanas aige.


|Méid (Beirt)|Cineál Dáta|Ainm
--- | ---|---|
|4|Uint32|Fritháireamh Deiridh
|4|Uint32|Uimhir Airíonna
|4|Uint32|Liosta Maoine
|1|Uint8|AinmLen
|AinmFad|char|Ainm
|?|?|Airmheán[n], áit a bhfuil n = 0:Liostaigh Maoine
|Roghnach| |
|?|?|Liosta Neadaithe
|13|uint8[]|Taifead Neamhnithe

áit:

* Is éard atá i `EndOffset` ná an fad ó thús an chomhaid go dtí deireadh an taifead nóid (.i. an chéad bheart de cibé rud a thagann ina dhiaidh). Is féidir é seo a úsáid chun scipeáil thar thaifid anaithnide nó nach bhfuil ag teastáil go héasca.

* Is ionann `NumProperties` agus líon na n-airíonna sa luach tuple a bhaineann leis an nód. Ní áirítear liosta neadaithe mar an eilimint dheireanach mar airí.

* Is é `PropertyListLen` fad an liosta maoine. Seo é an méid atá riachtanach chun airíonna ##NumProperties## a stóráil, a bhraitheann ar chineál sonraí na n-airíonna.

* Is é `NameLen` fad ainm an réada, i gcarachtair. Is cosúil gurb é an t-aon chás ina bhfuil sé seo 0 ná na liostaí barrleibhéil.

* Is é `ainm` ainm an réada. Níl aon fhoirceannadh nialasach.

* Is é `maoin[n]` an nú airí. Chun an fhormáid a fháil, féach Formáid Taifead maoine na rannóige. Scríobhtar airíonna go seicheamhach agus gan aon stuáil.

* Is é `NestedList` an liosta neadaithe, a léirítear láithreacht an liosta sin le taifead NULLComment ag an deireadh.


Is féidir iontráil liosta neadaithe a chinneadh trí sheiceáil an bhfuil bearta fágtha go dtí go sroichtear an EndOffset. Más amhlaidh atá, ba cheart an chéad taifead oibiachta eile a léamh díreach tar éis na hairí deiridh. Leanann an taifead oibiachta ansin 13 beart nialasach, a chomhcheanglaíonn ansin leis an EndOffset. Ní fios cén cuspóir nó riachtanas atá leis an iontráil NULLComment

### Formáid Taifead Maoine ###

Tá sonraí i dtaifead réadmhaoine faoi mhaoine atá mar chuid de Nód. Tá an leagan amach cuimhne seo a leanas ag taifead maoine:


|Méid (Beirt)|Cineál Sonraí|Ainm
--- | --- | ---
|1|char|CineálCód
|?|?|Sonraí

Léiríonn TypeCode cóid charachtair a ordaítear i ngrúpaí a dteastaíonn láimhseáil chomhchosúil uathu. Is féidir TypeCodes a chatagóiriú sna cineálacha seo a leanas agus is féidir TypeCode a bheith ar cheann de na cóid charachtair i measc na gcineálacha seo.

#### Cineálacha Príomhúla ####

```
Y: 2 byte signed Integer
C: 1 bit boolean (1: true, 0: false) encoded as the LSB of a 1 Byte value.
I: 4 byte signed Integer
F: 4 byte single-precision IEEE 754 number
D: 8 byte double-precision IEEE 754 number
L: 8 byte signed Integer
```

Is ionann sonraí sa taifead cineál scálach primitive agus ionadaíocht dhénártha an luacha, in ord beart beag-endian.

#### Cineálacha Eagar ####

```
f: Array of 4 byte single-precision IEEE 754 number
d: Array of 8 byte double-precision IEEE 754 number
l: Array of 8 byte signed Integer
i: Array of 4 byte signed Integer
b: Array of 1 byte Booleans (always 0 or 1)
```

Tá na Sonraí do Chineál Eagar níos casta agus tá sé sa struchtúr seo a leanas.


|Méid (Beirt)|Cineál Sonraí|Ainm
--- | --- | ---
|4|Uint32|Fad Eagar
|4|Uint32|Ionchódú
|4|Uint32|Fad Comhbhrúite
|?|?|Ábhar

### Cineálacha Speisialta ###

Seo a leanas na Cóid Chineálacha de Chineálacha Speisialta.

```
S: String
R: raw binary data
```

Léirítear an dá Chineál seo mar seo a leanas:


|Méid (Beirt)|Cineál Sonraí|Ainm
--- | --- | ---
|4|Uin32|Fad
|Fad| |

Níl an teaghrán foirceanta nialasach, agus d'fhéadfadh go mbeadh \0 carachtair ann (úsáidtear é seo i roinnt airíonna FBX).

## Tagairtí ##

* [FBX - An Autodesk SDK](https://help.autodesk.com/view/FBX/2017/ENU/)

* [Sonraíochtaí Formáid Chomhaid Dénártha FBX](https://code.blender.org/2013/08/fbx-binary-file-format-specification/)

* [FBX - Vicipéid](https://en.wikipedia.org/wiki/FBX#File_format )


