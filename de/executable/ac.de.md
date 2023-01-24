{
  "date" : "2023-01-11",
  "keywords" :["ac-Datei", "was ist eine aci-Datei", "Datei", "wie man eine ac-Datei öffnet", "ac-Dateierweiterung", "Erweiterung"],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Erfahren Sie mehr über das AC-Dateiformat und APIs, die ACCDB-Dateien erstellen und öffnen können.",
  "title" :"AC-Dateiformat - Autoconf-Skriptdatei",
  "linktitle" : "AC",
  "menu" : {
    "docs" : {
      "identifier":"executable-ac",
      "parent" : "executable"
}
},
  "lastmod" : "2020-01-11"
}

## Was ist eine AC-Datei?

AC-Datei ist die Autoconf-Skriptdatei. **Autoconf** ist ein erweiterbares Paket von M4-Makros, die Shell-Skripte erzeugen, um Software-Quellcodepakete automatisch zu konfigurieren. Diese Skripte können die Pakete ohne manuellen Benutzereingriff an viele Arten von UNIX-ähnlichen Systemen anpassen. Autoconf erstellt ein Konfigurationsskript für ein Paket aus einer Vorlagendatei, die die Betriebssystemfunktionen auflistet, die das Paket in Form von M4-Makroaufrufen verwenden kann.

Das Erstellen von Konfigurationsskripten mit Autoconf erfordert GNU M4. Sie sollten GNU M4 (mindestens Version 1.4.6, obwohl 1.4.13 oder höher empfohlen wird) installieren, bevor Sie Autoconf konfigurieren, damit das Konfigurationsskript von Autoconf es finden kann. Die von Autoconf erstellten Konfigurationsskripte sind in sich abgeschlossen, sodass ihre Benutzer Autoconf (oder GNU M4) nicht benötigen.

## Wie öffne ich eine AC-Datei?

AC steht für Automatische Konfiguration. Es ist ein von GNU Autoconf generiertes Skript, das es ermöglicht, den Software-Quellcode an verschiedene Posix-ähnliche Systeme anzupassen, indem es die erforderlichen Funktionen im Paket testet. Das Skript wird als AC-Datei bezeichnet.

## Wichtige Autotools-Komponenten

Ein Verständnis der GNU-Autotools (`automake`, `autoconf` usw.) kann bei der Arbeit mit Ebuilds hilfreich sein:

Autotools ist eine Sammlung verwandter Pakete, die, wenn sie zusammen verwendet werden, einen Großteil der Schwierigkeiten beseitigen, die mit der Erstellung portabler Software verbunden sind. Diese Tools werden zusammen mit einigen relativ einfachen, von Upstream bereitgestellten Eingabedateien verwendet, um das Build-System für ein Paket zu erstellen.

**Ein grundlegender Überblick darüber, wie die wichtigsten Autotools-Komponenten zusammenpassen.**

![A basic overview of how the main autotools components fit together](https://devmanual.gentoo.org/general-concepts/autotools/diagram.png "A basic overview of how the main autotools components fit together")

In einer einfachen Einrichtung:

- Das `autoconf`-Programm erstellt ein Konfigurationsskript entweder aus `configure.in` oder `configure.ac`.
- Das `automake`-Programm erzeugt ein Makefile.in aus einem Makefile.am.
- Das Skript „configure“ wird ausgeführt, um eine oder mehrere Makefile-Dateien aus Makefile.in-Dateien zu erstellen.
- Das `make`-Programm verwendet das Makefile, um das Programm zu kompilieren.

## Verweise
* [Autoconf-Software](https://www.gnu.org/software/autoconf/)
* [Die Grundlagen von Autotools](https://devmanual.gentoo.org/general-concepts/autotools/index.html)


