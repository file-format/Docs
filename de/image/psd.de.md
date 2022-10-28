{
  "date" : "2019-10-11",
  "keywords" :[ "psd-Datei", "psd-Dateiformat", "was ist eine psd-Datei", "Datei", "psd-Beispiel", "psd-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PSD - Photoshop-Bilddateiformat",
  "description":"Erfahren Sie mehr über das PSD-Dateiformat und APIs, die PSD-Dateien erstellen und öffnen können.",
  "linktitle" : "PSD",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Was ist eine PSD-Datei?

PSD, Photoshop Document, stellt das native Dateiformat von Adobe Photoshop dar, das für Grafikdesign und -entwicklung verwendet wird. PSD-Dateien können Bildebenen, Anpassungsebenen, Ebenenmasken, Anmerkungen, Dateiinformationen, Schlüsselwörter und andere Photoshop-spezifische Elemente enthalten. Photoshop-Dateien haben die Standarderweiterung .PSD und eine maximale Höhe und Breite von 30.000 Pixeln sowie eine Längenbeschränkung von zwei Gigabyte.

## PSD-Dateiformatspezifikationen ##

Daten in einer PSD-Datei werden in Big-Endian-Byte-Reihenfolge gespeichert. Dies impliziert das Austauschen der kurzen und langen Ganzzahlen beim Lesen oder Schreiben auf der Windows-Plattform. Das Photoshop-Dateiformat ist in fünf Hauptteile unterteilt. Es hat viele Längenmarkierungen, die verwendet werden können, um von einem Abschnitt zum nächsten zu wechseln. Die Längenmarkierungen werden normalerweise mit Bytes aufgefüllt, um auf das nächste 2- oder 4-Byte-Intervall zu runden. Die fünf Hauptteile sind:

* Dateikopf
* Farbmodusdaten
* Bildressourcen
* Ebenen- und Maskeninformationen
* Bilddaten

Aus Konformitätsgründen sollten Daten in alle diese Felder im Abschnitt geschrieben werden, da Photoshop möglicherweise versucht, den gesamten Abschnitt zu lesen. Es impliziert auch, dass beim Schreiben in eine Datei Nullen in übersprungene Felder geschrieben werden. Das Längenfeld in den längenbegrenzten Abschnitten sollte verwendet werden, um zu entscheiden, wann mit dem Lesen aufgehört werden soll. In den meisten Fällen gibt das Längenfeld die Anzahl der nachfolgenden Bytes und nicht der Datensätze an. Die folgenden Punkte müssen beim Lesen einer Datei beachtet werden.

* Die Werte in der Spalte "Länge" in allen Tabellen sind in Byte.
* Alle als Unicode-String definierten Werte bestehen aus:
* Ein 4-Byte-Längenfeld, das die Anzahl der Zeichen in der Zeichenfolge darstellt (nicht Bytes).
* Die Zeichenfolge von Unicode-Werten, zwei Bytes pro Zeichen.

### Dateikopf ###

Der Dateikopf enthält die grundlegenden Eigenschaften des Bildes.

|Länge|Beschreibung
---|---|
|4|Signatur: immer gleich '8BPS' . Versuchen Sie nicht, die Datei zu lesen, wenn die Signatur nicht mit diesem Wert übereinstimmt.
|2|Version: immer gleich 1. Versuchen Sie nicht, die Datei zu lesen, wenn die Version nicht mit diesem Wert übereinstimmt. (~*~*PSB~*~* Version ist 2.)
|6|Reserviert: muss Null sein.
|2|Die Anzahl der Kanäle im Bild, einschließlich aller Alphakanäle. Der unterstützte Bereich liegt zwischen 1 und 56.
|4|Die Höhe des Bildes in Pixel. Der unterstützte Bereich liegt zwischen 1 und 30.000.
|4|Die Breite des Bildes in Pixel. Der unterstützte Bereich liegt zwischen 1 und 30.000.
|2|Tiefe: Die Anzahl der Bits pro Kanal. Unterstützte Werte sind 1, 8, 16 und 32.
|2|Der Farbmodus der Datei. Unterstützte Werte sind: Bitmap # 0; Graustufen Nr. 1; Indiziert Nr. 2; RGB # 3; CMYK Nr. 4; Mehrkanal Nr. 7; Duoton Nr. 8; Labor Nr. 9.

### Farbmodus-Datenabschnitt ###

Der Datenbereich des Farbmodus ist wie folgt aufgebaut:


|Länge|Beschreibung
---|---|
|4|Die Länge der folgenden Farbdaten
|variable|Die Farbdaten

Farbmodusdaten sind nur für indizierte Farbe und Duplex verfügbar, wie durch das Modusfeld im Datei-Header-Abschnitt definiert. Für alle anderen Modi wird dieser Abschnitt durch 4-Byte-genullte Werte dargestellt. Bei indizierten Farbbildern beträgt die Länge 768, und die Farbdaten enthalten die Farbtabelle für das Bild in nicht verschachtelter Reihenfolge. Bei Duotone-Bildern enthalten Farbdaten die Duotone-Spezifikation (deren Format nicht dokumentiert ist). Andere Anwendungen, die Photoshop-Dateien lesen, können ein Duotone-Bild als graues Bild behandeln und beim Lesen und Schreiben der Datei einfach den Inhalt der Duotone-Informationen beibehalten.

### Abschnitt Bildressourcen ###

Der dritte Abschnitt der Datei enthält Bildressourcen. Es beginnt mit einem Längenfeld, gefolgt von einer Reihe von Ressourcenblöcken.


|Länge|Beschreibung
---|---|
|4|Länge des Bildressourcenabschnitts. Die Länge kann Null sein.
|Variable|Bildressourcen (Bildressourcenblöcke)

Bildressourcen werden verwendet, um Nicht-Pixel-Daten zu speichern, die Bildern zugeordnet sind, wie z. B. Stiftwerkzeugpfade. Sie werden als Ressourcenblöcke bezeichnet, da sie Daten enthalten, die in früheren Versionen von Photoshop in den Macintosh-Ressourcen gespeichert wurden. Die grundlegende Struktur von Bildressourcenblöcken ist wie folgt:


|Länge|Beschreibung
---|---|
|4|Signatur: '8BIM'
|2|Eindeutiger Bezeichner für die Ressource. Bildressourcen-IDs enthält eine Liste der von Photoshop verwendeten Ressourcen-IDs.
|Variable|Name: Pascal-String, aufgefüllt, um die Größe gleichmäßig zu machen (ein Null-Name besteht aus zwei Bytes von 0)
|4|Tatsächliche Größe der folgenden Ressourcendaten
|Variable|Die Ressourcendaten, beschrieben in den Abschnitten zu den einzelnen Ressourcentypen. Es ist gepolstert, um die Größe gleichmäßig zu machen.

Bildressourcen verwenden mehrere Standard-ID-Nummern.

### Ebenen- und Maskeninformationen ###

Der vierte Abschnitt einer Photoshop-Datei enthält Informationen zu Ebenen und Masken, z. B. Anzahl der Ebenen, Kanäle in den Ebenen, Mischbereiche, Keys für Anpassungsebenen, Effektebenen und Maskenparameter. Wenn keine Ebenen oder Masken vorhanden sind, wird dieser Abschnitt durch ein auf Null gesetztes 4-Byte-Feld dargestellt. Aufgrund der genullten Werte muss beim Lesen dieses Abschnitts besonders auf die Länge der Abschnitte geachtet werden. Die Anordnung des Ebenen- und Maskenabschnitts ist wie folgt:


|Länge|Beschreibung
---|---|
|4|Länge des Ebenen- und Maskeninformationsabschnitts. (PSB-Länge beträgt 8 Byte.)
|Variable|Ebeneninfo
|Variable|Informationen zu globalen Ebenenmasken
|Variable|Reihe markierter Blöcke, die verschiedene Datentypen enthalten.

#### Ebeneninfo ####

Die folgende Tabelle zeigt die allgemeine Organisation der Schichtinformationen.


|Länge|Beschreibung
---|---|
|4|Länge des Layer-Info-Abschnitts, aufgerundet auf ein Vielfaches von 2. (PSB-Länge beträgt 8 Byte.)
|2|Layer-Anzahl. Wenn es sich um eine negative Zahl handelt, ist ihr absoluter Wert die Anzahl der Ebenen und der erste Alphakanal enthält die Transparenzdaten für das zusammengeführte Ergebnis.
|Variable|Informationen zu jeder Ebene. Siehe Schichtdatensätze beschreibt die Struktur dieser Informationen für jede Schicht.
|Variable|Bilddaten des Kanals. Enthält für jede Schicht einen oder mehrere Bilddatensätze. Die Schichten sind in der gleichen Reihenfolge wie in den Schichtinformationen

### Bilddaten ###

Die Bildpixeldaten sind im Bilddatenabschnitt der Datei enthalten. Die Anordnung der Daten im Bilddatenabschnitt erfolgt in planarer Reihenfolge, dh zuerst alle roten Daten, dann alle grünen Daten usw. Jede Ebene wird in Abtastzeilenreihenfolge ohne Füllbytes gespeichert. Der Bilddatenabschnitt ist in einem Format angeordnet wie in der folgenden Tabelle gezeigt.

|Länge|Beschreibung
---|---|
|2|Komprimierungsverfahren: *0 = Rohbilddaten * 1 = RLE-komprimiert Die Bilddaten beginnen mit den Byte-Zählungen für alle Abtastzeilen (Zeilen * Kanäle), wobei jede Zählung als Zwei-Byte-Wert gespeichert wird. Die RLE-komprimierten Daten folgen, wobei jede Abtastzeile separat komprimiert wird. Die RLE-Komprimierung ist derselbe Komprimierungsalgorithmus, der von der Macintosh-ROM-Routine PackBits und dem TIFF-Standard verwendet wird. *2 = PLZ ohne Vorhersage *3 = PLZ mit Vorhersage.
|Variable|Die Bilddaten. Planare Ordnung = RRR GGG BBB usw.

## Verweise ##

* [PSD-Dateiformatspezifikationen – von Adobe](https://www.adobe.com/devnet-apps/photoshop/fileformatashtml/#50577409_pgfId-1030196)
* [Adobe Photoshop-Dateiformat](https://en.wikipedia.org/wiki/Adobe_Photoshop#Dateiformat)

