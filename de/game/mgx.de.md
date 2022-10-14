{
  "date" : "2021-09-08",
  "keywords" :[ "mgx-Datei", "mgx-Dateiformat", "was ist eine mgx-Datei", "Datei", "mgx-Beispiel", "mgx-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Erfahren Sie mehr über das MGX-Dateiformat von Age of Empires 2 Expansion Replay und APIs, die MGX-Dateien erstellen und öffnen können.",
  "title" :"MGX - Wiederholung der Erweiterung Age of Empires 2",
  "linktitle" :"MGX",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## Was ist eine MGX-Datei?

Eine Datei mit der Erweiterung .mgx ist eine aufgezeichnete Datei für das Spiel Age of Empires II: The Conquerors, die im Programm Age of Empires II wiedergegeben werden kann. Es enthält eine vollständige Aufzeichnung der vom Benutzer gespielten Kampagne. Es kann innerhalb des Programms Age of Empires II geladen und abgespielt werden. Nach der Wiedergabe zeigt das Spiel alle Ereignisse und Szenarien, die der Benutzer für die Kampagne geplant und gespielt hat.

## MGX-Dateiformat - Weitere Informationen

Das interne Dateiformat der MGX-Datei wurde ausgearbeitet und ist als teilweise validierte Information auf [Age of Empires 2: The Conquerors – Savegame File Format Specification] (https://github.com/stefan-kolb/aoc-mgx- Format). Die Spezifikationen beschreiben die Details in den folgenden Abschnitten.

### Strukturdefinitionen

Es wird angenommen, dass die Strukturdefinitionen des GPX-Dateiformats auf den [BinData Ruby Gem-Deklarationen] (https://github.com/dmendel/bindata/wiki) basieren, die eine Möglichkeit bieten, strukturierte Binärdaten zu lesen und zu schreiben. Dadurch kann der Programmierer das Format der Binärdaten angeben, die dann von BinData gelesen und geschrieben werden.

### MGX-Nachrichtenübermittlung

Die MGX-Nachrichtenübermittlung basiert auf zwei Arten von Nachrichten.

* GAMESTART - gibt die Spielstartbefehle an und ist bisher nicht validiert
* CHAT - beschreibt die Chatnachrichten im Spiel. Sowohl Spieler als auch das Spiel selbst (Gaia) können In-Game-Nachrichten senden.

### SPIELAKTIONEN

Es gibt mehrere [GAMEPLAY-Aktionen](https://github.com/stefan-kolb/aoc-mgx-format/blob/master/README.md#actions), die abgerufen wurden und deren Details verfügbar sind.

## Verweise

* [Age of Empires 2: The Conquerors – Savegame-Dateiformatspezifikation](https://github.com/stefan-kolb/aoc-mgx-format)

