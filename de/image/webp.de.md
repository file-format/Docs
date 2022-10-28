{
  "date" : "2019-10-11",
  "keywords" :[ "Webp-Datei", "Webp-Dateiformat", "Was ist eine Webp-Datei", "Datei", "Webp-Beispiel", "Webp-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"WEBP - Google-Rasterbild-Dateiformat",
  "description":"Erfahren Sie mehr über das WEBP-Dateiformat und APIs, die WEBP-Dateien erstellen und öffnen können.",
  "linktitle" : "WEBP",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Was ist eine WEBP-Datei?

WebP, eingeführt von Google, ist ein modernes Raster-Webbild-Dateiformat, das auf verlustfreier und verlustbehafteter Komprimierung basiert. Es bietet die gleiche Bildqualität, während die Bildgröße erheblich reduziert wird. Da die meisten Webseiten Bilder als effektive Darstellung von Daten verwenden, führt die Verwendung von WebP-Bildern auf Webseiten zu einem schnelleren Laden von Webseiten. Laut Google sind verlustfreie WebP-Bilder im Vergleich zu [PNGs](/de/image/png/) um 26 % kleiner, während verlustbehaftete WebP-Bilder 25–34 % kleiner sind als vergleichbare [JPEG](/de/image/jpeg/)-Bilder. Bilder werden basierend auf dem Index der strukturellen Ähnlichkeit (SSIM) zwischen WebP und anderen Bilddateiformaten verglichen. WebP ist ein Schwesterprojekt des Multimedia-Containerformats [WebM](https://en.wikipedia.org/wiki/WebM).

## Überblick über WebP-Funktionen ##

WebP-Bilder verwenden den Komprimierungsprozess basierend auf der Vorhersage von Pixeln aus ihren umgebenden Blöcken, was dazu führt, dass Pixel in einer einzigen Datei mehrfach verwendet werden. Es unterstützt animierte Bilder und wird voraussichtlich in Zukunft weitere Funktionen unterstützen. Google hat den Quellcode [online] (https://developers.google.com/speed/webp/download) für seinen Encoder und Decoder zur Verfügung gestellt, um ihn bei Bedarf zu verwenden. Das WebP-Image bietet Unterstützung für:

* **Verlustbehaftete Komprimierung:** Die verlustbehaftete Komprimierung basiert auf [VP8](http://en.wikipedia.org/wiki/VP8) Keyframe-Codierung. VP8 ist ein Videokomprimierungsformat, das von On2 Technologies als Nachfolger der Formate VP6 und VP7 entwickelt wurde.
* **Verlustfreie Komprimierung:** Das verlustfreie Komprimierungsformat wird vom WebP-Team entwickelt.
* **Transparenz:** 8-Bit-Alphakanal ist nützlich für grafische Bilder. Der Alpha-Kanal kann zusammen mit verlustbehaftetem RGB verwendet werden, eine Funktion, die derzeit mit keinem anderen Format verfügbar ist.
* **Animation:** Unterstützt echtfarbige animierte Bilder.
* **Metadaten:** Es kann EXIF- und XMP-Metadaten enthalten (z. B. von Kameras verwendet).
* **Farbprofil:** Es kann ein eingebettetes ICC-Profil haben.

Die verlustbehaftete WebP-Komprimierung verwendet Predictive Coding, um ein Bild zu codieren, dieselbe Methode, die vom VP8-Videocodec verwendet wird, um Keyframes in Videos zu komprimieren. Die prädiktive Codierung verwendet die Werte in benachbarten Pixelblöcken, um die Werte in einem Block vorherzusagen, und codiert dann nur die Differenz.

Die verlustfreie WebP-Komprimierung verwendet bereits gesehene Bildfragmente, um neue Pixel exakt zu rekonstruieren. Es kann auch eine lokale Palette verwenden, wenn keine interessante Übereinstimmung gefunden wird.

## Datei Format ##

Das WebP-Dateiformat basiert auf dem Dokumentenformat RIFF (Resource Interchange File Format). Der WebP-Container bietet Unterstützung für mehr als nur ein einzelnes Bild, das als VP8-Keyframe codiert ist. Das Grundelement einer RIFF-Datei ist ein Chunk, der besteht aus:


|Feld|Beschreibung
---|---|
|Chunk FourCC: 32 Bit|ASCII-Vierzeichencode, der zur Chunk-Identifikation verwendet wird
|Chunk-Größe: 32 Bit (uint32)|Die Größe des Chunks ohne dieses Feld, die Chunk-ID oder das Padding
|Chunk Payload: Chunk Size bytes|Die Datennutzlast. Wenn die Chunk-Größe ungerade ist, wird ein einzelnes Füllbyte ~-~-, das 0 ~-~- sein sollte, hinzugefügt
|ChunkHeader ('ABCD')|Wird verwendet, um den FourCC- und Chunk-Size-Header einzelner Chunks zu beschreiben, wobei 'ABCD' der FourCC für den Chunk ist. Die Größe dieses Elements beträgt 8 Bytes.

### WebP-Header ###

Ein WebP-Datei-Header sieht wie folgt aus:

* RIFF-Header – 32 Bits, die die ASCII-Zeichen „R“ „I“ „F“ „F“ darstellen
* Dateigröße - 32 Bits (uint32), die die Größe der Datei in Bytes ab Offset 8 darstellen. Der maximale Wert dieses Felds beträgt 2^32 minus 10 Bytes und somit beträgt die Größe der gesamten Datei höchstens 4 GB minus 2 Bytes .
* 'WEBP' - 32 Bits, die die ASCII-Zeichen 'W' 'E' 'B' 'P' darstellen

### Verlustbehaftetes Dateiformat ###

WebP-Bilder verwenden das verlustbehaftete Dateiformat, wenn das Bild auf verlustbehafteter Codierung basiert und keine erweiterten/erweiterten Funktionen wie Transparenz, Animation, Alpha usw. erfordert. Verlustbehaftete Bilder sind kleiner und werden auch von älteren Anwendungen unterstützt.

Die WebP-Datei besteht in diesem Fall aus:

* 12 Bytes Header der WebP-Datei
* VP8-Stück

Der [VP8 Data Format and Decoding Guide](https://tools.ietf.org/html/rfc6386) veranschaulicht die Spezifikationen des VP8-Bitstream-Formats.

### Verlustfreies Dateiformat ###

Dieses Layout wird verwendet, wenn das Bild auf verlustfreier Codierung basiert und die erweiterten Funktionen des externen Formats nicht benötigt werden. Ältere Anwendungen können solche Dateien jedoch möglicherweise nicht lesen.

Die WebP-Datei besteht in diesem Fall aus:

* 12 Bytes Header der WebP-Datei
* VP8L-Stück

## Verweise ##

* [Referenz für WebP-Entwickler – von Google](https://developers.google.com/speed/webp/)
* [WebP-Dateiformat – von Wikipedia](https://en.wikipedia.org/wiki/WebP)

