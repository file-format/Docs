{
  "date": "2021-08-29",
  "keywords": [
"ade",
"pratęsimas",
"failą",
"Dokumento formatas",
"Duomenų bazės failo tipas",
"Duomenų bazės failo formatas",
"Microsoft Access."
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie ADE failo formatą ir API, kurios gali kurti ir atidaryti ADE failus.",
  "title": "ADE – prieiga prie projekto plėtinio failo",
  "linktitle": "ADE",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-ad-lte"
}
},
  "lastmod": "2021-08-29"
}

## Kas yra ADE failas?

Failas su plėtiniu .ade yra Microsoft Access Project failas, kuriame yra sukompiliuota Microsoft Access ADP projekto faile esančios informacijos išvestis. Informacija, esanti Access projekto faile, išskyrus Visual Basic for Applications (VBA), pateikiama ADE failuose. Duomenys šiuose failuose saugomi suspaustu formatu, siekiant sumažinti failo dydį ir pagerinti Access našumą. Kadangi ADE yra sukompiliuota Access projekto failo išvestis, bet koks VBA šaltinio kodas, kuris yra projekto dalis, išlieka apsaugotas neleidžiant jam būti išvesties dalimi. ADE failus galima atidaryti naudojant Microsoft Access 365.

## ADE failo formatas – daugiau informacijos

ADE yra sudaryti prieigos duomenų bazės failai, kurie saugomi diske kaip dvejetainiai failai. Šių failų vidinė failų struktūra nežinoma.

The ADE files can create issues in opening based on the version of Microsoft Access that has been used to create these files. Access databases that are using the 64-bit version of Microsoft Access 2010 and that are compiled as MDE, [ACCDE](/database/accde/), or ADE files have to be recompiled in Microsoft Access 2021 Service Pack 1 (SP1) to work correctly with Access 2010 SP1. Ši problema kyla dėl to, kad Access 2010 SP1 naudoja naujesnę VBE7.dll failo versiją (7.00.1619 versiją).

## Nuorodos

* [Problema dėl Access ADE failų](https://learn.microsoft.com/en-us/office/troubleshoot/access/error-run-compiled-mde-accde-ade)

* [Kurius prieigos failų formatus naudoti] (https://support.microsoft.com/en-us/office/which-access-file-format-should-i-use-012d9ab3-d14c-479e-b617-be66f9070b41)


