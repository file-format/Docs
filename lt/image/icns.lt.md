{
  "date": "2021-06-29",
  "keywords": [
"ICNS",
"pratęsimas",
"failą",
"formatu",
"vaizdas",
"Apple piktogramos vaizdas",
"macOS",
"Apple",
"Piktograma"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "ICNS – „Apple“ piktogramos vaizdas",
  "description": "Sužinokite apie ICNS failo formatą ir API, kurios gali kurti ir atidaryti ICNS failus.",
  "linktitle": "ICNS",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-icn-lts"
}
},
  "lastmod": "2021-06-29"
}

## Kas yra ICNS failas? ##

MacOS programų naudojamas piktogramos formatas vadinamas ICNS failu. Tai leidžia naudoti 1 bitų ir 8 bitų alfa juostas ir išsaugo vieną ar daugiau nuotraukų, dažniausiai padarytų iš [PNG](/image/png/) dokumentų. Programos piktograma macOS naršyklėje ir sąsajoje rodoma naudojant ICNS failus.

Atsižvelgiant į vietą, ta pati stiliaus piktograma gali turėti kelis nustatymus. ICNS formatas buvo daug pakeistas ir išsivystė taip, kad dabar jis gali būti naudojamas kaip įvairių suderinamų formatų pagrindas. Štai keletas kitų svarbių dalykų, kuriuos turite žinoti:

* IconFamily Resource, Macintosh Icon, Macintosh OS X Icon, Mac OS Icon, Apple Icon, Mac OS X Icon Resource ir Mac OS icons Resource yra keletas kitų pavadinimų. 

* Informacijai apie piktogramas naudojamas šaltinis šaltinio šakoje.

* Daugeliu atvejų faile yra daug vaizdų. Palaikomi 1612 pikselių kvadratiniai ir 1024, 512, 256, 128, 48, 32 ir 16 pikselių kvadratiniai vaizdo dydžiai.



## ICNS failo formatas ##

ICNS duomenų formatas yra vieno ar kelių vaizdų kapsulė, palaikanti 1 bito juostas ir daugybę vaizdo būsenų.
Operacinė sistema gali pakeisti piktogramų paveikslėlių dydį, kad atitiktų reikiamą ekrano dydį. Didesnės piktogramos nuotraukos paprastai išsaugomos kaip [JPEG](/image/jpeg/) 2000 arba [PNG](/image/png/) failai. Galimi ir suspaustų, ir nesuspaustų ICNS failų tipai.

Antraštė ir dvejetainės piktogramos duomenys sudaro ICNS failo struktūrą. Antraštėje yra 8 baitai duomenų, iš kurių keturi yra stebuklingi, o keturi – failo ilgio. Kiekvienos piktogramos paveikslėlio tipas ir dydis saugomi piktogramų duomenų skyriuje, po kurio pateikiami dvejetainiai vaizdo duomenys. Paveikslėlio dydis lemia dvejetainės sekcijos dydį.

## Techninė specifikacija Nr.

### Antraštė ###

|Offsetas|Dydis|Tikslas
---|---|---|
|0|4|Magic literal, turi būti icns (0x69, 0x63, 0x6e, 0x73)
|4|4|Failo ilgis, baitais, pirmiausia msb


### Piktogramos duomenys ###

|Offsetas|Dydis|Tikslas
---|---|---|
|0|4|Piktogramos tipas
|4|4|Duomenų ilgis, baitais (įskaitant tipą ir ilgį), pirmiausia msb
|8|Kintamasis|Piktogramos duomenys

### Suspaudimas ###

Pikselių duomenys tam tikru mastu suglaudinami. 32 bitų (is32, il32, ih32, it32) ir ARGB (ic04, ic05) pikseliai dažnai suglaudinami (viename kanale) panašiai kaip PackBits.

|Lead Value|Uodegos baitai|Rezultatas (nesuglaudintas)
---|---|---|
|0 - 127|1 - 128|1 - 128 baitai
|128 - 255|1 baitas|3 - 130 kopijų

## Nuoroda ##

* [ICNS – Vikipedija](https://en.wikipedia.org/wiki/Apple_Icon_Image_format)


