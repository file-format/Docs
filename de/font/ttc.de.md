{
  "date" : "2021-02-25",
"Schlüsselwörter": [ "ttc-Datei", "ttc-Dateiformat", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TTC - TrueType-Sammlungsdateiformat",
  "description":"Eine TrueType Collection (TTC)-Datei kombiniert mehrere Schriftarten in einer einzigen Datei. Sowohl Apple als auch Microsoft verwendeten TTF auf Mac- und Windows-Betriebssystemen.",
  "linktitle" : "TTC",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2021-02-25"
}

## Was ist eine TTC-Datei?
Die TTC wird als TrueType Collection abgekürzt und ist eine Erweiterung des TrueType-Formats. Eine TTC-Datei kann die mehreren Schriftartdateien darin kombinieren. Diese Dateien sind nützlich, um mehrere Schriftarten zu kombinieren, die viele Glyphen gemeinsam haben. Vor Windows 2000 wurden die TTC-Dateien in chinesischen, japanischen und koreanischen Versionen von Windows verwendet, aber später war die Unterstützung für alle Regionen verfügbar.


## Die Struktur der Schriftsammlungsdatei
Eine TTC-Datei besteht aus einer TTC-Header-Tabelle, Tabellenverzeichnissen und mehreren OpenType-Tabellen. Der TTC-Header muss am Anfang der Datei stehen. Für jede Schriftart muss ein vollständiges Tabellenverzeichnis vorhanden sein. Das TableDirectory-Format sollte ähnlich sein wie in einer Nicht-Sammlungsdatei. Die Tabellenzählungen in allen Verzeichnissen innerhalb einer TTC-Datei werden vom Beginn einer TTC-Datei an berechnet.
Auf die Tabellen in einer TTC-Datei wird über das Tabellenverzeichnis ihrer jeweiligen Schriftarten verwiesen. Einige der OpenType-Tabellen müssen mehrmals erscheinen, einmal für jede in der TTC hinzugefügte Schriftart. Während die anderen Tabellen von mehreren Schriftarten in der TTC-Datei gemeinsam genutzt werden können.

### TTC-Header
Bisher sind zwei Versionen der TTC-Header-Tabelle verfügbar:
- Version 1.0 wird für TTC-Dateien ohne digitale Signaturen verwendet.
- Version 2.0 kann für TTC-Dateien mit oder ohne digitale Signatur verwendet werden.
Hier sind die TTC-Header-Tabellen beider Versionen:

**TTC-Header-Version 1.0:**

|Typ|Name|Beschreibung|
---|---|---|
|TAG|ttcTag|Font Collection ID string: 'ttcf' (wird für Schriftarten mit CFF- oder CFF2-Konturen sowie TrueType-Konturen verwendet)|
|uint16|majorVersion|Hauptversion des TTC-Headers, = 1.|
|uint16|minorVersion|Nebenversion des TTC-Headers, = 0.|
|uint32|numFonts|Anzahl der Schriftarten in TTC|
|Offset32|tableDirectoryOffsets[numFonts]|Array von Offsets zum TableDirectory für jede Schriftart vom Anfang der Datei|

**TTC-Header-Version 2.0:**

|Typ|Name|Beschreibung|
---|---|---|
|TAG|ttcTag |Font-Collection-ID-String: 'ttcf'|
|uint16| majorVersion |Hauptversion des TTC-Headers, = 2.|
|uint16| minorVersion |Nebenversion des TTC-Headers, = 0.|
|uint32| numFonts |Anzahl Schriftarten in TTC|
|Offset32| tableDirectoryOffsets[numFonts] |Array von Offsets zum TableDirectory für jede Schriftart vom Anfang der Datei|
|uint32| dsigTag |Tag, das angibt, dass eine DSIG-Tabelle existiert, 0x44534947 ('DSIG') (null, wenn keine Signatur)|
|uint32| dsigLength |Die Länge (in Bytes) der DSIG-Tabelle (null, wenn keine Signatur)|
|uint32| dsigOffset |Der Offset (in Bytes) der DSIG-Tabelle vom Anfang der TTC-Datei (null, wenn keine Signatur)|

## Verweise
* [Die OpenType-Schriftartdatei](https://docs.microsoft.com/en-us/typography/opentype/spec/otff)
* [TrueType (Wikipedia)](https://en.wikipedia.org/wiki/TrueType)

