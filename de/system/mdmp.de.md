{
  "date" : "2022-08-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MDMP-Datei - Windows-Minidump-Dateiformat",
  "description":"Erfahren Sie mehr über das MDMP-Dateiformat und APIs, die MDMP-Dateien erstellen und öffnen können.",
  "linktitle" :"MDMP",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2022-08-19"
}

## Was ist eine MDMP-Datei?

Eine MDMP-Datei ist ein Speicherabbild einer Anwendung unter Microsoft Windows, das erstellt wird, wenn die Anwendung nicht normal geschlossen wird oder abstürzt. Es enthält Informationen und Datendumps, die zum Debuggen der Absturzursache verwendet werden können. MDMP-Dateien sind auf Anwendungen anwendbar, die von beliebigen Plattformen wie Java, C++, .NET und anderen erstellt wurden. Neben MDMP,

Zu den Anwendungen, die MDMP-Dateien öffnen können, gehört Microsoft Visual Studio Debugger.

## MDMP-Dateiformat

MDMP-Dateien werden als Binärdateien auf Datenträger gespeichert und können mit dem Microsoft Visual Studio-Debugger geöffnet werden. Es enthält die folgenden Informationen, um den Grund für den Absturz zu ermitteln.

* Details der Stop-Meldung, ihrer Parameter und anderer Daten
* Liste der geladenen Treiber
* Prozessorkontext (PRCB) für den Prozessor, der nicht mehr funktioniert
* Prozessinformationen und Kernelkontext (EPROCESS) für den gestoppten Prozess
* Prozessinformationen und Kernelkontext (ETHREAD) für den beendeten Thread
* Aufrufliste im Kernelmodus für den beendeten Thread

Diese Informationen helfen, herauszufinden, was passiert ist, das Problem zu beheben und zu verhindern, dass es erneut auftritt.

### Minidump analysieren

Windows benötigt eine Auslagerungsdatei auf dem Startvolume, um eine Speicherabbilddatei zu erstellen. Die Auslagerungsdatei wird auf dem Startvolume erstellt und sollte mindestens 2 Megabyte (MB) groß sein. Die Dump-Datei wird erstellt, wenn eine Anwendung abstürzt. Im Falle eines zweiten Problems wird eine zweite kleine Speicherabbilddatei erstellt, während die vorherige erhalten bleibt. Der Name der Dump-Datei ist eindeutig, um ein Überschreiben zu vermeiden.

Windows führt eine Liste aller Speicherabbilddateien im Ordner %SystemRoot%\Minidump. Sie können MDMP-Dateien analysieren, indem Sie sie wie in den folgenden Schritten beschrieben im Visual Studio-Debugger ausführen.

## Wie öffne ich eine MDMP-Datei in Visual Studio?

Die folgenden Schritte können verwendet werden, um eine MDMP-Datei in Visual Studio zu öffnen.

* Wählen Sie in Visual Studio im Menü Datei die Option Öffnen | aus Crash-Dump.
* Navigieren Sie zu der Dump-Datei, die Sie öffnen möchten.
* Wählen Sie Öffnen.

## Bezug

* [So lesen Sie die kleine Speicherabbilddatei, die von Windows erstellt wird, wenn ein Absturz auftritt](https://docs.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump -Datei)

