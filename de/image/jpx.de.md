{
  "date" : "2021-02-10",
  "keywords" :[ "jpx-Datei", "jpx-Dateiformat", "was ist eine jpx-Datei", "Datei", "jpx-Beispiel", "jpx-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JPX - Bilddateiformat",
  "description":"Erfahren Sie mehr über das JPX-Dateiformat und APIs, die JPX-Dateien erstellen und öffnen können.",
  "linktitle" :"JPX",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-02-10"
}

## Was ist eine JPX-Datei? ##

Eine Datei mit der Erweiterung .jpx ist eine Erweiterung des Dateiformats JPEG 2000. Es verwendet hauptsächlich die JPEG 2000-Komprimierung und bietet auch erweiterte Funktionen wie mehrere Ebenen für ein Bild, verschiedene Farbräume, Deckkraft und fragmentierte Codeströme. JPX erlaubt neben der JPEG 2000-Komprimierung auch andere Komprimierungen wie JBIG, CCITT Group3, CCITT Group4 usw. Das JPX-Dateiformat wurde als [ISO/IEC 15444-2](https://www.iso.org/standard/33160.html)-Standard genehmigt, konnte jedoch aufgrund der umfangreichen Verwendung von [JPEG ](/de/image/jpeg/) Dateiformat. Zu den Anwendungen, die JPX-Dateien öffnen können, gehören Corel PaintShop Pro, Adobe Photoshop 2020, Adobe Illustrator 2020 und CorelDraw Graphics Suite 2020.

## Kurze Geschichte

Im Jahr 2000 entwarf das Komitee der Joint Photographic Experts Group JP2 mit dem Ziel, ihren eigenen, auf diskreter Cosinustransformation basierenden JPEG-Standard mit dieser neuen Wavelet-basierten Methode zu verbessern. Das JPEG-Komitee wollte seine Basismethoden lizenzgebührenfrei zur Verfügung stellen. Im JP2-Lizenzwettbewerb unter 20 Unternehmen gewannen sie mit knapper Mehrheit. JPEG 2000 wurde zum ISO-Standard erklärt, obwohl die meisten Webbrowser seit 2017 nicht bereit sind, JPEG 2000 zu unterstützen. 2004 wurde das ISO/IEC 15444-2-Format als Erweiterung des JP2-Dateiformats öffentlich akzeptiert.

## JPX-Dateiformat

Das JPX-Dateiformat wurde entwickelt, um die Anforderungen von Anwendungen zu erfüllen, die Datenstrukturen benötigen, die über die durch das Dateiformat [JP2](/de/image/jp2/) definierte Funktionalität hinausgehen. Eine JP2-Datei mit nicht kompatiblen Erweiterungen könnte auf dem Markt zu Verwirrung führen, da einige Leser einige JP2-Dateien interpretieren können, andere jedoch nicht. JPX ist die Antwort auf die Vermeidung solcher Probleme in Anwendungen.

### Dateiidentifikation

JPX-Dateien werden als [JPF](/de/image/jpf/) gespeichert, wenn sie in einem herkömmlichen Computerdateisystem gespeichert werden. Aus diesem Grund wird der JPX-Begriff im Vergleich zum JPF am seltensten verwendet. Eine JPX-Datei beginnt mit den folgenden Bytes:

`00 00 00 0c 6a 50 20 20 0d 0a 87 0a ?? ?? ?? ?? 66 74 79 70 6a 70 78 20".

### Dateiorganisation

Ähnlich wie JP2 ist eine JPX-Datei eine Sammlung von Boxen mit einer binären Struktur, wobei die Boxen in einer zusammenhängenden Reihenfolge angeordnet sind. Das erste Kästchen gibt mit seinem ersten Byte den Anfang der Datei und das letzte Byte des letzten Kästchens repräsentiert das letzte Byte der Datei.
Die Binärstruktur einer Box in einer JPX-Datei ist identisch mit der im Dateiformat [JP2](/de/image/jp2/) definierten.

### Speicherung von CodeStream in JPX

Das JPX-Dateiformat ermöglicht die Aufteilung des Bild-Codestreams in Fragmente. Dadurch ist es möglich, eine einzelne Kachel des Bildes zu modifizieren und die modifizierte Kachel an das Ende der Datei zu schreiben, ohne die gesamte Datei neu schreiben zu müssen. Das ursprüngliche [JP2](/de/image/jp2/)-Dateiformat schränkt das Speichern des gesamten Codestreams in einem zusammenhängenden Teil der Datei ein, was für Bildbearbeitungsanwendungen problematisch sein kann, die möglicherweise eine einzelne Kachel des Bildes ändern und erreichen möchten die obige Unterstützbarkeit durch das JPX-Dateiformat. Die Fragmentierung des Bild-Codestreams macht das JPX-Dateiformat dem JP2-Dateiformat überlegen. Darüber hinaus ermöglicht das JPX-Dateiformat das Kombinieren mehrerer Codestreams und das Erzeugen eines gerenderten Ergebnisses. Codestreams können als Compositing und Animation kombiniert werden.

## Verweise ##

* [Überblick über JPEG 2000](https://jpeg.org/jpeg2000)

