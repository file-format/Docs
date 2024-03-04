{
  "date": "2020-11-11",
  "keywords": [
"NDF",
"pratęsimas",
"failą",
"Dokumento formatas",
"Duomenų bazės failo tipas",
"Duomenų bazės failo formatas",
"Duomenų bazės failai"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie MDF failo formatą ir API, kurios gali kurti ir atidaryti NDF failus.",
  "title": "NDF failo formatas – SQL serverio pagrindinės duomenų bazės failas",
  "linktitle": "NDF",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-nd-ltf"
}
},
  "lastmod": "2020-08-12"
}

## Kas yra NDF failas?

Failas su plėtiniu .ndf yra antrinis duomenų bazės failas, naudojamas [Microsoft SQL Server](https://en.wikipedia.org/wiki/Microsoft_SQL_Server) vartotojo duomenims saugoti. NDF yra antrinis saugojimo failas, nes SQL serveris saugo vartotojo nurodytus duomenis pirminiame saugojimo faile, žinomame kaip [MDF](/database/mdf/). NDF duomenų failas yra neprivalomas ir yra vartotojo apibrėžtas, kad būtų galima tvarkyti duomenų saugyklą, jei pirminis MDF failas naudoja visą skirtą vietą. Paprastai jis saugomas atskirame diske ir gali plisti į kelis saugojimo įrenginius. Norint atidaryti NDF failus, būtina turėti MDF failus.

## NDF failo formatas

NDF failo formatas nesiskiria nuo [MDF](/database/mdf/) ir naudoja puslapius kaip pagrindinį duomenų saugojimo vienetą. kiekvienas puslapis prasideda 96 baitų antrašte, kuri apima:

 * Puslapio ID
 * Struktūros tipas
 * Įrašų skaičius puslapiuose
 * Rodikliai į ankstesnius ir kitus puslapius

### NDF failo struktūra

MDF failo duomenų struktūra yra tokia.

 * 0 puslapis: antraštė
 * 1 puslapis: pirmasis PFS
 * 2 puslapis: pirmasis GAM
 * 3 puslapis: pirmasis SGAM
 * 4 puslapis: nenaudotas
 * 5 puslapis: nenaudotas
 * 6 puslapis: pirmasis DCM
 * 7 puslapis: pirmasis BCM

#### NDF failo antraštė

Visų failų puslapyje 0 yra antraštė, kurioje saugomi failo metaduomenys.

#### Laisva puslapio vieta (PFS)
PFS nustato paskirstymo būseną ir nustato laisvos vietos kiekį.

 * 1 bitas: nurodo, ar puslapis priskirtas, ar ne.
 * 2 bitas: nurodo, ar puslapis yra įvairaus masto.
 * 3 bitas: nurodo, kad šis puslapis yra IAM puslapis.
 * 4 bitas: nurodo, kad šiame puslapyje yra vaiduoklio įrašų
 * 5–7 bitai: kombinuota trijų bitų reikšmė, nurodanti puslapio pilnumą:
   * 0: puslapis tuščias
   * 1: puslapis užpildytas 1–50 %
   * 2: puslapis užpildytas 51–80 %
   * 3: puslapis užpildytas 81–95 %
   * 4: puslapis užpildytas 96–100 %

## Duomenų failo puslapis

SQL serverio duomenų failo puslapiai prasideda nuo nulio (0) ir nuosekliai didėja. Kiekvienas failas atpažįstamas pagal unikalų failo ID numerį. Failo ID ir puslapio numerio pora unikaliai identifikuoja puslapį duomenų bazėje. Puslapių numerių duomenų bazėje pavyzdys yra toks, kaip šiame paveikslėlyje.

{{< figure src="../ndf.png" alt="NDF duomenų bazės failo formatas" >}}

Šiame pavyzdyje rodomi puslapių numeriai duomenų bazėje, kurioje yra 4 MB pirminis duomenų failas ir 1 MB antrinis duomenų failas.

## Nuorodos

 * [Duomenų bazių failai ir failų grupės](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-files-and-filegroups?view=sql-server-ver16)
 * [Duomenų bazės atskyrimas ir pridėjimas – SQL serveris](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-detach-and-attach-sql-server?view=sql-server- 15 versija)
 * [SQL serverio duomenų failo anatomijos analizė](https://blog.pythian.com/analyzing-sql-server-data-file-anatomy/)

