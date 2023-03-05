{
  "date" : "2019-10-11",
  "keywords" :[ "dng-Datei", "dng-Dateiformat", "was ist eine dng-Datei", "Datei", "dng-Beispiel", "dng-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DNG - Digitalkamera-Bilddateiformat",
  "description":"Erfahren Sie mehr über das DNG-Dateiformat und APIs, die DNG-Dateien erstellen und öffnen können.",
  "linktitle" : "DNG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Was ist eine DNG-Datei?

DNG ist ein Bildformat für Digitalkameras, das zum Speichern von Rohdateien verwendet wird. Es wurde von Adobe im September 2004 entwickelt. Es wurde im Wesentlichen für die digitale Fotografie entwickelt. DNG ist eine Erweiterung des [TIFF](/de/image/tiff/)/EP-Standardformats und verwendet in erheblichem Umfang Metadaten. Um Rohdaten von Digitalkameras mit der Leichtigkeit der Flexibilität und künstlerischen Kontrolle zu bearbeiten, entscheiden sich Fotografen für Kamera-Rohdateien. JPEG- und TIFF-Formate speichern Bilder, die von der Kamera verarbeitet werden, daher ist in solchen Formaten nicht viel Spielraum für Änderungen verfügbar.

## Geschichte und Versionen des DNG-Dateiformats

Bisher gab es 5 Versionen der DNG-Spezifikation. Version 1.0.0.0 wurde im September 2004 zusammen mit der Veröffentlichung von „2.3“ (ACR- und DNG-Konverter) eingeführt. Im Februar 2005 wurde die Version 1.1.0.0 veröffentlicht. Im Mai 2008 wurde die Version 1.2.0.0 veröffentlicht und in "4.4" verwendet. Version 1.3.0.0 wurde im Juni 2009 veröffentlicht. Version 1.4.0.0 erschien 2012.

## DNG-Dateiformat

Während Camera Raw-Dateien unverarbeitete oder gering verarbeitete Daten direkt vom Sensor erfassen. Da sie Filmnegativen ähneln, werden Camera Raw-Formate auch als „Digitale Negative“ bezeichnet. Vorteil von Rohformaten ist die erhöhte künstlerische Kontrolle für den Endnutzer. Der Benutzer kann verschiedene Parameterbereiche gemäß den Anforderungen wie Weißabgleich, Tonemapping, Rauschunterdrückung, Schärfen usw. anpassen. Auf der anderen Seite muss die Camera Raw-Datei für jede Verwendung durch eine Software oder einen Konverter verarbeitet werden.

Da für Camera Raw-Dateien kein Standardformat verfügbar war, führte dies zu mehreren Problemen für den Endbenutzer. Diese Probleme wurden von Adobe behoben und ein nicht-proprietäres Format für Camera Raw-Dateien definiert. Das Format ist als Digital Negative oder DNG bekannt. DNG kann von einer Vielzahl von Hard- und Software zur Verarbeitung von Rohdateien verwendet werden. Darüber hinaus kann DNG auch als Zwischenformat zum Speichern von Bildern verwendet werden, die ursprünglich von Kameras mit eigenen proprietären Rohformaten aufgenommen wurden.

### DNG-Dateiformatspezifikationen

In diesem Abschnitt beschreiben wir das DNG-Format als Erweiterung von TIFF 6.0.

* **Dateierweiterungen**: DNG verwendet die Erweiterungen „.DNG“ oder „.TIF“.
* **SubIFD-Bäume**: DNG unterstützt keine SubIFD-Ketten, stattdessen empfiehlt DNG die Verwendung von SubIFD-Bäumen, wie in den TIFF-EP-Spezifikationen erwähnt. Die höchste Qualität und Auflösung kann NewSubFileType von 0 verwenden, während die Thumbnails mit reduzierter Qualität NewSubFileType gleich 1 verwenden sollten. Es wird auch empfohlen, ist aber nicht erforderlich, dass das erste IFD ein Thumbnail mit niedriger Qualität oder Auflösung haben muss.
* **Byte-Reihenfolge**: Die Byte-Reihenfolge muss von DNG-Lesegeräten unterstützt werden, auch für Dateien eines bestimmten Kameramodells.
* **Maskierte Pixel**: Die meisten Kamerasensoren berechnen vollständig maskierte Pixel am Rand des Sensors durch Schwarzkodierung. Diese Pixel können entweder eingeschlossen oder beschnitten werden, bevor das Bild im DNG-Format gespeichert wird. Wenn die maskierten Pixel nicht getrimmt werden, muss die Fläche dieser Pixel im ActiveArea-Tag angegeben werden. Die von diesen Pixeln gesammelten Informationen über den Schwarz-Codierungspegel sollten verwendet werden, bevor die Rohdaten gespeichert werden, oder können in die DNG-Datei aufgenommen werden, die den Schwarzpegel angibt.
* **Defekte Pixel**: Vor dem Speichern von Rohdaten als DNG sollten defekte Pixel ausgeschlossen werden.
* **Metadaten**: Metadaten können auf eine der folgenden Arten in DNG aufgenommen werden:
** Durch die Verwendung von TIFF-EP- oder EXIF-Metadaten-Tags
** Über das IPTC-Metadaten-Tag (33723)
** Verwendung des XMP-Metadaten-Tags (700)
* **Eigene Daten**: Normalerweise schließen Anbieter proprietäre Daten in die Rohdatei ein, die von ihren eigenen Konvertern verwendet werden. DNG speichert seine proprietären Daten in privaten Tags, privaten IFDs und in einer privaten MakerNote. Anbieter müssen die DNGPrivateData- und MakerNoteSafety-Tags verwenden, um sicherzustellen, dass Anwendungen, die DNG-Dateien bearbeiten, diese proprietären Daten bewahren.

Im Folgenden sind einige wichtige Einschränkungen und Erweiterungen von TIFF-Tags aufgeführt.

**BitsproSample**

8 bis 32 Bit/Sample werden unterstützt. Wenn SamplesPerPixel ungleich 1 ist, muss für jedes Sample dieselbe Tiefe vorhanden sein.

**Kompression**

Zwei Komprimierungs-Tag-Werte werden unterstützt:

* Wert Nr. 1: Unkomprimierte Daten.
* Wert Nr. 7: JPEG-komprimierte Daten, entweder Baseline-DCT-JPEG oder verlustfreie JPEG-Komprimierung.

**Fotometrische Interpretation**

Die folgenden Werte werden nur für Thumbnail- und Vorschau-IFDs unterstützt:

* 1 = SchwarzIstNull. Angenommen, in einem Gamma 2,2-Farbraum zu sein.
* 2 = RGB. Vermutlich im sRGB-Farbraum.
* 6 = YCbCr. Wird für JPEG-codierte Vorschaubilder verwendet.

Die folgenden Werte werden für das Roh-IFD unterstützt und gelten als nativer Farbraum der Kamera:

* 32803 # CFA (Farbfilter-Array).
* 34892 # LinearRaw.

**Orientierung**

Das Orientierungstag wird für Dateibrowser verwendet, damit sie eine verlustfreie Rotation von DNG-Dateien durchführen können. DNG-Lesegeräte müssen alle möglichen Ausrichtungen unterstützen, einschließlich gespiegelter Ausrichtungen.

## Funktionen in der neuesten Version von DNG

DNG Version 1.4 Oktober 2012 hat die folgenden erweiterten Funktionen.

* Standard-Benutzerzuschnitt
* Transparenz
* Fließkomma (HDR)
* Verlustbehaftete Komprimierung
* Proxys

## Verweise ##

* [DNG-Spezifikationen – von Adobe](https://www.kronometric.org/phot/processing/DNG/dng_spec_1.4.0.0.pdf)
* [Digitales Negativ – Wikipedia](https://en.wikipedia.org/wiki/Digital_Negative)
* [DNG – Das öffentliche Archivformat für Digitalkamera-Rohdaten](https://helpx.adobe.com/photoshop/digital-negative.html)

