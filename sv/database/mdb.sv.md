{
  "date" : "2020-11-11",
  "keywords" :[ "MDB", "tillägg", "fil", "filformat", "Databasfiltyp", "Databasfilformat", "Databasfiler" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Läs mer om MDB-filformat och API:er som kan skapa och öppna MDB-filer.",
  "title" :"MDB-filformat - En Microsoft Access-databasfil",
  "linktitle" : "MDB",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-11"
}

## Vad är en MDB fil?

En fil med filtillägget .mdb är en Microsoft Access-databasfil som är ett RDBMS (Relational Database Management System). Den lagrar data i databastabeller som är länkade till varandra via primära och främmande nycklar. MDB-filen innehåller fullständig struktur av databastabeller, frågor, lagrade procedurer. MDB är standardfilformatet för Microsoft Access 2003. De laterala versionerna av Microsoft Access använder filformaten [ACCDB](/sv/database/accdb/), vilket är det senaste filformatet hittills. MDB-filer kan öppnas med applikationer som Microsoft Access, MDB Viewer, MDBOpener och kan konverteras till ACCDB, [CSV](/sv/spreadsheet/csv/), Excel-format, etc.

## MDB filformat

Det finns offentliga specifikationer tillgängliga för MDB-format och det förblir Microsofts proprietära filformat. Microsoft tillhandahåller dock anslutningsåtkomst till MDB-filen med Open Database Connectivity-standarden (ODBC) och Visual Basic for Applications (VBA). Den inofficiella MDB-guiden ger en kort informell beskrivning av MDB-formatet baserat på reverse engineering och kan konsulteras för att veta om specifikationerna.

### Sidor

Enligt den inofficiella MDB-guiden består en MDB-fil av sidor med fast storlek (2048 byte för Jeb DB3 och 4096 byte för Jet DB 4). Den första byten anger typen av sida. Följande är de viktigaste sidtyperna:

`Första sidan:` Den innehåller databashuvudinformation som också inkluderar identifieringen av Jet DB-versionen som filen är kompatibel med. Dessutom innehåller den också filsäkerhetsinformation och en karta över sidanvändning.

`Tabelldefinitionssida:` En tabelldefinitionssida anger kolumner, datatyper, index och annan information. Den använder ytterligare sidor om det behövs och inkluderar en karta över sidor som innehåller raddata för denna tabell.

`Datasidor:` Datasidorna är de faktiska databehållarna där data lagras i rader. Den använder underordnade sidor för att lagra långa datavärden.

En enda Microsoft Access-databas kan bestå av flera filer som gör det möjligt att överskrida fil- och tabellstorleksbegränsningar. Detta underlättar att lägga formulär och kod i en front-end MDB-fil på användarens skrivbord och data i en annan backend MDB-filer på servrar som är anslutna till nätverket.

## Referenser ##

* [Åtkomstspecifikationer](https://support.microsoft.com/en-us/office/access-specifications-0cf3c66f-9cf2-4e32-9568-98c1025bb47c)
