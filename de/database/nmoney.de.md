{
  "date" : "2023-05-17",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Erfahren Sie mehr über das NMONEY-Dateiformat und APIs, mit denen NMONEY-Dateien erstellt und geöffnet werden können.",
  "title" :"NMONEY-Datei – Denaro-Kontodateiformat",
  "linktitle" : "NMONEY",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2023-05-17"
}

## Was ist eine NMONEY-Datei?

Eine NMONEY-Datei ist eine Datenbankdatei zur Speicherung von Finanzdaten, die die Erfolgsbilanz von Finanztransaktionen enthält. Es wurde von Nickvision entwickelt und in der Nickvision Denaro-Software verwendet, einer persönlichen Finanzsoftwareanwendung. Zu den in einer NOMONEY-Datei gespeicherten Daten gehören Informationen zu Kredit- und Debittransaktionen für ein Konto.

NOMONEY-Dateien können mit der Anwendung [Github](https://github.com/NickvisionApps/Denaro) geöffnet werden.

## Über Denaro Software

Denaro wurde ursprünglich von [Nickvision](https://nickvision.org/) als Produkt entwickelt, das später in eine Open-Source-Software-App umgewandelt wurde, die auf [Github](https://github.com/NickvisionApps/Denaro) gehostet wurde. . Seitdem wurde die App nur auf Github geändert und aktualisiert. Die App wird in C# in der Windows-Benutzeroberfläche mit dem Windows App SDK (derzeit WinUI 3) entwickelt.

### Von Denaro angebotene Funktionen

* Verwalten Sie mehrere Konten gleichzeitig mit der beliebtesten und bekanntesten Tab-Oberfläche
* Filtern Sie Transaktionen nach Typ, Gruppe oder Datum
* Wiederholen Sie Transaktionen wie Rechnungen, die jeden Monat anfallen
* Überweisen Sie Geld von einem Konto auf ein anderes
* Exportieren Sie die Daten eines Kontos als CSV-Datei und importieren Sie eine CSV-, OFX- oder QIF-Datei, um Transaktionen zu einem Konto hinzuzufügen

## Denaro-Dateiformat – Weitere Informationen

Denaro-Dateien werden im Binärdateiformat auf der Disc gespeichert. Finanzdaten werden als Datenbankdatei im Dateiformat **.SQLITE3** gespeichert. SQLITE ist eine leichte SQL-Datenbankdatei, die mit der SQLite-Software erstellt wurde. Es bietet eine eigenständige Datenbank-Engine, die eine voll funktionsfähige und äußerst zuverlässige Datenbank bereitstellen kann. SQLite-Datenbankdateien können verwendet werden, um umfangreiche Inhalte zwischen Systemen auszutauschen, indem diese Dateien einfach über das Netzwerk ausgetauscht werden. SQLite-Bindungen gibt es für Programmiersprachen wie C, [C#](/programming/cs/), [C++](/programming/cpp/), [Java](/programming/java/), [PHP](/programming/ php/) und viele andere.

## Verweise

* [Nickvision](https://nickvision.org/)
* [NIckVision – Github](https://github.com/NickvisionApps/Denaro)

