{
  "date" : "2020-08-20",
  "keywords" :[ "woff-Datei", "woff-Dateiformat", "was ist eine woff-Datei", "Datei", "woff-Beispiel", "woff-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"WOFF - Web-offenes Dateiformat",
  "description":"Eine WOFF-Datei ist ein offenes Schriftformat, das im Web Open Font Format erstellt wurde.",
  "linktitle" : "WOFF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-09-30"
}

## Was ist eine WOFF-Datei?

Eine Datei mit der Erweiterung .woff ist eine Webfont-Datei, die auf dem Web Open Font Format (WOFF) basiert. Es verfügt über einen formatspezifischen komprimierten Container, der entweder auf TrueType- (.TTF) oder OpenType- (.OTT) Schriftarten basiert. WOFF wurde mit dem Ziel eingeführt, Webfonts von Fontdateien zu unterscheiden, die in Desktop-Anwendungen verwendet werden. Darüber hinaus zielt das Format darauf ab, die Latenz bei der Übertragung von Schriftarten vom Server zum Computer des Clients über das Netzwerk zu reduzieren. Es sind mehrere Tools verfügbar, die WOFF-Dateien in TTF- und andere Schriftartdateiformate konvertieren können.

## **WOFF-Dateiformat**

Das WOFF-Schriftformat komprimiert Schriftdatentabellen von tabellenbasierten sfnt-Strukturen, die in verschiedenen Schriftarten wie TrueType, OpenType und Open Font Format verwendet werden. Es ist wie ein Container für diese Schrifttypen und bietet auch Platz, um die Metadaten der Schriftart und Daten zur privaten Nutzung aufzunehmen, die in den Container aufgenommen werden sollen. Konverter verwenden die sfnt-Dateien in eine Datei im WOFF-Format und Benutzeragenten stellen die codierte Datei zur Verwendung mit dem Webdokument wieder her. Es ist anzumerken, dass die wiederhergestellten Schriftartdaten in allen Aspekten exakt mit dem eingegebenen Schriftartformat übereinstimmen.

WOFF-Datei-Dienstprogramme enthalten oft zusätzliche Funktionen wie Glyph-Subsetting, Validierung oder das Hinzufügen von Schriftartfunktionen, dies ist jedoch nicht erforderlich. Sowohl der Ersteller als auch der Benutzer müssen sicherstellen, dass die Gültigkeit der zugrunde liegenden Zeichensatzdaten erhalten bleibt.

### WOFF-Dateistruktur

Die WOFF-Dateistruktur ähnelt der von sfnt-Schriftarten. Es basiert auf einem Tabellenverzeichnis, das die Längen und Versätze zu den einzelnen Schriftdatentabellen enthält. Alle Tabellen werden nach diesen ersten Informationen befolgt. Die Datei enthält eine Schriftartendatenbank, die mit der Originalschriftart identisch ist. Die Reihenfolge der Tabellen ist ebenfalls gleich, aber jede kann komprimiert sein. Das WOFF-Tabellenverzeichnis ersetzt jedoch das ursprüngliche Tabellenverzeichnis.

Eine WOFF-Datei besteht aus Folgendem:

* WOFFHeader - Dateiheader mit grundlegendem Schriftarttyp und Version, zusammen mit Offsets zu Metadaten und privaten Datenblöcken.
* TableDirectory - Verzeichnis der Schrifttabellen, das die Originalgröße, komprimierte Größe und Position jeder Tabelle in der WOFF-Datei angibt.
* FontTables - Die Schriftartdatentabellen aus der eingegebenen sfnt-Schriftart, komprimiert, um die Bandbreitenanforderungen zu reduzieren.
* ExtendedMetadata – Ein optionaler Block erweiterter Metadaten, die im XML-Format dargestellt und zur Speicherung in der WOFF-Datei komprimiert werden.
* PrivateData – Ein optionaler Block privater Daten zur Verwendung durch den Schriftdesigner, die Gießerei oder den Anbieter.

### WOFF-Header
Der WOFF-Header besteht aus einer identifizierenden Signatur, die die Art der in der Datei enthaltenen Daten angibt. Der WOFF-Header zusammen mit seinen Feldern sieht wie folgt aus.

|Typ|Feldname|Beschreibung|
---|---|---|
|UInt32|Signatur |0x774F4646 'wOFF' |
|UInt32| Flavor |Die "sfnt-Version" der Eingabeschriftart.|
|UInt32| length |Gesamtgröße der WOFF-Datei.|
|UInt16| numTables |Anzahl der Einträge im Verzeichnis der Schrifttabellen.|
|UInt16| reserviert |reserviert; auf Null setzen.|
|UInt32| totalSfntSize |Gesamtgröße, die für die unkomprimierten Schriftartdaten benötigt wird, einschließlich des sfnt-Headers, des Verzeichnisses und der Schriftarttabellen (einschließlich Auffüllen).|
|UInt16| majorVersion |Hauptversion der WOFF-Datei.|
|UInt16| minorVersion |Nebenversion der WOFF-Datei.|
|UInt32| metaOffset |Offset zum Metadatenblock, vom Anfang der WOFF-Datei.|
|UInt32| metaLength |Länge des komprimierten Metadatenblocks.|
|UInt32| metaOrigLength |Unkomprimierte Größe des Metadatenblocks.|
|UInt32| privOffset |Offset zum privaten Datenblock, vom Anfang der WOFF-Datei.|
|UInt32| privLength |Länge des privaten Datenblocks.|


## **Verweise**
* [w3 WOFF-Dateiformat](https://www.w3.org/TR/WOFF/)

