{
  "date" : "2019-10-11",
  "keywords" :[ "ico-Datei", "ico-Dateiformat", "was ist eine ico-Datei", "Datei", "ico-Beispiel", "ico-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ICO - Bilddateiformat",
  "description":"Erfahren Sie mehr über das ICO-Dateiformat und APIs, die ICO-Dateien erstellen und öffnen können.",
  "linktitle" :"ICO",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Was ist eine ICO-Datei?

Dateien mit der Erweiterung ICO sind Bilddateitypen, die als Symbol zur Darstellung einer Anwendung auf [Microsoft Windows] (https://www.microsoft.com/en-us/windows) verwendet werden. Diese gibt es in unterschiedlicher Größe, Farbunterstützung und Auflösung, um den Anforderungen des Displays gerecht zu werden. Ein weiteres ähnliches Bilddateiformat unter Microsoft Windows ist [CUR](/de/image/cur/) für die Cursordarstellung und definiert einen Hotspot im Bildheader. Auf MacOS dienen ICNS-Dateiformate demselben Zweck wie ICO-Dateien. Mehrere Online-Websites sowie Anwendungen bieten die Möglichkeit, solche Dateien zu erstellen und andere Bildformate wie [BMP](/de/image/bmp/), [PNG](/de/image/png/) usw. in das Symboldateiformat zu konvertieren. Der offizielle IANA-registrierte Internetmedientyp für ICO-Dateien ist image/vnd.microsoft.icon.

## Kurze Geschichte ##

Symbole wurden mit dem Start von Microsoft Windows 1.0 eingeführt. Diese waren 32x32 groß und einfarbig. Mit der Einführung von win32 wurde die Unterstützung für Symbolbilder in Echtfarbe mit einer Größe von bis zu 256 x 256 Pixel eingeführt. Windows XP war das erste, das 32-Bit-Farbsymbolbilder unterstützte, wodurch dem Symbol halbtransparente Bereiche wie Schatten, Anti-Aliasing und glasähnliche Effekte hinzugefügt werden konnten. Microsoft empfahl für Windows XP nur Symbolgrößen bis zu 48×48 Pixel. Windows Vista hat dem Windows Explorer eine 256 × 256 Pixel große Symbolansicht sowie Unterstützung für das komprimierte [PNG] (/de/image/png/)-Format hinzugefügt. Bei Benutzern, die höhere Auflösungen und hohe DPI-Modi verwenden, werden größere Symbolformate (z. B. 256 × 256) empfohlen.

## ICO-Dateiformat ##

Eine einzelne ICO-Datei besteht aus einem oder mehreren kleinen Bildern in mehreren Größen und Farbtiefen. Das Vorhandensein von Bildern in mehreren Größen dient der angemessenen Skalierung bei unterschiedlichen Bildschirmauflösungen. Alle Werte in ICO/CUR-Dateien werden in der Byte-Reihenfolge [little-endian](https://en.wikipedia.org/wiki/Little-endian) dargestellt.

Die ICO-Datei besteht aus einem Icon-Header, einem Icon-Verzeichnis,

|Feld|Beschreibung
---|---|
|Icon Header|Speichert allgemeine Informationen über die ICO-Datei.
|Verzeichnis[1..n]|Speichert allgemeine Informationen über jedes Bild in der Datei.
|Icon #1|Die eigentlichen "Daten" für das erste Bild im alten AND/XOR DIB-Format oder neuerem PNG
|...|
|Symbol #n|Daten für das letzte Symbolbild

### Header ###

|Offset|Größe (in Bytes)|Zweck
---|---|---|
|0|2|Reserviert. Muss immer 0 sein.
|2|2|Gibt den Bildtyp an: 1 für Symbolbild (.ICO), 2 für Cursorbild (.CUR). Andere Werte sind ungültig.
|4|2|Gibt die Anzahl der Bilder in der Datei an.

### Verzeichnis ###

Das in einer ICO-Datei enthaltene Verzeichnis, dargestellt als ICONDIR-Struktur, enthält eine ICONDIRECTORY-Struktur für jedes Bild in der Datei. Darauf folgt ein zusammenhängender Block aller Bild-Bitmap-Daten. Dies ist wie unten gezeigt.

|Offset|Größe|Beschreibung
---|---|---|
|0 (0)|1|Breite, sollte 0 sein, wenn 256 Pixel
|1 (1)|1|Höhe, sollte 0 sein, wenn 256 Pixel
|2 (2)|1|Farbanzahl, sollte 0 sein, wenn mehr als 256 Farben vorhanden sind
|3 (3)|1|Reserviert, sollte 0 sein
|4 (4)|2|Farbebenen im .ICO-Format sollten 0 oder 1 sein, oder der X-Hotspot im .CUR-Format
|6 (6)|2|Bits pro Pixel im .ICO-Format oder der Y-Hotspot im .CUR-Format
|8 (8)|4|Größe der Bitmap-Daten in Bytes.
|12 (C)|4|Offset in der Datei.

## Verweise ##

* [ICO – von Wikipedia](https://en.wikipedia.org/wiki/ICO_(file_format))
* [IANA - vnd.microsoft.icon](http://www.iana.org/assignments/media-types/image/vnd.microsoft.icon)

