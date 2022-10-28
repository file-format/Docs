{
  "date" : "2019-12-10",
  "keywords" :[ "XLSB", "Datei", "Erweiterung", "Dateiformat", "Excel-Binärtabellendatei" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Ihr Dateiformat-Leitfaden, um zu wissen, was eine XLSB-Datei und APIs sind, die sie erstellen und öffnen können.",
  "title" :"Was ist eine XLSB-Datei?",
  "linktitle" : "XLSB",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## Was ist eine XLSB-Datei?

Das XLSB-Dateiformat gibt das Excel-Binärdateiformat an, bei dem es sich um eine Sammlung von Datensätzen und Strukturen handelt, die den Inhalt von Excel-Arbeitsmappen angeben. Der Inhalt kann unstrukturierte oder halbstrukturierte Zahlentabellen, Text oder sowohl Zahlen als auch Text, Formeln, externe Datenverbindungen, Diagramme und Bilder umfassen. Im Gegensatz zu [XLSX](/de/spreadsheet/xlsx/) (das auf dem Open XML-Dateiformat basiert) repräsentiert XLSB eine binäre Excel-Arbeitsmappendatei. XLSB-Dateien können schneller gelesen und geschrieben werden, was sie für die Arbeit mit großen Dateien nützlich macht. XLSB wird selten zum Speichern von Arbeitsmappen verwendet, da XLSX (und zuvor [XLS](/de/spreadsheet/xls/)) die am häufigsten vom Benutzer ausgewählten Dateiformate zum Speichern von Arbeitsmappen sind. Es kann von Microsoft Office 2007 und höher geöffnet werden.

## XLSB-Dateiformatspezifikationen ##

Die Dateiformatspezifikationen für das XLSB-Dateiformat wurden bereits 2008 als Version 1.0 veröffentlicht. Seitdem wurden die Spezifikationen mehrmals überarbeitet und die neueste Version der Spezifikationen (v 10.0) wurde im April 2018 veröffentlicht. Die Spezifikationen sind öffentlich von Microsoft als [[MS-XLSB] - Excel Binary File Format-Spezifikationen](https:/ /msdn.microsoft.com/en-us/library/cc313133(v#office.12).aspx) und sollte von jedem zum Lesen oder Schreiben von Dateien im XLSB-Dateiformat konsultiert werden.

## XLSB-Dateistruktur ##

Eine XLSB-Datei ist ein Paket, das aus einer Sammlung von Teilen besteht. Diese Teile enthalten Informationen über den Inhalt einer Arbeitsmappe, einschließlich Arbeitsmappendaten und der Struktur des Pakets. Einige Teile enthalten Informationen, die unter Verwendung von binären Datensätzen gespeichert sind, einige als XML, während andere Informationen enthalten, die als binärer Strom von Bytes gespeichert sind. Jeder binäre Datensatz enthält null oder mehr strukturierte Felder, die die Arbeitsmappendaten enthalten.

#### Paket ####

Ein XLSB-Paket ist ein [ZIP](/de/compression/zip/)-Archiv, das genau einen Arbeitsmappenteil enthalten muss. Dieser Teil muss das Ziel einer Beziehung in diesem Paketbeziehungsteil sein. Der Arbeitsmappenteil ist der Anfangsteil im XLSB-Dokument.

#### Teil ####

Ein Teil ist ein Strom von Bytes, dem ein Inhaltstyp zugeordnet ist, der die Art und den Typ des in dem Teil gespeicherten Inhalts angibt. Einige Teile speichern Informationen im Binärformat, während andere Informationen als XML speichern. Der Abschnitt [parts enumeration](https://msdn.microsoft.com/en-us/library/dd924091(v#office.12).aspx) des Spezifikationsdokuments listet die gültigen Teile, Inhaltstypen und erforderlichen/optionalen Beziehungen zwischen auf alle teile in einem paket.

#### Beziehung ####

Eine Quelle und eine Zielressource sind durch eine Beziehung verbunden. Eine Beziehung kann sein:

**Paketbeziehung:** wobei das Ziel ein Teil und die Quelle das Paket als Ganzes ist

**Teil-zu-Teil-Beziehung:** wobei das Ziel ein Teil und die Quelle ein Teil des Pakets ist

**Explizite Beziehung:** Wo eine Ressource vom Inhalt eines Quellteils referenziert wird, indem auf den ID-Attributwert eines Beziehungselements verwiesen wird

**implizite Beziehung** ist eine Beziehung, die nicht explizit ist

**Interne Beziehung:** wobei das Ziel ein Teil des Pakets ist

**Externe Beziehung:** wobei das Ziel eine externe Ressource ist, die nicht im Paket enthalten ist

#### Aufzeichnung ####

Ein Datensatz ist der grundlegende Baustein zum Speichern von Informationen zu Features in einer Arbeitsmappe. Jeder binäre Datensatz ist eine Folge von Bytes variabler Länge. Ein binärer Datensatz besteht aus drei Komponenten:

* ein Datensatztyp
* eine Datensatzgröße und
* die Datensatzdaten, die für diesen Datensatztyp spezifisch sind.

**Datensatztyp:** Der Datensatztyp zeigt den durch den Datensatz angegebenen Datensatztyp an. Es spezifiziert auch die Struktur von Datensatzdaten, die für diesen Datensatz spezifisch sind. Die gültigen Datensatztypen sind im Abschnitt [Record Enumeration](https://msdn.microsoft.com/en-us/library/dd953057(v#office.12).aspx) des Spezifikationsdokuments aufgeführt. Der Datensatztyp muss ein oder zwei Bytes betragen und muss größer oder gleich 128 und kleiner als 16384 sein.

**Datensatzgröße:** Die Datensatzgröße gibt die Anzahl der Bytes an, die die Gesamtgröße der Datensatzdaten angibt. Dieser Wert MUSS ein bis vier Bytes betragen. Dieser Wert MUSS ein Byte sein, wenn das High-Bit im Low-Byte gleich 0 ist; andernfalls MUSS dieser Wert größer als ein Byte sein. Wenn die Anzahl der Bytes größer als ein Byte ist, gibt das hohe Bit in jedem nachfolgenden Byte an, ob ein zusätzliches Byte verwendet wird. Wenn das High-Bit des zweiten Bytes gleich 1 ist, dann MUSS dieser Wert ein zusätzliches drittes Byte verwenden. Wenn das High-Bit des dritten Bytes gleich 1 ist, dann MUSS dieser Wert ein zusätzliches viertes Byte verwenden. Das High-Bit des vierten Bytes MUSS ignoriert werden. Der Wert besteht aus den sieben niedrigen Bits jedes kombinierten Bytes. Die niederwertigsten Bits sind im ersten Byte enthalten, und jedes nachfolgende Byte enthält höherwertige Bits als das vorherige Byte.

**Datensatzdaten:** Die Datensatzdatenkomponente enthält Felder, die einem bestimmten Datensatztyp entsprechen und den Rest des Datensatzes umfassen. Die Reihenfolge und Struktur der Felder für einen bestimmten Datensatztyp, die in der Datensatzaufzählung aufgeführt sind, werden im entsprechenden Abschnitt für diesen Datensatztyp in Datensätze angegeben. Die Gesamtgröße der Datensatzdatenkomponente MUSS gleich der Datensatzgröße sein. Felder in der Datensatzdatenkomponente können einfache Werte, Arrays von Werten, Strukturen aus mehreren Feldern, Arrays von Feldern und Arrays von Strukturen enthalten.

#### Beispiel für XLSB-Datensatz ####

Der folgende Datensatztyp und die folgende Datensatzgröße geben einen **BrtCommentText**-Datensatz mit einer Größe von 200 Byte an:

11111101 00000100 11001000 00000001 [Datensatzfelder]

Das erste Byte ist 11111101, was einen niedrigen Wert von 125 angibt und dass der Datensatztyp ein zweites Byte erfordert. Das zweite Byte ist 00000100 und gibt einen hohen Wert von 4 * 128 an, was 512 entspricht. Der Datensatztypwert ist 125 + 512 oder 637, was einem **BrtCommentText**-Datensatztyp entspricht. Das nächste Byte ist 11001000, was einen niedrigen Wert von 72 angibt und dass die Datensatzgröße ein zweites Byte erfordert. Das zweite Byte ist 00000001, was einen höheren Wert von 1 * 128 angibt und dass die Datensatzgröße kein zusätzliches Byte erfordert. Die Datensatzgröße beträgt 72 + 128 oder 200, was die Gesamtgröße der Datensatzdatenkomponente in Byte angibt. Die Felder in der Datensatzdatenkomponente werden durch **BrtCommentText** angegeben.

## Verweise ##

* [[MS-XLSB] - Excel (.xlsb) Binärdateiformat](https://msdn.microsoft.com/en-us/library/cc313133(v#office.12).aspx)

