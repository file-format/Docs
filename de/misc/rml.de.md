{
  "date" : "2022-01-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RML - Elixir-Berichtsvorlagendatei",
  "description":"Erfahren Sie mehr über RML-Dateien und APIs, die RML-Dateien erstellen und öffnen können.",
  "linktitle" :"RML",
  "menu" : {
    "docs" : {
"identifier": "misc-rml",
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-12"
}

## Was ist eine RML-Datei?

Eine RML-Datei ist eine Berichtsvorlagendatei mit der Berichts-Engine [Elixir Repertoire](https://elixirtech.com/repertoire-2/). Die Vorlagendatei wird zum Generieren von Berichten verwendet, wobei die Datenquelle mit dem Elixir-Dateisystem verbunden ist. Die Daten werden gelesen und in die RML-Vorlagendatei eingefügt und können in eine Reihe verschiedener Dateiformate wie [PDF](/de/pdf/), [RTF](/de/word-processing/rtf/) und Tabellenkalkulation [XLS] exportiert werden. (/de/spreadsheet/xls/). Die Elixir Repertoire Reporting Engine kann mit einer Vielzahl von JDBC-Datenquellen verbunden werden.

## RML-Dateiformat

Die Details der internen Dateistruktur des RML-Dateiformats sind nicht öffentlich verfügbar. Die Dateien werden intern von der Elixir Repertoire-Anwendung generiert und gespeichert, um Berichte mit Daten aus den verbundenen Datenquellen zu erstellen. Die RML-Vorlagendatei enthält das Gesamtlayout und Platzhalterinformationen des Abschlussberichts, der aus den Daten generiert werden soll.

## Wie erstelle ich eine RML-Vorlagendatei?

Um eine RML-Vorlage in Elixir Repertoire zu generieren, können die folgenden Schritte befolgt werden.

1. Verbinden Sie eine JDBC-Datenquelle mit dem Dateisystem.
1. Starten Sie den Berichtsvorlagen-Assistenten
1. Verwenden Sie die Software, um die .ds-Datei der Datenquelle zu suchen
1. Wählen Sie tabellarischen Bericht als Exportoption
1. Wählen Sie die Felder aus, die in die Berichtsvorlage aufgenommen werden sollen
1. Wenn Sie schließlich auf die Schaltfläche „Fertig stellen“ klicken, wird First report.rml zum Repository hinzugefügt und geöffnet, um die Registerkarte „Layout“ anzuzeigen.

## Verweise

* [Elixir-Repertoire](https://elixirtech.com/repertoire-2/)

