---
date: 2022-05-09
Autor:
  display_name: Kashif Iqbal
draft: false
toc: true
title: "PYI-Dateiformat - Definition der Python-Schnittstelle"
linktitle: "PYI"
description: "Erfahren Sie mehr über das PYI-Dateiformat und APIs, die PYI-Dateien erstellen und öffnen können."
menu:
  docs:
    parent: "programming"
lastmod: 2022-05-09
---

## Was ist eine PYI-Datei?

Eine PYI-Datei ist eine Python-Schnittstellendefinitionsdatei, die eine Code-Stub-Referenz für die Implementierung der Schnittstelle enthält. Jedes Python-Modul wird als .pyi-Stub dargestellt, bei dem es sich um eine normale Python-Datei handelt, jedoch mit leeren Methoden. Die Syntax von PYI-Dateien ist die gleiche wie die eines regulären Python-Moduls. Die Implementierung der leeren Methoden wird dem Endbenutzer überlassen, um das spezifische Ziel zu erreichen, für das das Modul geschrieben wurde. Darin unterscheiden sich PYI-Dateien von [PY](/de/programming/py/)-Dateien, die die vollständige Implementierung des Programms enthalten. PYI-Dateien können mit Texteditoren wie Notepad, Notepad++, Microsoft Visual Studio Code und JetBrains PyCharm geöffnet werden.

## PYI-Dateiformat

PYI-Dateien werden als reine Textdateien gespeichert, die mit jedem Texteditor geöffnet werden können. Python ist eine Interpretersprache, die eine Typprüfung durchführt, wenn der Code ausgeführt wird. In einem solchen Fall sind PYI-Dateien insofern von Vorteil, als Entwickler die Typen eines Moduls manuell definieren und überprüfen können, während sie die Anwendung schreiben.

## Verweise ##

* [Schnittstellen - Java](https://en.wikipedia.org/wiki/Interface_(Java))
* [PYM-Interpreter](https://github.com/interpreters/pym)

