{
  "date" : "2019-10-11",
  "keywords" :[ "djvu-Datei", "djvu-Dateiformat", "was ist eine djvu-Datei", "Datei", "djvu-Beispiel", "djvu-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DJVU-Dateiformat",
  "description":"Erfahren Sie mehr über das DJVU-Dateiformat und APIs, die DJVU-Dateien erstellen und öffnen können.",
  "linktitle" : "DJVU",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Was ist eine DJVU-Datei?

DjVu, ausgesprochen als „déjà vu“, ist ein Grafikdateiformat, das für gescannte Dokumente und Bücher gedacht ist, insbesondere für solche, die eine Kombination aus Text, Zeichnungen, Bildern und Fotos enthalten. Es wurde von AT&T Labs entwickelt. Es verwendet mehrere Techniken wie Bildebenentrennung von Text und Hintergrundbildern, progressives Laden, arithmetische Codierung und verlustbehaftete Komprimierung für bitonale Bilder. Da die DJVU-Datei komprimierte, aber qualitativ hochwertige Farbbilder, Fotos, Texte und Zeichnungen enthalten kann und daher auf weniger Platz gespeichert werden kann, wird sie im Internet als eBooks, Handbücher, Zeitungen, alte Dokumente usw. verwendet.

DjVu kann als überlegene Alternative zu [PDF](/de/pdf/) eingestuft werden. DjVu zugeordnete Dateierweiterungen sind .DJVU oder .DJV. DjVu kann Komprimierungsverhältnisse erreichen, die etwa 5 – 10 besser sind als bestehende Methoden wie [JPEG](/de/image/jpeg/) & [GIF](/de/image/gif/) für Farbdokumente und 3 – 8 Mal besser als [TIFF]( /image/tiff/) in Schwarz-Weiß-Dokumenten. Gescannte Dokumente mit 300 DPI und Vollfarbe bis zu 25 MB können auf 30 bis 100 KB komprimiert werden. Ebenso können Schwarz-Weiß-Dokumente auf 5 bis 30 KB komprimiert werden. Eine durchschnittliche HTML-Seite kann bis zu 50 KB groß sein, daher können diese Dokumente problemlos ins Netz hochgeladen werden.

## Kurze Geschichte ##

Die DjVu-Technologie wurde in AT&T-Labors von [Yann LeCun](https://en.wikipedia.org/wiki/Yann_LeCun), [Léon Bottou](https://en.wikipedia.org/wiki/L%C3% A9on_Bottou), Patrick Haffner und Paul G von 1996 bis 2001. Das DjVu-Dateiformat wurde mehrfach überarbeitet, zuletzt 2005.


|Version|Veröffentlichungsdatum|Anmerkungen
---|---|---|
|1–19|1996–1999|Dies sind die Entwicklungsversionen.
|20|April 1999|Einzelseite wurde in Mehrseitenformat geändert.
|23|Juli 2002|CID-Chunk
|24|Februar 2003|LTAnno Chunk
|21|September 1999|Indirektes Speicherformat ersetzt. Textsuchebene wurde hinzugefügt.
|22|April 2001|Seitenausrichtung, Farbe JB2
|25|Mai 2003|NAVM-Stück. Unterstützung für DjVu-Lesezeichen wurde hinzugefügt.
|26|April 2005|Text-/Zeilenanmerkungen

## DjVu-Dateiformat ##

DjVu-Dokumente sind IFF85-Dateien. Die Struktur stellt eine Hierarchie von Containern bereit, die Informationen in einer DjVu-Datei enthalten. Diese Container werden auch „Chunks“ genannt. Chunk-Typ und Chunk-ID beschreiben, wie der Chunk verwendet wird. Es gibt einen 4-Byte-Header gefolgt von einer IFF-Struktur. Die ersten vier Bytes einer DjVu-Datei sind 0x41 0x54 0x26 0x54. Dieser Abschnitt behandelt die verschiedenen Arten von DjVu-Dokumenten und die entsprechenden Chunks, aus denen sie bestehen.


|Chunk-ID|Nutzung
---|---|
|FORM|Der zusammengesetzte Chunk mit den ersten vier Datenbytes des FORM-Chunks, die eine sekundäre Kennung sind.
|FORM:DJVM|Ein mehrseitiges DjVu-Dokument. Zusammengesetzter Chunk, der den DIRM-Chunk enthält.
|FORM:DJVU|Einseitiges DjVu-Dokument. Zusammengesetzter Chunk, der die Chunks enthält, aus denen eine Seite in einem Djvu-Dokument besteht.
|FORM:DJVI|Eine „geteilte“ DjVu-Datei, die über den INCL-Chunk eingebunden wird. Freigegebene Anmerkungen und Formenwörterbuch.
|FORM:THUM|Zusammengesetzter Chunk, der die TH44-Chunks enthält, die eingebettete Thumbnails sind.
|DIRM|Seitennameninformationen für mehrseitige Dokumente.
|NAVM|Lesezeicheninformationen
|ANTa, ANTz|Anmerkungen einschließlich anfänglicher Ansichtseinstellungen und überlagerter Hyperlinks, Textfelder usw.
|TXTa, TXtz|Unicode Text- und Layoutinformationen.
|Djbz|Freigegebene Formtabelle.
|Sjbz|BZZ komprimierte bitonale JB2-Daten, die zum Speichern der Maske verwendet werden.
|FG44|IW44-Daten, die zum Speichern des Vordergrunds verwendet werden
|BG44|IW44-Daten, die zum Speichern des Hintergrunds verwendet werden
|TH44|IW44-Daten, die zum Speichern eingebetteter Miniaturbilder verwendet werden
|WMRM|JB2-Daten zum Entfernen eines Wasserzeichens erforderlich
|FGbz|Color JB2-Daten. Bietet eine Farbe für jeden (Blit oder Form?) im entsprechenden Sjbz-Chunk.
|INFO|Informationen über eine DjVu-Seite
|INCL|Die ID eines enthaltenen FORM:DJVI-Chunks.
|BGjp|JPEG-kodierter Hintergrund
|FGjp|JPEG-kodierter Vordergrund
|Smmr|G4-codierte Maske

### DJVU-Komprimierung

Ein einzelnes Bild wird in viele verschiedene Bilder aufgeteilt, und dann wird jedes Bild separat komprimiert. Für die Erstellung einer DjVu-Datei wird das Bild zunächst in drei Bilder aufgeteilt, ein Hintergrund-, Vordergrund- und ein Maskenbild. Typischerweise sind die Hintergrund- und Vordergrundbilder Farbbilder mit niedrigerer Auflösung; aber das Maskenbild ist ein Bild mit höherer Auflösung und typischerweise wird der Text dort gespeichert. Nach der Trennung werden das Vordergrund- und das Hintergrundbild durch einen Wavelet-basierten Kompressionsalgorithmus IW44 komprimiert, während das Maskenbild unter Verwendung eines anderen Verfahrens namens JB2 komprimiert wird.

Die JB2-Kodierungsmethode eliminiert einen Großteil der Redundanz im Textbild, indem identische Formen auf der Seite identifiziert werden, wie z. B. das mehrfache Vorkommen eines Zeichens in einer bestimmten Schriftart. JB2 codiert zunächst die Bitmap jeder eindeutigen Form, indem es die Redundanz zwischen ähnlichen Formen ausnutzt. Dann kodiert es die Stellen, an denen jede Form auf der Seite erscheint. Sowohl JB2 als auch IW44 verlassen sich auf einen neuen Typ adaptiver binärer arithmetischer Codierer namens ZP-Codierer, der jede verbleibende Redundanz innerhalb weniger Prozent der Shannon-Grenze herausquetscht. Der ZP-Codierer ist adaptiv und schneller als andere näherungsweise binäre arithmetische Codierer.

## Verweise ##

* [DjVu - Wikipedia](https://en.wikipedia.org/wiki/DjVu)
* [DjVu-Dateiformat](https://www.cuminas.jp/docs/techinfo/DjVu3Spec.pdf)

