{
  "date" : "2021-02-25",
  "keywords" :[ "bdf-Datei", "bdf-Dateiformat", "was ist eine bdf-Datei", "Datei", "bdf-Beispiel", "bdf-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"BDF - Glyphen-Bitmap-Verteilungsformat",
  "description":"Erfahren Sie mehr über das BDF-Dateiformat und APIs, die BDF-Dateien erstellen und öffnen können.",
  "linktitle" :"BDF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2021-02-25"
}

## Was ist eine BDF-Datei?
BDF-Dateien sind menschenlesbar und werden normalerweise in einer ASCII-Codierung verteilt. Die Datei beginnt mit globalen Informationen, die für die gesamte Schriftart relevant sind, gefolgt von den Informationen und Bitmaps für die einzelnen Glyphen. Die darin enthaltenen Daten zeigen die Schriftart für eine einzelne Größenausrichtung. Die in mehr als einer Richtung zu verwendenden Metriken können in einer einzigen Datei enthalten sein. In der BDF-Datei ist jedes Element in einer separaten Textzeile in der Datei enthalten. Leerzeichen werden verwendet, um die Elemente in einer Zeile zu trennen.

## BDF-Dateiformat
Die BDF-Kurzform für Glyph Bitmap Distribution Format; Eigentum von Adobe ist ein Dateiformat zum Speichern von Schriftarten vom Typ Bitmap. Der Inhalt hat die Form einer Textdatei, die sowohl für Computer als auch für Menschen lesbar sein soll. Das BDF wird insbesondere in Unix X Window-Umgebungen verwendet. Es wurde weitgehend durch das angeblich effizientere PCF-Fontformat sowie durch OpenType- und TrueType-Fonts ersetzt.
### BDF-Dateistruktur
Eine BDF-Schriftartdatei besteht aus drei Abschnitten:

- ein globaler Abschnitt, der für alle Glyphen in einer Schriftart gilt.
- ein Abschnitt mit einem separaten Eintrag für jede Glyphe.
- die ENDFONT-Anweisung.

## Beispiel
Hier ist eine Beispielschrift, die eine Glyphe für ASCII-Großbuchstaben „A“ enthält. Seine globalen Deklarationen beginnen mit der "STARTFONT"-Zeile und enden mit der "CHARS"-Zeile
```
STARTFONT 2.1
FONT -gnu-unifont-medium-r-normal--16-160-75-75-c-80-iso10646-1
SIZE 16 75 75
FONTBOUNDINGBOX 16 16 0 -2
STARTPROPERTIES 2
FONT_ASCENT 14
FONT_DESCENT 2
ENDPROPERTIES
CHARS 1
STARTCHAR U+0041
ENCODING 65
SWIDTH 500 0
DWIDTH 8 0
BBX 8 16 0 -2
BITMAP
00
00
00
00
18
24
24
42
42
7E
42
42
42
42
00
00
ENDCHAR
ENDFONT
```



## Verweise
* [Glyph Bitmap Distribution Format](https://en.wikipedia.org/wiki/Glyph_Bitmap_Distribution_Format)
* [Glyph Bitmap Distribution Format (BDF) Specification](https://adobe-type-tools.github.io/font-tech-notes/pdfs/5005.BDF_Spec.pdf)

