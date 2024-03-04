{
  "date": "2019-10-11",
  "keywords": [
"fodg failą",
"fodg failo formatas",
"kas yra fodg failas",
"failą",
"fodg pavyzdys",
"fodg failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "FODG – „OpenDocument“ piešinio failo formatas",
  "description": "Sužinokite apie FODG failo formatą ir API, kurios gali kurti ir atidaryti FODG failus.",
  "linktitle": "FODG",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-fod-ltg"
}
},
  "lastmod": "2019-09-10"
}

## Kas yra FODG failas?

Failas su plėtiniu .fodg yra Apache OpenOffice Drawing failo formatas, skirtas piešimo elementams saugoti. Jis pagrįstas failo formato specifikacijomis, nurodytomis Struktūrinės informacijos standartų pažanga (OASIS). Kitas panašus OpenOffice grafikos failo formatas yra [ODG](/image/odg/), kuriame piešimo elementai saugomi kaip vektorinis vaizdas. FODG failus galima atidaryti naudojant OpenOffice ir LibreOffice. Kiti OpenOffice palaikomi failų formatai, pavyzdžiui, yra [ODT](/word-processing/odt/), ODF, [ODP](/presentation/odp/) ir [ODS](/spreadsheet/ods/).

## FODG failo formatas

FODG is based on the OpenDocument's XML file format that conforms to OASIS OpenDocument Format ISO/IEC 26300. Jis turi internetinės medijos tipo programą/vnd.oasis.opendocument.graphics ir taip pat atitinka org.oasis-open.opendocument public.composite-content. XML struktūra yra bendra visiems dokumentų tipams, pvz., skaičiuoklėms, piešimo failams ir tekstiniams dokumentams. OpenOffice dokumentai naudojasi problemų atskyrimo pranašumais, atskirdami turinį, stilius, metaduomenis ir programos parametrus į keturis atskirus XML failus.

`<office:document-content> ` – dokumento turinys ir turinyje naudojami automatiniai stiliai.
`<office:document-styles> ` – dokumento turinyje naudojami stiliai ir pačiuose stiliuose naudojami automatiniai stiliai.
`<office:document-meta>` - Document meta information, such as the author or the time of the last save action.
`<office:document-settings> ` – konkrečios programos nustatymai, pvz., lango dydis arba spausdintuvo informacija.

## Nuorodos Nr.
 * [Future Specifications for v 1.3 Standardization ](https://docs.oasis-open.org/office/OpenDocument/v1.3/cs01/OpenDocument-v1.3-cs01.zip)
 * [OASIS Open Document Format for Office Applications](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=office)
 * [OpenDocument formatas – Vikipedija](https://en.wikipedia.org/wiki/OpenDocument)

