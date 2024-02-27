{
  "date" : "2023-01-09",
  "keywords" : [ "ABCDDB", "what is a ABCDDB file", "extension", "file", "file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "Lær om ABCDDB filformat og API'er, der kan oprette og åbne ABCDDB filer.",
  "title" : "ABCDDB-filformat - Apple-adressebogs kontaktlistedatabasefil",
  "linktitle" : "ABCDDB",
  "menu" : {
    "docs" : {
      "identifier":"database-abcddb-da",
      "parent" : "database"
}
},
  "lastmod" : "2020-01-09"
}

## Hvad er ABCDDB fil?

Filen med filtypenavnet **.ABCDDB** står for Apple Address Book Contact List Database. Det tilhører applikationen **Adressebog**, også kendt som **Kontakter**. Det er en indbygget applikation og inkluderet i iOS- og macOS-operativsystemer. Applikationen Kontakter gør det muligt for brugere at gemme og organisere information relateret til deres kontakter, herunder enkeltpersoner, virksomheder og organisationer. Denne app giver brugerne mulighed for at holde styr på detaljer såsom navne, adresser, telefonnumre og e-mailadresser, samt at kategorisere deres kontakter i grupper.

## Relation til SQLite og Typical Path

Apples adressebog (også kendt som kontakter) gemmer kontaktoplysninger som vCards i metadata-mappen. **Filen _ABCDDB_ er faktisk _SQLite 3 datafil_**.

SQLite er et populært databasestyringssystem, der er designet til at være let og selvstændigt. Det bruges i mange forskellige typer software og enheder. SQLite er en type RDBMS, hvilket betyder, at den gemmer data i tabeller, der er relateret til hinanden gennem nøgler. Den kan håndtere en række datatyper, herunder heltal, flydende kommatal, strenge og binære data. Derudover understøtter SQLite transaktioner, som gør det muligt for brugere at udføre flere databaseoperationer sammen som en enkelt arbejdsenhed.

Filen med ABCDDB-udvidelsen gemmes typisk her

`~/Library/Application Support/AddressBook/AddressBook-v22.abcddb`

## Retter korrupt kontaktdatabase

Tag venligst først sikkerhedskopien, før du forsøger at gøre dette. Så skal du navigere til

`~/Library/Application Support/AddressBook`

I den mappe finder du tre filer inklusive den med .abcddb-udvidelsen

- `adressebog-v22.abcddb`
- `adressebog-v22.abcddb-wal`
- `adressebog-v22.abcddb-shm`

Slet alle disse filer og genåbn kontakterne, det vil begynde at fungere igen.

## Gendan AddressBook-database fra Backup

Antag, at dine adressebogsdatabasekontakter er gemt i `adressebog-v22.abcddb`

- Sikkerhedskopier først dine adressebogsdata og luk alle applikationer.
- Flyt din databasefil til `~/Library/Application Support/AddressBook` undermappe
- Start **Adressebog.app**.

## Eksporter ABCDDB-fildata til Microsoft Access

Da filen er SQLite 3-datafil, kan du eksportere dataene i abcddb-filen til Microsoft Access ved hjælp af ODBC-stikket.

SQLite ODBC-forbindelsen er et softwarebibliotek og en driver, der gør det muligt for programmer, der understøtter ODBC-grænsefladen, at oprette forbindelse til en SQLite-database. Det inkluderer et bibliotek, der definerer ODBC-grænsefladen, og en driver, der oversætter denne grænseflade til opkald til SQLite API. For at bruge SQLite ODBC-stikket skal du først installere det og derefter konfigurere en ODBC-datakilde på din computer. Efter at have gennemført disse trin, vil enhver applikation, der er udstyret med ODBC-understøttelse, være i stand til at oprette forbindelse til datakilden og hente data fra SQLite-databasen.

## Referencer
 * [Fix corrupted Contacts database](https://discussions.apple.com/docs/DOC-10581)
 * [Kontaktdatabase til Mac](https://nitroreward.weebly.com/blog/contact-database-for-mac)
 * [Hvordan kan jeg åbne eller eksportere en abcddb-fil i Windows 7 Excel?](https://apple.stackexchange.com/questions/52888/how-can-i-open-or-export-a-abcddb-file-in -windows-7-excel)

