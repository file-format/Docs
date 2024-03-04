{
  "date": "2020-11-11",
  "keywords": [
"MDF",
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
  "description": "Sužinokite apie MDF failo formatą ir API, kurios gali kurti ir atidaryti MDF failus.",
  "title": "MDF failo formatas – SQL serverio pagrindinės duomenų bazės failas",
  "linktitle": "MDF",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-md-ltf"
}
},
  "lastmod": "2020-08-12"
}

## Kas yra MDF failas?

Failas su plėtiniu .mdf yra pagrindinis duomenų bazės failas, kurį [Microsoft SQL Server](https://en.wikipedia.org/wiki/Microsoft_SQL_Server) naudoja vartotojo duomenims saugoti. Tai labai svarbu, nes visi duomenys yra saugomi šiame faile. MDF failas saugo vartotojų duomenis reliacinėse duomenų bazėse formos stulpeliuose, eilutėse, laukuose, indeksuose, rodiniuose ir lentelėse. SQL serveris leidžia nustatyti automatinio augimo ir automatinio susitraukimo parametrus, kad būtų teigiamas poveikis duomenų bazės veikimui. MDF failus galima įkelti ir pridėti prie duomenų bazės naudojant Microsoft SQL Server. MDF failai turi programos / okteto srauto mime tipą.

## MDF failo formatas

Pagrindinis duomenų saugojimo vienetas SQL Server yra puslapis. Duomenų bazei priskirtas saugojimo puslapis yra padalintas į loginius puslapius, numeruojamus nuo 0 iki n. Vienas puslapis prasideda 96 baitų antrašte, kurią sudaro puslapio ID, struktūros, kuriai puslapis priklauso, tipas, įrašų skaičius puslapyje ir rodyklės į ankstesnį ir kitą puslapius.

### Failo struktūra

MDF failo duomenų struktūra yra tokia.

 * 0 puslapis: antraštė
 * 1 puslapis: pirmasis PFS
 * 2 puslapis: pirmasis GAM
 * 3 puslapis: pirmasis SGAM
 * 4 puslapis: nenaudotas
 * 5 puslapis: nenaudotas
 * 6 puslapis: pirmasis DCM
 * 7 puslapis: pirmasis BCM

#### Failo antraštė

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

## Nuorodos

 * [Duomenų bazių failai ir failų grupės](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-files-and-filegroups?view=sql-server-ver15)
 * [Duomenų bazės atskyrimas ir pridėjimas – SQL serveris](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-detach-and-attach-sql-server?view=sql-server- 15 versija)
 * [SQL serverio duomenų failo anatomijos analizė](https://blog.pythian.com/analyzing-sql-server-data-file-anatomy/)

