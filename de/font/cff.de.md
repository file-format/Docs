{
  "date" : "2020-08-20",
  "keywords" :[ "cff-Datei", "cff-Dateiformat", "was ist eine cff-Datei", "Datei", "cff-Beispiel", "cff-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CFF - Kompaktes Schriftdateiformat",
  "description":"Erfahren Sie mehr über das CFF-Dateiformat und APIs zum Erstellen und Öffnen von CFF-Dateien.",
  "linktitle" : "CFF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-21"
}

## Was ist eine CFF-Datei?

Eine Datei mit der Erweiterung .cff ist ein Compact Font Format und wird auch als PostScript Type 1 oder CIDFont bezeichnet. CFF fungiert als Container zum gemeinsamen Speichern mehrerer Schriftarten in einer einzigen Einheit, die als FontSet bezeichnet wird. Das Design von CFF-Fonts ermöglicht das Einbetten von PostScript-Sprachcode, der zusätzliche Flexibilität und Erweiterbarkeit des Formats für die Verwendung mit Druckerumgebungen ermöglicht. CFF-Schriftartendateien können mit APIs wie [Aspose.Font](https://products.aspose.com/font) geöffnet und konvertiert werden.

## CFF-Dateiformat

CFF-Dateien sind Binärdateien, die ein strukturiertes Datenlayout, definierte Datentypen, einen Header, eine Glyphenorganisation und Tabellenwörterbücher enthalten. Weitere Einzelheiten hierzu finden Sie in den [Spezifikationen für kompaktes Schriftformat] (https://docs.microsoft.com/en-us/typography/opentype/spec/cff).

### Datenlayout
Das Datenlayout des CFF-Dateiformats ist wie unten gezeigt.

|Eintrag|Kommentare|
---|---|
|Kopfzeile|–|
|NameINDEX|–|
|Top DICT INDEX|–|
|Zeichenfolge INDEX|–|
|Global Subr INDEX|–|
|Codierungen–Zeichensätze|–|
|FDSelect|Nur CIDFonts|
|CharStrings INDEX|pro Schriftart|
|Font DICT INDEX|pro Schriftart, nur CIDFonts|
|Privates DICT|pro Schriftart|
|Local Subr INDEX|per-font or per-Private DICT for CIDFonts|
|Urheberrechts- und Markenhinweise|–|

### Datentypen

CFF-Datentypen werden in der folgenden Tabelle gezeigt.

|Name|Bereich|Beschreibung|
---|---|---|
|Karte8|0 –255|1-Byte-Zahl ohne Vorzeichen|
|Karte16|0 – 65535|2-Byte-Zahl ohne Vorzeichen|
|Offset|variiert|1-, 2-, 3- oder 4-Byte-Offset (angegeben durch das OffSize-Feld)|
|OffSize|1–4|1-Byte-Zahl ohne Vorzeichen gibt die Größe eines oder mehrerer Offset-Felder| an
|SID|0 – 64999|2-Byte-String-Kennung|

### Header

Die Binärdaten beginnen mit einem Header mit dem in der folgenden Tabelle gezeigten Format.

|Typ|Name|Beschreibung|
---|---|---|
|Card8|major|Hauptversion formatieren (beginnend bei 1)|
|Card8|minor|Minor-Version formatieren (beginnend bei 0)|
|Karte8|hdrGröße| Header-Größe (Byte)|
|OffSize|offSize|Absoluter Offset (0) Größe|

## Verweise

* [Compact Font Format Table](https://docs.microsoft.com/en-us/typography/opentype/spec/cff)
* [CFF-Dateiformat](https://adobe-type-tools.github.io/font-tech-notes/pdfs/5176.CFF.pdf)
* [CFF2 Chartset](https://docs.microsoft.com/en-us/typography/opentype/spec/cff2charstr)

