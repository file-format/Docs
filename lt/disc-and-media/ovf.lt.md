{
  "date": "2021-08-10",
  "keywords": [
".ovf failą",
"Dokumento formatas",
"kas yra .ovf failas",
"failą",
"failo plėtinys"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite, kas yra .ovf failo formatas ir API, kuriomis galima kurti ir atidaryti OVF failus.",
  "title": "OVF failo formatas – atidarykite virtualizacijos failą",
  "linktitle": "OVF",
  "menu": {
    "docs": {
      "parent": "disc-and-media",
      "identifier": "disc-and-media-ov-ltf"
}
},
  "lastmod": "2022-01-03"
}

## Kas yra OVF failas?

OVF failas yra tekstinis failas, kuriame yra informacijos apie programinės įrangos, kuri veikia virtualioje mašinoje, pakavimą ir platinimą. Jis suformatuotas pagal [Open Virtualization Standard Specifications](https://www.dmtf.org/standards/ovf), kuriame aprašomi visi reikalavimai (pvz., sauga, perkeliamumas, efektyvumas ir išplečiamumas), taikomi programoms paleisti virtualiose mašinose. Tarptautinė standartizacijos organizacija (ISO) priėmė OVF kaip ISO 17203 standartą.

## Trumpa OVF failo formato istorija

OVF failo formatą pristatė DMTF (Distributed Management Task Force), kuri sukuria atvirus valdymo standartus. Jis nepriklauso nuo bet kokios konkrečios hipervizoriaus ar instrukcijų rinkinio architektūros. OVF pakete yra viena ar daugiau virtualių sistemų, kurių kiekviena gali būti įdiegta virtualioje mašinoje.

## OVF failo formatas – daugiau informacijos

OVF paketą sudaro keli failai, patalpinti viename kataloge. Tarp jų yra tiksliai vienas OVF deskriptoriaus (su plėtiniu .ovf) failas, saugomas [XML](/web/xml/) failo formatu. Jame aprašoma supakuota virtualios mašinos informacija ir metaduomenų informacija apie OVF paketą, pvz.:

 * vardas
 * techninės įrangos reikalavimus
 * nuorodos į kitus failus OVF pakete ir
 * human-readable descriptions

Kiti failai, kuriuos galima rasti OVF pakete, apima vieną ar daugiau disko vaizdų ir pasirinktinai sertifikatų failus bei kitus pagalbinius failus.

## Nuorodos

* [Open Virtualization Format – DMTF](https://www.dmtf.org/standards/ovf)

* [OVF failo formato specifikacijos](https://www.dmtf.org/sites/default/files/standards/documents/DSP0243_1.1.0.pdf)


