{
  "date" : "2019-10-11",
  "keywords" :[ "psb-Datei", "psb-Dateiformat", "was ist eine psb-Datei", "Datei", "psb-Beispiel", "psb-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PSB - Photoshop Big Image-Dateiformat",
  "description":"Erfahren Sie mehr über das PSB-Dateiformat und APIs, die PSB-Dateien erstellen und öffnen können.",
  "linktitle" : "PSB",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Was ist eine PSB-Datei?
Adobe Photoshop speichert Dateien in zwei Formaten. Dateien mit einer Größe von 30.000 x 30.000 Pixel werden mit der PSD-Erweiterung gespeichert, und Dateien, die größer als PSD bis zu 300.000 x 300.000 Pixel sind, werden mit der PSB-Erweiterung gespeichert, die als „Photoshop Big“ bekannt ist. Genauer gesagt können PSB-Dateien bis zu 4 EB (über 4,2 Milliarden GB) groß sein, mit Bildern, die eine Höhe und Breite von bis zu 300.000 Pixel haben. PSDs hingegen dürfen maximal 2 GB und Bildabmessungen von 30.000 Pixeln haben.

PSB ist auch als Großformat für Photoshop bekannt und unterstützt alle Photoshop-Funktionen wie Ebenen, Effekte und Filter. Photoshop kann PSB-Dateien in [PSD](/de/image/psd/), [JPG](/de/image/jpeg/) konvertieren. , [PNG](/de/image/png/), [EPS](/de/page-description-language/eps/), [GIF](/de/image/gif/) und auch andere Formate. Das große Photoshop-Dokumentformat ist verfügbar, sobald die Funktion des Dateiverwaltungsbereichs im Photoshop-Dialogfeld „Voreinstellungen“ aktiviert ist.

## Informationen zum Dateiformat ##

Das Photoshop-Dateiformat ist in fünf Hauptabschnitte mit vielen Längenmarkierungen unterteilt, die zwischen den Abschnitten verschoben werden können.

|Dateiformat
---|
|Datei-Header
|Farbmodusdaten
| Bildressourcen
|Ebenen- und Maskeninformationen
|(((
Bilddaten
)))

### Dateikopf ###

Der Dateikopf hat eine feste Länge von 26 Bytes und enthält die grundlegenden Eigenschaften des Bildes.

BYTE-Signatur [4] – Entspricht „8BPS“.

WORD-Version [2] – Versionsnummer, PSD Nr. 1, PSB Nr. 2.

BYTE Reserviert [6] – Reserviert und immer Null.

WORD-Kanäle [2] – Anzahl der Farbkanäle im Bild, einschließlich Alphakanäle. Sein Wert reicht von 1 bis 56.

LONG Rows [4] – Höhe des Bildes in Pixel, PSD 1-30.000, PSB 1-300.000.

LONG Columns [4] – Breite des Bildes in Pixel, PSD 1-30.000, PSB 1-300.000.

WORD-Tiefe [2] – Anzahl der Bits pro Kanal. Unterstützte Werte sind 1,8,16 und 32.

WORD-Modus [2] – Farbmodus der Datei.

#### Modus Beschreibung ####


|Modus|Beschreibung
---|---|
|0|Bitmap (monochrom)
|1|Graustufen
|2|Indiziert
|3|RGB
|4|CMYK
|7|Mehrkanal
|8|Duoton (Halbton)
|9|Lab

### Farbmodusdaten ###

Nach dem Datei-Header-Abschnitt folgt der Farbmodus-Datenabschnitt. Der Block beginnt mit einer LONG-Zahl, die die Länge des Blocks in Bytes angibt. Die Struktur der Farbmodusdaten ist wie folgt:

4 Bytes – Die Länge der folgenden Farbdaten.

Variable – Farbdaten

Wenn der Modusfeldwert im Header-Abschnitt nicht Indizierte Farbe oder Duplex ist, ist die Länge des Blocks 0 und es gibt keine Daten nach dem Längenfeld.

Für indizierte Farbbilder beträgt die Länge 768 Bytes, die eine Palette mit 256 Farben enthalten. Bei Duplex enthalten die Daten Bildschirmparameter und andere zugehörige Informationen.

### Bildressourcen ###

Nach dem Farbmodusdatenabschnitt ist der dritte Block der Bildressourcenabschnitt. Die ersten vier Bytes sind eine LONG-Zahl, die die Länge des Blocks angibt, gefolgt von einer Reihe von Ressourcenblöcken. Die Struktur des Bildressourcenblocks ist wie folgt:

BYTE Typ [4] – Signatur '8BIM'

WORT-ID [2] – Bildressourcen-ID. Es gibt eine Liste von Ressourcen-IDs, die über den Referenzlink eingesehen werden kann.

BYTE Name [Variable] – Name: Pascal String mit gerader Länge. ** **

LONG Size [4] – Tatsächliche Größe der folgenden Ressourcendaten.

BYTE Data [Variable} – Ressourcendaten. Es ist gepolstert, um eine gleichmäßige Größe zu erzielen.

Einige der Ressourcenformate werden im Folgenden kurz erläutert:

**Ressourcenformat für Raster und Hilfslinien:** Raster- und Hilfslinieninformationen werden im Ressourcenblock gespeichert. Diese Ressourcenblöcke enthalten ein 16-Byte-Raster und einen Leitkopf, gefolgt von 5-Byte-Blöcken mit Leitinformationen.

**Thumbnail-Ressourcenformat:** Thumbnail-Informationen werden im Bildressourcenblock für die Vorschauanzeige gespeichert, der aus einem 28-Byte-Header und JFIF-Thumbnail in RGB besteht.

**Ressourcenformat für Farbaufnehmer:** Farbaufnehmerinformationen werden im Bildressourcenblock mit einem 8-Byte-Header gespeichert, gefolgt von einem Block mit Farbaufnehmerinformationen variabler Länge.

### Ebenen- und Maskeninformationen ###

Der vierte Block ist ein Schicht- und Maskeninformationsblock und enthält Informationen über die Schichten und Masken. Schichtinformationen werden zuerst gespeichert und dann Maskeninformationen.

**Schichtinformationen:** Schichtinformationen beginnen mit einem LONG-Wert, der die Länge der Schichtinformationen anzeigt. Danach gibt es einen WORD-Wertzähler, der die Anzahl der folgenden Layer-Datensätze anzeigt.

[8] – Länge der Schichten

[2] – Schichtanzahl

[Variable] – Informationen zu jeder Ebene.

[Variable] – Kanalbilddaten.** **

**Maskeninformationen:** Die Maskenstruktur hat das folgende Format:


|Datenstruktur|Feldname| Beschreibung
---|---|---|
|WORT| Overlay-Farbraum| (nicht dokumentiert)
|BYTE[8]| Farbkomponenten| 4x2 Byte Farbkomponenten
|WORT| Deckkraft| 0#transparent, 1#undurchsichtig
|BYTE| Art| 0#invertiert, 1#geschützt, 128#gespeicherten Wert verwenden
|BYTE| Polsterung| auf Null gesetzt

### Bilddaten ###

Der letzte Abschnitt enthält die Bildpixeldaten. Die Bilddaten werden als eine Reihe von Sequenzen in Ebenen gespeichert, dh zuerst alle roten Daten, dann alle grünen Daten usw. WORD am Anfang jeder Zeile zeigt die Größe in Bytes bezogen auf jede Abtastzeile.

[2] – Kompressionsverfahren:

[Variable] – Bilddaten in planarer Reihenfolge, dh RRRR, GGGG, BBBB usw.

Komprimierungsmethoden:

0 – Raw Bilddaten

1 – RLE komprimiert

2 – Reißverschluss ohne Vorhersage

3 – Reißverschluss mit Vorhersage

## Bezug ##

* [PSB-Dateiformat – von Adobe] (https://www.adobe.com/devnet-apps/photoshop/fileformatashtml/)
* [PSB – Wikipedia](https://en.wikipedia.org/wiki/Adobe_Photoshop#Dateiformat)

