{
  "date" : "2020-08-20",
  "keywords" :[ "cff2-Datei", "cff2-Dateiformat", "was ist eine cff2-Datei", "Datei", "cff2-Beispiel", "cff2-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CFF2 - Kompaktes Schriftdateiformat Version 2",
  "description":"Erfahren Sie mehr über das CFF2-Dateiformat und APIs zum Erstellen und Öffnen von CFF2-Dateien.",
  "linktitle" : "CFF2",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-21"
}

## Was ist eine CFF2-Datei?

Das CFF2-Dateiformat ist die Version 2.0 des CFF-Dateiformats und ermöglicht eine effiziente Speicherung von Glyphenumrissen und Metadaten ähnlich dem CFF-Dateiformat. CFF2 unterscheidet sich von CFF darin, dass es im Zusammenhang mit einer OpenType-Schriftart als 'sfnt'-Tabelle mit dem Tag CFF2 verwendet werden soll. Es kann nicht als eigenständiges Programm verwendet werden und hängt von Daten in anderen OpenType-Tabellen ab.

## CFF2-Dateiformat

Die [CFF2-Dateiformatspezifikationen](https://docs.microsoft.com/en-us/typography/opentype/spec/cff2) enthalten Details zum internen Datenlayout, zu Datentypen, Tabellen und anderen internen Informationen zum Dateiformat. Es kann als Entwicklerreferenz verwiesen werden. Einige Details dazu sind wie folgt.

### Datenlayout

Die binären Daten des CFF2-Dateiformats sind logisch als eine Anzahl separater Datenstrukturen organisiert. Das Layout innerhalb der Binärdaten ist wie in der folgenden Tabelle gezeigt.

|Eintrag |Kommentare|
---|---|
|Kopfzeile |Fester Ort|
|Top DICT| Fester Standort|
|Globaler Subr-INDEX| Fester Standort|
|Variation |Speichern|
|FDSelect |Nur vorhanden, wenn mehr als ein Font DICT im Font DICT INDEX vorhanden ist.|
|Schriftart DICT INDEX ||
|Array von Schriftarten DICT| In Schriftart DICT INDEX enthalten.|
|Privates DICT| Eine pro Schriftart DICT.|

Nur die ersten drei Strukturen basieren auf festen Standorten. Die restlichen werden über Offsets erreicht, und ihre Reihenfolge kann geändert werden.

### Datentypen

Das CFF2-Dateiformat verwendet die folgenden Datentypen.

|Name |Bereich |Beschreibung|
---|---|---|
|uint8 |0 bis 255 |8-Bit-Zahl ohne Vorzeichen|
|uint16 |0 bis 65535| 16-Bit-Zahl ohne Vorzeichen|
|uint32 |0 bis 4294967295| 32-Bit-Zahl ohne Vorzeichen|
|Offset |variiert| 1, 2, 3 oder 4 Byte-Offsets (angegeben durch das OffSize-Feld in einer Indextabelle)|
|OffSize |1 bis 4| Eine 1-Byte-Zahl ohne Vorzeichen gibt die Größe eines Offset-Felds oder von Feldern| an

Es speichert alle numerischen Multibyte-Daten und Offset-Felder in Big-Endian-Byte-Reihenfolge. Das CFF2-Format ist frei von Füllbytes, da es keine Ausrichtungsbeschränkungen berücksichtigt.

### DICT-Daten

CFF2-Dateien enthalten die Schriftartwörterbuchdaten als Schlüssel-Wert-Paare in einem kompakten Token-Format. Wörterbuchschlüssel werden als 1- oder 2-Byte-Operatoren codiert, und Wörterbuchwerte werden als numerische Operanden mit variabler Größe codiert. Es gibt drei Strukturen, die das DICT-Datenformat verwenden: „Top DICT“, „Font DICT“ und „Private DICT“. Eine Reihe von ganzzahligen Operandentypen unterschiedlicher Größe sind definiert und wie in der folgenden Tabelle gezeigt codiert (das erste Byte des Operanden ist b0, das zweite ist b1 und so weiter).

|Größe |b0 Bereich |Wertebereich |Werteberechnung|
---|---|---|---|
|1 |32 bis 246| -107 bis +107 |b0 - 139|
|2 |247 bis 250| +108 bis +1131 |(b0 - 247) * 256 + b1 + 108|
|2 |251 bis 254| -1131 bis -108| -(b0 - 251) * 256 - b1 - 108|
|3 |28| -32768 bis +32767| b1 << 8 | b2|
|5 |29| -(2^31) bis +(2^31 - 1)| b1 << 24 \| b2 << 16 \| b3 << 8 \| b4|

### Header

Die Binärdaten beginnen mit einem Header mit dem in der nachstehenden Tabelle gezeigten Format.

|Typ |Name |Beschreibung|
---|---|---|
|uint8| Hauptversion| Hauptversion formatieren. Auf 2 setzen.|
|uint8| Nebenversion| Nebenversion formatieren. Auf Null setzen.|
|uint8| Kopfzeilengröße| Header-Größe (Byte).|
|uint16| topDictLength| Länge der obersten DICT-Struktur in Bytes.|

## Verweise

* [CFF2-Dateiformat](https://docs.microsoft.com/en-us/typography/opentype/spec/cff2)

