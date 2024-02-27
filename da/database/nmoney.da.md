{
  "date": "2023-05-17",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om NMONEY filformat og API'er, der kan oprette og åbne NMONEY filer.",
  "title": "NMONEY-fil - Denaro-kontofilformat",
  "linktitle": "NMONEY",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-nmone-day"
}
},
  "lastmod": "2023-05-17"
}

## Hvad er en NMONEY fil?

En NMONEY-fil er en finansiel datalagringsdatabasefil, der indeholder track record af finansielle transaktioner. Det blev udviklet af Nickvision og blev brugt i Nickvision Denaro-softwaren, som er en personlig økonomisk softwareapplikation. Data gemt i en NOMONEY-fil inkluderer kredit- og debettransaktionsoplysninger til en konto.

NOMONEY-filer kan åbnes med applikationen [Github](https://github.com/NickvisionApps/Denaro).

## Om Denaro Software

Denaro was initially developed by [Nickvision](https://nickvision.org/) as a product that was later converted to an open-source software app hosted on [Github](https://github.com/NickvisionApps/Denaro). Since then app has been modified and updated on Github only. The app is developed in C# in Windows UI with Windows App SDK (WinUI 3 as at this time).

### Funktioner, der tilbydes af Denaro

 * Administrer flere konti samtidigt med dens mest populære og velkendte fanegrænseflade
 * Filtrer transaktioner efter type, gruppe eller dato
 * Gentag transaktioner, såsom regninger, der opstår hver måned
 * Overfør penge fra en konto til en anden
 * Eksporter dataene fra en konto som en CSV-fil og importer en CSV-, OFX- eller QIF-fil for at tilføje transaktioner til en konto

## Denaro filformat - flere oplysninger

Denaro-filer gemmes på disk i binært filformat. Finansielle data gemmes som en databasefil i **.SQLITE3** filformat. SQLITE er en letvægts SQL-databasefil oprettet med SQLite-softwaren. Det giver selvstændig databasemotor, der er i stand til at levere fuldt udstyret og yderst pålidelig database. SQLite-databasefiler kan bruges til at dele rigt indhold mellem systemer ved blot at udveksle disse filer over netværket. SQLite-bindinger findes for programmeringssprog såsom C, [C#](/programming/cs/), [C++](/programming/cpp/), [Java](/programming/java/), [PHP](/programming/php/) og mange andre.

## Referencer

 * [Nickvision](https://nickvision.org/)
 * [NIckVision - Github](https://github.com/NickvisionApps/Denaro)

