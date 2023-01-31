{
  "date" : "2022-11-17",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"BIF-Datei - Ventana Whole Slide Image Format",
  "description":"Erfahren Sie mehr über das BIF-Dateiformat und APIs, die BIF-Dateien erstellen und öffnen können.",
  "linktitle" : "BIF",
  "menu" : {
    "docs" : {
      "identifier":"image-bif",
      "parent" : "image"
}
},
  "lastmod" : "2022-11-17"
}

## Was ist eine BIF-Datei?

Eine BIF-Datei ist eine Rasterbilddatei, die das Bild der Objektträgerprobe enthält. Es besteht aus mehreren TIFF-Bildern, die von Diabetrachtungsanwendungen zu einem einzigen zusammengesetzten Bild kombiniert werden. BIF-Dateien werden vom digitalen Diascanner von Ventana Medical Systems erstellt und sind vollständig kompatibel mit der BigTIFF-Variante der [TIFF](/de/image/tiff/) v 6.0-Definition.

## BIF-Dateiformat

Eine BIF-Datei wird als binäre Bilddatei gespeichert und besteht aus bis zu 200.000 x 200.000 Pixeln. Dies kann zu großen Dateien führen, die die Größenbeschränkung von 4 GB überschreiten, die durch die vom TIF-Standard definierten 32-Bit-Dateizeiger auferlegt wird. Bei 64-Bit-Dateizeigern wird diese Dateigrößenbarriere jedoch durch die BigTIFF-Variante des TIFF-Standards überwunden.

### Wer verwendet die BIF-Datei?

BIF-Dateien werden von digitalen Diascannern verwendet, um digitale Kopien von Diaproben zu scannen und zu erstellen. Wenn Sie ein Pathologe sind, können Sie diese BIF-Dateien in Diabetrachtungsanwendungen öffnen. Mit einem hohen Detaillierungsgrad und hochauflösenden Daten können Sie ein Objektträgerbild vergrößern und verkleinern, um Probenabschnitte mehr oder weniger detailliert anzuzeigen. Die in diesen Dateien vorhandene [XML](/de/web/xml/)-Metadatendatei definiert, wie die Bilder kombiniert werden sollen, und das Bild, das als Miniaturansicht der Datei verwendet werden soll.

## Wie öffnet man eine BIF-Datei?

Sie können BIF-Dateien öffnen mit:

* OpenSlide (plattformübergreifend)
* ImageJ (plattformübergreifend)
* NetScope-Viewer (Windows)

## Verweise ##

* [Roche Digital Pathology BIF Whitepaper](https://diagnostics.roche.com/content/dam/diagnostics/Blueprint/en/pdf/rmd/Roche-Digital-Pathology-BIF-Whitepaper.pdf)

