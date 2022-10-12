{
  "date" : "2020-08-20",
  "keywords" :[ "otf-Datei", "otf-Dateiformat", "was ist eine otf-Datei", "Datei", "otf-Beispiel", "otf-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OTF - Dateiformat für TrueType-Schriftarten",
  "description":"Erfahren Sie mehr über das OTF-Dateiformat und APIs, die OTF-Dateien erstellen und öffnen können.",
  "linktitle" :"OTF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-09-21"
}

## Was ist eine OTF-Datei?

Eine Datei mit der Erweiterung .otf bezieht sich auf das OpenType-Schriftformat. Das OTF-Schriftartformat ist besser skalierbar und erweitert die vorhandenen Funktionen von [TTF](/de/font/ttf/)-Formaten für digitale Typografie. OTF wurde von Microsoft und Adobe entwickelt und kombiniert die Funktionen von PostScript- und TrueType-Schriftformaten. Dadurch eignet sich das OTF-Format für die Mehrheit der Schreibsysteme und wird daher einheitlich auf den wichtigsten Computerplattformen verwendet. Das OpenType-Schriftformat wird von Mac OS X und Windows 2000 und höher unterstützt.

## Kurze Geschichte

Die Anforderung von OpenType-Schriftarten entstand als Anforderung für ein ausdrucksstärkeres Schriftartformat, das mit feiner Typografie umgehen konnte. Darüber hinaus sollte es den Anforderungen des komplexen Verhaltens vieler Schriftsysteme der Welt gerecht werden. Microsoft versuchte Anfang der 1990er Jahre, Apples fortschrittliche Typografietechnologie, die als GX Typografie bekannt ist, zu lizenzieren. Das ging nicht gut und als Ergebnis begann Microsoft 1994 damit, seine eigene TrueType-Font-Technologie zu verbessern. Zu den Änderungen gehörte auch die Einführung eines besser geeigneten Font-Formats, das auch die Eigenschaften von Adobes Type 1 (PostScript)-Font-Formaten erfüllt.

Adobe schloss sich 1996 Microsoft in seinen Bemühungen an, sowohl Apples TrueType- als auch seine eigenen Typ-1-Schriftartformate zu ersetzen. Dies führte zu einer Kombination beider zugrunde liegender Schriftformate, um die Einschränkungen zu überwinden und neue Erweiterungen hinzuzufügen. Diese neue Technologie wurde im selben Jahr unter dem Namen **OpenType** eingeführt.

## OTF-Dateiformatspezifikationen

OTF-Spezifikationen sind von Microsoft öffentlich verfügbar und können aus Entwicklersicht herangezogen werden. Wie TTF verwendet es dieselbe 'sfnt'-Containerstruktur und ist mit den TrueType-Spezifikationen kompatibel. Daten in einer OpenType-Schriftartdatei werden für verschiedene Zwecke verwendet, z. B. zum Berechnen des Textlayouts, zum Definieren von Glyphen als TrueType- oder Compact Font Format (CFF)-Konturen, zum Bereitstellen von monochromen oder farbigen Bitmaps oder SVG-Dokumenten als alternative Glyphenbeschreibungen und Metadateninformationen.

### OTF-Datentypen
OTF-Dateien verwenden die folgenden Datentypen, die alle in Big Endian vorliegen.

|Datentyp| Beschreibung|
---|---|
|uint8| 8-Bit-Ganzzahl ohne Vorzeichen.|
|int8| 8-Bit-Ganzzahl mit Vorzeichen.|
|uint16| 16-Bit-Ganzzahl ohne Vorzeichen.|
|int16| 16-Bit-Ganzzahl mit Vorzeichen.|
|uint24| 24-Bit-Ganzzahl ohne Vorzeichen.|
|uint32| 32-Bit-Ganzzahl ohne Vorzeichen.|
|int32| 32-Bit-Ganzzahl mit Vorzeichen.|
|Behoben| 32-Bit-Festkommazahl mit Vorzeichen (16.16)|
|VWORT| int16, das eine Größe in Font-Design-Einheiten beschreibt.|
|UFWORT| uint16, das eine Menge in Font-Design-Einheiten beschreibt.|
|F2DOT14| Vorzeichenbehaftete 16-Bit-Festzahl mit den niedrigen 14 Bits des Bruchs (2,14).|
|LONGDATETIME| Datum und Uhrzeit in Sekunden seit 12:00 Uhr, 1. Januar 1904, UTC. Der Wert wird als 64-Bit-Ganzzahl mit Vorzeichen dargestellt.|
|Tag| Array aus vier uint8s (Länge = 32 Bits), das verwendet wird, um eine Tabelle, eine Designvariationsachse, ein Skript, ein Sprachsystem, eine Funktion oder eine Baseline zu identifizieren|
|Offset16| Kurzer Offset zu einer Tabelle, dasselbe wie uint16, NULL-Offset = 0x0000|
|Offset32| Langes Offset zu einer Tabelle, dasselbe wie uint32, NULL-Offset = 0x00000000|
|Version16Punkt16| Gepackter 32-Bit-Wert mit Haupt- und Nebenversionsnummern. (Siehe Tabelle Versionsnummern.)|

### OTF-Tabellenverzeichnis

Eine OTF-Datei beginnt mit einem Tabellenverzeichnis. Dieses Verzeichnis ist die oberste Sammlung der Tabellen in der Schriftartdatei. Abhängig von der Anzahl der Schriftarten in einer Datei kann sich das Tabellenverzeichnis an einer anderen Stelle in der Datei befinden. Wenn beispielsweise die Schriftartdatei nur eine Schriftart enthält, beginnt das Tabellenverzeichnis bei Byte 0 der Datei. Im Falle einer Sammlung mehrerer OpenType-Schriftarten
der Anfang des Tabellenverzeichnisses wird im TTCHeader angegeben.

|Typ |Name |Beschreibung|
---|---|---|
|uint32 |sfntVersion| 0x00010000 oder 0x4F54544F ('OTTO')|
|uint16| numTables |Anzahl der Tabellen.|
|uint16| searchRange |Maximale Potenz von 2 kleiner oder gleich numTables, multipliziert mit 16 ((2\**floor(log2(numTables))) * 16, wobei „**“ ein Potenzierungsoperator ist).|
|uint16 |entrySelector Log2 der maximalen Potenz von 2 kleiner oder gleich numTables (log2(searchRange/16), was gleich floor(log2(numTables))) ist.|
|uint16 |rangeShift |numTables mal 16, minus searchRange ((numTables * 16) - searchRange).|
|tableRecord| tableRecords[numTables] |Array von Tabellendatensätzen – eines für jede Tabelle der obersten Ebene in der Schriftart|


### Tabellenaufzeichnung

Für jede Tabelle der obersten Ebene in der Schriftart gibt es einen Tabellendatensatz, der aus den folgenden Feldern besteht.

|Typ| Name| Beschreibung|
---|---|---|
|Tag| TischTag| Tabellenkennung.|
|uint32| Prüfsumme| Prüfsumme für diese Tabelle.|
|Offset32| Versatz| Versatz vom Anfang der Schriftdatei.|
|uint32| length Länge dieser Tabelle.|

Jede Tabelle in der OpenType-Schriftartdatei wird durch Namen dargestellt, die als Tabellen-Tags bezeichnet werden. Es ist ein Muss, dass alle Datensätze im Array in aufsteigender Reihenfolge nach Tag sortiert werden.

## Verweise
* [OpenType-Schriftspezifikationen von Microsoft](https://docs.microsoft.com/en-us/typography/opentype/spec/overview)
* [TrueType-Übersicht](https://docs.microsoft.com/en-us/typography/truetype/)

