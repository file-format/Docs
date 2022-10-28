{
  "date" : "2022-03-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CR2-Dateiformat - Canon Raw 2-Bilddatei",
  "description":"Erfahren Sie mehr über das CR2-Dateiformat und APIs, die CR2-Dateien erstellen und öffnen können.",
  "linktitle" : "CR2",
  "menu" : {
    "docs" : {
"identifier":"image-cr2",
      "parent" : "image"
}
},
  "lastmod" : "2022-03-26"
}

## Was ist eine CR2-Datei?

Eine CR2-Datei (Camera RAW 2) ist eine RAW-Bilddatei, die von Digitalkameras von Canon erstellt wurde. Es speichert die ursprünglichen, unverarbeiteten, verlustfreien Bilddaten, die von der Kamera erfasst wurden. Das CR2-Dateiformat wurde von Canon für seine Digitalkameras entwickelt und kann hochwertige Bilder mit bis zu 14 Bit RGB aufzeichnen. Dies erzeugt qualitativ hochwertige Bilder mit genügend Raum für die Nachbearbeitung. Das CR2-Bildformat wurde von Canon in seinen Kameramodellen 350D, 20D und 1D verwendet. CR2-Dateien sind RAW-Dateien und enthalten zusätzliche Metadateninformationen wie Kamerainformationen, Objektivinformationen, Belichtungsreiheninformationen, Weißabgleich und andere Einstellungen.

## CR2-Dateiformat

CR2-Dateien werden als Binärdateien im Canon-eigenen Dateiformat auf der Speicherkarte der Kamera gespeichert. Das CR2-Dateiformat ersetzte das ursprünglich verwendete CRW-Dateiformat und wurde später selbst durch das Canon RAW 3-Dateiformat ersetzt. Das CR2-Dateiformat basiert auf den [TIFF](/de/image/tiff/)-Spezifikationen, die über 4 Bilddateiverzeichnisse (IFDs) verfügen.

|Offset |Inhalt |Kommentar|
---|---|---|
|0x0000 |Header |enthält die Bytereihenfolge, die Version und den Offset zum RAW-Bild|
|berechnet |IFD#0 |dieser Teil enthält den Exif-Abschnitt, der den Makernotes-Abschnitt enthält.
Informationen zu Bild#0|
|berechnetes |Bild#0 |kleine Version des Bildes (ein Viertel der Größe des Originals), komprimiert in Jpeg|
|berechnet |IFD#1 |Informationen zu Bild#1.|
|berechnetes |Bild#1 |kleine Version des Bildes, komprimiert in Jpeg|
|berechnet |IFD#2 |Informationen zu Bild#2.|
|berechnetes |Bild#2 |kleine Version des Bildes, nicht komprimiert|
|in der Kopfzeile| IFD#3| Informationen zu Bild Nr. 3, das RAW-Bild in voller Dimension|
|berechnet |Bild#3 |RAW-Bilddaten, verlustfrei komprimiert in Jpeg (keine RGB-Daten!)|

## Vorteil des CR2-Dateiformats

Das Speichern von Bildern im RAW-Format ermöglicht eine umfangreiche Nachbearbeitung des Fotos, z. B. die Anpassung des Weißabgleichs. Bei anderen Bilddateiformaten wie [JPEG](/de/image/jpeg/) ist dies weitaus schwieriger und mit großem Qualitätsverlust verbunden.

## Ist CR2 besser als JPEG?

CR2-Dateien sind Rohdateien ohne Datenverlust und somit ohne Qualitätsverlust. JPEG hingegen ist ein verlustbehaftetes Bilddateiformat, da einige Daten verloren gehen, um die Datei zu verkleinern. Daher sind die CR2-Dateien von hoher Qualität und besser für Retuschen und Verbesserungen geeignet.

## Verweise

* [CR2-Dateiformat](http://lclevy.free.fr/cr2/)

