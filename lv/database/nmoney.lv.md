{
  "date": "2023-05-17",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par NMONEY faila formātu un API, kas var izveidot un atvērt NMONEY failus.",
  "title": "NMONEY fails — Denaro konta faila formāts",
  "linktitle": "NMONEY",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-nmone-lvy"
}
},
  "lastmod": "2023-05-17"
}

## Kas ir NMONEY fails?

NMONEY fails ir finanšu datu glabāšanas datu bāzes fails, kas satur finanšu darījumu ierakstus. To izstrādāja Nickvision un izmantoja Nickvision Denaro programmatūrā, kas ir personīgās finanšu programmatūras lietojumprogramma. Datos, kas glabājas NOMONEY failā, ir ietverta informācija par konta kredīta un debeta darījumiem.

NOMONEY failus var atvērt ar lietojumprogrammu [Github](https://github.com/NickvisionApps/Denaro).

## Par Denaro programmatūru

Denaro was initially developed by [Nickvision](https://nickvision.org/) as a product that was later converted to an open-source software app hosted on [Github](https://github.com/NickvisionApps/Denaro). Since then app has been modified and updated on Github only. The app is developed in C# in Windows UI with Windows App SDK (WinUI 3 as at this time).

### Denaro piedāvātās funkcijas

 * Pārvaldiet vairākus kontus vienlaikus, izmantojot vispopulārāko un pazīstamāko cilnes saskarni
 * Filtrējiet darījumus pēc veida, grupas vai datuma
 * Atkārtojiet darījumus, piemēram, rēķinus, kas notiek katru mēnesi
 * Pārskaitiet naudu no viena konta uz citu
 * Eksportējiet datus no konta kā CSV failu un importējiet CSV, OFX vai QIF failu, lai kontam pievienotu darījumus

## Denaro faila formāts — vairāk informācijas

Denaro faili tiek saglabāti diskā binārā faila formātā. Finanšu dati tiek glabāti kā datu bāzes fails **.SQLITE3** faila formātā. SQLITE ir viegls SQL datu bāzes fails, kas izveidots ar SQLite programmatūru. Tas nodrošina autonomu datu bāzes dzinēju, kas spēj nodrošināt pilnībā aprīkotu un ļoti uzticamu datu bāzi. SQLite datu bāzes failus var izmantot, lai koplietotu bagātīgu saturu starp sistēmām, vienkārši apmainoties ar šiem failiem tīklā. SQLite saite pastāv tādām programmēšanas valodām kā C, [C#](/programming/cs/), [C++](/programming/cpp/), [Java](/programming/java/), [PHP](/programming/php/) un daudzām citām.

## Atsauces

 * [Nickvision](https://nickvision.org/)
 * [NIckVision — Github](https://github.com/NickvisionApps/Denaro)

