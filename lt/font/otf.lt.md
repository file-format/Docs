{
  "date": "2020-08-20",
  "keywords": [
"otf failą",
"otf failo formatas",
"kas yra otf failas",
"failą",
"otf pavyzdys",
"otf failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "OTF – „TrueType“ šrifto failo formatas",
  "description": "Sužinokite apie OTF failų formatą ir API, kurios gali kurti ir atidaryti OTF failus.",
  "linktitle": "OTF",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-ot-ltf"
}
},
  "lastmod": "2020-09-21"
}

## Kas yra OTF failas?

Failas su plėtiniu .otf reiškia OpenType šrifto formatą. OTF šrifto formatas yra labiau keičiamas ir išplečia esamas [TTF](/font/ttf/) formatų funkcijas, skirtas skaitmeninei tipografijai. Microsoft ir Adobe sukurtas OTF sujungia PostScript ir TrueType šriftų formatų funkcijas. Dėl to OTF formatas yra tinkamas daugumai rašymo sistemų, todėl jis vienodai naudojamas pagrindinėse kompiuterių platformose. OpenType šrifto formatą palaiko Mac OS X ir Windows 2000 ir naujesnės versijos.

## Trumpa istorija

The requirement of OpenType fonts originated as a requirement for a more expressive font format that could handle fine typography. In addition, it was aimed to meet the requirements of complex behaviour of many of the world's writing systems. Microsoft attempted to license Apple's advanced typography technology, known as GX Typography, in the early 1990's. This didn't go well and as a result, Microsoft started enhancing its owns TrueType font technology in 1994. Modifikacijos taip pat buvo įtrauktos į tinkamesnį šrifto formatą, kuris taip pat atitinka Adobe tipo 1 (PostScript) šriftų formatų ypatybes.

Adobe 1996 m. prisijungė prie Microsoft pastangų pakeisti Apple TrueType ir savo Type 1 šriftų formatus. Dėl to buvo derinami abu pagrindiniai šriftų formatai, siekiant įveikti apribojimus ir pridėti naujų plėtinių. Ši nauja technologija buvo pristatyta tais pačiais metais pavadinimu **OpenType**.

## OTF failo formato specifikacijos

OTF specifications are available publicly by Microsoft and can be referred to from developer's perspective. Like TTF, it uses the same 'sfnt' container structure and is compatible with the TrueType specifications. Data inside an OpenType font file is used for different purposes such as calculating the text layout, defining glyphs as TrueType or Compact Font Format (CFF) outlines, providing monochromatic or color bitmaps or SVG documents as alternate glyph descriptions, and meta-data information.

### OTF duomenų tipai
OTF failuose naudojami šie duomenų tipai, kurie yra Big Endian.

|Duomenų tipas| Aprašymas|
---|---|
|uint8| 8 bitų sveikasis skaičius be ženklų.|
|int8| 8 bitų sveikasis skaičius.|
|uint16| 16 bitų sveikasis skaičius be ženklų.|
|int16| 16 bitų sveikasis skaičius.|
|uint24| 24 bitų sveikasis skaičius be ženklų.|
|uint32| 32 bitų sveikasis skaičius be ženklų.|
|int32| 32 bitų sveikasis skaičius.|
|Pataisytas| 32 bitų fiksuoto taško numeris (16.16)|
|FWORD| int16, kuris apibūdina kiekį šrifto dizaino vienetais.|
|UFWORD| uint16, kuris apibūdina kiekį šrifto dizaino vienetais.|
|F2DOT14| 16 bitų pasirašytas fiksuotas skaičius su maža 14 bitų trupmena (2.14).|
|LONGDATETIME| Data ir laikas rodomi sekundžių skaičiumi nuo 12:00 vidurnakčio, 1904 m. sausio 1 d., UTC. Reikšmė pateikiama kaip 64 bitų sveikasis skaičius su ženklu.|
|Žyma| Keturių uint8 masyvas (ilgis = 32 bitai), naudojamas identifikuoti lentelę, dizaino varianto ašį, scenarijų, kalbos sistemą, funkciją arba bazinę liniją|
|Poslinkis16| Trumpas poslinkis į lentelę, toks pat kaip uint16, NULL poslinkis = 0x0000|
|Poslinkis32| Ilgas poslinkis į lentelę, toks pat kaip uint32, NULL poslinkis = 0x00000000|
|Versija16Dot16| Supakuota 32 bitų reikšmė su pagrindiniais ir nedideliais versijų numeriais. (Žr. lentelės versijų numerius.)|

### OTF lentelių katalogas

OTF failas prasideda lentelės katalogu. Šis katalogas yra aukščiausio lygio lentelių rinkinys šrifto faile. Atsižvelgiant į šriftų skaičių faile, lentelės katalogas gali būti skirtingose failo vietose. Pavyzdžiui, jei šrifto faile yra tik vienas šriftas, lentelės katalogas prasideda nuo 0 failo baito. Jei surinkti keli OpenType šriftai,
lentelės katalogo pradžia nurodoma TTCHader.

|Tipas |Vardas |Aprašymas|
---|---|---|
|uint32 |sfntVersion| 0x00010000 arba 0x4F54544F (OTTO)|
|uint16| numTables |Lentelių skaičius.|
|uint16|	searchRange	|Maximum power of 2 less than or equal to numTables, times 16 ((2\**floor(log2(numTables))) * 16, kur ** yra eksponencijos operatorius).|
|uint16 |entrySelector Log2, kurio maksimali galia 2 yra mažesnė arba lygi numTables (log2(searchRange/16), kuri yra lygi floor(log2(numTables))).|
|uint16	|rangeShift	|numTables times 16, minus searchRange ((numTables * 16) – paieškos diapazonas).|
|tableRecord| tableRecords[numTables] |Lentelių įrašų masyvas – po vieną kiekvienai šrifto aukščiausio lygio lentelei|


### Lentelės įrašas

Kiekvienai šrifto aukščiausio lygio lentelei yra lentelės įrašas, kurį sudaro šie laukai.

|Tipas| Vardas| Aprašymas|
---|---|---|
|Žyma| tableTag| Lentelės identifikatorius.|
|uint32| kontrolinė suma| Šios lentelės kontrolinė suma.|
|Poslinkis32| kompensuoti| Poslinkis nuo šrifto failo pradžios.|
|uint32| ilgis Šios lentelės ilgis.|

Kiekviena OpenType šrifto failo lentelė yra pavaizduota pavadinimais, vadinamais lentelės žymomis. Būtina, kad visi masyvo įrašai būtų rūšiuojami didėjimo tvarka pagal žymą.

## Nuorodos
 * [Microsoft pateiktos OpenType šrifto specifikacijos](https://learn.microsoft.com/en-us/typography/opentype/spec/overview)
 * [TrueType apžvalga](https://learn.microsoft.com/en-us/typography/truetype/)

