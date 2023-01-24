{
  "date" : "2023-01-17",
  "keywords" :[ "DSN", "was ist eine DSN-Datei", "Erweiterung", "Datei", "Dateiformat", "Datenbankdateityp", "Datenbankdateiformat", "Datenbankdateien" ],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Erfahren Sie mehr über das DSN-Dateiformat und APIs, die DSN-Dateien erstellen und öffnen können.",
  "title" :"DSN-Dateiformat - Datenbankquellnamendatei",
  "linktitle" : "DSN",
  "menu" : {
    "docs" : {
      "identifier":"database-dsn",
      "parent" : "database"
}
},
  "lastmod" : "2020-01-17"
}

## Was ist eine DSN-Datei?

DSN steht für "Data Source Name" und ist ein Dateiformat, das zum Speichern von Datenbankverbindungsinformationen verwendet wird. DSN-Dateien werden normalerweise in Verbindung mit ODBC (Open Database Connectivity) verwendet und ermöglichen einen einfachen Zugriff auf eine bestimmte Datenbank, indem sie die erforderlichen Informationen zum Herstellen einer Verbindung bereitstellen, z. B. Servername, Benutzername und Kennwort. Die Datei ist normalerweise im Klartext und kann mit einem Texteditor erstellt und bearbeitet werden. Es kann auf verschiedenen Betriebssystemen wie Windows, Linux und Mac verwendet werden.

## Wie erstelle ich eine DSN-Datei?

Die Methode zum Erstellen einer DSN-Datei kann je nach Betriebssystem und verfügbaren Tools variieren. Die folgenden Schritte bieten einen allgemeinen Überblick über den Vorgang zum Erstellen einer DSN-Datei auf einem Windows-System.

1. Öffnen Sie den ODBC-Datenquellen-Administrator, indem Sie im Startmenü nach „ODBC-Datenquellen“ suchen.
2. Wählen Sie die Registerkarte „System-DSN“ und klicken Sie auf die Schaltfläche „Hinzufügen“.
3. Wählen Sie den passenden Treiber für die Datenbank aus, zu der Sie eine Verbindung herstellen möchten, und klicken Sie auf „Fertig stellen“.
4. Geben Sie die erforderlichen Informationen ein, um eine Verbindung zur Datenbank herzustellen, z. B. Servername, Benutzername und Kennwort.
5. Klicken Sie auf „OK“, um die DSN-Datei zu speichern.

Alternativ können Sie eine DSN-Datei manuell erstellen, indem Sie eine einfache Textdatei mit der Erweiterung .dsn erstellen und die erforderlichen Verbindungsinformationen im folgenden Format eingeben:

```
[ODBC]
DRIVER=driver_name
SERVER=server_name
DATABASE=database_name
UID=username
PWD=password
```

Sie können dann den Pfad dieser Datei als DSN in Ihrem Code/Skript verwenden, um eine Verbindung zur Datenbank herzustellen.

## Programme, die die DSN-Datei öffnen

Eine DSN-Datei ist eine einfache Textdatei, die Informationen speichert, die zum Herstellen einer Verbindung mit einer Datenbank verwendet werden, wie z. B. Servername, Benutzername und Kennwort. Es wird normalerweise in Verbindung mit ODBC (Open Database Connectivity) verwendet, um einen einfachen Zugriff auf eine bestimmte Datenbank zu ermöglichen.

Um den Inhalt einer DSN-Datei zu öffnen und anzuzeigen, können Sie einen beliebigen Texteditor wie Notepad, Sublime Text, Atom usw. verwenden. Mit diesen Programmen können Sie die DSN-Datei öffnen und die darin gespeicherten Verbindungsinformationen anzeigen.

Um jedoch die DSN-Datei zu verwenden, um eine Verbindung zu einer Datenbank herzustellen und Operationen wie SELECT, INSERT, UPDATE, DELETE usw. auszuführen, ist ein Programm mit ODBC-Unterstützung erforderlich, z. B. eine Programmiersprache wie Python, Java, C# oder ein Datenbankverwaltungstool wie Microsoft Access , ist SQL Server Management Studio erforderlich. Diese Programme können die Informationen in der DSN-Datei verwenden, um eine Verbindung zur Datenbank herzustellen und die gewünschte Operation auszuführen.

## Verweise
* [Was ist ein DSN (Datenquellenname)?](https://support.microsoft.com/en-us/topic/what-is-a-dsn-data-source-name-ae9a0c76-22fc-8a30- 606e-2436fe26e89f)
* [Wie erstelle ich einen Datei-DSN zur Verwendung als Datenquelle für ODBC-Importe?](https://www.ibm.com/support/pages/how-do-i-create-file-dsn-use-data- source-odbc-importe)

