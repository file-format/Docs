{
  "date": "2021-09-08",
  "keywords": [
"rel fil",
"rel filformat",
"hvad er en rel fil",
"fil",
"rel eksempel",
"rel filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om REL-filformat og API'er, der kan oprette og åbne REL-filer.",
  "title": "REL - Relocatable Module File",
  "linktitle": "REL",
  "menu": {
    "docs": {
      "parent": "game",
      "identifier": "game-re-dal"
}
},
  "lastmod": "2021-09-08"
}

## Hvad er en REL fil?
En fil med filtypenavnet .rel kan bruges til flere slags formål. Derfor er det med hensyn til spilklassificering kendt som en flytbar modulfil, der bruges af nogle Nintendo Wii-spil, såsom Brawl, Super Smash Bros og Mario Kart Wii. Det omfatter gameplay-data, inklusive karaktermodeller og stadier. REL-filer fungerer på samme måde som .DLL-filer, der bruges af Microsoft Windows.

## REL filformat
I et REL-filformat er filen opdelt i flere sektioner, grupperet efter lignende adgang, f.eks. læsedata i én sektion, al eksekverbar kode placeres i en anden osv. Filen starter med en header-sektion, efterfulgt af:
- Tabel med sektionsinfo.
- Sektionsdataene.
- Flytteoplysninger.

### Filoverskrift
Filen starter med en header på op til 0x4C bytes:
| Offset | Størrelse | Feltnavn | Beskrivelse |
--------------------|---------------|-------------------|---------------------------------|
| 0x00 | 4 | id | Arbitrary identification number. Must be unique amongst all RELs used by a game. Must not be 0. |
| 0x04 | 4 | næste | Pointer til næste modul, udfyldt ved kørsel. |
| 0x08 | 4 | forrige | Pointer til forrige modul, udfyldt under kørsel. |
| 0x0c | 4 | antalSektioner | Antal sektioner i filen. |
| 0x10 | 4 | sectionInfoOffset | Offset til starten af sektionstabellen. |
| 0x14 | 4 | navnOffset | Offset til ASCII-streng, der indeholder navnet på modulet. Kan være NULL. I forhold til starten af REL-fil. |
| 0x18 | 4 | navnestørrelse | Modulnavnets størrelse i bytes. |
| 0x1c | 4 | version | Versionsnummer for REL-filformatet. |
| 0x20 | 4 | bssStørrelse | Størrelsen på '.bss'-sektionen. |
| 0x24 | 4 | relOffset | Offset til flyttetabellen. |
| 0x28 | 4 | impOffset | Offset til imp-tabel. |
| 0x2c | 4 | impSize | Størrelse af imp-tabellen i bytes. |
| 0x30 | 1 | prologSection | Index into section table which prolog is relative to. Skip if this field is 0. |
| 0x31 | 1 | epilogSection | Index into section table which epilog is relative to. Skip if this field is 0. |
| 0x32 | 1 | unresolvedSection | Index into section table which unresolved is relative to. Skip if this field is 0. |
| 0x33 | 1 | bssSektion | Indeks i sektionstabel, som bss er i forhold til. Fyldt på køretid! |
| 0x34 | 4 | prolog | Offset til specificeret sektion af _prolog-funktionen. |
| 0x38 | 4 | epilog | Offset til specificeret sektion af _epilog-funktionen. |
| 0x3c | 4 | uafklaret | Offset til specificeret sektion af _unresolved-funktionen. |
| 0x40 | 4 | align | Version ≥ 2 only. Alignment constraint on all sections, expressed as power of 2. |
| 0x44 | 4 | bssAlign | Version ≥ 2 only. Alignment constraint on all '.bss' section, expressed as power of 2. |
| 0x48 | 4 | fixSize | Kun version ≥ 3. Hvis REL er forbundet med OSLinkFixed (i stedet for OSLink), kan pladsen efter denne adresse bruges til andre formål (såsom BSS). |

### Sektionsinfotabel
Sektionsinformationstabellen indeholder **numSections**-indgange hver 0x8 bytes lang:
| Offset | Størrelse | Beskrivelse |
-------|------------|-------------|
| 0x0 | 30 bits | Offset fra begyndelsen af REL til sektionen. Hvis dette er nul, er sektionen en ikke-initialiseret sektion (dvs. .bss). |
| 0x3,6 | 1 bit | Ukendt. |
| 0x3,7 | 1 bit | Eksekverbart flag; hvis dette er 1, er sektionen eksekverbar. |
| 0x4 | 4 | Længde i bytes af sektionen. Hvis dette er nul, springes denne post over. |
| 0x8 | Næste post | Næste post |

### Flyttedata
Flyttedataene er en eller flere lister med 0x8 byte-strukturer. Slutningen af hver liste er markeret med den særlige typekode 203:
| Offset | Navn | Størrelse | Beskrivelse |
-------|------------|------------|-----|
| 0x0 | forskydning | 2 | Offset i bytes fra den forrige flytning til denne. Hvis dette er første flytning i afsnittet, er dette i forhold til afsnitsstart. |
| 0x2 | type | 1 | Flyttetypen. Beskrevet nedenfor. |
| 0x3 | afsnit | 1 | Den del af symbolet, der skal flyttes imod. For den særlige flyttetype 202 er dette i stedet nummeret på den sektion i denne fil, som følgende flytteposter gælder for. |
| 0x4 | tilføje | 4 | Forskydning i bytes af symbolet, der skal flyttes imod, i forhold til starten af dets sektion. Dette er en absolut adresse i stedet for flytninger mod main.dol. |
| 0x8 | Næste post | Næste post | Næste post |


 



## Referencer 

* [Relocatable Object Module Format](https://en.wikipedia.org/wiki/Relocatable_Object_Module_Format)



