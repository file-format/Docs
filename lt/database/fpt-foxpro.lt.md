{
  "date": "2023-06-12",
  "keywords": [
"fpt",
"fpt failą",
"foxpro fpt failas",
"FoxPro lentelės atmintinė",
"kas yra fpt failas",
"Kaip atidaryti fpt failą",
"failą",
"fpt failo plėtinys",
"pratęsimas"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "FPT failo formatas – „FoxPro Table Memo“.",
  "description": "Sužinokite apie FPT FoxPro formatą ir API, kurios gali kurti ir atidaryti FPT failus.",
  "linktitle": "FPT FoxPro",
  "menu": {
    "docs": {
      "identifier": "database-fpt-foxpro-lt",
      "parent": "database"
}
},
  "lastmod": "2023-06-12"
}

## Kas yra FPT failas?

An "FPT" file is a file extension associated with the FoxPro database management system. In FoxPro, the FPT file contains memo fields associated with a table. Memo fields are used to store large amounts of text or binary data, such as lengthy descriptions, documents, or images, which may not fit in a regular database field.

Štai kaip veikia FoxPro failų struktūra:

– **DBF (duomenų bazės failas):** tai pagrindinis failas, kuriame yra struktūriniai duomenys lentelės formatu, įskaitant įprastus laukus. Kiekvienas įrašas atitinka lentelės eilutę, o kiekvienas įrašo laukas atitinka stulpelį.

- **FPT (atminties failas):** FPT failas naudojamas atmintinės laukams, susietiems su DBF failo įrašais, saugoti. Kiekvienas atmintinės laukas atitinka įrašą DBF faile, o FPT faile saugomas tikrasis atmintinės turinys.

- **CDX (indekso failas):** šiuose failuose saugomi indeksai, kurie pagerina duomenų paiešką ir rūšiavimą DBF faile.

Jei turite FoxPro duomenų bazę su pastabų laukais, kiekvienai lentelei turėtumėte turėti atitinkamus DBF, FPT ir galbūt CDX failus. FPT faile yra dvejetainių duomenų ir jis nėra skirtas atidaryti tiesiogiai naudojant teksto rengyklę. Vietoj to jis pasiekiamas ir valdomas naudojant FoxPro programą arba kitus suderinamus duomenų bazės įrankius.

## Ryšys su FoxPro

FPT failas yra susietas su FoxPro, kuri yra reliacinė duomenų bazių valdymo sistema (DBVS), kurią iš pradžių sukūrė Fox Software, o vėliau įsigijo Microsoft. Yra įvairių versijų, o Visual FoxPro (VFP) yra viena iš labiausiai žinomų. Visual FoxPro buvo galinga ir populiari duomenų bazių valdymo sistema, naudojama kuriant darbalaukio ir kliento-serverio programas.

Pagrindinės Visual FoxPro funkcijos:

– **Lentelinė duomenų saugykla:** leido vartotojams kurti ir tvarkyti struktūrinius duomenis lentelėse su laukais ir įrašais, panašiais į kitas duomenų bazių sistemas.
– **Atmintinių laukų palaikymas:** Visual FoxPro palaiko atmintinės laukus, kuriuose galima saugoti didelius teksto ar dvejetainių duomenų kiekius.
– **Interaktyvi kūrimo aplinka:** turėjo vizualinę kūrimo aplinką, kurioje naudodamiesi grafine sąsaja galite kurti formas, ataskaitas ir programas.
– **SQL palaikymas:** Visual FoxPro palaikoma SQL (struktūrinės užklausos kalba), leidžianti pateikti užklausas ir apdoroti duomenis naudojant standartinę SQL sintaksę.
- **Objektinis programavimas:** Visual FoxPro palaiko objektinį programavimą, kuris leido sukurti daugiau modulinių ir prižiūrimų programų.
– **Indeksavimas ir paieška:** suteikė indeksavimo galimybes, kad būtų galima greičiau ieškoti ir rūšiuoti duomenis.
– **Ataskaitų teikimo įrankiai:** Visual FoxPro įtraukė įrankius ataskaitoms kurti ir generuoti pagal duomenų bazėje saugomus duomenis.
– **Suderinamumas:** leido integruoti su kitais Microsoft produktais ir technologijomis.

Please note that Microsoft ended mainstream support for Visual FoxPro in 2007, and extended support ended in 2015. Tai reiškia, kad nors esamos programos, sukurtos naudojant FoxPro, vis tiek gali veikti, Microsoft nepateikia jokių oficialių naujinimų ar saugos pataisų. Be to, šiuolaikinės plėtros tendencijos pakrypo į žiniatinklio ir debesijos pagrindu veikiančias programas, atsirado naujesnių duomenų bazių valdymo sistemų.

## Kaip atidaryti FPT failą?

Programos, kurios atidaro FPT failus, apima

– Microsoft Visual FoxPro (mokama)

## Kiti FPT failai

- [FPT - Alpha Five Table Memo File](/database/fpt-alphafive/)
- [FPT - FileMaker Pro Database Memo File](/database/fpt/)

## Nuorodos
* [Visual FoxPro](https://en.wikipedia.org/wiki/Visual_FoxPro)


