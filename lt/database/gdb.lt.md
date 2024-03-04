{
  "date": "2022-05-08",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "GDB failo formatas – ESRI failo geoduomenų bazės failas",
  "description": "Sužinokite apie GDB failo formatą ir API, kurios gali kurti ir atidaryti GDB failus.",
  "linktitle": "GDB",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-gd-ltb"
}
},
  "lastmod": "2022-05-08"
}

## Kas yra GDB failas?

ESRI failo geoduomenų bazė (FileGDB) yra failų rinkinys disko aplanke, kuriame yra susiję geoerdviniai duomenys, pvz., objektų duomenų rinkiniai, elementų klasės ir susijusios lentelės. Tam, kad jis veiktų, tam tikrus kitus failus reikia laikyti kartu su .gdb failu tame pačiame kataloge. Užklausos gali būti vykdomos .gdb faile, kad būtų galima tvarkyti erdvinius ir neerdvinius duomenis.

## GDB failo formatas – daugiau informacijos

Failų geoduomenų bazės sudarytos iš septynių sistemos lentelių ir vartotojo duomenų. Vartotojo duomenys gali būti saugomi šių tipų duomenų rinkiniuose:

* Funkcijų klasė

* Funkcijų duomenų rinkinys

* Mozaikos duomenų rinkinys

* Rastrinis katalogas

* Rastrinis duomenų rinkinys

* Scheminis duomenų rinkinys

* Lentelė (neerdvinė)

* Įrankių dėžės


Funkcijų duomenų rinkiniuose gali būti funkcijų klasių ir šių tipų duomenų rinkinių:

* Priedai

* Su funkcija susieta anotacija

* Geometriniai tinklai

* Tinklo duomenų rinkiniai

* Siuntiniai audiniai

* Santykių pamokos

* Reljefai

* Topologijos


Numatytasis maksimalus duomenų rinkinių dydis failų geoduomenų bazėse yra 1 TB. Didžiausias dydis gali būti padidintas iki 256 TB dideliems duomenų rinkiniams (dažniausiai rastriniams). Tai valdoma konfigūracijos raktiniu žodžiu. Norėdami gauti daugiau informacijos, žr. failų geoduomenų bazių konfigūravimo raktažodžius.

Failų geoduomenų bazėse taip pat gali būti potipių ir domenų, jose gali būti atliekama patikros / prisiregistravimo replikacija ir vienpusės kopijos.

Failų geoduomenų bazę vienu metu gali pasiekti keli vartotojai. Jei vartotojai redaguoja, jie turi redaguoti skirtingus duomenų rinkinius.

## GDB failo formato specifikacijos ##

Failas GDB yra ESRI patentuotas formatas ir jo specifikacijos nėra viešai prieinamos. Dėl šios priežasties failo GDB failo formato duomenys negalėjo būti dokumentuojami niekur kitur, išskyrus kai kuriuos šaltinius, kurie tai padarė [partially](https://github.com/rouault/dump_gdbtable/wiki/FGDB-Spec) taikant atvirkštinę inžineriją.

## Nuorodos Nr.

* [FGDB specifikacijos](https://github.com/rouault/dump_gdbtable/wiki/FGDB-Spec)


