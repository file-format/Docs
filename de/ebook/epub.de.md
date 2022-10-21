{
  "date" : "2019-12-12",
  "keywords" :[ "EPUB", "Datei", "Erweiterung", "Format", "E-Book", "Digitales Buch" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Erfahren Sie mehr über das EPUB-Dateiformat und APIs, die EPUB-Dateien erstellen und öffnen können.",
  "title" :"Was ist eine EPUB-Datei?",
  "linktitle" :"EPUB",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2019-12-12"
}

## Was ist eine EPUB-Datei?

Dateien mit der Erweiterung .epub sind ein E-Book-Dateiformat, das ein digitales Standardveröffentlichungsformat für Verlage und Verbraucher bietet. Das Format ist inzwischen so weit verbreitet, dass es von vielen E-Readern und Softwareanwendungen unterstützt wird. Unter Mac OS bietet beispielsweise die vorinstallierte **Books**-Software Unterstützung zum Öffnen solcher Dateien. Darüber hinaus gibt es eine Menge kompatibler Software für Smartphones, Tablets und Computer. EPUB-Dateistandards werden vom [International Digital Publishing Forum](https://idpf.org/epub/30/spec/epub30-publications.html)(IDPF) verwaltet. Die Version EPUB 3 wird auch von der Book Industry Study Group (BISG), einem führenden Buchhandelsverband für standardisierte Best Practices, Forschung, Informationen und Veranstaltungen, für die Paketierung von Inhalten unterstützt.

## Kurze Geschichte des EPUB-Dateiformats

* **Oktober 2007** - EPUB 2.0 wurde genehmigt
* **September 2010** - Wartungsupdate wurde veröffentlicht
* **Oktober 2011** - EPUB 3.0-Spezifikationen traten in Kraft
* **Juni 2014** – Kleineres Wartungsupdate wurde veröffentlicht, um die Version 3.0 zu ersetzen
* **Januar 2017** - EPUB 3.1 trat in Kraft

## EPUB-Dateiformat

Das EPUB-Dateiformat ist ein Archiv, das in die Erweiterung [ZIP](/de/compression/zip/) umbenannt werden kann und dessen Inhalt angezeigt werden kann, indem das Archiv mit einem beliebigen Archiv-Extraktor extrahiert wird. Es ist ein offenes XML-basiertes Format und besteht aus HTML-Dateien, Bildern, CSS-Stylesheets und anderen Elementen. Es kann auch über eine Reihe von Softwareanwendungen und APIs in PDF, Mobi und mehrere andere Dateiformate konvertiert werden.

{{< figure src="../epub.png" alt="EPUB-Dateiformat" >}}

**EPUB E-Book geöffnet mit Mac OS Books Application**

Das EPUB-Dateiformat basiert auf den folgenden drei offenen Standards.

### Offene öffentliche Struktur (OPS) ###

Eine EPUB 2.0-Datei verwendet XHTML 1.1, um den Inhalt einer Veröffentlichung zu erstellen. Im Wesentlichen bedeutet dies, dass eine EPUB-Datei aus einer oder mehreren Webseiten besteht. Auch wenn Sie den gesamten Inhalt eines Buches oder einer Zeitung auf einer einzigen Seite zusammenfassen könnten, ist es aus Leistungs- und Kompatibilitätsgründen besser, dass eine solche Datei 300 KB nicht überschreitet. Stil und Layout werden wie bei normalen Webseiten mithilfe von Cascading Style Sheets (CSS) definiert. In EPUB-Dateien muss eine Teilmenge (begrenzte Befehlsfolge) von CSS2 verwendet werden. Viele der neuen Features von CSS3, wie abgerundete Kästchen oder Schlagschatten, sind noch nicht verfügbar. Aus Gründen der Abwärtskompatibilität kann ein Ersteller auch DTBook anstelle von XHTML verwenden, um den Inhalt zu codieren.

### Offenes Verpackungsformat (OPF) ###

Dieser Teil der Spezifikationen befasst sich mit strukturellen Informationen wie Metadaten (wer ist der Autor und der Herausgeber, wie lautet der Titel usw.), dem Manifest (eine Liste aller Dateien in einer epub-Datei) und dem Inhaltsverzeichnis. Diese Daten werden alle unter Verwendung von XML eingebettet.

### Offenes Containerformat (OCF) ###

Wie die obigen Beschreibungen deutlich gemacht haben sollten, besteht ein EPUB-Dokument aus einer Reihe von Dateien. Die OCF-Spezifikationen definieren, wie all diese Dateien in einer einzigen Containerdatei verpackt werden. Hierfür wird die ZIP-Komprimierung verwendet.

## Unterstützte Bilddateiformate ##

Das EPUB-Dateiformat unterstützt die folgenden Bilddateiformate.

* [GIF](/de/image/gif/)
* [JPG](/de/image/jpeg/)
* [PNG](/de/image/png/)
* [SVG](/de/Seitenbeschreibungssprache/svg/)

## Verweise ##

* [EPUB – von Wikipedia](https://en.wikipedia.org/wiki/EPUB)

