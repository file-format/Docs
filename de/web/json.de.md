---
date: 2019-10-11
keywords: "json, .json, JSON-Dateiformat, So öffnen Sie JSON-Dateien, JavaScript-Objektnotation, JSON-Datenformat, .json-Dateiformat"
Autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: "JSON-Dateiformat - Was ist eine JSON-Datei?"
linktitle: "JSON"
description: "Erfahren Sie mehr über das JSON-Dateiformat und APIs, die JSON-Dateien erstellen und öffnen können."
menu:
  docs:
    parent: "web"
lastmod: 2020-04-12
---

## Was ist eine JSON-Datei?

JSON (JavaScript Object Notation) ist ein offenes Standarddateiformat zum Teilen von Daten, das menschenlesbaren Text zum Speichern und Übertragen von Daten verwendet. JSON-Dateien werden mit der Erweiterung .json gespeichert. JSON erfordert weniger Formatierung und ist eine gute Alternative für [XML](/de/web/xml/). JSON ist von JavaScript abgeleitet, aber ein sprachunabhängiges Datenformat. Das Generieren und Parsen von JSON wird von vielen modernen Programmiersprachen unterstützt. *application/json* ist der für JSON verwendete Medientyp.

## JSON-Dateiformat – Kurze Geschichte

Es bestand ein Bedarf an Server-zu-Client-Kommunikation in Echtzeit, was zur Entwicklung von JSON führte. Das JSON-Format wurde erstmals im März 2001 von Douglas Crockford spezifiziert. JSON basierte auf dem Standard ECMA-262 3rd Edition – Dezember 1999, der eine Teilmenge von JavaScript ist.

Die erste Ausgabe des JSON-Standards ECMA-404 wurde im Oktober 2013 von Ecma International veröffentlicht. RFC 7159 wurde 2014 zur Hauptreferenz für die Verwendung von JSON im Internet. Im November 2017 wurde ISO/IEC 21778:2017 als internationaler Standard veröffentlicht. RFC 8259 wurde am 13. Dezember 2017 von The Internet Engineering Task Force veröffentlicht und ist die aktuelle Version des Internet-Standards STD 90.

## JSON-Dateistruktur

JSON-Daten werden in **Schlüssel/Wert**-Paaren geschrieben. Schlüssel und Wert werden durch einen Doppelpunkt (:) in der Mitte getrennt, wobei sich der Schlüssel links und der Wert rechts befindet. Unterschiedliche Schlüssel/Wert-Paare werden durch ein Komma (,) getrennt. Der Schlüssel ist eine Zeichenfolge, die von doppelten Anführungszeichen umgeben ist, z. B. "Name". Die Werte können von den folgenden Typen sein.

- "Nummer".
- `String`: Folge von Unicode-Zeichen, umgeben von doppelten Anführungszeichen.
- `Boolean`: Wahr oder Falsch.
- `Array`: Eine Liste von Werten, die beispielsweise von eckigen Klammern umgeben sind

```json
[ "Apfel", "Banane", "Orange" ]
```

- „Objekt“: Eine Sammlung von Schlüssel/Wert-Paaren, die beispielsweise von geschweiften Klammern umgeben sind

```json
{"name": "Jack", "age": 30, "favoriteSport": "Fußball"}
```

JSON-Objekte können auch verschachtelt werden, um die Struktur der Daten darzustellen. Unten sehen Sie ein Beispiel für ein JSON-Objekt.

### Beispiel für JSON-Format

```json
{
   "name":"Jack",
   "age":30,
   "contactNumbers":[
      {
         "type":"Home",
         "number":"123 123-123"
      },
      {
         "type":"Office",
         "number":"321 321-321"
      }
   ],
   "spouse":null,
   "favoriteSports":[
      "Football",
      "Cricket"
   ]
}
```

## Was ist die maximale Größe der JSON-Datei?

Die maximale Größe einer JSON-Datei ist praktisch unbegrenzt. Sie kann so lang sein, wie der zu speichernde Inhalt Platz benötigt.

Wenn es darum geht, das JSON-Dateiformat zum Übertragen von Daten über das Internet zu verwenden, muss man auf die verfügbaren Ressourcen des Computers achten. Wenn große JSON-Daten übertragen werden, wird die Übertragung beeinträchtigt, wenn der Client-Browser über begrenzten Arbeitsspeicher verfügt.


Es gibt keine feste Grenze, die durch die Spezifikation definiert ist, aber Sie müssen darauf achten, dass die Ressourcen auf den Computern Ihrer Benutzer nicht erschöpft werden, da dies deren Benutzererfahrung schnell beeinträchtigt und sie Ihre App wahrscheinlich verlassen werden.

## JSON vs. XML

**XML** ist ein weiteres gängiges und weit verbreitetes Dateiformat für den Datenaustausch über das Internet. Beim Datenaustausch zwischen Anwendungen haben Entwickler die Möglichkeit, sowohl XML- als auch JSON-Dateiformate zu verwenden. Aus den folgenden Gründen wird JSON jedoch als die bequemste Methode für den Datenaustausch zwischen Anwendungen über das Internet angenommen.

1. JSON bietet im Vergleich zu XML-Dateiformaten eine klare und leichter lesbare Ansicht der Daten
1. JSON reduziert den Overhead der Datenübertragung über das Internet, da es im Vergleich zu XML weniger Zeichen hat, um denselben Datensatz zu definieren
1. Moderne Programmiersprachen bieten integrierte Parser, um die JSON-Antwort über das Web zu parsen.

## Hast Du gewusst?

Sie können ein Mitwirkender bei FileFormat.com werden, um die Dateiformat-Community mit Ihren Erkenntnissen auf dem Laufenden zu halten. Wenn Sie etwas über JSON- oder Webdateiformate mitteilen möchten, können Sie Ihre Ergebnisse im Abschnitt [Web File Format News](https://news.fileformat.com/t/Web) veröffentlichen, damit die Leute mehr darüber erfahren können.

## Verweise

- [JSON - Wikipedia](https://en.wikipedia.org/wiki/CSS)
- [Eine Einführung in JSON](https://www.digitalocean.com/community/tutorials/an-introduction-to-json)

