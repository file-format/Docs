{
  "date" : "2023-01-09",
  "keywords" : [ "ABCDDB", "what is a ABCDDB file", "extension", "file", "file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "Lär dig om ABCDDB-filformat och API:er som kan skapa och öppna ABCDDB-filer.",
  "title" : "ABCDDB filformat - Apple adressbok kontaktlista databasfil",
  "linktitle" : "ABCDDB",
  "menu" : {
    "docs" : {
      "identifier":"database-abcddb-sv",
      "parent" : "database"
}
},
  "lastmod" : "2020-01-09"
}

## Vad är en ABCDDB fil?

Filen med tillägget **.ABCDDB** står för Apple Address Book Contact List Database. Den tillhör applikationen **Adressbok**, även känd som **Kontakter**. Det är en inbyggd applikation och ingår i iOS och macOS operativsystem. Appen Kontakter gör det möjligt för användare att spara och organisera information relaterad till deras kontakter, inklusive individer, företag och organisationer. Denna app låter användare hålla reda på detaljer som namn, adresser, telefonnummer och e-postadresser, samt att kategorisera sina kontakter i grupper.

## Relation med SQLite och Typical Path

Apples adressbok (även känd som kontakter) lagrar kontaktinformation som vCards i metadatamappen. **Filen _ABCDDB_ är faktiskt _SQLite 3-datafil_**.

SQLite är ett populärt databashanteringssystem som är designat för att vara lätt och fristående. Det används i många olika typer av programvara och enheter. SQLite är en typ av RDBMS, vilket betyder att den lagrar data i tabeller som är relaterade till varandra genom nycklar. Den kan hantera en rad datatyper, inklusive heltal, flyttal, strängar och binära data. Dessutom stöder SQLite transaktioner, vilket gör det möjligt för användare att utföra flera databasoperationer tillsammans som en enda arbetsenhet.

Filen med tillägget ABCDDB lagras vanligtvis här

`~/Library/Application Support/AddressBook/AddressBook-v22.abcddb`

## Fixar korrupt kontaktdatabas

Ta först säkerhetskopian innan du försöker göra detta. Gå sedan till

`~/Library/Application Support/AddressBook`

I den katalogen hittar du tre filer inklusive den med tillägget .abcddb

- `adressbok-v22.abcddb`
- `adressbok-v22.abcddb-wal`
- `adressbok-v22.abcddb-shm`

Ta bort alla dessa filer och öppna kontakterna igen, det kommer att börja fungera igen.

## Återställ adressbokens databas från säkerhetskopia

Antag att dina adressbokdatabaskontakter är lagrade i `addressbook-v22.abcddb`

- Säkerhetskopiera först din adressboksdata och avsluta alla applikationer.
- Flytta din databasfil till underkatalogen `~/Library/Application Support/AddressBook`
- Starta **Address Book.app**.

## Exportera ABCDDB-fildata till Microsoft Access

Eftersom filen är SQLite 3-datafil kan du exportera data inuti abcddb-filen till Microsoft Access med hjälp av ODBC-anslutningen.

SQLite ODBC-anslutningen är ett mjukvarubibliotek och en drivrutin som gör det möjligt för applikationer som stöder ODBC-gränssnittet att ansluta till en SQLite-databas. Den innehåller ett bibliotek som definierar ODBC-gränssnittet och en drivrutin som översätter detta gränssnitt till anrop till SQLite API. För att använda SQLite ODBC-anslutningen måste du först installera den och sedan ställa in en ODBC-datakälla på din dator. Efter att ha slutfört dessa steg kommer alla program som är utrustade med ODBC-stöd att kunna ansluta till datakällan och hämta data från SQLite-databasen.

## Referenser
 * [Fix corrupted Contacts database](https://discussions.apple.com/docs/DOC-10581)
 * [Kontaktdatabas för Mac](https://nitroreward.weebly.com/blog/contact-database-for-mac)
 * [Hur kan jag öppna eller exportera en abcddb-fil i Windows 7 Excel?](https://apple.stackexchange.com/questions/52888/how-can-i-open-or-export-a-abcddb-file-in -windows-7-excel)

