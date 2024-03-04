{
  "date": "2023-01-10",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "WOFF2 failas – žiniatinklio atvirojo šrifto formato 2.0 failas",
  "description": "Sužinokite, kas yra WOFF2 failas ir API, kurios gali sukurti ir atidaryti WOFF2 failą.",
  "linktitle": "WOFF2",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-woff-lt2"
}
},
  "lastmod": "2023-01-10"
}

## Kas yra WOFF2 failas?

WOFF2 yra šrifto failo formatas, kuris yra labiau suspausta žiniatinklio atvirojo šrifto formato (WOFF) versija. Jis buvo sukurtas siekiant sumažinti žiniatinklio šriftų failo dydį, leidžiantį juos įkelti greičiau ir naudoti mažiau pralaidumo. WOFF2 naudoja glaudinimo algoritmą, vadinamą Brotli, kad suspaustų šrifto duomenis, todėl failų dydžiai gali būti žymiai mažesni nei lygiaverčiai [WOFF](/font/woff/) šriftai. Šį formatą palaiko dauguma šiuolaikinių žiniatinklio naršyklių, įskaitant Chrome, Firefox, Safari, Opera ir Edge (14 ir naujesnės versijos).

## WOFF2 failo formatas – daugiau informacijos

WOFF2 šrifto failo vidinė failo struktūra susideda iš kelių skirtingų dalių, įskaitant antraštę, metaduomenis, lentelės katalogą ir pačius šrifto duomenis.

 1. Antraštėje pateikiama informacija apie bendrą failo formatą, įskaitant versijos numerį ir faile esančių lentelių skaičių.

 1. Metaduomenų skiltyje pateikiama tokia informacija kaip šrifto pavadinimas, autorių teisės ir kita su šriftu susijusi informacija.

 1. Lentelių kataloge yra informacijos apie skirtingas lenteles, kurios sudaro šriftą, įskaitant jų vietą faile ir ilgį.

 1. Patys šrifto duomenys yra suskirstyti į kelias skirtingas lenteles, kurių kiekvienoje yra konkreti informacija apie šriftą, pvz., jo simboliai ir juos atitinkantys glifai. Šiose lentelėse gali būti:

 * Glyf lentelėje pateikiami tikri šrifto kontūrai, įskaitant kiekvieno simbolio formą ir dydį.
 * Lentelėje galva pateikiama bendra informacija apie šriftą, pvz., jo versijos numeris, dizaino dydis ir pan.
 * Lentelėje hmtx pateikiama informacija apie šrifto metriką, įskaitant simbolių plotį ir padėtį.
 * Kiekviena lentelė suglaudinama ir išsaugoma WOFF2 failo formatu, kai ji baigia kodavimo procesą.

Bendra struktūra sukurta taip, kad būtų galima greitai analizuoti ir dekoduoti, kad interneto naršyklės galėtų greitai ir efektyviai įkelti ir rodyti šriftą svetainėje.

### WOFF2 antraštė
WOFF antraštę sudaro identifikuojantis parašas, nurodantis į failą įtrauktų duomenų rūšį. WOFF antraštė kartu su jos laukais yra tokia.

|Tipas|Lauko pavadinimas|Aprašymas|
---|---|---|
|UInt32|parašas |0x774F4632 'wOF2' |
|UInt32| flavor |Įvesties šrifto sfnt versija.|
|UInt32| ilgis |Bendras WOFF failo dydis.|
|UInt16| numTables |Įrašų skaičius šriftų lentelių kataloge.|
|UInt16| rezervuotas |Rezervuotas; nustatyti į nulį.|
|UInt32| totalSfntSize |Bendras dydis, reikalingas nesuspaustiems šrifto duomenims, įskaitant sfnt antraštę, katalogą ir šriftų lenteles (įskaitant užpildymą).|
|UInt32| totalCompressedSize Bendras suspausto duomenų bloko ilgis.|
|UInt16| majorVersion |Pagrindinė WOFF failo versija.|
|UInt16| minorVersion |Nedidelė WOFF failo versija.|
|UInt32| metaOffset |Poslinkis į metaduomenų bloką, nuo WOFF failo pradžios.|
|UInt32| metaLength |Suspausto metaduomenų bloko ilgis.|
|UInt32| metaOrigLength |Nesuspaustas metaduomenų bloko dydis.|
|UInt32| privOffset |Poslinkis į privačių duomenų bloką, nuo WOFF failo pradžios.|
|UInt32| privLength |Privačių duomenų bloko ilgis.|


## Nuorodos
 * [w3 WOFF2 failo formatas](https://www.w3.org/TR/WOFF2/)

