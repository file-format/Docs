{
  "date" : "2021-04-08",
  "keywords" :[ "rpm-Datei", "rpm-Dateiformat", "was ist eine rpm-Datei", "Datei", "rpm-Beispiel", "rpm-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RPM - Red Hat Package Manager-Datei",
  "description":"Erfahren Sie mehr über das RPM-Dateiformat und APIs, die RPM-Dateien erstellen und öffnen können.",
  "linktitle" : "RPM",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-09"
}

## Was ist eine RPM-Datei?

Eine Datei mit der Erweiterung .rpm ist ein Betriebssystempaket von Red Hat Linux für die Installation von Programmen auf Linux-Systemen. Der Red Hat Package Manager verwendet das RPM-Dateiformat und ist ein kostenloses und Open-Source-Paketverwaltungssystem. Obwohl RPM-Dateien unverändert für die Installation von Programmen verwendet werden können, können diese mit dem Debian-Programm namens Alien in andere Paketformate wie [DEB](/de/compression/deb/) konvertiert werden.

## RPM-Dateiformat

Eine RPM-Datei ist eine Binärdatei, die eine Reihe von Dateien enthalten kann. Meistens sind RPM-Dateien "binäre RPMs", die die kompilierten ausführbaren Dateien der Software sind. Die RPM-Datei kann Quell-RPMs (SRPMs) enthalten, die zum Erstellen des Pakets aus dem Quellcode verwendet werden können. Das RPM-Dateiformat besteht aus vier Abschnitten.

* Lead - Es identifiziert die Datei als RPM-Datei
* Signatur - Kann verwendet werden, um die Integrität und/oder Authentizität sicherzustellen
* Header - Enthält Metadaten einschließlich Paketname, Version, Architektur, Dateiliste usw.
* Dateiarchiv - Auch bekannt als Nutzdaten, die normalerweise im cpio-Format vorliegen, komprimiert mit [GZIP](/de/compression/gz/)

## Verweise

* [RPM – Wikipedia](https://rpm.org)
* [RPM-Dokumentation](https://rpm.org/documentation.html)

