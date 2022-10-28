{
  "date" : "2021-06-09",
  "keywords" :[ "cda", "Datei", "Erweiterung", "Format", "was ist eine cda-Datei", "Musik", "cda-Dateiformat", "Spezifikation des cda-Dateiformats"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Erfahren Sie mehr über das CDA-Dateiformat und APIs, die CDA-Dateien erstellen, konvertieren und öffnen können.",
  "title" :"CDA - CD-Audio-Track-Shortcut-Datei",
  "linktitle" : "CDA",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-06-09"
}

## Was ist eine CDA-Datei?
Eine Datei mit der Erweiterung .cda ist eine kleine Stub-Datei, die von Microsoft Windows für jeden Audiotrack auf einer Audio-CD generiert wird. Diese Dateien enthalten typische Informationen wie Titelzeiten und eine Windows-Verknüpfung, mit der Benutzer auf die spezifischen Audiospuren zugreifen können. Die CDA-Dateien sind keine Musik, aber sie verweisen auf eine Musikdatei, die irgendwo auf dem Speicher vorhanden ist. Wir können es als Abkürzung einer Audiodatei bezeichnen, die sich auf einer CD befindet.
## CDA-Dateiformat
Das CDA-Dateiformat wird verwendet, um einem Computer mitzuteilen, welche Audiodatei auf einer CD wiedergegeben werden soll. Daher werden die CDA-Dateien getrennt von einer CD, die sie darstellen, nutzlos. Die CDA-Dateien werden allgemein als RIFF-Ressourcen betrachtet. In der aktuellen Version der .cda-Datei gibt es nur einen Chunk namens „CDDA“, der nur einen Datenblock namens „FMT“ enthält. Dieser Block ist 24 Bytes lang. Die von Windows erstellte Kennung wird vom CD-Laufwerk von Windows 95 und Windows 98 verwendet, und sein Player kann keine Verbindung zu FreeDB oder CDDB herstellen. Damit es Songtitel und den Künstlernamen anzeigen kann, müssen Sie diese Informationen manuell in die Datei cdplayer.ini eintragen.

### Organisation einer CDA-Datei
Die folgende Tabelle zeigt die Informationen über typische Offsets:
| Offset | Länge | Inhalt |
---|---|---|
| 0x00 | 4 | die 4 ASCII-Zeichen "RIFF" |
| 0x04 | 4 | die Größe des folgenden Chunks: immer 36 (44 - 8), auf 4 Bytes (Intel-Reihenfolge) |
| 0x08 | 4 | Chunk-Identifikator: die 4 ASCII-Zeichen "CDDA" |
| 0x0C | 4 | die 3 ASCII-Zeichen "fmt" gefolgt von einem Leerzeichen |
| 0x10 | 4 | Länge des Chunks: immer 24, auf 4 Bytes (Intel-Reihenfolge) |
| 0x14 | 2 | Version des CD-Formats, auf 2 Bytes (Intel-Reihenfolge). Im Mai 2006 immer gleich 1. |
| 0x016 | 2 | Nummer des Bereichs, auf 2 Bytes (Intel-Reihenfolge). Die erste Spur hat die Nummer 1. |
| 0x18 | 4 | Kennung, die von Windows für cdplayer.exe berechnet wird. |
| 0x1c | 4 | Bereichs-Offset, in Anzahl der Frames (Intel-Reihenfolge) |
| 0x20 | 4 | Dauer des Tracks, Gesamtzahl der Frames (Intel-Reihenfolge) |
| 0x24 | 1 | Bereichsposition: Rahmen |
| 0x25 | 1 | Bereichsposition: Sekunden |
| 0x26 | 1 | Bereichsposition: Minuten |
| 0x27 | 1 | ein Nullbyte (binärer Wert 0) |
| 0x28 | 1 | Dauer des Tracks: Frames |
| 0x29 | 1 | Dauer des Titels: Sekunden |
| 0x2a | 1 | Dauer des Titels: Minuten |
| 0x2b | 1 | ein Nullbyte (binärer Wert 0) |

## Verweise ##

* [.cda-Datei – von Wikipedia](https://en.wikipedia.org/wiki/.cda_file)


