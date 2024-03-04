{
  "date": "2019-12-12",
  "keywords": [
"SQLite",
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
  "description": "Sužinokite apie SQLITE failo formatą ir API, kurios gali kurti ir atidaryti SQLITE failus.",
  "title": "SQLite failo formatas",
  "linktitle": "SQLITE",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-sqlit-lte"
}
},
  "lastmod": "2020-11-09"
}

## Kas yra SQLite failas?

Failas su plėtiniu .sqlite yra lengvas SQL duomenų bazės failas, sukurtas naudojant [SQLite](https://www.sqlite.org/index.html) programinę įrangą. Tai yra duomenų bazė pačiame faile ir įgyvendina savarankišką, visas funkcijas turintį, labai patikimą [SQL](/database/sql/) duomenų bazės variklį. SQLite duomenų bazės failus galima naudoti norint dalytis turtingu turiniu tarp sistemų, paprasčiausiai keičiantis šiais failais tinkle. Beveik visi mobilieji telefonai ir kompiuteriai naudoja SQLite duomenims saugoti ir dalytis, o tai yra failo formato pasirinkimas kelių platformų programoms. Dėl kompaktiško naudojimo ir lengvo naudojimo jis pateikiamas kartu su kitomis programomis. SQLite susiejimas egzistuoja tokioms programavimo kalboms kaip C, [C#](/programming/cs/), [C++](/programming/cpp/), [Java](/programming/java/), [PHP](/programming/php/) ir daugeliui kitų.

## SQLite failo formatas

SQLite iš tikrųjų yra C kalbos biblioteka, kuri įgyvendina SQLite RDBMS naudodama SQLite failo formatą. Kasdien tobulėjant naujiems įrenginiams, jo failo formatas buvo suderinamas atgal, kad tilptų senesni įrenginiai. SQLite failo formatas laikomas ilgalaikiu duomenų archyvo formatu.

### Duomenų bazės failas

SQLite duomenų bazė visiškai palaikoma naudojant du failus.
 * Pagrindinės duomenų bazės failas – yra visa SQLite duomenų bazės būsena
 * Atšaukimo žurnalas – papildoma informacija saugoma antrame faile ir naudojama atliekant operacijas. Jei SQLite veikia WAL režimu, išlaikomas rašymo galvutės žurnalo failas.

#### Žurnalo failas

Šis failas skirtas saugoti visą informaciją, kuri saugoma, jei paskutinės operacijos nepavyktų užbaigti, pavyzdžiui, kompiuterio gedimo atveju. Šis failas naudojamas atkurti duomenų bazės failo nuoseklią būseną.

#### Puslapiai

Pagrindinis SQLite duomenų bazės failas susideda iš vieno ar daugiau puslapių. Bet kuriuo metu kiekvienas pagrindinės duomenų bazės puslapis yra naudojamas vieną kartą, ty vienu iš šių:

 * Užrakinimo baitų puslapis
 * Nemokamo sąrašo puslapis
   * Nemokamo sąrašo magistralinis puslapis
   * Nemokamo sąrašo lapų puslapis
 * B formos medžio puslapis
   * Stalo b-medžio interjero puslapis
   * Lentelės b-medžio lapų puslapis
   * Indekso b-medžio vidinis puslapis
   * Indekso b formos medžio lapų puslapis
 * Naudingojo krovinio perpildymo puslapis
 * Žymeklio žemėlapio puslapis

SQLite duomenų bazės failų dydis gali svyruoti nuo kelių kilobaitų iki kelių gigabaitų.

### SQLite antraštė

The SQLite database header is located in the first 100 bytes of the database file. Every valid SQLite database file starts with 16 bytes (in hex):53 51 4c 69 74 65 20 66 6f 72 6d 61 74 20 33 00. Išsami informacija apie antraštės laukus yra tokia, kaip šioje lentelėje.

|Offsetas|Dydis|Aprašymas|
---|---|---|
|0|16|Antraštės eilutė: SQLite formatas 3\000|
|16|2|Duomenų bazės puslapio dydis baitais. Turi būti dviejų laipsnis nuo 512 iki 32768 imtinai arba vertė 1, reiškianti 65536 puslapio dydį.|
|18|1|Failo formato rašymo versija. 1 už palikimą; 2 už WAL.|
|19|1|Failo formato skaitymo versija. 1 už palikimą; 2 už WAL.|
|20|1|Baitai nepanaudotos rezervuotos vietos kiekvieno puslapio pabaigoje. Paprastai 0.|
|21|1|Didžiausia įterptosios naudingosios apkrovos dalis. Turi būti 64.|
|22|1|Mažiausia įdėtos naudingosios apkrovos dalis. Turi būti 32.|
|23|1|Naudingosios lapų apkrovos dalis. Turi būti 32.|
|24|4|Failų keitimo skaitiklis.|
|28|4|Duomenų bazės failo dydis puslapiais. Antraštės duomenų bazės dydis.|
|32|4|Pirmojo laisvojo sąrašo pagrindinio puslapio puslapio numeris.|
|36|4|Bendras laisvojo sąrašo puslapių skaičius.|
|40|4|Scheminis slapukas.|
|44|4|Schemos formato numeris. Palaikomi schemų formatai yra 1, 2, 3 ir 4.|
|48|4|Numatytasis puslapio talpyklos dydis.|
|52|4|Didžiausio b-medžio šakninio puslapio puslapio numeris, kai veikia automatinio vakuuminio arba laipsninio vakuumo režimai, arba nulis kitaip.|
|56|4|The database text encoding. A value of 1 means UTF-8. 2 reikšmė reiškia UTF-16le. 3 reikšmė reiškia UTF-16be.|
|60|4|Vartotojo versija, kurią nuskaito ir nustatė user_version pragma.|
|64|4|True (ne nulis) laipsniniam vakuuminiam režimui. Klaidingas (nulis) kitaip.|
|68|4|Programos ID, kurį nustatė PRAGMA application_id.|
|72|20|Rezervuota plėtrai. Turi būti nulis.|
|92|4|Versija galioja numeriui.|
|96|4|SQLITE_VERSION_NUMBER|

## Nuorodos Nr.

* [SQLite failo formatas – SQLite](https://www.sqlite.org/fileformat2.html)

* [SQLite – Vikipedija](https://en.wikipedia.org/wiki/SQLite)

* [SQLite – C kalbos specifikacijos](https://www.sqlite.org/c3ref/intro.html)


