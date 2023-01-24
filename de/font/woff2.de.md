{
  "date" : "2023-01-10",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"WOFF2-Datei - Web Open Font Format 2.0-Datei",
  "description":"Erfahren Sie, was eine WOFF2-Datei und APIs sind, die eine WOFF2-Datei erstellen und öffnen können.",
  "linktitle" : "WOFF2",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2023-01-10"
}

## Was ist eine WOFF2-Datei?

WOFF2 ist ein Schriftdateiformat, das eine stärker komprimierte Version des Web Open Font Format (WOFF) ist. Es wurde entwickelt, um die Dateigröße von Webfonts zu reduzieren, damit sie schneller geladen werden und weniger Bandbreite verbrauchen. WOFF2 verwendet einen Komprimierungsalgorithmus namens Brotli, um die Schriftdaten zu komprimieren, was zu Dateigrößen führen kann, die erheblich kleiner sind als die entsprechenden [WOFF](/de/font/woff/)-Schriftarten. Dieses Format wird von den meisten modernen Webbrowsern unterstützt, darunter Chrome, Firefox, Safari, Opera und Edge (ab Version 14).

## WOFF2-Dateiformat - Weitere Informationen

Die interne Dateistruktur einer WOFF2-Schriftartdatei besteht aus mehreren verschiedenen Teilen, einschließlich einer Kopfzeile, Metadaten, einem Tabellenverzeichnis und den Schriftdaten selbst.

1. Der Header enthält Informationen über das Gesamtformat der Datei, einschließlich der Versionsnummer und der Anzahl der Tabellen, die in der Datei vorhanden sind.

1. Der Abschnitt „Metadaten“ enthält Informationen wie Schriftartnamen, Copyright und andere schriftbezogene Informationen.

1. Das Tabellenverzeichnis enthält Informationen über die verschiedenen Tabellen, aus denen die Schriftart besteht, einschließlich ihrer Position in der Datei und ihrer Länge.

1. Die Schriftartdaten selbst sind in mehrere verschiedene Tabellen unterteilt, von denen jede spezifische Informationen über die Schriftart enthält, wie z. B. ihre Zeichen und ihre entsprechenden Glyphen. Diese Tabellen können enthalten:

* Die 'glyf'-Tabelle enthält die eigentlichen Schriftumrisse, einschließlich der Form und Größe jedes Zeichens.
* Die 'head'-Tabelle enthält allgemeine Informationen über die Schriftart, wie z. B. Versionsnummer, Designgröße usw.
* Die 'hmtx'-Tabelle enthält Informationen über die Metrik der Schriftart, einschließlich der Breite und Position der Zeichen.
* Jede Tabelle wird komprimiert und im WOFF2-Dateiformat gespeichert, nachdem sie den Kodierungsprozess abgeschlossen hat.

Die Struktur insgesamt ist darauf ausgelegt, ein schnelles Parsen und Decodieren zu ermöglichen, sodass Webbrowser die Schriftart schnell und effizient laden und auf einer Website anzeigen können.

### WOFF2-Kopfzeile
Der WOFF-Header besteht aus einer identifizierenden Signatur, die die Art der in der Datei enthaltenen Daten angibt. Der WOFF-Header zusammen mit seinen Feldern sieht wie folgt aus.

|Typ|Feldname|Beschreibung|
---|---|---|
|UInt32|Signatur |0x774F4632 'wOF2' |
|UInt32| Flavor |Die "sfnt-Version" der Eingabeschriftart.|
|UInt32| length |Gesamtgröße der WOFF-Datei.|
|UInt16| numTables |Anzahl der Einträge im Verzeichnis der Schrifttabellen.|
|UInt16| reserviert |reserviert; auf Null setzen.|
|UInt32| totalSfntSize |Gesamtgröße, die für die unkomprimierten Schriftartdaten benötigt wird, einschließlich des sfnt-Headers, des Verzeichnisses und der Schriftarttabellen (einschließlich Auffüllen).|
|UInt32| totalCompressedSize Gesamtlänge des komprimierten Datenblocks.|
|UInt16| majorVersion |Hauptversion der WOFF-Datei.|
|UInt16| minorVersion |Nebenversion der WOFF-Datei.|
|UInt32| metaOffset |Offset zum Metadatenblock, vom Anfang der WOFF-Datei.|
|UInt32| metaLength |Länge des komprimierten Metadatenblocks.|
|UInt32| metaOrigLength |Unkomprimierte Größe des Metadatenblocks.|
|UInt32| privOffset |Offset zum privaten Datenblock, vom Anfang der WOFF-Datei.|
|UInt32| privLength |Länge des privaten Datenblocks.|


## Verweise
* [w3 WOFF2-Dateiformat](https://www.w3.org/TR/WOFF2/)

