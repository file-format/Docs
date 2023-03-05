{
  "date" : "2023-01-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Erfahren Sie mehr über das Unreal Static Meshes VPK-Dateiformat und APIs, die VPK-Dateien erstellen und öffnen können.",
  "title" :"VPK-Datei - Unreal Static Meshes-Datei",
  "linktitle" : "VPK",
  "menu" : {
    "docs" : {
      "identifier":"game-vpk",
      "parent" : "game"
}
},
  "lastmod" : "2023-01-16"
}

## Was ist eine VPK-Datei?

Eine .vpk-Datei ist ein Dateiformat, das von der **Source Engine**, einer von Valve Corporation entwickelten Spiel-Engine, verwendet wird. VPK-Dateien werden zum Verpacken von Spielinhalten wie Modellen, Texturen und Sounds verwendet und werden häufig in Spielen wie Team Fortress 2, Left 4 Dead und Counter-Strike: Global Offensive verwendet. Die Dateien können mit einer Vielzahl von Tools wie GCFScape und VPK Tool geöffnet und extrahiert werden.

## VPK-Dateiformat - Weitere Informationen

VPK-Dateien werden als Binärdateien auf der Disc gespeichert. Eine einzelne vpk-Datei kann Teil eines VPK-Pakets sein oder als unabhängige VPK-Rohdatei fungieren. Zu den Informationen, die in einer VPK-Datei gespeichert werden können, gehören Karten, Materialien, Spielinhalte und Choreografieszenen.

### Wie erstelle ich eine VPK-Datei?

Abhängig von den verfügbaren Tools gibt es mehrere Möglichkeiten, eine .vpk-Datei zu erstellen.

1. „Verwendung des VPK-Tools“: Dies ist ein Befehlszeilentool, das zum Erstellen und Extrahieren von VPK-Dateien verwendet werden kann. Eine VPK-Datei kann mit dem folgenden Befehl erstellt werden:
```
"vpk.exe -M <directory> <output_file.vpk>"
```
Dadurch wird eine VPK-Datei aus dem angegebenen Verzeichnis erstellt und als angegebene Ausgabedatei gespeichert.

1. `Verwenden des Hammer Editors:` Der Hammer Editor ist ein im Source SDK enthaltenes Tool, das zum Erstellen und Bearbeiten von Levels für Spiele verwendet werden kann, die die Source-Engine verwenden. Es enthält auch die Möglichkeit, VPK-Dateien zu erstellen, indem Sie mit der rechten Maustaste auf einen Ordner auf der Registerkarte „Dateisystem“ klicken und „VPK erstellen“ auswählen.

1. „Valve's VPK Creator verwenden:“ Dies ist ein von Valve entwickeltes Tool, das zum Verpacken und Verteilen von Spielinhalten verwendet wird. Dieses Tool kann zum Erstellen von VPK-Dateien verwendet werden und ist auch das offizielle Tool zum Erstellen von VPK-Dateien.

## Verweise

* [Ventilsoftware](https://www.valvesoftware.com/en/)
* [VPK-Entwicklerressourcen](https://developer.valvesoftware.com/wiki/GCF)

