{
  "date" : "2019-12-09",
  "keywords" :[ "zl-Datei", "zl-Dateiformat", "was ist eine zl-Datei", "Datei", "zl-Beispiel", "zl-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ZL - komprimiertes ZLIP-Dateiformat",
  "description":"Erfahren Sie mehr über das ZL-Dateiformat und APIs, die ZL-Dateien erstellen und öffnen können.",
  "linktitle" : "ZL",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-14"
}

## Was ist eine ZL-Datei?

Eine Datei mit der Erweiterung .zl ist ein ZLIP-komprimiertes Dateiformat, das eine Variante des DEFLATE-Komprimierungsalgorithmus zum Komprimieren von Dateien verwendet. Es ist unabhängig von CPU-Typ, Betriebssystem, Dateisystem und Zeichensatz und kann daher zum Austausch von Informationen verwendet werden. Technische Spezifikationen der ZLIP-Komprimierung sind auf der [IETF-Website](https://tools.ietf.org/html/rfc1950) verfügbar und können aus Entwicklersicht herangezogen werden.

## ZL-Dateiformat

Ein zlib-Stream hat die folgende Struktur:

* `CMF (Compression Method and flags)` - Dieses Byte ist in Abhängigkeit von dem Kompressionsverfahren in ein 4-Bit-Kompressionsverfahren und ein 4-Bit-Informationsfeld unterteilt.
```
bits 0 to 3  CM     Compression method
bits 4 to 7  CINFO  Compression info
```
* `CM (Komprimierungsmethode)` - Gibt die in der Datei verwendete Komprimierungsmethode an. Seine Werte und das entsprechende Komprimierungsverfahren sind wie folgt.

| CM-Wert| Komprimierung|
|---|---|
|CM = 8|DEFLATE mit einer Fenstergröße bis 32K|
|CM = 15|Reserviert|

* `CINFO (Compression info)` - Für CM = 8 ist CINFO der Basis-2-Logarithmus der LZ77-Fenstergröße minus acht (CINFO=7 gibt eine 32K-Fenstergröße an).

* `FLG (FLaGs)` - Dieses Flag-Byte ist wie folgt aufgeteilt:
```
  bits 0 to 4  FCHECK  (check bits for CMF and FLG)
  bit  5       FDICT   (preset dictionary)
  bits 6 to 7  FLEVEL  (compression level)
````

## Verweise ##

* [Zlib-Dateiformatspezifikationen](https://tools.ietf.org/html/rfc1950)

