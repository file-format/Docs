{
  "date" : "2023-01-17",
  "keywords" : [ "DSN", "what is a DSN file", "extension", "file", "file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "Meer informatie over de DSN-bestandsindeling en API's waarmee DSN-bestanden kunnen worden gemaakt en geopend.",
  "title" : "DSN-bestandsindeling - Databasebronnaambestand",
  "linktitle" : "DSN",
  "menu" : {
    "docs" : {
      "identifier":"database-dsn-nl",
      "parent" : "database"
}
},
  "lastmod" : "2020-01-17"
}

## Wat is een DSN-bestand?

DSN staat voor Data Source Name en het is een bestandsformaat dat wordt gebruikt om databaseverbindingsinformatie op te slaan. DSN-bestanden worden doorgaans gebruikt in combinatie met ODBC (Open Database Connectivity) en zorgen voor gemakkelijke toegang tot een specifieke database door de nodige informatie te verstrekken om er verbinding mee te maken, zoals de servernaam, gebruikersnaam en wachtwoord. Het bestand is meestal in platte tekst en kan worden gemaakt en bewerkt met een teksteditor. Het kan op verschillende besturingssystemen worden gebruikt, zoals Windows, Linux en Mac.

## Hoe maak ik een DSN-bestand aan?

De methode voor het maken van een DSN-bestand kan variëren, afhankelijk van het besturingssysteem en de beschikbare tools. De volgende stappen bieden een algemeen overzicht van het proces voor het maken van een DSN-bestand op een Windows-systeem.

1. Open de ODBC Data Source Administrator door te zoeken naar ODBC Data Sources in het startmenu.
2. Selecteer het tabblad Systeem-DSN en klik op de knop Toevoegen.
3. Selecteer het juiste stuurprogramma voor de database waarmee u verbinding wilt maken en klik op Voltooien.
4. Vul de benodigde informatie in om verbinding te maken met de database, zoals de servernaam, gebruikersnaam en wachtwoord.
5. Klik op OK om het DSN-bestand op te slaan.

Als alternatief kunt u handmatig een DSN-bestand maken door een tekstbestand met de extensie .dsn te maken en de benodigde verbindingsgegevens in te voeren in het formaat:

```
[ODBC]
DRIVER=driver_name
SERVER=server_name
DATABASE=database_name
UID=username
PWD=password
```

U kunt vervolgens het pad van dit bestand als DSN in uw code/script gebruiken om verbinding te maken met de database.

## Programma's die het DSN-bestand openen

Een DSN-bestand is een tekstbestand waarin informatie wordt opgeslagen die wordt gebruikt om verbinding te maken met een database, zoals de servernaam, gebruikersnaam en wachtwoord. Het wordt doorgaans gebruikt in combinatie met ODBC (Open Database Connectivity) om gemakkelijke toegang tot een specifieke database te bieden.

Om de inhoud van een DSN-bestand te openen en te bekijken, kunt u elke teksteditor gebruiken, zoals Kladblok, Sublime Text, Atom, enz. Met deze programma's kunt u het DSN-bestand openen en de verbindingsinformatie bekijken die daarin is opgeslagen.

Om het DSN-bestand echter te gebruiken om verbinding te maken met een database en bewerkingen uit te voeren zoals SELECT, INSERT, UPDATE, DELETE enz., is een programma met ODBC-ondersteuning nodig, zoals een programmeertaal zoals Python, Java, C# of een databasebeheertool zoals Microsoft Access , is SQL Server Management Studio vereist. Deze programma's kunnen de informatie in het DSN-bestand gebruiken om verbinding te maken met de database en de gewenste bewerking uit te voeren.

## Referenties

* [Wat is een DSN (gegevensbronnaam)?](https://support.microsoft.com/en-us/topic/what-is-a-dsn-data-source-name-ae9a0c76-22fc-8a30- 606e-2436fe26e89f)



