{
  "date" : "2019-10-11",
  "keywords" :[ "h", ".hh", "was ist eine .hh-Datei", "wie man eine .hh-Datei öffnet", "Erweiterung", "Datei", ".hh-Datei", ".hh-Dateiformat", " .hh-Dateierweiterung",".HH-Dateibeispiel"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HH - C++ Header-Dateiformat",
  "description":"Erfahren Sie mehr über das HH-Dateiformat und APIs, die HH-Dateien erstellen und öffnen können.",
  "linktitle" : "HH",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-06-20"
}

## Was ist eine HH-Datei?

Eine Datei mit der Erweiterung .hh ist eine C++-Headerdatei, die die Deklaration von Variablen, Konstanten und Funktionen enthält. Diese Deklarationen werden von den entsprechenden C++-Implementierungsdateien verwendet, die normalerweise als [.cpp](/de/programming/cpp/)-Dateien gespeichert werden, die die eigentliche Implementierung der Benutzerlogik enthalten. Auf die .hh-Header-Dateien wird in den Implementierungs-CPP-Dateien unter Verwendung der Direktive "#include" verwiesen. Sie können Ihrem C++-Projekt so viele Headerdateien wie möglich hinzufügen, um Deklarationen auf Projektebene einzuschließen.

## .HH-Dateiformat

Eine .hh-Datei ist eine reine Textdatei, die unter Berücksichtigung der Definitionsregeln der Header-Datei erstellt wird. Zu den häufigsten Informationen, die in einer .hh-Datei deklariert werden, gehören die folgenden.

**`Variablen`** - Im Fall von objektorientierter Programmierung (OOP) enthält eine Klassenheaderdatei Definitionen aller Variablen auf Klassenebene, auf die über die Quellcodedateien der Implementierung zugegriffen werden kann
**`Methods Declaration`** - Alle Methodendeklarationen sind in den .h-Headerdateien enthalten, damit sie über mehrere Implementierungsdateien zugänglich sind.
**`Nicht-Inline-Funktionsdefinitionen`** - Header-Dateien können auch Definitionen von Nicht-Inline-Methoden enthalten.
**`Message Maps`** – Eine Headerdatei kann im Falle einer MFC-Quellcodeimplementierung auch Message Maps enthalten. In diesem Fall sind die Message Maps mit der Funktionalitätsimplementierung verknüpft, die mit UI-Elementen wie Schaltflächen, Kontrollkästchen, Optionsfeldern usw. verknüpft ist.

## Unterschied zwischen .H- und .HH-Dateien

Anscheinend gibt es keinen solchen Unterschied zwischen den .h- und .hh-Header-Dateien außer der empfohlenen Art, diese für die jeweiligen Sprachen zu verwenden, dh [C](/de/programming/c/) oder C++. Die Benennung Ihrer Header-Dateien nach diesen Sprachen hilft Ihnen, diese in einem großen Projekt zu unterscheiden, das eine Mischung aus C- und C++-Implementierungen sein kann.

Wenn die Kopfzeilen außerdem durch Erweiterungen getrennt sind, kann Ihr Redakteur die entsprechende Formatierung automatisch anwenden.

Insgesamt schadet die Unterscheidung dieser beiden Dateiformate nicht, ist aber vorteilhaft und wird zur Unterscheidung von C und C++ empfohlen.

### Kopfschutz

Header-Dateien können zu komplexen Fehlern führen, wenn mehrere Deklarationen in derselben Datei enthalten sind, weil andere Header-Dateien hinzugefügt wurden. Diese doppelten Definitionen führen zu Compilerfehlern. Diese problematische Situation kann durch einen Mechanismus namens Header Guard vermieden werden, bei dem es sich um bedingte Kompilierungsdirektiven handelt, wie unten gezeigt.

```
#ifndef ANY_UNIQUE_NAME_HERE_HPP
#define ANY_UNIQUE_NAME_HERE_HPP

// your declarations (and certain types of definitions) here

#endif
```
Mit diesem Header prüft der Präprozessor, ob der `ANY_UNIQUE_NAME_HERE_HPP` bereits definiert wurde. Wenn der Header wiederholt in dieselbe Datei eingefügt wird, wird der Inhalt des Headers ignoriert.

## Verweise

* [Header Filer – Microsoft](https://docs.microsoft.com/en-us/cpp/cpp/header-files-cpp?view=msvc-160)
* [Unterschied zwischen .h- und .hh-Dateiformaten](https://stackoverflow.com/questions/10354321/c-reason-why-using-hh-as-extension-for-c-header-files)

