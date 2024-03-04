{
  "date": "2020-08-20",
  "keywords": [
"cff2 failą",
"cff2 failo formatas",
"kas yra cff2 failas",
"failą",
"cff2 pavyzdys",
"cff2 failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "CFF2 – kompaktinio šrifto failo formato 2 versija",
  "description": "Sužinokite apie CFF2 failo formatą ir API, kad sukurtumėte ir atidarytumėte CFF2 failus.",
  "linktitle": "CFF2",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-cff-lt2"
}
},
  "lastmod": "2020-10-21"
}

## Kas yra CFF2 failas?

CFF2 file format is the version 2.0 of the CFF file format and allows efficient storage of glyph outlines and metadata similar to the CFF file format. CFF2 differs from CFF in that it is intended to be used in the context of an OpenType font as a 'sfnt' table with the tag CFF2. Ji negali būti naudojama kaip atskira programa ir priklauso nuo duomenų kitose OpenType lentelėse.

## CFF2 failo formatas

[CFF2 file format specifications](https://learn.microsoft.com/en-us/typography/opentype/spec/cff2) pateikiama išsami informacija apie vidinių duomenų išdėstymą, duomenų tipus, lenteles ir kitą vidinę informaciją apie failo formatą. Jis gali būti pateiktas kūrėjo nuorodai. Kai kurios detalės apie tai pateikiamos toliau.

### Duomenų išdėstymas

CFF2 failo formato dvejetainiai duomenys yra logiškai suskirstyti į keletą atskirų duomenų struktūrų. Dvejetainių duomenų išdėstymas yra toks, kaip parodyta šioje lentelėje.

|Įrašas |Pastabos|
---|---|
|Antraštė |Fiksuota vieta|
|Top DICT| Fiksuota vieta|
|Global Subr INDEX| Fiksuota vieta|
|Variacija |Parduotuvė|
|FDSirinkite |Pateikti tik tada, jei šriftų DICT INDEX yra daugiau nei vienas šriftas DICT.|
|Šrifto DICT INDEKSAS ||
|Šriftų masyvas DICT| Įtraukta į Šrifto DICT INDEX.|
|Privatus DICT| Vienas šriftas DICT.|

Tik pirmosios trys struktūros yra pagrįstos fiksuotomis vietomis. Likusieji pasiekiami perskaitymu, o jų eilės tvarka gali būti keičiama.

### Duomenų tipai

CFF2 failo formatas naudoja šiuos duomenų tipus.

|Pavadinimas |Diapazonas |Aprašymas|
---|---|---|
|uint8 |nuo 0 iki 255 |8 bitų be ženklo numeris|
|uint16 |0 iki 65535| 16 bitų be ženklo numeris|
|uint32 |0 iki 4294967295| 32 bitų nepaženklintas numeris|
|Poslinkis |kinta| 1, 2, 3 arba 4 baitų poslinkiai (nurodyti rodyklės lentelės lauke OffSize)|
|OffSize |1–4| 1 baito nepaženklintas skaičius nurodo poslinkio lauko ar laukų dydį|

Jame saugomi visi kelių baitų skaitmeniniai duomenys ir poslinkio laukai didžiųjų baitų tvarka. CFF2 formate nėra užpildymo baitų, nes jis nepaiso jokių lygiavimo apribojimų.

### DICT duomenys

CFF2 failuose yra šrifto žodyno duomenys kaip raktų ir reikšmių poros kompaktišku atpažinimo formatu. Žodyno klavišai koduojami kaip 1 arba 2 baitų operatoriai, o žodyno reikšmės koduojamos kaip kintamo dydžio skaitmeniniai operandai. Yra trys struktūros, kuriose naudojamas DICT duomenų formatas: Top DICT, Font DICT ir Private DICT. Apibrėžiama keletas įvairaus dydžio sveikųjų skaičių operandų tipų ir yra užkoduoti, kaip parodyta šioje lentelėje (pirmasis operando baitas yra b0, antrasis yra b1 ir t. t.).

|Dydis |b0 diapazonas |Verčių diapazonas |Vertės apskaičiavimas|
---|---|---|---|
|1 |32–246| -107 iki +107 |b0 - 139|
|2	|247 to 250|	+108 to +1131	|(b0 - 247) * 256 + b1 + 108|
|2	|251 to 254|	-1131 to -108|	-(b0 - 251) * 256 – b1 – 108|
|3 |28| -32768 iki +32767| b1 << 8 | b2|
|5 |29| -(2^31) iki +(2^31 - 1)| b1 << 24 \| b2 << 16 \| b3 << 8 \| b4|

### Antraštė

Dvejetainiai duomenys prasideda antrašte, kurios formatas parodytas toliau esančioje lentelėje.

|Tipas |Vardas |Aprašymas|
---|---|---|
|uint8| pagrindinė versija| Formatuokite pagrindinę versiją. Nustatykite 2.|
|uint8| minorVersija| Formatuoti mažesnę versiją. Nustatyti į nulį.|
|uint8| headerSize| Antraštės dydis (baitais).|
|uint16| topDictLength| Viršutinės DICT struktūros ilgis baitais.|

## Nuorodos

 * [CFF2 failo formatas](https://learn.microsoft.com/en-us/typography/opentype/spec/cff2)

