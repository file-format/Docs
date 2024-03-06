{
  "date": "2021-08-24",
  "keywords": [
"trc fails",
"trc faila formātā",
"kas ir trc fails",
"failu",
"trc piemērs",
"trc faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par TRC faila formātu un API, kas var izveidot un atvērt TRC failus.",
  "title": "TRC — SQL servera izsekošanas fails",
  "linktitle": "TRC",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-tr-lvc"
}
},
  "lastmod": "2021-08-24"
}

## Kas ir TRC fails?
Fails ar paplašinājumu .trc satur Miscrosoft SQL servera datu bāzes darbības izsekošanas rezultātus. Šos failus izveido programmatūra SQL Server Profiler; parasti komplektā ar Microsoft SQL Server programmatūru. Datu bāzes administratori var analizēt datu bāzes paziņojumu secību un var pārskatīt izsekošanas žurnālu, ja ir aizdomas par kādām kļūdām vai brīdinājumiem. Šie faili parasti atrodas tipiskajā MSSQL mapē LOG, kas atrodas Windows operētājsistēmas direktorijā Program Files.

## TRC faila formāts
TRC faila formātu izmanto SQL Server Profiler, lai automātiski ģenerētu jaunu pēdu nesen izpildītajiem MS SQL servera paziņojumiem. SQL Server Profiler izmanto noklusējuma veidni jebkurai jaunai izsekojamībai. Tomēr programmatūra ietver vairākas iepriekš definētas veidnes noteikta veida notikumu uzraudzībai. Arī SQL Server Profiler var izmantot, lai izveidotu veidnes, kas definē notikumu klases un datu kolonnas, kas jāiekļauj trasēšanā.

### Iepriekš definētas veidnes
Šeit ir saraksts ar dažām iepriekš definētām veidnēm, kas iekļautas SQL Server Profiler:
- **SP_Counts**: tver saglabāto procedūru izpildes uzvedību laika gaitā.
- **Standarta**: vispārīgs sākumpunkts izsekošanas izveidei.
- **TSQL**: tver visus Transact-SQL paziņojumus, ko klienti iesniedz SQL Server, un izdošanas laiku.
- **TSQL_Duration**: tver visus Transact-SQL paziņojumus, ko klienti iesniedz SQL Server, to izpildes laiku un grupē tos pēc ilguma.
- **TSQL_Grouped**: izmantojiet, lai izpētītu vaicājumus no konkrēta klienta vai lietotāja.
- **TSQL_Locks**: izmantojiet, lai novērstu strupceļu problēmas, bloķētu taimautu un bloķētu eskalācijas notikumus.
- **TSQL_Replay**: izmantojiet, lai veiktu iteratīvu regulēšanu, piemēram, etalona testēšanu.
- **TSQL_SPs**: izmantojiet, lai analizētu saglabāto procedūru komponentu soļus.
- **Tuning**: izmantojiet, lai izveidotu izsekošanas izvadi, ko Database Engine Tuning Advisor var izmantot kā darba slodzi datu bāzu regulēšanai.
### Korelējiet izsekošanu ar Windows veiktspējas žurnāla datiem
SQL Server Profiler var izmantot, lai atvērtu Microsoft Windows veiktspējas žurnālu, lai izvēlētos skaitītājus korelēšanai ar izsekošanu un parādītu atlasītos veiktspējas skaitītājus kopā ar izsekošanu MS SQL Server Profiler GUI. Lai norādītu veiktspējas žurnāla datus, kas korelē ar atlasīto izsekošanas notikumu, SQL Server Profiler sistēmas pārrauga datu loga rūtī tiek parādīta vertikāla sarkana josla.


## Atsauces Nr.

* [SQL Server Profiler](https://learn.microsoft.com/en-us/sql/tools/sql-server-profiler/sql-server-profiler?view=sql-server-ver15)


