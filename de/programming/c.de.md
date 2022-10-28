{
  "date" : "2020-01-10",
  "keywords" :[ "c", ".c", "was ist eine c-Datei", "wie man eine c-Datei öffnet", "Erweiterung", "Datei", "c-Datei", "c-Dateiformat", "c-Dateierweiterung"] ,
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Programmierdatei für C - C-Sprache",
  "description":"Erfahren Sie mehr über das C-Dateiformat und APIs, die C-Dateien erstellen und öffnen können.",
  "linktitle" : "C",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-01-10"
}

## Was ist eine C-Datei?

Eine mit der Dateierweiterung c gespeicherte Datei ist eine Quellcodedatei, die in der Programmiersprache C geschrieben ist. Die **C-Datei** enthält die gesamte Implementierung der Anwendungsfunktionalität in Form von Quellcode. Die Deklaration des Quellcodes wird in die Header-Dateien geschrieben, die mit der Erweiterung [.h](/de/programming/h/) gespeichert werden. C++ ist die moderne Form der C-Sprache und wird heutzutage zur Entwicklung der meisten Software verwendet.

## Kurze Geschichte

Die C-Sprache entstand als Ergebnis der Erstellung verschiedener Dienstprogramme für das UNIX-Betriebssystem. Denis Ritchie, der Mann hinter der Entwicklung dieser Programmiersprache, begann die Arbeit ursprünglich in den 1960er und frühen 1970er Jahren.

## C-Dateiformat

C-Dateien werden im Nur-Text-Dateiformat gemäß der Syntax der Programmiersprache geschrieben. Eine typische C-Datei hat:

* import-Anweisung am Anfang der Datei, um Header-Dateien zu importieren
* eine oder mehrere Methoden, um die gewünschte Funktionalität zu implementieren

### Header-Import

Die Header-Dateien mit der Erweiterung .h enthalten notwendige Include-Anweisungen zum Einschließen anderer Funktionsdateien in das Projekt. Außerdem enthalten diese die Deklarationen von Methoden, die in der Implementierungsdatei definiert sind. Header-Dateien werden mit der unten gezeigten include-Anweisung eingebunden.

```
#include <filename.h>
```

### Implementierung des Quellcodes

Die eigentliche Umsetzung der funktionalen Anforderungen sind als Methoden in der C-Datei kodiert. Jede Methode in einer C-Datei hat einen Rückgabetyp, einen Methodennamen und möglicherweise einige Eingabeparameter. Wenn der Rückgabetyp nicht void ist, gibt die Methode möglicherweise einen Wert zurück.

### C-Code-Beispiel
Hier ist ein Beispielprogramm:

```
long some_function();
/* int */ other_function();

/* int */ calling_function()
{
    long test1;
    register /* int */ test2;

    test1 = some_function();
    if (test1 > 0)
          test2 = 0;
    else
          test2 = other_function();
    return test2;
}
```



## **Verweise** ##

* [Klassenimplementierung – von Wikipedia](https://en.wikipedia.org/wiki/Class_implementation_file)

