{
  "date": "2019-12-12",
  "keywords": [
"SQLite",
"pagarinājumu",
"failu",
"faila formātā",
"Datu bāzes faila tips",
"Datu bāzes faila formāts",
"Datu bāzes faili"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par SQLITE failu formātu un API, kas var izveidot un atvērt SQLITE failus.",
  "title": "SQLite faila formāts",
  "linktitle": "SQLITE",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-sqlit-lve"
}
},
  "lastmod": "2020-11-09"
}

## Kas ir SQLite fails?

Fails ar paplašinājumu .sqlite ir viegls SQL datu bāzes fails, kas izveidots, izmantojot programmatūru [SQLite](https://www.sqlite.org/index.html). Tā ir datu bāze pašā failā un ievieš autonomu, pilnvērtīgu, ļoti uzticamu [SQL](/database/sql/) datu bāzes dzinēju. SQLite datu bāzes failus var izmantot, lai koplietotu bagātīgu saturu starp sistēmām, vienkārši apmainoties ar šiem failiem tīklā. Gandrīz visi mobilie tālruņi un datori izmanto SQLite datu glabāšanai un koplietošanai, un tas ir faila formāta izvēle starpplatformu lietojumprogrammām. Pateicoties kompaktai lietošanai un vienkāršai lietošanai, tas ir iekļauts citu lietojumprogrammu komplektācijā. SQLite saite pastāv tādām programmēšanas valodām kā C, [C#](/programming/cs/), [C++](/programming/cpp/), [Java](/programming/java/), [PHP](/programming/php/) un daudzām citām.

## SQLite faila formāts

SQLite patiesībā ir C valodas bibliotēka, kas ievieš SQLite RDBMS, izmantojot SQLite faila formātu. Katru dienu attīstoties jaunām ierīcēm, tā faila formāts ir saglabāts atpakaļsaderīgs, lai pielāgotos vecākām ierīcēm. SQLite faila formāts tiek uzskatīts par datu ilgtermiņa arhīva formātu.

### Datu bāzes fails

SQLite datu bāze tiek pilnībā uzturēta, izmantojot divus failus.
 * Galvenā datu bāzes fails — satur pilnu SQLite datu bāzes stāvokli
 * Rollback Journal — saglabā papildu informāciju otrajā failā un tiek izmantota darījumu veikšanas laikā. Ja SQLite ir WAL režīmā, tiek uzturēts rakstīšanas galviņas žurnālfails.

#### Žurnāla fails

Šis fails ir paredzēts, lai saglabātu visu saglabāto informāciju gadījumā, ja pēdējo darījumu nevarētu pabeigt tādos gadījumos kā datora avārija. Šis fails tiek izmantots, lai atjaunotu datu bāzes faila konsekventu stāvokli.

#### Lapas

Galvenais SQLite datu bāzes fails sastāv no vienas vai vairākām lapām. Jebkurā brīdī katrai galvenās datubāzes lapai ir vienreizējs lietojums, kas ir viens no šiem:

 * Bloķēšanas baitu lapa
 * Bezmaksas saraksta lapa
   * Brīvā saraksta stumbra lapa
   * Brīvā saraksta lapu lapa
 * B-koka lapa
   * Tabulas b-koka interjera lapa
   * Tabulas b-koka lapu lapa
   * Indeksa b-koka iekšējā lapa
   * Indeksa b-koka lapu lapa
 * Lietderīgās slodzes pārpildes lapa
 * Rādītāja kartes lapa

SQLite datu bāzes failu lielums var būt no dažiem kilobaitiem līdz dažiem gigabaitiem.

### SQLite galvene

The SQLite database header is located in the first 100 bytes of the database file. Every valid SQLite database file starts with 16 bytes (in hex):53 51 4c 69 74 65 20 66 6f 72 6d 61 74 20 33 00. Sīkāka informācija par galvenes laukiem ir norādīta nākamajā tabulā.

|Nobīde|Izmērs|Apraksts|
---|---|---|
|0|16|Galvenes virkne: SQLite formāts 3\000|
|16|2|Datubāzes lapas izmērs baitos. Jābūt pakāpei divi no 512 līdz 32768 ieskaitot, vai vērtībai 1, kas apzīmē lapas izmēru 65536.|
|18|1|Faila formāta rakstīšanas versija. 1 mantojumam; 2 par WAL.|
|19|1|Faila formāta lasīšanas versija. 1 mantojumam; 2 par WAL.|
|20|1|Baiti neizmantotas rezervētas vietas katras lapas beigās. Parasti 0.|
|21|1|Maksimālā iegultās lietderīgās kravas daļa. Jābūt 64.|
|22|1|Minimālā iegultās kravnesības daļa. Jābūt 32.|
|23|1|Lapu kravnesības daļa. Jābūt 32.|
|24|4|Failu izmaiņu skaitītājs.|
|28|4|Datubāzes faila lielums lapās. Galvenes datu bāzes lielums.|
|32|4|Pirmās brīvā saraksta maģistrāles lapas lappuses numurs.|
|36|4|Kopējais brīvā saraksta lapu skaits.|
|40|4|Shēmas sīkfails.|
|44|4|Shēmas formāta numurs. Atbalstītie shēmas formāti ir 1, 2, 3 un 4.|
|48|4|Noklusējuma lapas kešatmiņas lielums.|
|52|4|Lielākās saknes b-koka lapas lappuses numurs automātiskā vakuuma vai inkrementālā vakuuma režīmā vai nulle pretējā gadījumā.|
|56|4|The database text encoding. A value of 1 means UTF-8. Vērtība 2 nozīmē UTF-16le. Vērtība 3 nozīmē UTF-16be.|
|60|4|Lietotāja versija, ko nolasa un iestata user_version pragma.|
|64|4|True (nav nulles) inkrementālajam vakuuma režīmam. Nepatiess (nulle) pretējā gadījumā.|
|68|4|Lietojumprogrammas ID, ko iestatījis PRAGMA application_id.|
|72|20|Rezervēts paplašināšanai. Jābūt nullei.|
|92|4|Versija derīga numuram.|
|96|4|SQLITE_VERSION_NUMBER|

## Atsauces Nr.

* [SQLite faila formāts — SQLite](https://www.sqlite.org/fileformat2.html)

* [SQLite — Wikipedia](https://en.wikipedia.org/wiki/SQLite)

* [SQLite — C valodas specifikācijas](https://www.sqlite.org/c3ref/intro.html)


