{
  "date": "2019-10-11",
  "keywords": [
"odp failą",
"odp failo formatas",
"kas yra odp failas",
"failą",
"odp pavyzdys",
"odp failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ODP – OpenOffice pristatymo failo formatas",
  "description": "Sužinokite apie ODP failo formatą ir API, kurios gali kurti ir atidaryti ODP failus.",
  "linktitle": "ODP",
  "menu": {
    "docs": {
      "parent": "presentation",
      "identifier": "presentation-od-ltp"
}
},
  "lastmod": "2019-09-10"
}

## Kas yra ODP failas?

Failai su plėtiniu .odp yra pristatymo failo formatas, kurį OpenOffice.org naudoja OASISOpen standarte. Pateikties failas yra skaidrių rinkinys, kuriame kiekvieną skaidrę gali sudaryti tekstas, vaizdai, formatavimas, animacija ir kita laikmena. Šios skaidrės pateikiamos auditorijai skaidrių demonstravimo pavidalu su pasirinktiniais pristatymo nustatymais. ODP failus galima atidaryti naudojant programas, kurios atitinka OpenDocument formatą (pvz., OpenOffice arba StarOffice).

## Trumpa istorija

ODP failo formato specifikacijos yra pagrįstos standartu, sukurtu kaip ODF specifikacijos. Šios specifikacijos praeityje buvo sukurtos trimis versijomis, kurias sukūrė ir paskelbė OASIS:

2005 – 1.0 versija buvo paskelbta 2005 m. gegužės mėn
2007 – 1.1 versija buvo paskelbta 2007 m. vasario mėn
2011 – 1.2 versija buvo paskelbta 2011 m. rugsėjo mėn

Pereinant nuo ODF 1.0 prie 1.1 versijų buvo gana nedidelių pakeitimų. [ODF 1.2 version](https://www.oasis-open.org/standards#opendocumentv1.2) yra naujausia ODF specifikacijų versija, todėl kūrėjai turėtų pasikonsultuoti su ja, kurdami programas, susijusias su ODS skaitymu/rašymu.

## Failo formato specifikacijos

OpenDocument formatas palaiko dokumento atvaizdavimą kaip vieną XML dokumentą ir kelių antrinių dokumentų rinkinį pakete kaip [ZIP](/compression/zip/) archyvą. Kiekviename faile iš ZIP archyvo saugoma dalis viso dokumento. Kiekviename antriniame dokumente saugomas tam tikras dokumento aspektas. Pavyzdžiui, viename antriniame dokumente yra stiliaus informacija, o kitame – dokumento turinys. Įprastą ODF dokumentą sudaro šie komponentai:

* `content.xml` – dokumento turinys ir turinyje naudojami automatiniai stiliai.

* `styles.xml` – dokumento turinyje naudojami stiliai ir pačiuose stiliuose naudojami automatiniai stiliai.

* `meta.xml` – dokumento metainformacija, pvz., autorius arba paskutinio išsaugojimo veiksmo laikas.

* `settings.xml` – konkrečios programos nustatymai, pvz., lango dydis arba spausdintuvo informacija.


Be šių, pakete gali būti daug kitų antrinių dokumentų, tokių kaip dokumento miniatiūra, vaizdai ir kt.

Skaičiuoklės dokumentų failai yra ODF failų poaibis, kuriame turinys (lapai) saugomas subdokumente content.xml.

## Nuorodos

* [OpenDocument – Vikipedija](https://en.wikipedia.org/wiki/OpenDocument)


