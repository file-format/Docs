{
  "date" : "2022-08-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HDMP-Datei - Windows-Heap-Dump-Dateiformat",
  "description":"Erfahren Sie mehr über das HDMP-Dateiformat und APIs, die HDMP-Dateien erstellen und öffnen können.",
  "linktitle" : "HDMP",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2022-08-19"
}

## Was ist eine HDMP-Datei?

Die HDMP-Datei ist ein unkomprimiertes Speicherabbild, wenn eine Anwendung oder ein Programm aufgrund eines Fehlers abstürzt. Es wird nur von Windows XP/Vista erstellt und enthält einen Dump des Anwendungsstatus, als es abgestürzt ist. Unkomprimiert nehmen die HDMP-Dateien mehr Platz auf der Disc ein als die Minidump-Dateien [MDMP](/de/system/mdmp/), die zu Berichtszwecken komprimiert werden.

Zu den Anwendungen, die zum **Öffnen** oder Analysieren von HDMP-Dateien verwendet werden können, gehört Microsoft Visual Studio mit Debugging-Tools für Windows.

## HDMP-Dateiformat

HDMP-Dateien werden als Binärdateien auf der Disc gespeichert und bieten keinen Nutzen, wenn sie ohne entsprechende Anwendungen geöffnet werden. Diese enthalten relevante Systemdaten, die beim Auftreten des Fehlers aufgezeichnet wurden.

### Unterschied zwischen HDMP- und MDMP-Dateiformaten

HDMP sind unkomprimierte Speicherabbilddateien. Im Gegensatz dazu handelt es sich bei MDMP um Mini-Dump-Dateien, die zur Verringerung der Dateigröße komprimiert und zur Meldung des Problems an Microsoft gesendet werden.

## Bezug ##

* [DMP – Microsoft](https://docs.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)

