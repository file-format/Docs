{
  "date" : "2022-04-01",
  "keywords" :[ "nkit-Datei", "nkit-Dateiformat", "was ist eine nkit-Datei", "Datei", "nkit-Beispiel", "nkit-Dateierweiterung", "Erweiterung", "Format", "nkit-Fußzeile", "Datei Format von nkit"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Erfahren Sie mehr über das NKIT-Dateiformat und APIs, die NKIT-Dateien erstellen und öffnen können.",
  "title" :"NKIT - Disk-Image-Dateiformat",
  "linktitle" : "NKIT",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2022-04-01"
}

## Was ist eine NKIT-Datei?

Eine NKIT-Datei ist ein Disk-Image von Daten, die aus NintendoWii- und GameCube-Spielen extrahiert wurden. NKIT ist für das Nintendo Toolkit-Format. Die resultierende Komprimierungsdatei [ISO](/de/compression/iso/) verwendet die Hauptdaten dieser Spiele, um mit Emulatorprogrammen wie Dolphin, Swiss und Nintendont ausgeführt zu werden. NKit ist in rohen (iso) und komprimierten (gcz) Dateiformaten erhältlich, die beide unter Berücksichtigung der Spielbarkeit und Größe entwickelt wurden.

## NKIT-Dateiformat

Das NKit-Dateiformat ist ein verlustfreies Format und wird zum Verkleinern und Wiederherstellen von Nintendo Wii- und GameCube-Images verwendet. Die Formate sind in ISO- und GCZ-Dateiformaten für alle GameCube- und Wii-Spiele verfügbar.

|System |Format |Hardware unterstützt |Dolphin unterstützt |Wiederherstellbar 1:1 |Hinweise|
---|---|---|---|---|---|
|GameCube| nkit.iso| Ja |Ja| Ja |Wie komprimierte GameCube-ISO|
|GameCube| nkit.gcz| Nein| Ja| Ja |GCZ ist Dolphins eigenes blocksuchbares Komprimierungsformat|
|Wii| nkit.iso| Nein Ja| Ja| RVT-H-Format nur in Dolphin| abspielbar
|Wii| nkit.gcz| Nein Ja| Ja| RVT-H in GCZ nur in Dolphin spielbar|

### NKIT-Header

Der Header des NKIT-Dateiformats lautet wie folgt.

|Offset |Länge |Name|
---|---|---|
|0x200 |0x4 |NKit-Header 'NKIT'|
|0x204 |0x4 |NKit-Version ' v01'|
|0x208 |0x4 |Quellbild original CRC32|
|0x20C |0x4 |NKit CRC – macht den CRC32 der NKit-Datei gleich dem Quell-CRC bei 0x208 (bei 0x4 in GCZ)|
|0x210 |0x4 |Quellbildlänge|
|0x214 |0x4 |Erzwungene Junk-ID (Wenn Disc-ID unterschiedlich ist – selten – nur GameCube)|
|0x218 |0x4 |Wii-Update-Partition CRC32, falls beim Konvertieren entfernt|

## Verweise ##

* [NKIT-Dateiformat - von gbatemp](https://wiki.gbatemp.net/wiki/NKit/NKitFormat)

