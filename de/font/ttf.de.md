{
  "date" : "2020-08-20",
  "keywords" :[ "ttf-Datei", "ttf-Dateiformat", "was ist eine ttf-Datei", "Datei", "ttf-Beispiel", "ttf-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TTF - Dateiformat für TrueType-Schriftarten",
  "description":"TrueType-Schriftarten (TTF) basieren auf technischen Spezifikationen für digitale Schriftarten, die ursprünglich von Apple, Inc. entwickelt wurden. Sowohl Apple als auch Microsoft verwendeten TTF auf Mac- und Windows-Betriebssystemen.",
  "linktitle" : "TTF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-09-21"
}

## Was ist eine TTF-Datei?

Eine Datei mit der Erweiterung .ttf stellt Schriftartdateien dar, die auf der Schriftarttechnologie der TrueType-Spezifikationen basieren. Es wurde ursprünglich von Apple Computer, Inc. für Mac OS entwickelt und eingeführt und später von Microsoft für Windows OS übernommen. TrueType-Schriftarten bieten eine Anzeige in höchster Qualität auf Computerbildschirmen und Druckern ohne Abhängigkeit von der Auflösung. Alle modernen Anwendungen, die Schriftarten verwenden, können mit TTF-Dateien arbeiten. TTF-Schriftdateien sind im Internet frei verfügbar und können auch in andere Schriftdateiformate wie OTF und WOFF konvertiert werden.

## Kurze Geschichte

Das TTF-Schriftformat wurde in den 1980er Jahren von Apply Computer, Inc. für MacOS entwickelt und zielte darauf ab, einige technische Einschränkungen des Typ-1-Formats von Adobe zu beheben. Apple hat 1991 Unterstützung für TrueType-Schriftarten in Mac integriert. Das Designziel hinter TTF-Schriftarten war Effizienz bei der Speicherung und Verarbeitung sowie Erweiterbarkeit. Basierend auf dieser Erweiterbarkeit können bestehende Schriftarten in das TrueType-Format konvertiert werden.

Microsoft verwendete die TrueType-Schriftarten erstmals im April 1992 in Windows 3.1, nachdem Apple zugestimmt hatte, TrueType an Microsoft zu lizenzieren. Es verbesserte den Rasterisierungsmechanismus und verbesserte seine Effizienz und Leistung.

## Spezifikationen des True Type-Dateiformats

Eine TrueType-Schriftartdatei ist eine Binärdatei, die aus einer Folge verketteter Tabellen besteht. Jede Tabelle ist eine Folge von Wörtern und hat einen Namen, der als "Tag" bekannt ist. Jedes Tag ist vom Datentyp uint32 und besteht aus vier Zeichen. Die erste Tabelle in der Datei ist das Font-Verzeichnis, das Zugriff auf andere Tabellen in der Font-Datei gewährt. Zeichensatzdaten sind in anderen Tabellen enthalten, die nach der Zeichensatzverzeichnistabelle folgen. Da auf jede Tabelle über ihr Tag zugegriffen werden kann, können die Tabellen in der Datei in beliebiger Reihenfolge erscheinen.

Die erforderlichen Tabellen und ihre Tag-Namen sind in der folgenden Tabelle aufgeführt.

|**Tag**|**Tabelle**|
---|---|
|'cmap'| Zuordnung von Zeichen zu Glyphen|
|'glyf'| Glyphendaten|
|'Kopf'| Schriftkopf |
|'hea'| horizontale Kopfzeile|
|'hmtx'| horizontale Metriken|
|'loca'| Index zum Ort|
|'maxp'| maximales Profil|
|'Name'| Benennung|
|'posten'| PostScript|

### Datentypen
TrueType-Schriftarten verwenden die Standard-Ganzzahl und zusätzliche Datentypen, wie in der folgenden Tabelle aufgeführt.

|**Datentyp** | **Beschreibung** |
---|---|
|shortFrac| 16-Bit-Bruch mit Vorzeichen|
|Behoben| 16,16-Bit-Festkommazahl mit Vorzeichen|
|FWort| 16-Bit-Ganzzahl mit Vorzeichen, die eine Menge in FUnits beschreibt, die kleinste messbare Entfernung im em-Raum.|
|uFWort| 16-Bit-Ganzzahl ohne Vorzeichen, die eine Menge in FUnits beschreibt, die kleinste messbare Entfernung im em-Raum.|
|F2Punkt14| Vorzeichenbehaftete 16-Bit-Festzahl, wobei die niedrigen 14 Bits einen Bruch darstellen.|
|longDateTime| Das lange interne Format eines Datums in Sekunden seit 12:00 Uhr, 1. Januar 1904. Es wird als vorzeichenbehaftete 64-Bit-Ganzzahl dargestellt.|

### Font-Verzeichnis

Die erste Tabelle in der TrueType-Schriftart ist das Schriftartenverzeichnis, das Zugriff auf die Informationen bietet, die für den Zugriff auf Daten in anderen Tabellen erforderlich sind. Es besteht weiterhin aus:

* `Offset subtable` - zeichnet die Tabellen in der Schriftart auf und stellt Offset-Informationen bereit, um auf jede Tabelle im Verzeichnis zuzugreifen
* `Tabellenverzeichnis` - Enthält Einträge für jede Tabelle in der Schriftart

#### Offset-Untertabelle
Die Offset-Untertabelle ist unten gezeigt.

|**Typ**|**Name**|**Beschreibung**|
---|---|---|
|uint32| Scaler-Typ| Ein Tag, um den OFA-Skalierer anzugeben, der zum Rastern dieser Schriftart verwendet werden soll; Weitere Informationen finden Sie im Hinweis zum Scaler-Typ unten.|
|uint16| numTables| Anzahl Tische|
|uint16| Suchbereich| (maximale Potenz von 2 <= numTables)*16|
|uint16| entrySelector| log2(maximale Potenz von 2 <= numTables)|
|uint16| rangeShift| numTables*16-Suchbereich|

#### Tabellenverzeichnis
Das Tabellenverzeichnis kommt direkt nach der Offset-Untertabelle. Seine Struktur ist wie in der folgenden Tabelle gezeigt.

|**Typ**|**Name**|**Beschreibung**|
---|---|---|
|uint32| Tag| 4-Byte-Kennung|
|uint32| Prüfsumme| Prüfsumme für diese Tabelle|
|uint32| Versatz| Versatz vom Anfang von sfnt|
|uint32| Länge| Länge dieser Tabelle in Byte (tatsächliche Länge nicht aufgefüllte Länge)|

Jede Tabelle in einer Schriftartdatei muss einen eigenen Tabellenverzeichniseintrag haben. Einträge in einer Tabelle müssen aufsteigend nach Tag sortiert werden.


## Verweise
* [Referenzhandbuch für TrueType-Schriftarten](https://developer.apple.com/fonts/TrueType-Reference-Manual/)
* [TrueType-Übersicht](https://docs.microsoft.com/en-us/typography/truetype/)

