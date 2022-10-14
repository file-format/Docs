{
  "date" : "2019-12-12",
  "keywords" :[ "LRF", "Datei", "Erweiterung", "Format", "eBook", "Digitales Buch" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Erfahren Sie mehr über das LRF-Dateiformat und APIs, die LRF-Dateien erstellen und öffnen können.",
  "title" :"LRF-Dateiformat - Eine Sony Portable Reader-Datei",
  "linktitle" :"LRF",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2019-12-12"
}

## Was ist eine LRF-Datei?

Eine Datei mit der Erweiterung .lrf ist eine Broad Band eBook (BBeB)-Datei, die Daten für ein Sony BBeB enthält, einschließlich Text, Bilder und Paginierungsdaten. Die Datei wird in einem komprimierten Binärformat gespeichert, das einen Header, eine bestimmte Anzahl von Objekten und einen Objektindex enthält. LRF- und LRX-Dateien schließen die beiden verfügbaren BBeB-Buchformate ein. Die LRF-Dateien sind nicht verschlüsselt und können aus [LRX](/de/ebook/lrf/)-Dateien kompiliert werden. Die LRF-Dateien können aus mehreren anderen Dateitypen konvertiert werden, einschließlich PDF und HTML. Wenn Ihr Computer die LRF-Datei nicht öffnen kann, haben Sie wahrscheinlich nicht die Software zum Öffnen oder Bearbeiten der LRF-Dateien installiert. Programme, die LRF-Dateien öffnen können, sind Calibre, BookDesigner, Makelrf und Canon Book Creator für Windows, Calibre für Linux, Calibre und Sony Reader für Macintosh.

## Kurze Geschichte

Der LRF-Dateityp wird in erster Linie mit Line Rider von [inXile entertainment](https://en.wikipedia.org/wiki/InXile_Entertainment) in Verbindung gebracht. Der Line Rider ist ein Internet-Physikspielzeug und wurde im September 2006 von einem slowenischen Universitätsstudenten, Boštjan Čadež, erfunden. eBook-eReader der Marke Sony (wie Sony PRS-500-Lesegeräte und Sony Librie) verwenden die LRF-Dateierweiterung für ihre Dokumente und Texte. Dieser proprietäre Dateityp ist jetzt veraltet, ebenso wie die zugehörigen LRS- und LRX-Dateien. Diese drei Dateitypen bildeten das BroadBand eBook (BBeB), das 2010 eingestellt wurde, als Sony begann, seine eBooks im EPUB-Format zu verkaufen.

## LRF-Dateiformat

Detaillierte Spezifikationen des LRF-Dateiformats sind verfügbar unter [Webarchiv](https://web.archive.org/web/20110809071744/http://www.sven.de/librie/Librie/LrfFormat). Eine LRF-Datei besteht aus:
* eine Überschrift
* eine Reihe von Objekten
* ein Objektindex.

Alle diese Werte sind in Intel-Reihenfolge (LSB zuerst).

### LRF-Header

|Offset (hex) |Größe(bytes) |Name/Bedeutung| Beispielwert|
---|---|---|---|
|0 |8| LRF-Signatur| 4C 00 52 00 46 00 00 00 = "LRF" in Unicode|
|8 |2| Version?| 999 in den meisten Dateien|
|A |2| "Pseudo-Verschlüsselung" |Schlüsselbyte 48|
|0C |4| RootObjectID| 0x0044|
|10 |8| AnzahlDerObjekte |342|
|18 |8| ObjektIndexOffset| 0x00093440|
|20 |4| unbekannt| 0|
|24 |1| Flaggen| (16 - von hinten nach vorne, 1 = von vorne nach hinten) 16|
|25 |1| unbekannt |(Auffüllen?) 0|
|26 |2| unbekannt| 1600|
|28 |2| unbekannt| (Auffüllen?) 0|
|2A |2| Höhe?| 600|
|2C |2| Breite?| 800|
|2E |1| unbekannt| 24|
|2F |1| unbekannt |(Auffüllen?) 0|
|30 |0x14| unbekannt| Nullen|
|44 |4| Objekt-ID von nur PlaneStream (0x1E)-Objekt| 0x0042|
|48 |4| unbekannt |0x1536|
|4C |2| XMLCompSize| 0x035C|


## Verweise

* [LRF-Dateiformat](https://web.archive.org/web/20110809071744/http://www.sven.de/librie/Librie/LrfFormat)
* [BBeB – Von Wikipedia](https://en.wikipedia.org/wiki/BBeB)

