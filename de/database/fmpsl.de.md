{
  "date" : "2022-05-25",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Erfahren Sie mehr über das FMPSL-Dateiformat und APIs, die FMPSL-Dateien erstellen und öffnen können.",
  "title" :"FMPSL-Dateiformat – FileMaker Pro 12 Snapshot Link-Datei",
  "linktitle" : "FMPSL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2022-05-25"
}

## Was ist eine FMPSL-Datei?

Eine FMPSL-Datei ist eine Snapshot-Datei einer Datenbank, die mit FileMaker Pro 12 erstellt wurde. Sie speichert die abgefragten Ergebnisse aus der Datenbank zusammen mit anderen Informationen wie dem visuellen Layout und sichtbaren Informationen. Die FMPSL-Datei kann verwendet werden, um all diese Daten in einer anderen Instanz der FileMaker Pro-Datenbank wiederherzustellen. Dieses Dateiformat wurde mit der Einführung von FileMaker Pro v 12 eingeführt. Vor dieser Version wurden die Snapshot-Links als FPSL-Dateiformat in FileMaker Pro v 11 eingeführt. FMPSL-Dateien können mit FileMaker Pro Advanced-Software geöffnet werden. Andere von FileMaker Pro unterstützte Dateiformate sind [FP5](/de/database/fp5/), [FP7](/de/database/fp7/) und [FMP12](/de/database/fmp12/).

## FMPSL-Dateiformat

Die internen Dateiformatdetails von FMPSL-Dateien sind nicht öffentlich als Referenz für Entwickler verfügbar.

### Wie speichere ich Datensätze als FMPSL-Datei?

Daten aus der FileMaker Pro-Datenbank können mit den folgenden Schritten als Snapshot-Link-Datei gespeichert werden.

1. Suchen Sie die Datensätze in der Datenbank, die als Snapshot-Link-Datei gespeichert werden müssen.
1. Speichern Sie die Datei mit der Option „Datensatz als Schnappschuss-Link senden“ im Menü, indem Sie einen Dateinamen eingeben.
1. Verwenden Sie die durchsuchten Datensätze, um den gesamten Satz gefundener Datensätze zu speichern.

Die generierte Snapshot-Datei wird unter dem angegebenen Namen auf der Disc gespeichert.

## Verweise

* [Frühere Versionen von FileMaker Pro-Dateiformaten in das FMP12-Dateiformat konvertieren](https://fmhelp.filemaker.com/help/16/fmp/en/index.html#page/FMP_Help/converting-files.html)
* [Datensätze als Snapshot-Link-Datei speichern](https://fmhelp.filemaker.com/help/12/fmp/en/html/import_export.17.5.html)

