{
  "date" : "2021-09-08",
  "keywords" :[ "pcc-Datei", "pcc-Dateiformat", "was ist eine pcc-Datei", "Datei", "pcc-Beispiel", "pcc-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Erfahren Sie mehr über das Mass Effect PCC-Dateiformat und APIs, die PCC-Dateien erstellen und öffnen können.",
  "title" :"PCC - Mass Effect Package-Datei",
  "linktitle" : "PCC",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## Was ist eine PCC-Datei?

Eine Datei mit .pcc ist eine [Mass Effect Game](https://www.ea.com/games/mass-effect/mass-effect-3)-Datei, die Spieldaten enthält, um Spielinhalte wie Modelle, Texturen und zu ändern Räume. Mass Effect 2 und 3 sind erste Shooter-Spiele, die auf der Gaming-Engine Unreal Engine 3 basieren. Das Spiel wurde ursprünglich von [Bioware](https://www.bioware.com/about/) entwickelt, die den Großteil der Spielressourcen in ihrem proprietären PCC-Dateiformat behielten. Bioware wurde von Electronic Arts übernommen, einem weltweit führenden Verlag für interaktive Unterhaltung.

## PCC-Dateiformat - Weitere Informationen

PCC-Dateien enthalten komprimierte und/oder unkomprimierte Strukturen, die zur gesamten Dateiorganisation beitragen.

### Komprimierte PCC-Struktur

Eine komprimierte PCC-Datei besteht aus Tabellen und Daten, die in Chunks segmentiert sind. Jeder Chunk enthält eine variable Anzahl komprimierter Blöcke.

* `Chunks Header` - Ein 16 Byte langer allgemeiner Header, der Informationen über die Chunks enthält.
* „Chunk Header“ – Ein 16-Byte-Header, der Informationen über die komprimierten Rohdaten enthält, die in der Blockform enthalten sind.

### Unkomprimierte PCC-Struktur

Unkomprimierte PCC-Dateien sind in die folgenden fünf Teile unterteilt.

* `Header` - enthält grundlegende Informationen über die Struktur der PCC-Datei.
* „Namenstabelle“ – enthält den im Paket gefundenen Namen, einschließlich Importklassen, Exporte und Exporteigenschaften.
* `Import Table` - enthält alle vom PCC importierten Klassen und Objekte.
* `Export Table` - enthält alle im Paket gespeicherten Objekte. Jeder Export kann in der Größe variieren.

## Verweise

* [Me3Explorer - PCC-Dateiformat](https://me3explorer.fandom.com/wiki/PCC_File_Format)
* [Mass Effect-Spiel] (https://www.ea.com/games/mass-effect/mass-effect-3)
* [Bioware](https://www.bioware.com/about/)

