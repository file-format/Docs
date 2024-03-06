{
  "date": "2021-09-08",
  "keywords": [
"rel fails",
"rel faila formāts",
"kas ir rel fails",
"failu",
"rel piemērs",
"rel faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par REL faila formātu un API, kas var izveidot un atvērt REL failus.",
  "title": "REL — pārvietojams moduļa fails",
  "linktitle": "REL",
  "menu": {
    "docs": {
      "parent": "game",
      "identifier": "game-re-lvl"
}
},
  "lastmod": "2021-09-08"
}

## Kas ir REL fails?
Failu ar paplašinājumu .rel var izmantot vairākiem mērķiem. Tāpēc spēļu klasifikācijas ziņā tas ir pazīstams kā pārvietojams moduļa fails, ko izmanto dažas Nintendo Wii spēles, piemēram, Brawl, Super Smash Bros un Mario Kart Wii. Tas ietver spēles datus, tostarp rakstzīmju modeļus un posmus. REL faili darbojas līdzīgi kā .DLL faili, ko izmanto Microsoft Windows.

## REL faila formāts
REL faila formātā fails ir sadalīts vairākās sadaļās, kas sagrupētas pēc līdzīgas piekļuves, piemēram, vienā sadaļā tiek lasīti tikai dati, viss izpildāmais kods tiek ievietots citā utt. Fails sākas ar galvenes sadaļu, kam seko:
- Tabula ar sadaļas informāciju.
- sadaļas dati.
- Informācija par pārvietošanu.

### Faila galvene
Fails sākas ar galveni līdz 0x4C baitiem:
| Ofseta | Izmērs | Lauka nosaukums | Apraksts |
--------------------|---------------|-------------------|---------------------------------|
| 0x00 | 4 | id | Arbitrary identification number. Must be unique amongst all RELs used by a game. Must not be 0. |
| 0x04 | 4 | nākamais | Rādītājs uz nākamo moduli, kas aizpildīts izpildlaikā. |
| 0x08 | 4 | iepriekšējā | Rādītājs uz iepriekšējo moduli, kas aizpildīts izpildlaikā. |
| 0x0c | 4 | numSections | Sadaļu skaits failā. |
| 0x10 | 4 | sadaļaInfoNobīde | Nobīde līdz sadaļas tabulas sākumam. |
| 0x14 | 4 | nameOffset | Nobīde uz ASCII virkni, kas satur moduļa nosaukumu. Var būt NULL. Relatīvi pret REL faila sākumu. |
| 0x18 | 4 | nosaukumsIzmērs | Moduļa nosaukuma lielums baitos. |
| 0x1c | 4 | versija | REL faila formāta versijas numurs. |
| 0x20 | 4 | bssIzmērs | Sadaļas .bss lielums. |
| 0x24 | 4 | relOffset | Nobīde uz pārvietošanas tabulu. |
| 0x28 | 4 | impOffset | Nobīde uz imp tabulu. |
| 0x2c | 4 | impSize | imp tabulas lielums baitos. |
| 0x30 | 1 | prologSection | Index into section table which prolog is relative to. Skip if this field is 0. |
| 0x31 | 1 | epilogSection | Index into section table which epilog is relative to. Skip if this field is 0. |
| 0x32 | 1 | unresolvedSection | Index into section table which unresolved is relative to. Skip if this field is 0. |
| 0x33 | 1 | bssSection | Indeksējiet sadaļu tabulā, ar kuru bss ir relatīvs. Aizpildīts izpildlaikā! |
| 0x34 | 4 | prolog | Nobīde norādītajā funkcijas _prolog sadaļā. |
| 0x38 | 4 | epilogs | Nobīde norādītajā funkcijas _epilog sadaļā. |
| 0x3c | 4 | neatrisināts | Nobīde norādītajā funkcijas _unresolved sadaļā. |
| 0x40 | 4 | align | Version ≥ 2 only. Alignment constraint on all sections, expressed as power of 2. |
| 0x44 | 4 | bssAlign | Version ≥ 2 only. Alignment constraint on all '.bss' section, expressed as power of 2. |
| 0x48 | 4 | fixSize | Tikai versija ≥ 3. Ja REL ir saistīts ar OSLinkFixed (nevis OSLink), atstarpi aiz šīs adreses var izmantot citiem mērķiem (piemēram, BSS). |

### Sadaļas informācijas tabula
Sadaļas informācijas tabulā ir **numSections** ieraksti, katrs 0 x 8 baitus garš:
| Ofseta | Izmērs | Apraksts |
-------|------------|-------------|
| 0x0 | 30 biti | Nobīde no REL sākuma līdz sadaļai. Ja tā ir nulle, sadaļa ir neinicializēta sadaļa (ti, .bss). |
| 0x3,6 | 1 bits | Nezināms. |
| 0x3,7 | 1 bits | Izpildāmais karogs; ja tas ir 1, sadaļa ir izpildāma. |
| 0x4 | 4 | Sadaļas garums baitos. Ja tas ir nulle, šis ieraksts tiek izlaists. |
| 0x8 | Nākamais ieraksts | Nākamais ieraksts |

### Pārvietošanas dati
Pārvietošanas dati ir viens vai vairāki 0x8 baitu struktūru saraksti. Katra saraksta beigas ir apzīmētas ar speciālo tipa kodu 203:
| Ofseta | Vārds | Izmērs | Apraksts |
-------|------------|------------|-----|
| 0x0 | kompensēt | 2 | Nobīde baitos no iepriekšējās pārvietošanas uz šo. Ja šī ir pirmā pārvietošana sadaļā, tas attiecas uz sadaļas sākumu. |
| 0x2 | tips | 1 | Pārvietošanas veids. Aprakstīts zemāk. |
| 0x3 | sadaļa | 1 | Simbola sadaļa, pret kuru pārvietoties. Īpašajam pārvietošanas veidam 202 šis ir tās sadaļas numurs šajā failā, uz kuru attiecas šādi pārvietošanas ieraksti. |
| 0x4 | pievienot | 4 | Simbola nobīde baitos, pret kuru pārvietot, attiecībā pret tā sadaļas sākumu. Tā vietā tā ir absolūta adrese pārvietošanai vietnē main.dol. |
| 0x8 | Nākamais ieraksts | Nākamais ieraksts | Nākamais ieraksts |


 



## Atsauces 

* [Relocatable Object Module Format](https://en.wikipedia.org/wiki/Relocatable_Object_Module_Format)



