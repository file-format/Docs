{
  "date" : "2019-10-11",
  "keywords" :[ "xpm-Datei", "xpm-Dateiformat", "was ist eine xpm-Datei", "Datei", "xpm-Beispiel", "xpm-Dateierweiterung", "Erweiterung", "Format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XPM - X PixMap-Dateiformat",
  "description":"Erfahren Sie mehr über das XPM-Dateiformat und APIs, die XPM-Dateien erstellen und öffnen können.",
  "linktitle" :"XPM",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Was ist eine XPM-Datei?

Eine Datei mit der Erweiterung .xpm ist ein Bilddateiformat, das vom X Windows-System verwendet wurde. Es unterstützt transparente Pixel und zielt normalerweise darauf ab, Symbol-Pixmaps zu erstellen. Es unterstützt Schwarzweiß-, Graustufen- und Farb-Pixmap-Daten. Diese wurden so entworfen, dass sie von Hand bearbeitet werden können und in [C](/de/programming/c/)-Code eingefügt werden können. Zu diesem Zweck sind XPM-Dateien im Nur-Text-Dateiformat und folgen der Syntax der C-Programmiersprache. XPM-Dateien können mit einer Vielzahl von Bildbetrachtungsprogrammen geöffnet werden, z
CorelDRAW Graphics Suite 2020, Corel PaintShop Pro, IrfanView und Canvas X.

## XPM-Dateiformat

Das XPM-Dateiformat verwendet die C-Syntax, um diese in C- und C++-Programme integrieren zu können. Es besteht aus den folgenden sechs verschiedenen Abschnitten.

* \<Values>
* \<Colors>
* \<Pixels>
* \<Extensions>

Die Abschnitte sind eigentlich ein Array von Zeichenfolgen wie folgt.

```
/* XPM */
static char*<variable_name>[] = {
  <Values>
  <Colors>
  <Pixels>
  <Extensions>
};
```
Im Folgenden finden Sie die Details der einzelnen Abschnitte.

`<Values> ` - Dieser Abschnitt ist eine Zeichenfolge, die vier oder sechs Ganzzahlen enthält, die zur Basis 10 stehen und entsprechen:

* Pixmap-Breite und -Höhe
* Anzahl der Farben
* Anzahl der Zeichen pro Pixel
* optionale Hotspot-Koordinaten und XPMEXT-Tag

`<Colors> ` - Dieser Abschnitt enthält so viele Zeichenketten wie es Farben gibt. Jede Saite ist wie folgt:

```
<chars>{<key><color> }+
```
`<Pixels> ` - Dieser Abschnitt besteht aus<height> Saiten und<width> \*<chars_per_pixel> Figuren. Jeder<chars_per_pixel> length string sollte eine der zuvor definierten Gruppen in sein<Colors> Sektion.

`<Extension> ` - Der Erweiterungsabschnitt muss, wenn er nicht leer ist, im gekennzeichnet werden<Values> Sektion. Es kann aus mehreren bestehen<Extension> Unterabschnitte, die von den folgenden zwei Arten sein können:

* eine eigenständige Zeichenfolge, die wie folgt zusammengesetzt ist: XPMEXT<extension-name><extension-data>
* oder ein Block, der aus mehreren Strings besteht:XPMEXT<extension-name><related extension-data composed of several strings>

## Verweise

* [XPM – Wikipedia](https://en.wikipedia.org/wiki/X_PixMap)
* [XPM-Handbuch](http://www.xfree86.org/current/xpm.pdf)

