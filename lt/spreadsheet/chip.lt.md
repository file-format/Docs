{
  "date": "2023-03-01",
  "keywords": [
"lusto failas",
"kas yra lusto failas",
"failą",
"kaip atidaryti lusto failą",
"lusto failo plėtinys",
"pratęsimas"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "CHIP failo formatas – Microarray anotacijos failas",
  "description": "Sužinokite apie CHIP failo formatą ir API, kurios gali kurti ir atidaryti CHIP failus.",
  "linktitle": "CHIP",
  "menu": {
    "docs": {
      "identifier": "spreadsheet-chip-lt",
      "parent": "spreadsheet"
}
},
  "lastmod": "2023-03-01"
}

## Kas yra CHIP failas?

CHIP failas yra mikromasyvo anotacijos failas ir yra susijęs su genų rinkinio praturtinimo analizės (GSEA) programine įranga. GSEA yra skaičiavimo metodas, kuriuo įvertinama, ar iš anksto nustatytas genų rinkinys (genų rinkinys) rodo statistiškai reikšmingus skirtumus tarp dviejų biologinių būsenų, pvz., sveikų ir sergančių audinių arba vaistais apdorotų ir neapdorotų ląstelių. Norint atlikti GSEA, reikia genų ekspresijos duomenų rinkinio ir genų rinkinio duomenų bazės. Genų rinkinio duomenų bazėje yra informacijos apie genų rinkiniuose esančius genus, pvz., jų funkciją, kelią ar specifinę audinių raišką.

A CHIP file is a specific type of gene set database that is used by GSEA. It contains information about the genes and gene sets that are relevant to the microarray platform being used in the experiment. The CHIP file provides annotations for each probe on the microarray, such as the gene symbol, gene name, gene description, and chromosomal location. This information is used to match the probes with the genes in the gene expression dataset and to assign them to the appropriate gene sets for GSEA analysis.

Norėdami naudoti CHIP failą GSEA, turite jį importuoti į programinę įrangą ir susieti su savo mikromasyvų duomenų rinkiniu. GSEA palaiko įvairias mikromasyvų platformas ir daugeliui jų teikia iš anksto sukurtus CHIP failus. Tačiau taip pat galite sukurti savo CHIP failą naudodami anotacijų duomenų bazes iš išorinių šaltinių, tokių kaip NCBI arba Ensembl.

## Daugiau informacijos

CHIP failas nėra skaičiuoklė, tačiau jį galima atidaryti ir redaguoti skaičiuoklių programoje, pvz., Microsoft Excel arba Google Sheets. CHIP failas yra tam tikro tipo tekstinis failas, kuriame yra skirtukais atskirtų duomenų, kuriuos galima lengvai importuoti į skaičiuoklės programą, kad būtų galima peržiūrėti ir redaguoti.

Skaičiuoklės programoje galite manipuliuoti CHIP failo duomenimis, kad pridėtumėte, pašalintumėte arba keistumėte anotacijas apie genus ir genų rinkinius mikromasyvoje. Pavyzdžiui, galite naudoti skaičiuoklės programą, kad pridėtumėte pasirinktines anotacijas genams, kurie neįtraukti į pradinį CHIP failą, arba sujungtumėte kelis CHIP failus iš skirtingų šaltinių į vieną failą.

Tačiau svarbu pažymėti, kad CHIP failas turi tam tikrą formatą ir struktūrą, kuri turi būti palaikoma, kad būtų suderinama su GSEA programine įranga. Jei modifikuojate CHIP failo turinį skaičiuoklės programoje, turėtumėte įsitikinti, kad pakeitimai nepakeis failo formato ar turinio taip, kad galėtų turėti įtakos GSEA analizės tikslumui ar galiojimui.

## Kaip atidaryti CHIP failą?

Kadangi CHIP faile yra skirtukais atskirtų duomenų, taigi, jei norite peržiūrėti skaičiuoklės duomenis, galite juos atidaryti Microsoft Excel.

## Nuorodos
* [GSEA](https://en.wikipedia.org/wiki/Gene_set_enrichment_analysis)
