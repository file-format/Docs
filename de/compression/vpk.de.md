{
  "date" : "2022-03-01",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VPK-Datei - PlayStation Vita-Anwendungspaket-Dateiformat",
  "description":"Erfahren Sie mehr über das VPK-Dateiformat und APIs, die VPK-Dateien erstellen und öffnen können.",
  "linktitle" : "VPK",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-03-01"
}

## Was ist eine VPK-Datei?

Eine Datei mit der Erweiterung .vpk ist eine komprimierte Archivpaketdatei, die zum Installieren von Drittanbieter-Apps auf der Sony PlayStation Vita-Spielekonsole verwendet wird. Diese Dateien können nur auf der Jailbreak Vita PlayStation von HENkaku installiert werden, die es PS Vita und PSTV ermöglicht, angepasste, von Benutzern erstellte Inhalte zu verwenden. Eine VPK-Archivdatei enthält alle Inhalte, aus denen das Spiel besteht, einschließlich Bildern wie [PNG](/de/image/png/)-Dateien, Einstellungsdateien wie [.bin](/de/disc-and-media/bin/) und alle Konfigurationen im Dateiformat [XML](/de/web/xml/).

## VPK-Dateiformat

VPK-Dateien werden als standardmäßig komprimierte [ZIP](/de/compression/zip/)-Archive auf Disc gespeichert. Diese können mehrere Ordner und andere zugehörige Dateien für die Apps von Drittanbietern enthalten, die auf der Vita Gaming Console installiert werden sollen. Um den Inhalt der VPK-Paketdatei anzuzeigen, benennen Sie die Erweiterung von .vpu in .zip um und extrahieren Sie den Inhalt mit standardmäßigen Dekomprimierungsprogrammen wie WinZip oder WinRAR.

Valvesoftware bietet detaillierte Informationen zum [VPK-Dateiformat](https://developer.valvesoftware.com/wiki/VPK_File_Format), auf die aus Entwicklersicht verwiesen werden kann.

## Wie installiere ich VPK-Dateien?

Die VPK-Dateien können über das Befehlszeilendienstprogramm VPK.exe installiert werden. Auf Windows-Betriebssystemen können Dateien in der Datei vpk.exe abgelegt werden, die eine \*.vpk zurückgibt, die alle gepackten Dateien enthält. Alternativ kann das Befehlszeilentool wie folgt verwendet werden.

### VPK erstellen und Dateien hinzufügen

```
vpk <dirname>
```

### VPK-Dateien extrahieren

```
vpk x <vpkfile> <filename1> <filename2> ...
```

## VPK-Viewer

* [VRF VPK Viewer](https://github.com/SteamDatabase/ValveResourceFormat)

## Verweise

* [VPK-Dateiformat](https://developer.valvesoftware.com/wiki/VPK_File_Format)
* [VPK-Dateien](https://developer.valvesoftware.com/wiki/VPK)

