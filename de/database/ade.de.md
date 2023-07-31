{
  "date" : "2021-08-29",
  "keywords" :[ "ade", "extension", "file", "file format", "Database File Type", "Database File Format", "Microsoft Access" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Erfahren Sie mehr über das ADE-Dateiformat und APIs, die ADE-Dateien erstellen und öffnen können.",
  "title" :"ADE - Zugriff auf die Projekterweiterungsdatei",
  "linktitle" : "ADE",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-08-29"
}

## Was ist eine ADE-Datei?

Eine Datei mit der Erweiterung .ade ist eine Microsoft Access-Projektdatei, die die kompilierte Ausgabe der Informationen enthält, die in der Microsoft Access ADP-Projektdatei enthalten sind. Informationen in der Access-Projektdatei, außer Visual Basic for Applications (VBA), sind in kompilierter Form in ADE-Dateien verfügbar. Daten werden in diesen Dateien in komprimiertem Format gespeichert, um die Dateigröße zu reduzieren und die Leistung in Access zu verbessern. Da ADE die kompilierte Ausgabe der Access-Projektdatei ist, bleibt jeder VBA-Quellcode, der Teil des Projekts ist, geschützt, indem nicht zugelassen wird, dass er Teil der Ausgabe ist. ADE-Dateien können in Microsoft Access 365 geöffnet werden.

## ADE-Dateiformat – Weitere Informationen

ADE sind kompilierte Access-Datenbankdateien, die als Binärdateien auf der Disc gespeichert werden. Die interne Dateistruktur dieser Dateien ist nicht bekannt.

Die ADE-Dateien können Probleme beim Öffnen verursachen, basierend auf der Version von Microsoft Access, die zum Erstellen dieser Dateien verwendet wurde. Access-Datenbanken, die die 64-Bit-Version von Microsoft Access 2010 verwenden und die als MDE-, [ACCDE](/de/database/accde/)- oder ADE-Dateien kompiliert wurden, müssen in Microsoft Access 2021 Service Pack 1 (SP1) neu kompiliert werden ordnungsgemäß mit Access 2010 SP1 funktionieren. Dieses Problem tritt auf, weil Access 2010 SP1 eine neuere Version der Datei VBE7.dll (Version 7.00.1619) verwendet.

## Verweise

* [Problem mit Access ADE-Dateien](https://learn.microsoft.com/en-us/office/troubleshoot/access/error-run-compiled-mde-accde-ade)
* [Zu verwendende Access-Dateiformate](https://support.microsoft.com/en-us/office/which-access-file-format-should-i-use-012d9ab3-d14c-479e-b617-be66f9070b41)

