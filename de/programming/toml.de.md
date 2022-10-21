---
date: 2019-10-11
keywords: "toml, .toml, toml-Dateiformat, wie man toml-Dateien öffnet, .toml-Erweiterung, toml-Erweiterung"
Autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: "TOML-Dateiformat"
linktitle: "TOML"
description: "Erfahren Sie mehr über das TOML-Dateiformat und APIs, die TOML-Dateien erstellen und öffnen können."
menu:
  docs:
    parent: "programming"
lastmod: 2020-12-01
---

## Was ist eine TOML-Datei? ##

TOML (Tom's Obvious Minimal Language) ist ein minimales Konfigurationsdateiformat, das die Erweiterung .toml verwendet. TOML zielt darauf ab, leicht lesbar zu sein, Wörterbüchern eindeutig zuzuordnen und einfach in verschiedene Datenstrukturen zu parsen. TOML hat eine Open-Source-Spezifikation, die Community-Beiträge erhalten hat. TOML wird von vielen Programmiersprachen wie C, C#, Dart, Elixir, Erlang, Go, Java, PHP, Python, Ruby, Swift usw. unterstützt. Der MIME-Typ für TOML-Dateien ist *application/toml*.


## TOML-Dateiformat ##

TOML-Dateien bestehen hauptsächlich aus Schlüssel/Wert-Paaren, Abschnitten/Tabellen, Kommentaren und müssen ein gültiges UTF-8-codiertes Unicode-Dokument sein. TOML unterstützt die Datentypen String, Integer, Float, Boolean, Datetime, Array und Table (Hash-Tabelle/Wörterbuch). TOML unterscheidet zwischen Groß- und Kleinschreibung.

### Syntax ###

- **Schlüssel-Wert-Paare**: Schlüssel-Wert-Paare werden durch Gleichheitszeichen (=) getrennt. Jedes Paar muss sich in einer neuen Zeile befinden.

```toml
zuerst = "Tom"
last = "Preston-Werner"
```

- **Kommentare**: Kommentare beginnen mit dem Hash-Symbol (#).

```toml
# Dies ist ein TOML-Dokument.
```

- **Strings**: Strings sind in Anführungszeichen (") eingeschlossen.

```toml
string = "Beispiel-String"
```

- **Mehrzeilige Zeichenfolgen**: Mehrzeilige Zeichenfolgen sind von drei Anführungszeichen (""") umgeben.

```toml
[Heimatadresse]
street = """123 Tornado Alley
Suite 16"""
city = "East Centerville"
Zustand = "KS"
```

- **Ganzzahlen/Floats**

```toml
Ganzzahl = 20
Schwimmer = 20,5
```

- **Booleans**: Booleans sind immer Kleinbuchstaben.

```toml
bool1 = wahr
bool2 = falsch
```

- **Date-Time**: Für DateTime können Sie ein RFC 3339-formatiertes Datum und Uhrzeit verwenden, wie im folgenden Beispiel gezeigt.

```toml
offset_date_time = 1979-05-27 07:32:00Z
local_date_time = 1979-05-27T07:32:00
local_date = 1979-05-27
Ortszeit = 07:32:00
```

- **Arrays**: Arrays werden von eckigen Klammern umgeben, wobei die Elemente durch Kommas (,) getrennt sind.

```toml
Farben = [ "rot", "gelb", "grün" ]
```

- **Tabellen**: Tabellen sind Sammlungen von Schlüssel/Wert-Paaren, die durch Kopfzeilen in einer neuen Zeile definiert sind, die von eckigen Klammern ([]) umgeben sind. Die Tabelle endet, wenn ein neuer Header bereitgestellt wird oder wenn die Datei endet.

```toml
[Heimatadresse]
street = """123 Tornado Alley
Suite 16"""
city = "East Centerville"
Zustand = "KS"

[Büro adresse]
street = """123 Tornado Alley
Suite 16"""
city = "East Centerville"
Zustand = "KS"
```

Inline-Tabellen sind von geschweiften Klammern ({}) umgeben, wobei jedes Schlüssel/Wert-Paar durch Komma (,) getrennt ist.

```toml
name = { first = "Tom", last = "Pitt" }
```

## Verweise ##

- [TOML - Wikipedia](https://en.wikipedia.org/wiki/TOML)
- [TOML](https://toml.io/de/)

