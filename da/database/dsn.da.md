{
  "date" : "2023-01-17",
  "keywords" : [ "DSN", "what is a DSN file", "extension", "file", "file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "Lær om DSN-filformat og API'er, der kan oprette og åbne DSN-filer.",
  "title" : "DSN-filformat - Databasekildenavnefil",
  "linktitle" : "DSN",
  "menu" : {
    "docs" : {
      "identifier":"database-dsn-da",
      "parent" : "database"
}
},
  "lastmod" : "2020-01-17"
}

## Hvad er en DSN fil?

DSN står for Data Source Name, og det er et filformat, der bruges til at gemme databaseforbindelsesoplysninger. DSN-filer bruges typisk i forbindelse med ODBC (Open Database Connectivity) og giver nem adgang til en specifik database ved at give de nødvendige oplysninger for at oprette forbindelse til den, såsom servernavn, brugernavn og adgangskode. Filen er normalt i almindelig tekst og kan oprettes og redigeres ved hjælp af en teksteditor. Det kan bruges på forskellige operativsystemer som Windows, Linux og Mac.

## Hvordan opretter man en DSN-fil?

Metoden til at oprette en DSN-fil kan variere baseret på operativsystemet og de tilgængelige værktøjer. De følgende trin giver et generelt overblik over processen til at oprette en DSN-fil på et Windows-system.

1. Åbn ODBC Data Source Administrator ved at søge efter ODBC Data Sources i startmenuen.
2. Vælg fanen System DSN og klik på knappen Tilføj.
3. Vælg den relevante driver til den database, du ønsker at oprette forbindelse til, og klik på Udfør.
4. Udfyld de nødvendige oplysninger for at oprette forbindelse til databasen, såsom servernavn, brugernavn og adgangskode.
5. Klik på OK for at gemme DSN-filen.

Alternativt kan du oprette en DSN-fil manuelt ved at oprette en almindelig tekstfil med filtypenavnet .dsn og indtaste de nødvendige forbindelsesoplysninger i formatet:

```
[ODBC]
DRIVER=driver_name
SERVER=server_name
DATABASE=database_name
UID=username
PWD=password
```

Du kan derefter bruge stien til denne fil som DSN i din kode/script for at oprette forbindelse til databasen.

## Programmer, der åbner filen DSN

En DSN-fil er en almindelig tekstfil, der gemmer oplysninger, der bruges til at oprette forbindelse til en database, såsom servernavn, brugernavn og adgangskode. Det bruges typisk i forbindelse med ODBC (Open Database Connectivity) for at give nem adgang til en specifik database.

For at åbne og se indholdet af en DSN-fil kan du bruge en hvilken som helst teksteditor, såsom Notesblok, Sublime Text, Atom osv. Disse programmer giver dig mulighed for at åbne DSN-filen og se forbindelsesinformationen, der er gemt i den.

Men for at bruge DSN-filen til at oprette forbindelse til en database og udføre operationer som SELECT, INSERT, UPDATE, DELETE osv., et program med ODBC-understøttelse, såsom et programmeringssprog som Python, Java, C# eller et databasestyringsværktøj som Microsoft Access , SQL Server Management Studio er påkrævet. Disse programmer kan bruge oplysningerne i DSN-filen til at oprette forbindelse til databasen og udføre den ønskede handling.

## Referencer

* [Hvad er et DSN (Data Source Name)?](https://support.microsoft.com/en-us/topic/what-is-a-dsn-data-source-name-ae9a0c76-22fc-8a30- 606e-2436fe26e89f)



