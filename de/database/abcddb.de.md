{
  "date" : "2023-01-09",
  "keywords" :[ "ABCDDB", "was ist eine ABCDDB-Datei", "Erweiterung", "Datei", "Dateiformat", "Datenbankdateityp", "Datenbankdateiformat", "Datenbankdateien" ],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Erfahren Sie mehr über das ABCDDB-Dateiformat und APIs, die ABCDDB-Dateien erstellen und öffnen können.",
  "title" :"ABCDDB-Dateiformat - Apple-Adressbuch-Kontaktlisten-Datenbankdatei",
  "linktitle" : "ABCDDB",
  "menu" : {
    "docs" : {
      "identifier":"database-abcddb",
      "parent" : "database"
}
},
  "lastmod" : "2020-01-09"
}

## Was ist eine ABCDDB-Datei?

Die Datei mit der Erweiterung **.ABCDDB** steht für Apple Address Book Contact List Database. Es gehört zur Anwendung **Adressbuch**, auch bekannt als **Kontakte**. Es ist eine integrierte Anwendung und in den Betriebssystemen iOS und macOS enthalten. Die Kontaktanwendung ermöglicht es Benutzern, Informationen zu ihren Kontakten zu speichern und zu organisieren, einschließlich Einzelpersonen, Unternehmen und Organisationen. Mit dieser App können Benutzer Details wie Namen, Adressen, Telefonnummern und E-Mail-Adressen verfolgen und ihre Kontakte in Gruppen kategorisieren.

## Beziehung zu SQLite und typischer Pfad

Das Adressbuch von Apple (auch bekannt als Kontakte) speichert Kontaktinformationen als vCards im Metadatenordner. **Die Datei _ABCDDB_ ist eigentlich eine _SQLite 3-Datendatei_**.

SQLite ist ein beliebtes Datenbankverwaltungssystem, das leichtgewichtig und eigenständig ist. Es wird in vielen verschiedenen Arten von Software und Geräten verwendet. SQLite ist eine Art von RDBMS, dh es speichert Daten in Tabellen, die über Schlüssel miteinander in Beziehung stehen. Es kann eine Reihe von Datentypen verarbeiten, einschließlich Ganzzahlen, Gleitkommazahlen, Zeichenfolgen und Binärdaten. Darüber hinaus unterstützt SQLite Transaktionen, die es Benutzern ermöglichen, mehrere Datenbankoperationen zusammen als eine einzige Arbeitseinheit auszuführen.

Die Datei mit der Erweiterung ABCDDB wird normalerweise hier gespeichert

`~/Library/Application Support/AddressBook/AddressBook-v22.abcddb`

## Beschädigte Kontaktdatenbank reparieren

Bitte erstellen Sie zuerst die Sicherung, bevor Sie dies versuchen. Dann navigieren Sie bitte zu

`~/Library/Application Support/AddressBook`

In diesem Verzeichnis finden Sie drei Dateien, darunter die mit der Erweiterung .abcddb

- `Adressbuch-v22.abcddb`
- `Adressbuch-v22.abcddb-wal`
- `Adressbuch-v22.abcddb-shm`

Löschen Sie alle diese Dateien und öffnen Sie die Kontakte erneut, damit sie wieder funktionieren.

## Stellen Sie die Adressbuch-Datenbank aus der Sicherung wieder her

Angenommen, Ihre Adressbuch-Datenbankkontakte sind in `addressbook-v22.abcddb` gespeichert

- Sichern Sie zuerst Ihre Adressbuchdaten und beenden Sie alle Anwendungen.
- Verschieben Sie Ihre Datenbankdatei in das Unterverzeichnis `~/Library/Application Support/AddressBook`
- Starten Sie **Adressbuch.app**.

## Exportieren Sie ABCDDB-Dateidaten nach Microsoft Access

Da es sich bei der Datei um eine SQLite 3-Datendatei handelt, können Sie die Daten in der abcddb-Datei mithilfe des ODBC-Connectors in Microsoft Access exportieren.

Der SQLite-ODBC-Connector ist eine Softwarebibliothek und ein Treiber, mit denen Anwendungen, die die ODBC-Schnittstelle unterstützen, eine Verbindung zu einer SQLite-Datenbank herstellen können. Es enthält eine Bibliothek, die die ODBC-Schnittstelle definiert, und einen Treiber, der diese Schnittstelle in Aufrufe an die SQLite-API übersetzt. Um den SQLite-ODBC-Connector zu verwenden, müssen Sie ihn zuerst installieren und dann eine ODBC-Datenquelle auf Ihrem Computer einrichten. Nach Abschluss dieser Schritte kann jede Anwendung, die mit ODBC-Unterstützung ausgestattet ist, eine Verbindung zur Datenquelle herstellen und Daten aus der SQLite-Datenbank abrufen.

## Verweise
* [Beschädigte Kontaktdatenbank reparieren](https://discussions.apple.com/docs/DOC-10581)
* [Kontaktdatenbank für Mac](https://nitroreward.weebly.com/blog/contact-database-for-mac)
* [Wie kann ich eine abcddb-Datei in Windows 7 Excel öffnen oder exportieren?](https://apple.stackexchange.com/questions/52888/how-can-i-open-or-export-a-abcddb-file- in-Windows-7-Excel)

