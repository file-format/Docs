{
  "date" : "2019-12-12",
  "keywords" :[ "FBX", "soubor", "přípona", "formát", "3D formát souboru" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Váš průvodce formátem souborů, abyste věděli, co je soubor FBX a rozhraní API, která je mohou vytvořit a otevřít.",
  "title" :"FBX - Formát souboru 3D FilmBox",
  "linktitle" : "FBX",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor FBX?

FBX, FilmBox, je populární formát 3D souborů, který původně vyvinula společnost Kaydara pro MotionBuilder. V roce 2006 jej získala společnost Autodesk Inc a nyní je jedním z hlavních 3D výměnných formátů používaných mnoha 3D nástroji. FBX je k dispozici v binárním i ASCII formátu. Formát byl vytvořen, aby poskytoval interoperabilitu mezi aplikacemi pro vytváření digitálního obsahu. Pro převod z/do formátu souboru FBX je k dispozici mnoho nástrojů.

## Formát souboru FBX – Další informace

FBX je proprietární formát a specifikace jeho binárního formátu souboru nejsou oficiálně dostupné. C++ FBX SDK poskytuje Autodesk pro čtení, zápis a převod do/ze souboru FBX. Skript pro import a export Pythonu pro FBX je také dostupný v softwaru Blender, který nepoužívá FBX SDK.

### Textová struktura souborů

Textová struktura souborů je stromová a dokumentovaná jasně pojmenovanými identifikátory. Skládá se z vnořeného seznamu uzlů uspořádaných v hierarchii, kde každý uzel má:

* Identifikátor NodeType (název třídy)
* Nice vlastností s tím spojených, n-tice prvky jsou obvyklé primitivní datové typy: ##float, integer, string## atd.
* Seznam, který obsahuje uzly ve stejném formátu (rekurzivně).

Lze je logicky reprezentovat následovně:

```
NodeType: SomeProperty0a, SomeProperty0b, ... , {

 NestedNodeType1 : SomeProperty1a, ...
 NestedNodeType2 : SomeProperty2a, ... , {
 ... Sub-scope
 }

 ...
}
```

Některé standardní uzly jsou definovány jako implicitní seznam, kde každá položka sestává z vnořeného seznamu. Každá aplikace, která má v úmyslu přistupovat ke geometrii FBX, musí tento obsah analyzovat a dát mu užitečný význam. Příklad textového souboru FBX je uveden níže:

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

## Binární struktura souborů FBX souborů

Jak bylo uvedeno dříve, specifikace formátu souborů FBX nejsou pro FBX veřejně dostupné. Vzhledem k tomu, že Blender Foundation implementuje formát souboru FBX bez použití sady SDK poskytované společností, některé podrobnosti o formátu binárního souboru jsou [k dispozici](https://code.blender.org/2013/08/fbx-binary-file-format-specification/) jako součást jeho implementace.

Struktura binárních souborů má následující pořadí:

* Záhlaví
* Záznam objektu
* Zápatí

### Záhlaví FBX

Informace záhlaví souboru se skládá z 27 bajtů.

* Bajty 0 - 20: Kaydara FBX Binary \x00 (file-magic, se 2 mezerami na konci, pak NULL terminátor).
* Bajty 21 - 22: [0x1A, 0x00]## (neznámé, ale všechny pozorované soubory zobrazují tyto bajty).
* Bajty 23 - 26: unsigned int, číslo verze. 7300 pro verzi 7.3 například.

### Záznam objektu ###

Za záhlavím následuje záznam objektu, který je úplným záznamem uzlu s prázdným názvem a prázdným seznamem vlastností. Rekurzivně obsahuje celou formaci souboru.

### Zápatí ###

Sekce FBX Footer se nachází na konci souboru, jehož obsah není znám.

## Formáty záznamu ##

Záznamy v souboru FBX jsou kategorizovány jako:

* Záznamy uzlů
* Evidence majetku

### Formát záznamu uzlu ###

Každý formát záznamu uzlu je pojmenován a má následující rozložení paměti.


|Velikost (bajty)|Typ data|Název
--- | ---|---|
|4|UInt32|Koncový posun
|4|UInt32|NumProperties
|4|UInt32|PropertyListLen
|1|UInt8|JménoLen
|JménoDélka|znak|Jméno
|?|?|Vlastnost[n], kde n = 0:ListLen vlastností
|Volitelné| |
|?|?|Vnořený seznam
|13|uint8[]|Nulový záznam

kde:

* `EndOffset` je vzdálenost od začátku souboru do konce záznamu uzlu (tj. první bajt toho, co následuje). To lze použít ke snadnému přeskočení neznámých nebo nepotřebných záznamů.
* `NumProperties` je počet vlastností v n-tice hodnot přidružených k uzlu. Vnořený seznam jako poslední prvek se nepočítá jako vlastnost.
* `PropertyListLen` je délka seznamu vlastností. Toto je velikost požadovaná pro ukládání vlastností ##NumProperties##, která závisí na datovém typu vlastností.
* `NameLen` je délka názvu objektu ve znacích. Zdá se, že jediným případem, kdy je toto 0, jsou seznamy nejvyšší úrovně.
* `Název` je název objektu. Neexistuje žádná nulová výpověď.
* `Vlastnost[n]` je n-tá vlastnost. Formát viz sekce Vlastnost Formát záznamu. Vlastnosti se zapisují sekvenčně a bez odsazení.
* `NestedList` je vnořený seznam, jehož přítomnost je označena NULL–záznamem na samém konci.

Existenci položky vnořeného seznamu lze určit kontrolou, zda zbývají bajty do dosažení koncového posunu. Pokud ano, další záznam objektu by měl být načten přímo po poslední vlastnosti. Záznam objektu pak následuje po 13 nulových bajtech, které se pak spojí s EndOffset. Účel nebo požadavek položky NULL není znám a může ukazovat na nějakou funkci formátu.

### Formát záznamu majetku ###

Záznam vlastností obsahuje podrobnosti o vlastnostech, které jsou součástí Node. Záznam vlastnosti má následující rozložení paměti:


|Velikost (bajty)|Typ dat|Název
--- | --- | ---
|1|znak|Kód typu
|?|?|Data

TypeCode představují kódy znaků, které jsou seřazeny ve skupinách, které vyžadují podobné zacházení. TypeCodes lze rozdělit do následujících typů a TypeCode může být jedním z kódů znaků mezi těmito typy.

#### Primitivní typy ####

```
Y: 2 byte signed Integer
C: 1 bit boolean (1: true, 0: false) encoded as the LSB of a 1 Byte value.
I: 4 byte signed Integer
F: 4 byte single-precision IEEE 754 number
D: 8 byte double-precision IEEE 754 number
L: 8 byte signed Integer
```

Data v záznamu primitivního skalárního typu jsou přesně binární reprezentací hodnoty v pořadí bajtů typu little-endian.

#### Typy polí ####

```
f: Array of 4 byte single-precision IEEE 754 number
d: Array of 8 byte double-precision IEEE 754 number
l: Array of 8 byte signed Integer
i: Array of 4 byte signed Integer
b: Array of 1 byte Booleans (always 0 or 1)
```

Data pro typ pole jsou složitější a mají následující strukturu.


|Velikost (bajty)|Typ dat|Název
--- | --- | ---
|4|Uint32|Délka pole
|4|Uint32|Kódování
|4|Uint32|CompressedLength
|?|?|Obsah

### Speciální typy ###

Následují speciální typy TypeCodes.

```
S: String
R: raw binary data
```

Oba tyto kódy typu jsou reprezentovány následovně:


|Velikost (bajty)|Typ dat|Název
--- | --- | ---
|4|Uin32|Délka
|Délka| |

Řetězec není zakončen nulou a může obsahovat znaky \0 (toto se ve skutečnosti používá v některých vlastnostech FBX).

## Reference ##

* [FBX – The Autodesk SDK](https://help.autodesk.com/view/FBX/2017/ENU/)
* [Specifikace formátu binárního souboru FBX](https://code.blender.org/2013/08/fbx-binary-file-format-specification/)
* [FBX – Wikipedie](https://en.wikipedia.org/wiki/FBX#File_format)

