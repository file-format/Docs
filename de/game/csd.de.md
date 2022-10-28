{
  "date" : "2022-02-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Erfahren Sie mehr über CSD Steam Game Data Backup File Format und APIs.",
  "title" :"CSD-Dateiformat - Steam-Spieldaten-Sicherungsdatei",
  "linktitle" : "CSD",
  "menu" : {
    "docs" : {
"identifier": "game-csd",
      "parent" : "game"
}
},
  "lastmod" : "2022-02-08"
}

## Was ist eine CSD-Datei?

Eine CSD-Datei ist eine Spielsicherungsdatei, die vom Spieledienst **Steam** erstellt wird und Benutzern das Herunterladen und Verwalten von **Valve**-Spielen ermöglicht. Es enthält die Sicherungsdaten für Spiele, die zum Wiederherstellen eines gelöschten Spiels verwendet werden können. Steam kann das Spiel nur aus einer CSD-Datei wiederherstellen, wenn das Spiel vollständig heruntergeladen, installiert und über Steam gepatcht wurde. Um das Spiel aus der CSD-Datei wiederherzustellen, verwenden Sie die Option Steam → Gamesteam sichern und wiederherstellen und wählen Sie die Datei aus.

## CSD-Dateiformat – Weitere Informationen

Die interne Struktur des CSD-Dateiformats ist nicht öffentlich verfügbar und seine Dateiformatspezifikationen sind nicht als Referenz für Entwickler verfügbar. CSD-Dateien werden von den CSM- und ISS-Dateien begleitet, die ebenfalls Steam-Spieldateiformate sind.

### Wo finde ich Steam-Sicherungsdateien?

Die gesamten Steam-Sicherungsdateien finden Sie an den folgenden Orten:

* C:\Programme (x86)\Steam\steamapps\common\<game name> \ :
* \cfg\ - Benutzerdefinierte Konfigurationen und Konfigurationsskripte
* \downloads\ - Benutzerdefinierte Inhalte für Multiplayer-Spiele
* \maps\ - Benutzerdefinierte Karten, die während Multiplayer-Spielen installiert oder heruntergeladen wurden
* \materials\ - Benutzerdefinierte Texturen und Skins
* \SAVE\ - Gespeicherte Einzelspieler-Spiele

Der Speicherort von Spielen, die von Drittanbietern erstellt wurden, kann jedoch unterschiedlich sein und wird vom Entwickler des Spiels bestimmt.

### Wiederherstellung aus CSD-Sicherungsdatei

Installieren Sie Steam und melden Sie sich beim richtigen Steam-Konto an (weitere Anweisungen finden Sie unter Steam installieren).
* Starten Sie Steam
* Klicken Sie in der Steam-Anwendung oben links auf „Steam“.
* Wähle "Spiele sichern und wiederherstellen..."
* Wählen Sie „Vorheriges Backup wiederherstellen“
* Navigieren Sie zum Speicherort der Sicherungsdateien des Spiels
* Fahren Sie durch die Steam-Fenster fort, um die erforderlichen Spiele zu installieren.

## Verweise

* [Verwendung der Steam-Sicherungsfunktion](https://help.steampowered.com/en/faqs/view/4593-5CB7-DC3C-64F0)

