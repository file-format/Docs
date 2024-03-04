{
  "date" : "2022-03-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "CR2 failo formatas – „Canon Raw 2“ vaizdo failas",
  "description":"Sužinokite apie CR2 failo formatą ir API, kurios gali kurti ir atidaryti CR2 failus.",
  "linktitle" : "CR2",
  "menu" : {
    "docs" : {
      "identifier":"image-cr2-lt",
      "parent" : "image"
}
},
  "lastmod" : "2022-03-26"
}

## Kas yra CR2 failas?

CR2 (Camera RAW 2) failas yra RAW vaizdo failas, sukurtas naudojant Canon skaitmeninius fotoaparatus. Jis saugo originalius neapdorotus be nuostolių vaizdo duomenis, užfiksuotus fotoaparatu. CR2 failo formatą sukūrė Canon savo skaitmeniniams fotoaparatams ir jis gali įrašyti aukštos kokybės vaizdus iki 14 bitų RGB. Taip gaunami aukštos kokybės vaizdai su pakankamai vietos tolesniam apdorojimui. CR2 vaizdo formatą naudojo Canon savo 350D, 20D ir 1D fotoaparatų modeliuose. CR2 failai yra RAW failai ir juose yra papildomos metaduomenų informacijos, tokios kaip fotoaparato informacija, objektyvo informacija, kadrų kadrų informacija, baltos spalvos balansas ir kiti nustatymai.

## CR2 failo formatas

CR2 failai saugomi fotoaparato atminties kortelėje kaip dvejetainiai failai Canon patentuotu failo formatu. CR2 failo formatas pakeitė iš pradžių naudotą CRW failo formatą, o vėliau buvo pakeistas Canon RAW 3 formatu. CR2 failo formatas yra pagrįstas [TIFF](/image/tiff/) specifikacijomis, kuriose yra 4 vaizdo failų katalogai (IFD).

|Offsetas |Turinys |Komentaras|
---|---|---|
|0x0000 |Antraštė |yra baitų tvarka, versija ir poslinkis į RAW paveikslėlį|
|apskaičiuota |IFD#0 |šioje dalyje yra Exif skyrius, kuriame yra Makernotes skyrius.
Informacija apie paveikslėlį#0|
|apskaičiuota |paveikslėlis#0 |maža nuotraukos versija (ketvirtadalis originalo dydžio), suspausta Jpeg|
|apskaičiuota |IFD#1 |Informacija apie paveikslėlį#1.|
|apskaičiuota |paveikslėlis#1 |maža paveikslėlio versija, suglaudinta Jpeg|
|apskaičiuota |IFD#2 |Informacija apie paveikslėlį#2.|
|apskaičiuota |paveikslėlis#2 |maža nuotraukos versija, nesuspausta|
|antraštėje| IFD#3| Informacija apie 3 paveikslėlį, viso dydžio RAW vaizdą|
|apskaičiuota |vaizdas#3 |RAW vaizdo duomenys, be nuostolių suglaudinti Jpeg formatu (ne RGB duomenys!)|

## CR2 failo formato pranašumas

Nuotraukų saugojimas RAW formatu leidžia daug vėliau apdoroti nuotrauką, pavyzdžiui, pakoreguoti baltos spalvos balansą. Tai yra daug sudėtingiau ir su dideliu kokybės praradimu naudojant kitus vaizdo failų formatus, pvz., [JPEG](/image/jpeg/).

## Ar CR2 geriau nei JPEG?

CR2 failai yra neapdoroti failai, neprarandant duomenų, taigi ir neprarandant kokybės. Kita vertus, JPEG yra nuostolingas vaizdo failo formatas, nes prarandama dalis duomenų, kad failas būtų sumažintas. Taigi, CR2 failai yra aukštos kokybės ir tinkamesni retušavimui bei patobulinimams.

## Nuorodos

 * [CR2 failo formatas](http://lclevy.free.fr/cr2/)

