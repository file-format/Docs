{
  "date" : "2021-24-02",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MKS-Dateiformat",
  "keywords" :[ "mks", "Matroska-Video", "mkv-Format", "Datei", "Format", "Video"],
  "description":"Erfahren Sie mehr über das MKS-Dateiformat für nur von Matroska erstellte Untertitel und APIs, die MKS-Dateien erstellen und öffnen können.",
  "linktitle" :"MKS",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-25-02"
}

## Was ist eine MKS-Datei?

Die MKS-Dateien sind allgemein als Matroska-Dateien bekannt, die nur Untertitel enthalten. Obwohl die Matroska ein allgemeiner Dateicontainer ist, vermeidet sie das Aufbewahren von Informationen bestimmter Formate. Da Untertitel in einigen Audio- oder Videocontainern verwendet werden, achtet Matroska darauf, einige gängige Untertitelformate zu speichern. Es hilft Matroska, mit der Wachstumsrate konsistent zu sein. Sie müssen die unten angegebenen Punkte befolgen, um die Untertitel in Matroska zu speichern:

- Die „.mks“. die Erweiterung wird von der Matroska-Datei verwendet (die nur Untertitel enthält).
- **CodecPrivate** wird verwendet, um alle Codec-bezogenen Informationen zu speichern, die global für einen gesamten Stream gelten.
– Entfernen Sie die Start- und Stoppzeitstempel, die in einem nativen Zeitstempel-Speicherformat verwendet werden. Verwenden Sie stattdessen den Zeitstempel und die Dauer der Blöcke.
- Sie können alles mit einer transparenten Ebene verwenden, einschließlich eines Videos.

## Gängige Untertitelformate

Hier sind einige kurze Hinweise zu häufigeren Untertitelformaten, die in Matroska gespeichert sind:

### Bilder Untertitel
Das VobSub-Untertitelformat ist das erste Bilduntertitelformat, das in Matroska importiert werden kann. Dieses Format wird durch den Export der Untertitel von einer DVD generiert. Die Tracks sollten beim Speichern in Matroska getrennt werden, wenn das VobSub aus mehreren Streams besteht.

### SRT-Untertitel
Das SRT ist das einfachste und grundlegendste aller Untertitelformate. Es besteht aus den folgenden vier Teilen:
 



1. Eine Zahl, die die Reihenfolge des Untertitels angibt.
2. Zeit für das Erscheinen und Verschwinden des Untertitels auf dem Bildschirm.
3. Der Untertitel selbst.
4. Eine Leerzeile, um den Beginn des nächsten Untertitels anzuzeigen.
 



### SSA/ASS-Untertitel
Sub Station Alpha (SSA) ist ein Dateiformat, das vom beliebten Untertitel-Editor SubStation Alpha verwendet wird. Die SSA-Untertitel werden von Fansubbern häufig verwendet. Es hat die Fähigkeit, moderne Funktionen anzuzeigen, z. B. Karaoke, Positionierung, Styling usw.
 



### WebVTT-Untertitel
Das World Wide Web Consortium (W3C) hat das WebVTT entwickelt, das als „Web Video Text Tracks Format“ abgekürzt wird. Dieses Format wird verwendet, um externe Textspurressourcen in Verbindung mit dem HTML-Element auszuzeichnen.

### Untertitel für HDMV-Präsentationsgrafiken
Das HDMV-Präsentationsgrafik-Untertitelformat (HDMV PGS) ist eine Reihe von Bitmaps und wir können es überhaupt nicht als Text bezeichnen. Mit anderen Worten, Sie können sagen, dass es sich nur um eine zeitgesteuerte Abfolge von Grafikbildern handelt. Um die Informationen zu extrahieren, ist die Konvertierung von PGS in SRT ein notwendiger Prozess.

### HDMV-Textuntertitel
Der HDMV-Text ist als Textuntertitelformat bekannt, das auf Blu-rays verwendet wird. Matroska lässt nur den UTF-8-Zeichensatz zu, wenn die TextST-Untertitel gespeichert werden.

### DVB-Untertitel (Digital Video Broadcasting).
Das DVB-Untertitelformat wurde eingeführt, um die Übertragung und Anzeige von mehrsprachigen Untertiteln auf Fernsehsignalen zu regulieren. Ein typisches Untertitelungsformat würde es auch jedem Zuschauer ermöglichen, DVB-untertitelte Übertragungen anzusehen, unabhängig davon, welcher Hersteller die Übertragungssysteme sind.


## Verweise ##

- [Matroska-Untertitel] (https://www.matroska.org/technical/subtitles.html)

