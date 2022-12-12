{
  "date" : "2020-08-20",
  "keywords" :[ "soubor cff2", "formát souboru cff2", "co je soubor cff2", "soubor", "příklad cff2", "přípona souboru cff2", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CFF2 - Kompaktní formát souboru písem verze 2",
  "description":"Další informace o formátu souborů CFF2 a rozhraních API pro vytváření a otevírání souborů CFF2.",
  "linktitle" : "CFF2",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-21"
}

## Co je soubor CFF2?

Formát souboru CFF2 je verze 2.0 formátu souboru CFF a umožňuje efektivní ukládání obrysů glyfů a metadat podobných formátu souboru CFF. CFF2 se liší od CFF v tom, že je určen k použití v kontextu s fontem OpenType jako tabulka 'sfnt' s tagem CFF2. Nelze jej použít jako samostatný program a závisí na datech v jiných tabulkách OpenType.

## Formát souboru CFF2

[Specifikace formátu souboru CFF2](https://docs.microsoft.com/en-us/typography/opentype/spec/cff2) obsahuje podrobnosti o vnitřním rozložení dat, datových typech, tabulkách a další interní informace o formátu souboru. Může být odkazováno pro vývojáře. Některé podrobnosti o nich jsou následující.

### Rozložení dat

Binární data formátu souboru CFF2 jsou logicky organizována jako množství samostatných datových struktur. Rozložení v binárních datech je znázorněno v následující tabulce.

|Vstup |Komentáře|
---|---|
|Záhlaví |Pevné umístění|
|Top DICT| Pevné umístění|
|Globální dílčí INDEX| Pevné umístění|
|Varianta |Obchod|
|FDSelect |Přítomný pouze v případě, že je v INDEXU písma DICT více než jedno písmo DICT.|
|Písmo DICT INDEX ||
|Pole písma DICT| Zahrnuto v písmu DICT INDEX.|
|Soukromý DICT| Jeden na písmo DICT.|

Pouze první tři struktury jsou založeny na pevných místech. Zbývající jsou dosaženy pomocí offsetů a jejich pořadí lze změnit.

### Typy dat

Formát souboru CFF2 používá následující datové typy.

|Název |Rozsah |Popis|
---|---|---|
|uint8 |0 až 255 |8bitové číslo bez znaménka|
|uint16 |0 až 65535| 16bitové číslo bez znaménka|
|uint32 |0 až 4294967295| 32bitové číslo bez znaménka|
|Offset |liší se| 1, 2, 3 nebo 4 byte offsety (určené polem OffSize v indexové tabulce)|
|OffSize |1 až 4| 1-bajtové číslo bez znaménka určuje velikost pole nebo polí Offset|

Ukládá všechna vícebajtová numerická data a offsetová pole v pořadí bajtů big-endian. Formát CFF2 neobsahuje výplňové bajty, protože nerespektuje žádná omezení zarovnání.

### Údaje DICT

Soubory CFF2 obsahují data slovníku písem jako páry klíč–hodnota v kompaktním tokenizovaném formátu. Klíče slovníku jsou kódovány jako 1 nebo 2 bajtové operátory a hodnoty slovníku jsou kódovány jako číselné operandy s proměnnou velikostí. Existují tři struktury, které používají formát dat DICT: `Top DICT`, `Font DICT` a `Private DICT`. Je definováno několik typů celočíselných operandů různých velikostí a jsou kódovány tak, jak je uvedeno v následující tabulce (první bajt operandu je b0, druhý je b1 atd.).

|Velikost |rozsah b0 |Rozsah hodnot |Výpočet hodnoty|
---|---|---|---|
|1 |32 až 246| -107 až +107 |b0 - 139|
|2 |247 až 250| +108 až +1131 |(b0 - 247) * 256 + b1 + 108|
|2 |251 až 254| -1131 až -108| -(b0 - 251) * 256 - b1 - 108|
|3 |28| -32768 až +32767| b1 << 8 | b2|
|5 |29| -(2^31) až +(2^31 - 1)| b1 << 24 \| b2 << 16 \| b3 << 8 \| b4|

### Záhlaví

Binární data začínají záhlavím ve formátu uvedeném v tabulce níže.

|Typ |Název |Popis|
---|---|---|
|uint8| hlavníVerze| Formát hlavní verze. Nastavit na 2.|
|uint8| minorVersion| Formát vedlejší verze. Nastavit na nulu.|
|uint8| velikost záhlaví| Velikost záhlaví (bajty).|
|uint16| topDictLength| Délka horní struktury DICT v bajtech.|

## Reference

* [Formát souboru CFF2](https://docs.microsoft.com/en-us/typography/opentype/spec/cff2)

