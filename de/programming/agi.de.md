{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"AGI-Datei - Asterisk Gateway Interface-Dateiformat",
  "description":"Erfahren Sie anhand von Beispielen und APIs, die AGI-Dateien erstellen und öffnen können, was das AGI-Dateiformat ist.",
  "linktitle" : "AGI",
  "menu" : {
    "docs" : {
      "identifier": "programming-agi",
      "parent" : "programming"
}
},
  "lastmod" : "2022-10-30"
}

## Was ist eine AGI-Datei?

Eine AGI-Datei ist eine Skriptdatei, die vom Open-Source-Telefoniesystem Asterisk verwendet wird. Es enthält Informationen, die zur Automatisierung von Prozessen und des Asterisk-Wählplans verwendet werden können. Mittels AGI-Skriptdateien können Verbindungen zu relationalen Datenbanken wie PostgreSQL oder MySQL hergestellt werden. Darüber hinaus können AGI-Skripte auch für den Zugriff auf andere externe Ressourcen verwendet werden. AGI-Skripte können die Kontrolle über den Wählplan an ein externes AGI-Skript übergeben, sodass Asterisk komplexe Aufgaben ausführen kann.

## AGI-Dateiformat – Weitere Informationen

AGI-Skriptdateien werden als Textdateien gespeichert und können in jedem Texteditor geöffnet werden, um Änderungen vorzunehmen.

### Standardmuster der AGI-Kommunikation

Das AGI-Skript lädt die von Asterisk gesendeten Variablen und deren Werte. Ein allgemeines Aussehen dieser Variablen ist wie folgt.

```
agi_request: test.py
agi_channel: Zap/1-1
agi_language: en
agi_callerid:
agi_context: default
agi_extension: 123
agi_priority: 2
```

Auf diese Variablen folgt eine von Asterisk gesendete Leerzeile, die anzeigt, dass das AGI-Skript nun die Kontrolle über den Wählplan übernehmen kann.

### Programmiersprache für AGI Script Files

AGI-Skripte können normalerweise in Perl, [PHP](/de/programming/php/), [C](/de/programming/c/), Pascal oder Bourne Shell geschrieben werden.

## Verweise

* [Asterisk AGI-Skript] (https://www.oreilly.com/library/view/asterisk-the-future/9780596510480/ch09.html)

