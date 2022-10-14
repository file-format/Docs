---
date: 2022-05-09
Autor:
  display_name: Kashif Iqbal
draft: false
toc: true
title: "PYD-Dateiformat - Dynamisches Python-Modul"
linktitle: "PYD"
description: "Erfahren Sie mehr über das PYD-Dateiformat und APIs, die PYD-Dateien erstellen und öffnen können."
menu:
  docs:
    parent: "programming"
lastmod: 2022-05-09
---

## Was ist eine PYD-Datei?

Eine PYD-Datei ist eine in Python geschriebene dynamische Linkbibliothek, die zur Laufzeit von anderem Python-Code ausgeführt werden kann. Es enthält ein oder mehrere Python-Module, die die Wiederverwendung von Code erleichtern, und bietet eine Modularchitektur zum Schreiben von Anwendungen. PYD-Dateien können mit der Erweiterung .pyd erstellt und gespeichert werden, z. B. helloworld.pyd. Anwendungsentwickler können die Import-Anweisung verwenden, um die PYD-Module in ihre Anwendungen aufzunehmen. PYD-Dateien können mit Python Software Foundation Python geöffnet werden, das für Windows, Mac und Linux OS verfügbar ist.

## PYD-Dateiformat - Weitere Informationen

PYD-Dateien sind in der Programmiersprache Python geschrieben und werden durch Kompilieren des Python-Codes generiert.

## Unterschied zwischen PY- und PYD-Dateiformaten

Eine [PY](/de/programming/py/)-Datei enthält Quellcode, der unverändert ausgeführt wird und nicht als wiederverwendbarer Code in andere Python-Anwendungen eingebunden werden kann. Eine PYD-Datei ist jedoch eine dynamisch verknüpfte Bibliothek, die auf dem Windows-Betriebssystem verwendet werden kann.

## Wie erstelle ich eine PYD-Datei?

Eine PYD-Datei kann erstellt werden, indem ein Modul mit einem Namen erstellt wird, z. B. exmaple.pyd. Dieses Modul enthält die gesamte Funktionalität in Form einer oder mehrerer Funktionen, zB PyMod_example(). Wenn das Programm diese Bibliothek einbindet und aufruft, kann dies durch Importieren des Moduls erfolgen und die Funktion PyMod_example() wird ausgeführt.

## Verweise ##

* [Python-Erweiterungen in C/C++ erstellen](https://sebsauvage.net/python/mingw.html)
* [Python (Programmiersprache) - Wikipedia](https://en.wikipedia.org/wiki/Python_(programming_language))

