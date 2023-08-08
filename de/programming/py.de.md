---
date: 2019-10-11
keywords: "py, python, .py, py-Dateiformat, wie man eine py-Datei öffnet, wie man py-Dateien ausführt, wie man Python-Dateien ausführt, wie man Python ausführt"
Autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: "PY-Dateiformat"
linktitle: "PY"
description: "Erfahren Sie mehr über das PY-Dateiformat und APIs, die PY-Dateien erstellen und öffnen können."
menu:
  docs:
    parent: "programming"
lastmod: 2020-25-11
---

## Was ist eine PY-Datei? ##

Die Dateien mit der Erweiterung .py enthalten den Python-Quellcode. Die Python-Sprache ist heutzutage eine sehr berühmte Sprache geworden. Es kann für Systemskripting, Web- und Softwareentwicklung und Mathematik verwendet werden. Python unterstützt plattformübergreifende Kompatibilität; bedeutet, dass die in Python entwickelten Anwendungen auf verschiedenen Plattformen wie Windows, MAC, Linux, Raspberry Pi usw. funktionieren können. Python bietet eine einfache und leicht lesbare Syntax, die der englischen Sprache ähnelt. Entwickler können eine vernünftige Softwareanwendung schreiben, indem sie ein paar Zeilen Python-Code schreiben. Da Python auf einem Interpretersystem läuft, kann der Code ausgeführt werden, sobald er geschrieben ist, was ihn sehr gut für das Prototyping macht.

## Kurze Geschichte ##

Python wurde Ende der 1980er Jahre von Guido van Rossum als Nachfolger der Programmiersprache ABC konzipiert. Die Implementierung begann im Dezember 1989 mit Van Rossum als alleinigem Hauptentwickler. Er arbeitete bis zum 12. Juli 2018 an Python. Im Januar 2019 wählten die aktiven Python-Kernentwickler einen fünfköpfigen „Steering Council“, bestehend aus Nick Coghlan, Brett Cannon, Carol Willing, Barry Warsaw und Van Rossum, um das Projekt zu leiten.

### Versionen ###

- Python 2.0 wurde am 16. Oktober 2000 veröffentlicht.
- Python 3.0 wurde am 3. Dezember 2008 veröffentlicht.

## So führen Sie eine Py-Datei aus ##

Um die installierte Version von Python zu überprüfen, können Sie den folgenden Befehl verwenden:

```cmd
python --version
```

Dadurch wird die Version auf der Konsole wie ausgegeben

```cmd
Python 3.7.4
```

Wenn Python nicht auf Ihrem Computer installiert ist, können Sie zu [python.org](https://www.python.org/) gehen und Python für Ihr relevantes Betriebssystem herunterladen und installieren.

Um ein Python-Skript auszuführen, können Sie den folgenden Befehl verwenden:

```cmd
python helloworld.py
```

*helloworld.py* ist eine Skriptdatei, die den folgenden Code enthält

```py
print("Hello World from Python")
```

Dadurch wird Folgendes im Konsolenfenster gedruckt.

```cmd
Hello World from Python
```

Hinweis: Wenn Sie IDEs verwenden, bieten diese Schaltflächen auf dem Bildschirm oder verschiedene Tastenkombinationen zum Ausführen von Python. Beispielsweise wird in PyCharm mit dem Editor in PyCharm ein Play-Button angezeigt, mit dem Sie das Python-Skript ausführen können.

## PY-Dateiformat ##

Python wurde auf Lesbarkeit ausgelegt und hat Ähnlichkeiten mit Englisch und Mathematik. Python verwendet neue Zeilen, um den vollständigen Befehl anzuzeigen, im Gegensatz zu Semikolons oder Klammern, die in anderen Sprachen verwendet werden. Für Bereiche, Schleifen und Funktionen verlässt sich Python auf Einrückungen und Leerzeichen im Gegensatz zu geschweiften Klammern, die in anderen Sprachen verwendet werden.

### Syntax ###

Das Folgende ist ein Beispiel für die Python-Syntax.

```py
print("Hello World")

#Variables
name = "John"
age = 25
print(name)
print(age)

#While Loop
i = 1
while i < 3:
  print(i)
  i += 1
  
#For Loop
names = ["John", "Harry", "Tom"]
for name in names:
  print(name)
```

## Verweise ##

- [Python (Programmiersprache) - Wikipedia](https://en.wikipedia.org/wiki/Python_(programming_language))

