{
  "date" : "2022-07-21",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HDR-Dateiformat - Was ist eine HDR-Bilddatei?",
  "description":"Erfahren Sie mehr über das HDR-Dateiformat und APIs, die HDR-Dateien erstellen und öffnen können.",
  "linktitle" :"HDR",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2022-07-21"
}

## Was ist eine HDR-Datei?

Eine HDR-Datei ist ein HDR-Rasterbilddateiformat (High Dynamic Range) zum Speichern von Digitalkamerafotos. Es ermöglicht Bildbearbeitern, die Farbe und Helligkeit digitaler Bilder mit begrenztem Dynamikbereich zu verbessern. Diese Modifikation kann die Helligkeit um die Ecken herum verbessern, was zu einem nahezu natürlichen Bild führt. HDR-Dateien werden normalerweise als 32-Bit-Rasterbilder gespeichert. Adobe Photoshop kann HDR-Dateien erstellen und öffnen.

HDR-Dateien werden auch als HDRI bezeichnet.

## HDR-Dateiformat – Weitere Informationen

Das HDR-Dateiformat basiert auf dem ursprünglichen Dateiformat Radiance Picture (.pic). Die Pixeldaten einer HDR-Datei werden normalerweise unkomprimiert gespeichert, aber in einigen Fällen werden sie mit einem einfachen Lauflängencodierungssystem komprimiert.

### HDR-Dateistruktur

Eine HDR-Bilddatei besteht aus den folgenden drei Abschnitten:

* **Header:** Eine HDR-Datei wird durch die ersten Bytes in der Bilddatei identifiziert, dh "#?RADIANCE".
* **Resolution String:** Dem Header folgt eine einzelne Auflösungszeile, die aus 4 Werten besteht; eine X- und Y-Beschriftung, jeweils gefolgt von einem numerischen ganzzahligen Wert. Die Reihenfolge von X und Y zeigt die Drehung an. Die Kombination von X und Y mit positiven und negativen Werten deckt alle möglichen Bildausrichtungen und Drehungen ab.
* **Pixeldaten:** Die Pixeldaten einer HDR-Datei sind entweder unkomprimiert oder mit einer standardmäßigen Lauflängenkodierung komprimiert.

## Open-Source-HDR/HDRI-APIs

* **[imageinfo](https://github.com/xiaozhuai/imageinfo )** - Plattformübergreifende, superschnelle Single-Header-[C++](/de/programming/cpp/)-Bibliothek, um Bildgröße und -format ohne Laden/Decodieren zu erhalten.
* **[imgaeinfo-rs](https://github.com/xiaozhuai/imageinfo-rs)** – Rust-Bibliothek zum Abrufen von Bildgröße und -format ohne Laden/Decodieren. Unterstützt [.avif](/de/image/avif/), [.bmp](/de/image/bmp), [.cur](/de/image/cur/), [.dds](/de/image/dds/), [. gif](/de/image/gif/), hdr (pic), [heic (heif)](/de/image/heic/), [.icns](/de/image/icns/), [.ico](/de/image/ico /), [.jp2](/de/image/jp2/), [jpeg (jpg)](/de/image/jpeg/), [jpx](/de/image/jpx/), ktx, [png](/de/image/png /), [psd](/de/image/psd/), qoi, tga, tiff (tif) und webp.
* **[HdrHistogram](https://github.com/HdrHistogram/HdrHistogram)** – Java-Implementierung von HdrHistogram.

## Verweise

* [Radiance HDR](http://paulbourke.net/dataformats/pic/)
* [Bildinfo](https://github.com/xiaozhuai/bildinfo)

