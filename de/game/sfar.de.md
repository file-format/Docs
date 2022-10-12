{
  "date" : "2021-10-20",
  "keywords" :[ "sfar-Datei", "sfar-Dateiformat", "was ist eine sfar-Datei", "Datei", "sfar-Beispiel", "Mass Effect 3 DLC-Dateierweiterung", "Erweiterung", "Format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Erfahren Sie mehr über das Mass Effect 3 SFAR-Dateiformat und APIs, die SFAR-Dateien erstellen und öffnen können.",
  "title" :"SFAR - Mass Effect 3 DLC-Datei",
  "linktitle" :"SFAR",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-10-20"
}

## Was ist eine SFAR-Datei?

Eine Datei mit der Erweiterung .sfar ist eine Spieldatendatei, die von Mass Effect 3 verwendet wird, um seinen DLC (herunterladbare Inhalte) in einem komprimierten, proprietären Archiv zu speichern. Mass Effect 3 ist ein Spiel, das von Electronic Arts, einem führenden Spieleentwicklungsunternehmen, entwickelt wurde. Die in einer SFAR-Datei gespeicherten DLC-Inhalte werden verwendet, um das Spiel um zusätzliche Inhalte und Funktionen zu erweitern.

## SFAR-Dateiformat - Weitere Informationen

SFAR-Dateien werden als komprimierte Archivdateien im Binärdateiformat gespeichert/gespeichert. Diese verwenden sowohl LZX- als auch LZMA-Komprimierungsalgorithmen zum Komprimieren der Inhalte. SFAR-Dateien können mit dem DLC-Editor geöffnet werden, der mit ME3 Explorer geliefert wird. Zusätzlich zu SFAR kann der DLC-Editor andere Spieldateien wie [PCC](/de/game/pcc/) extrahieren.

## Spezifikationen des SFAR-Dateiformats

Eine SFAR-Datei ist in die folgenden vier Hauptabschnitte unterteilt.

### SFAR-Header

Der SFF-Header enthält Informationen zu den verschiedenen Chunks, aus denen die Datei besteht.

### SFAR-Dateitabelle

Die SFAR-Dateitabelle enthält eine Liste von Dateieinträgen, wobei jeder Eintrag 30 Bytes lang ist.

### Blockgrößentabelle

Die Blockgröße enthält mehrere Einträge, wobei jeder Eintrag 2 Bytes lang ist. Dieser Wert gibt die Blockgröße an, die einem Eintrag in der Dateitabelle entspricht.

### Blöcke

Block Chunks in einer SFAR-Datei enthalten die Daten in der SFAR-Datei.

## Verweise

* [DLC SFAR-Dateiformat - Forschung](https://www.tapatalk.com/groups/me3explorer/current-research-dlc-sfar-fileformat-t629.html)

