{
  "date": "2021-05-03",
  "keywords": [
"SDF",
"sdf-fil",
"hvad er sdf-fil",
"hvordan man åbner en sdf-fil",
"udvidelse",
"fil",
"sdf filformat",
"Database filtype",
"Database filformat",
"Database filer"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om SDF-filformat og API'er, der kan oprette og åbne SDF-filer.",
  "title": "SDF - SQL Server Compact Database File",
  "linktitle": "SDF",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-sd-daf"
}
},
  "lastmod": "2021-05-03"
}

## Hvad er SDF fil?
En fil med filtypenavnet .sdf indeholder Microsoft SQL Server Compact (SQL CE)-databasen, som også er kendt som en kompakt relationsdatabase; produceret af Microsoft til applikationer lavet til mobile enheder og desktops. Det understøtter både 32 og 64 bit operativsystem, og hele databasens indhold er inkluderet i en enkelt SDF-fil og kan optage mere end 4 GB diskplads. Af sikkerhedsmæssige årsager kan en .sdf-fil krypteres med 128-bit kryptering. SQL CE runtime afgør parallel flerbrugeradgang til .sdf-filen. SDF-filen kan kopieres via **QuickOnce**, eller den kan simpelthen kopieres til destination for systemimplementering.

## SDF filformat
En SDF-fil indeholder en database, som normalt kaldes kompakt relationsdatabase. En SDF-fil indeholder alle databaserelaterede oplysninger, og SQL Server Compact er en letvægts og gratis databasemotor, som bruges til at administrere .sdf-filerne. .sdf-filstørrelsen bør ikke overstige grænsen på 4 GB størrelse. SDF-filerne gemmer ikke oplysningerne om lagrede procedurer, udløsere eller visninger. Applikationer, der bruger en SQL CE-database, behøver ikke at angive stien til en SDF-fil i ADO.NET-forbindelsesstrengen, i stedet kan den nævnes som |DataDirectory|\database_name.sdf, der definerer databiblioteket, der defineres i assemblermanifestet for applikationen
.sdf-navnekonventionen er valgfri, og enhver filtypenavn kan bruges til at gemme filen. Opsætning af en adgangskode til databasefilen er et valgfrit trin. For at komprimere eller reparere databasen skal filen gemmes med muligheden for den **komprimerede/reparerede database**.

## Referencer

 * [SQL Server Compact - Wikipedia](https://en.wikipedia.org/wiki/SQL_Server_Compact)
 * [Brug af SQL Server Compact til ASP.NET-webapplikationer](https://learn.microsoft.com/en-us/previous-versions/aspnet/ms247257(v=vs.110))


