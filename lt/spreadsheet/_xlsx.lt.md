{
  "date": "2019-12-10",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Jūsų failo formato vadovas, kad sužinotumėte, kas yra _XLSX failas ir API, kurios gali kurti ir atidaryti _XLSX failus.",
  "title": "Kas yra _XLSX failas?",
  "linktitle": "_XLSX",
  "menu": {
    "docs": {
      "parent": "spreadsheet",
      "identifier": "spreadsheet-_xls-ltx"
}
},
  "lastmod": "2021-11-22"
}

## Kas yra _XLSX failas?

Failas su plėtiniu .\_xlsx iš tikrųjų yra [XLSX](/spreadsheet/xlsx/) failas, kurį pervardija kokia nors kita programa. Taip gali nutikti tam tikrais atvejais, kai failo pavadinime yra . failo pavadinimo pabaigoje. \_XLSX failus galima atidaryti Microsoft Excel, panašiai kaip XLSX failus, dar kartą pervardijant juos į .xlsx plėtinį.

## _XLSX failo formatas – daugiau informacijos

The _XLSX files are no different than the XLSX files and use the Open XML standard adopted by Microsoft back in 2000. Prieš XLSX [XLS](/spreadsheet/xls/) buvo pagrindinis failo formatas, naudojamas dirbant su Excel skaičiuoklėmis, siekiant išsaugoti dokumentus dvejetainiu formatu. Šis naujas XML pagrįstas failo formatas turėjo tokius privalumus, kaip mažas failų dydis, atsparumas failų sugadinimui ir gerai suformatuotas vaizdų atvaizdavimas. Šis naujas XML pagrįstas failo formatas tapo Office 2007 dalimi ir vykdomas ir naujose Microsoft versijose.

## \_XLSX failo formato specifikacijos

Kadangi \_XLSX failas yra XLSX failas, pervardytas, jo specifikacijos yra tokios pat kaip ir originalus failas. Tai tik archyvo failas, pagrįstas [ZIP](/compression/zip/) archyvinio failo formatu. Jei norite matyti šio archyvo turinį, tiesiog pervardykite failą į .zip plėtinį ir išskleiskite jį, kad peržiūrėtumėte šios Excel darbaknygės failus. Tuščioje darbaknygėje, išskleidus ją į failus, yra šie failai ir aplankai.

### [Content_Types].xml

Tai vienintelis failas, kuris randamas pagrindiniame lygyje, kai ištraukiamas ZIP failas. Jame pateikiami paketo dalių turinio tipai. Visos nuorodos į pakete esančius XML failus yra pateiktos šiame XML faile.

### \_rels (aplankas)

Tai aplankas Ryšiai, kuriame yra vienas XML failas, kuriame saugomi paketo lygio ryšiai. Nuorodos į pagrindines Xlsx failų dalis yra šiame faile kaip URI. Šie URI nustato kiekvienos pagrindinės dalies ryšio su paketu tipą. Tai apima ryšį su pagrindiniu biuro dokumentu, esančiu kaip xl/workbook.xml, ir kitas docProps dalis kaip pagrindines ir išplėstines ypatybes.

### docProps

Šiame aplanke yra visos dokumento ypatybės. Tai apima pagrindinių ypatybių rinkinį, išplėstinių arba konkrečiai programai būdingų ypatybių rinkinį ir dokumento miniatiūros peržiūrą. Tuščioje darbaknygėje šiame aplanke yra du failai, ty app.xml ir core.xml. core.xml yra tokia informacija kaip autorius, sukūrimo, išsaugojimo ir modifikavimo data. App.xml yra informacijos apie failo turinį.

### xl (aplankas)

Tai pagrindinis aplankas, kuriame yra visa informacija apie darbaknygės turinį. Pagal numatytuosius nustatymus jame yra šie aplankai:

* \_rels

*tema

* darbalapiai


ir šiuos xml failus:

* styles.xml

* darbaknygė.xml


## Nuorodos

* [MS-XLSX – .xlsx failo formatas](https://msdn.microsoft.com/en-us/library/dd922181(v#office.12).aspx)

* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-xlsx.php)


