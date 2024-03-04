{
  "date": "2019-12-10",
  "keywords": [
"ODS",
"failą",
"pratęsimas",
"Dokumento formatas",
"OpenDocument skaičiuoklė"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Jūsų failo formato vadovas, kad sužinotumėte, kas yra ODS failas ir API, kurios gali juos sukurti ir atidaryti.",
  "title": "Kas yra ODS failas? ",
  "linktitle": "ODS",
  "menu": {
    "docs": {
      "parent": "spreadsheet",
      "identifier": "spreadsheet-od-lts"
}
},
  "lastmod": "2019-12-10"
}

## Kas yra ODS failas?

Failai su plėtiniu .ods reiškia OpenDocument Spreadsheet Document formatą, kurį gali redaguoti vartotojas. Duomenys saugomi ODF faile į eilutes ir stulpelius. Tai XML pagrįstas formatas ir yra vienas iš kelių atvirų dokumentų formatų (ODF) šeimos potipių. Formatas nurodytas kaip OASIS paskelbtų ir prižiūrimų ODF 1.2 specifikacijų dalis. Kai kurios Windows programos ir kitos operacinės sistemos gali atidaryti ODS failus redaguoti ir valdyti, įskaitant Microsoft Excel, NeoOffice ir LibreOffice. ODS failus taip pat galima konvertuoti į kitus skaičiuoklių formatus, taip pat kaip [XLS](/spreadsheet/xls/), [XLSX](/spreadsheet/xlsx/) ir kitus, naudojant skirtingas programas.

## Trumpa istorija ##

ODS failo formato specifikacijos yra pagrįstos standartu, sukurtu kaip ODF specifikacijos. Šios specifikacijos praeityje buvo sukurtos trimis versijomis, kurias sukūrė ir paskelbė OASIS:

2005 – 1.0 versija buvo paskelbta 2005 m. gegužės mėn

2007 – 1.1 versija buvo paskelbta 2007 m. vasario mėn

2011 – 1.2 versija buvo paskelbta 2011 m. rugsėjo mėn

Pereinant nuo ODF 1.0 prie 1.1 versijų buvo gana nedidelių pakeitimų. [ODF 1.2 version](https://www.oasis-open.org/standards#opendocumentv1.2) yra naujausia ODF specifikacijų versija, todėl kūrėjai turėtų konsultuotis dėl programų, susijusių su ODS skaitymu / rašymu, kūrimo.

## ODS failo formatas ##

OpenDocument formatas palaiko dokumento vaizdavimą kaip vieną XML dokumentą ir kelių antrinių dokumentų rinkinį pakete kaip [ZIP](/compression/zip/) archyvą. Kiekviename faile iš ZIP archyvo saugoma dalis viso dokumento. Kiekviename antriniame dokumente saugomas tam tikras dokumento aspektas. Pavyzdžiui, viename antriniame dokumente yra stiliaus informacija, o kitame – dokumento turinys. Įprastą ODF dokumentą sudaro šie komponentai:

* `content.xml` – dokumento turinys ir turinyje naudojami automatiniai stiliai.

* `styles.xml` – dokumento turinyje naudojami stiliai ir pačiuose stiliuose naudojami automatiniai stiliai.

* `meta.xml` – dokumento metainformacija, pvz., autorius arba paskutinio išsaugojimo veiksmo laikas.

* `settings.xml` – konkrečios programos nustatymai, pvz., lango dydis arba spausdintuvo informacija.


Be šių, pakuotėje gali būti daug kitų antrinių dokumentų, tokių kaip dokumento miniatiūra, vaizdai ir kt.

Skaičiuoklės dokumentų failai yra ODF failų poaibis, kuriame turinys (lapai) saugomas subdokumente content.xml.

## Nuorodos Nr.

* [OpenDocument – Vikipedija](https://en.wikipedia.org/wiki/OpenDocument)


