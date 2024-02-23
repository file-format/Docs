{
  "date" : "2023-01-17",
  "keywords" : [ "DSN", "what is a DSN file", "extension", "file", "file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "Lär dig om DSN-filformat och API:er som kan skapa och öppna DSN-filer.",
  "title" : "DSN-filformat - Databaskällnamnsfil",
  "linktitle" : "DSN",
  "menu" : {
    "docs" : {
      "identifier":"database-dsn-sv",
      "parent" : "database"
}
},
  "lastmod" : "2020-01-17"
}

## Vad är en DSN fil?

DSN står för Data Source Name och det är ett filformat som används för att lagra databasanslutningsinformation. DSN-filer används vanligtvis tillsammans med ODBC (Open Database Connectivity) och möjliggör enkel åtkomst till en specifik databas genom att tillhandahålla nödvändig information för att ansluta till den, såsom servernamn, användarnamn och lösenord. Filen är vanligtvis i vanlig text och kan skapas och redigeras med hjälp av en textredigerare. Den kan användas på olika operativsystem som Windows, Linux och Mac.

## Hur skapar man en DSN-fil?

Metoden för att skapa en DSN-fil kan variera beroende på operativsystemet och de verktyg som är tillgängliga. Följande steg ger en allmän översikt över processen för att skapa en DSN-fil på ett Windows-system.

1. Öppna ODBC Data Source Administrator genom att söka efter ODBC Data Sources i startmenyn.
2. Välj fliken System DSN och klicka på knappen Lägg till.
3. Välj lämplig drivrutin för databasen du vill ansluta till och klicka på Slutför.
4. Fyll i nödvändig information för att ansluta till databasen, såsom servernamn, användarnamn och lösenord.
5. Klicka på OK för att spara DSN-filen.

Alternativt kan du skapa en DSN-fil manuellt genom att skapa en vanlig textfil med filtillägget .dsn och ange nödvändig anslutningsinformation i formatet:

```
[ODBC]
DRIVER=driver_name
SERVER=server_name
DATABASE=database_name
UID=username
PWD=password
```

Du kan sedan använda sökvägen till denna fil som DSN i din kod/skript för att ansluta till databasen.

## Program som öppnar filen DSN

En DSN-fil är en vanlig textfil som lagrar information som används för att ansluta till en databas, såsom servernamn, användarnamn och lösenord. Den används vanligtvis i kombination med ODBC (Open Database Connectivity) för att ge enkel åtkomst till en specifik databas.

För att öppna och visa innehållet i en DSN-fil kan du använda vilken textredigerare som helst som Notepad, Sublime Text, Atom, etc. Dessa program låter dig öppna DSN-filen och se anslutningsinformationen som är lagrad i den.

Men för att använda DSN-filen för att ansluta till en databas och utföra operationer som SELECT, INSERT, UPDATE, DELETE etc, ett program med ODBC-stöd, såsom ett programmeringsspråk som Python, Java, C# eller ett databashanteringsverktyg som Microsoft Access , SQL Server Management Studio krävs. Dessa program kan använda informationen i DSN-filen för att ansluta till databasen och utföra önskad operation.

## Referenser

* [Vad är ett DSN (Data Source Name)?](https://support.microsoft.com/en-us/topic/what-is-a-dsn-data-source-name-ae9a0c76-22fc-8a30- 606e-2436fe26e89f)



