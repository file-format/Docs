{
  "date": "2019-12-10",
  "keywords": [
"XLSX",
"failą",
"pratęsimas",
"Dokumento formatas",
"Excel",
"Skaičiuoklė"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite, kas yra XLSX failas ir API, kurios gali kurti ir atidaryti XLSX failus.",
  "title": "XLSX failo formatas – kas yra XLSX failas?",
  "linktitle": "XLSX",
  "menu": {
    "docs": {
      "parent": "spreadsheet",
      "identifier": "spreadsheet-xls-ltx"
}
},
  "lastmod": "2019-12-10"
}

## Kas yra XLSX failas?

**XLSX** is well-known format for Microsoft Excel documents that was introduced by Microsoft with the release of Microsoft Office 2007. Remiantis struktūra, sutvarkyta pagal atvirojo pakavimo konvencijas, kaip nurodyta OOXML standarto ECMA-376 [Part 2](https://www.ecma-international.org/publications-and-standards/standards/ecma-376/), naujas formatas yra ZIP paketas, kuriame yra daug XML failų. Pagrindinę struktūrą ir failus galima išnagrinėti tiesiog išpakavus .xlsx failą.

## Trumpa XLSX failo formato istorija

XLSX file format was introduced in 2007 and uses the Open XML standard adapted by Microsoft back in 2000. Prieš XLSX, įprastas failo formatas buvo [XLS](/spreadsheet/xls/), kuris buvo grynas dvejetainis failo formatas. Naujasis failo tipas prideda mažų failų dydžių, mažesnių sugadinimo pakeitimų ir gerai suformatuotų vaizdų pranašumų. Tai buvo 2000 m. pradžioje, kai Microsoft nusprendė imtis pakeitimų, kad atitiktų **Office Open XML** standartą. Iki 2007 m. šis naujas failo formatas tapo Office 2007 dalimi ir taikomas ir naujose Microsoft Office versijose.

## XLSX failo formato specifikacijos

Oficialią [XLSX file format specifications](https://learn.microsoft.com/en-us/openspecs/office_standards/ms-xlsx/2c5dee00-eff2-4b22-92b6-0738acd4475e) galima rasti internete iš Microsoft. Norėdami pamatyti, kas yra XLSX faile, tiesiog pervardykite jį į [ZIP](/compression/zip/) failą, pakeisdami jo plėtinį, tada išskleiskite jį, kad peržiūrėtumėte šios Excel darbaknygės failus. Tuščioje darbaknygėje, išskleidus ją į failus, yra šie failai ir aplankai.

### [Content_Types].xml ###

Tai vienintelis failas, kuris randamas pagrindiniame lygyje, kai ištraukiamas ZIP failas. Jame pateikiami paketo dalių turinio tipai. Visos nuorodos į pakete esančius XML failus yra pateiktos šiame XML faile.

### \_rels (aplankas) ###

Tai aplankas Ryšiai, kuriame yra vienas XML failas, kuriame saugomi paketo lygio ryšiai. Nuorodos į pagrindines Xlsx failų dalis yra šiame faile kaip URI. Šie URI nustato kiekvienos pagrindinės dalies ryšio su paketu tipą. Tai apima ryšį su pagrindiniu biuro dokumentu, esančiu kaip xl/workbook.xml, ir kitas docProps dalis kaip pagrindines ir išplėstines ypatybes.

### docProps ###

Šiame aplanke yra visos dokumento ypatybės. Tai apima pagrindinių ypatybių rinkinį, išplėstinių arba konkrečiai programai būdingų ypatybių rinkinį ir dokumento miniatiūros peržiūrą. Tuščioje darbaknygėje šiame aplanke yra du failai, ty app.xml ir core.xml. core.xml yra tokia informacija kaip autorius, sukūrimo, išsaugojimo ir modifikavimo data. App.xml yra informacijos apie failo turinį.

### xl (aplankas) ###

Tai pagrindinis aplankas, kuriame yra visa informacija apie darbaknygės turinį. Pagal numatytuosius nustatymus jame yra šie aplankai:

* \_rels

*tema

* darbalapiai


ir šiuos xml failus:

* styles.xml

* darbaknygė.xml


## XLSX formato pavyzdys Nr.


Kiekvienam darbaknygėje esančiam Excel darbalapiui yra vienas XML failas. Šiuos XML failus galite rasti aplanke xl/worksheets. Visa darbalapyje esanti informacija yra suskirstyta į skirtingus XML failo skyrius. Panagrinėkime pavyzdinį darbalapį iš darbaknygės, kuri parodyta kitame paveikslėlyje.

{{< figure src="../XLSX file format.png" alt="XLSX failo formatas" >}}

Kaip matyti, šiame darbalapyje yra langelių A1–B2 turinys ir vaizdas. Be to, ląstelė G13 šiuo metu yra aktyvi darbalapio langelis. Dabar panagrinėkime xl/worksheets/sheet1.xml failą, kad pamatytume, kaip ši informacija pateikiama XML faile. Šio XML failo turinys yra toks, kaip parodyta toliau.

{{< figure src="../XLSX File Format Details.png" alt="XPS failo formatas" >}}

1. Skirtuke pritaikyta temos spalva. Jis paminėtas XML faile su žyma<tabColor> sekant temos ID.
1. Skirtuko Selected reikšmė nustatyta į 1, o tai rodo, kad tai pasirinktas lapas
1. Kaip matyti pirmame paveikslėlyje aukščiau, darbalapio langelis G13 yra aktyvus langelis, kuris taip pat minimas XML faile.
1. Skirtukas sheetData rodo darbalapyje esančius duomenis. Tačiau matote, kad pradinio darbalapio turinio šioje dalyje niekur nėra. Taip yra todėl, kad tekstas netiesiogiai nurodomas iš sharedStrings XML lapo. Šis susiejimas užtikrina, kad kiekvienas tekstas būtų įrašytas tik vieną kartą ir kad būtų galima sutaupyti vietos dar kartą, į jį bus galima kreiptis dar kartą.
1. Vaizdas, kaip matote, yra nurodytas nuorodos ID rId2

## Prisidėti

Norite pasidalyti kažkuo apie XLSX arba skaičiuoklės failų formatus? Savo radinius galite paskelbti skiltyje [Spreadsheet File Format News](https://news.fileformat.com/t/Spreadsheet).

## Nuorodos

* [[MS-XLSX] – XLSX failo formatas](https://learn.microsoft.com/en-us/openspecs/office_standards/ms-xlsx/2c5dee00-eff2-4b22-92b6-0738acd4475e)

* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-xlsx.php)


