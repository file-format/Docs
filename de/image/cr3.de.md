{
  "date" : "2022-03-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CR3-Dateiformat - Canon Raw 3-Bilddatei",
  "description":"Erfahren Sie mehr über das CR3-Dateiformat und APIs, die CR3-Dateien erstellen und öffnen können.",
  "linktitle" :"CR3",
  "menu" : {
    "docs" : {
"identifier": "image-cr3",
      "parent" : "image"
}
},
  "lastmod" : "2022-03-26"
}

## Was ist eine CR3-Datei?

Eine CR3-Datei ist ein Canon-RAW-Bilddateiformat, das von ausgewählten Canon-Digitalkameras erstellt wird. Es wurde von Canon eingeführt, um das CR2-Dateiformat zu ersetzen, und wird von einigen Digitalgeräten von Canon verwendet. CR3-Dateien speichern die ursprünglichen, nicht verarbeiteten, verlustfreien Bilddaten, die von der Kamera erfasst wurden. Die Verwendung dieser Rohbilder liefert qualitativ hochwertige Bilder und lässt Fotografen viel Raum für die Bearbeitung. Neben den Hauptbilddaten speichern CR3-Dateien auch Metadateninformationen zum Bild.

## CR3-Dateiformat

CR3-Dateien werden als Binärdatei im ISO Base Media File Format (ISO/IEC 14496-12) auf der Disc gespeichert und enthalten auch benutzerdefinierte [Canon-Tags] (https://exiftool.org/TagNames/Canon.html#uuid). Es enthält auch den [Canon 'crx' codec](https://github.com/LibRaw/LibRaw/blob/master/src/decoders/crx.cpp), der eine Mischung aus JPEG-LS (Rice-Golomb + RLE Kodierung) und JPEG-2000 (LeGall 5/3 DWT + Quantifizierung).

## Benutzerdefinierte CR3-Tags

CR3-Dateien enthalten benutzerdefinierte Tags für verschiedene Zwecke. Einige dieser Tags lauten wie folgt.

|Tag-ID| Tag-Name| Beschreibbar |Werte / Notizen|
---|---|---|---|
|'CCTP' |CanonCCTP| - |--> Canon CCTP-Tags|
|'CMT1' |IFD0| - |--> EXIF-Tags|
|'CMT2' |ExifIFD| - |--> EXIF-Tags|
|'CMT3' |MakerNoteCanon| - |--> Canon-Tags|
|'CMT4' |GPSInfo| - |--> GPS-Tags|
|'CNCV' |KompressorVersion| nein| |
|'CNOP' |CanonCNOP| - |--> Canon CNOP-Tags|
|'CNTH' |CanonCNTH| - |--> Canon CNTH-Tags|
|'THMB' |ThumbnailImage| nein| |

## Verweise

* [CR2-Dateiformat](http://lclevy.free.fr/cr2/)
* [Canon-Tags](https://exiftool.org/TagNames/Canon.html#uuid)

