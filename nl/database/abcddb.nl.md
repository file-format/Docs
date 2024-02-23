{
  "date" : "2023-01-09",
  "keywords" : [ "ABCDDB", "what is a ABCDDB file", "extension", "file", "file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "Meer informatie over de ABCDDB-bestandsindeling en API's waarmee ABCDDB-bestanden kunnen worden gemaakt en geopend.",
  "title" : "ABCDDB-bestandsindeling - Apple-adresboek-databasebestand met contactpersonen",
  "linktitle" : "ABCDDB",
  "menu" : {
    "docs" : {
      "identifier":"database-abcddb-nl",
      "parent" : "database"
}
},
  "lastmod" : "2020-01-09"
}

## Wat is een ABCDDB-bestand?

Het bestand met de extensie **.ABCDDB** staat voor Apple Address Book Contact List Database. Het behoort tot de toepassing **Adresboek**, ook wel bekend als **Contacten**. Het is een ingebouwde applicatie en wordt meegeleverd met iOS- en macOS-besturingssystemen. Met de toepassing Contacten kunnen gebruikers informatie met betrekking tot hun contacten, inclusief individuen, bedrijven en organisaties, opslaan en ordenen. Met deze app kunnen gebruikers details bijhouden zoals namen, adressen, telefoonnummers en e-mailadressen, en hun contacten in groepen indelen.

## Relatie met SQLite en typisch pad

Apple's Adresboek (ook bekend als Contacten) slaat contactgegevens op als vCards in de map metagegevens. **Het bestand _ABCDDB_ is eigenlijk _SQLite 3 datafile_**.

SQLite is een populair databasebeheersysteem dat is ontworpen om lichtgewicht en op zichzelf staand te zijn. Het wordt in veel verschillende soorten software en apparaten gebruikt. SQLite is een type RDBMS, wat betekent dat het gegevens opslaat in tabellen die via sleutels aan elkaar gerelateerd zijn. Het kan een reeks gegevenstypen verwerken, waaronder gehele getallen, getallen met drijvende komma, tekenreeksen en binaire gegevens. Bovendien ondersteunt SQLite transacties, waardoor gebruikers meerdere databasebewerkingen samen als één werkeenheid kunnen uitvoeren.

Het bestand met de extensie ABCDDB wordt hier doorgaans opgeslagen

`~/Bibliotheek/Applicatieondersteuning/AddressBook/AddressBook-v22.abcddb`

## Corrupte contactendatabase repareren

Maak eerst een back-up voordat u dit probeert. Navigeer dan naar

`~/Bibliotheek/Applicatieondersteuning/Adresboek`

In die map vindt u drie bestanden, waaronder degene met de extensie .abcddb

- `adresboek-v22.abcddb`
- `adresboek-v22.abcddb-wal`
- `adresboek-v22.abcddb-shm`

Verwijder al deze bestanden en open de Contacten opnieuw. Het zal weer werken.

## Herstel de Adresboek-database vanuit een back-up

Stel dat uw adresboekdatabasecontacten zijn opgeslagen in `addressbook-v22.abcddb`

- Maak eerst een back-up van uw Adresboekgegevens en sluit alle toepassingen af.
- Verplaats uw databasebestand naar de submap `~/Bibliotheek/Application Support/AddressBook`
- Start **Adresboek.app**.

## Exporteer ABCDDB-bestandsgegevens naar Microsoft Access

Omdat het bestand een SQLite 3-gegevensbestand is, kunt u de gegevens in het abcddb-bestand exporteren naar Microsoft Access met behulp van de ODBC-connector.

De SQLite ODBC-connector is een softwarebibliotheek en stuurprogramma waarmee toepassingen die de ODBC-interface ondersteunen verbinding kunnen maken met een SQLite-database. Het bevat een bibliotheek die de ODBC-interface definieert, en een stuurprogramma dat deze interface vertaalt in oproepen naar de SQLite API. Als u de SQLite ODBC-connector wilt gebruiken, moet u deze eerst installeren en vervolgens een ODBC-gegevensbron op uw computer instellen. Na het voltooien van deze stappen kan elke applicatie die is uitgerust met ODBC-ondersteuning verbinding maken met de gegevensbron en gegevens ophalen uit de SQLite-database.

## Referenties
 * [Fix corrupted Contacts database](https://discussions.apple.com/docs/DOC-10581)
 * [Contactdatabase voor Mac](https://nitroreward.weebly.com/blog/contact-database-for-mac)
 * [Hoe kan ik een abcddb-bestand openen of exporteren in Windows 7 Excel?](https://apple.stackexchange.com/questions/52888/how-can-i-open-or-export-a-abcddb-file-in -windows-7-excel)

