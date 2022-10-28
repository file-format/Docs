{
  "date" : "2021-08-17",
  "keywords" :[ "UDF-Datei", "UDF-Dateiformat", "Was ist eine UDF-Datei", "Datei", "UDF-Beispiel", "UDF-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Erfahren Sie mehr über das UDF-Dateiformat und APIs, die UDF-Dateien erstellen und öffnen können.",
  "title" :"UDF - Universelle Disk-Formatdatei",
  "linktitle" : "UDF",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-17"
}

## Was ist eine UDF-Datei?
Die Datei mit der Erweiterung .udf ist ein Disk-Imaging-Format, das typischerweise zum Speichern von Dateien auf optischen Medien verwendet wird; kann zum Brennen von DVDs, CDs und anderen optischen Medien verwendet werden; speichert eine Sammlung von Dateien unter Verwendung der im UDF-Standard angegebenen Verzeichnisstruktur; ermöglicht das Löschen und Ändern von Dateien auf der Zieldisk, selbst nachdem sie geschrieben wurden. Die Optical Storage Technology Association hat das UDF-Dateisystem als Standard festgelegt, um ein gemeinsames Dateisystem für alle optischen Medien zu bilden, beispielsweise für wiederbeschreibbare optische Medien und schreibgeschützte Medien.

## UDF-Dateiformat
Das UDF-Dateiformat ist ein offenes, herstellerneutrales Dateisystem für Computerdatenspeicherung für eine Vielzahl von Medien. Es wurde häufig für DVDs und neuere optische Disc-Formate verwendet. Normalerweise beherrscht die Software ein UDF-Dateisystem in einem Batch-Prozess und schreibt es in einem Durchgang auf optische Medien. Wenn es jedoch Pakete auf wiederbeschreibbare Medien schreibt, ermöglicht die UDF das Erstellen, Löschen und Ändern von Dateien auf der Disc, ähnlich wie ein universelles Dateisystem auf Wechselmedien wie Flash-Laufwerken oder Disketten.
### UDF-Spezifikationen
Der UDF-Standard definiert die folgenden drei Dateisystemvarianten:

- **Plain Build**: Dies ist das ursprüngliche Format, das in allen UDF-Revisionen unterstützt wird. Es wurde in der ersten Version des Standards eingeführt, dieses Format kann auf allen Arten von Datenträgern verwendet werden, die wahlfreien Lese- oder Schreibzugriff ermöglichen, wie z. B. DVD+RW, Festplatten und DVD-RAM-Medien.
- **VAT-Build**: Wird speziell zum Schreiben auf einmal beschreibbare Medien verwendet. Die Mehrwertsteuer ist eine zusätzliche Struktur auf der Disc, die das Schreiben von Paketen ermöglicht. das heißt, physische Blöcke neu zuordnen, wenn Dateien oder andere Daten auf der Disc geändert oder gelöscht werden. Bei einmal beschreibbaren Medien wird die gesamte Disc virtualisiert, wodurch die einmal beschreibbare Natur für den Benutzer transparent wird; die Disc kann genauso behandelt werden wie eine wiederbeschreibbare Disc.
- **Spared (RW) build**: Wird speziell zum Schreiben auf wiederbeschreibbare Medien verwendet. Es fügt eine zusätzliche Sparing-Tabelle hinzu, um die Fehler zu verwalten, die schließlich auf Teilen der Disc auftreten, die mehrmals neu beschrieben wurden. Diese Tabelle speichert den Überblick über abgenutzte Sektoren und ordnet sie den funktionierenden Sektoren neu zu. Das Fehlermanagement von UDF gilt nicht für Systeme, die bereits eine andere Form des Fehlermanagements implementieren, wie z. B. Mount Rainier (MRW) für optische Datenträger oder einen Festplattencontroller für eine Festplatte.
 




## Verweise


* [Windows Imaging Format – von Wikipedia](https://en.wikipedia.org/wiki/Windows_Imaging_Format)


