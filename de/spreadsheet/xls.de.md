{
  "date" : "2019-12-16",
  "keywords" :[ "XLS", "Datei", "Erweiterung", "Dateiformat", "Excel", "Tabellenkalkulation" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Ihr Dateiformat-Leitfaden, um zu wissen, was eine XLS-Datei und APIs sind, die sie erstellen und öffnen können.",
  "title" :"Was ist das XLS-Dateiformat? Lernen Sie von Dateiformatexperten!",
  "linktitle" :"XLS",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-16"
}

## Was ist eine XLS-Datei?

Dateien mit der Erweiterung XLS stellen das Excel-Binärdateiformat dar. Solche Dateien können von Microsoft Excel sowie anderen ähnlichen Tabellenkalkulationsprogrammen wie OpenOffice Calc oder Apple Numbers erstellt werden. Von Excel gespeicherte Dateien werden als Arbeitsmappe bezeichnet, wobei jede Arbeitsmappe ein oder mehrere Arbeitsblätter enthalten kann. Daten werden gespeichert und Benutzern im Tabellenformat im Arbeitsblatt angezeigt und können numerische Werte, Textdaten, Formeln, externe Datenverbindungen, Bilder und Diagramme umfassen. Mit Anwendungen wie Microsoft Excel können Sie Arbeitsmappendaten in verschiedene Formate exportieren, darunter [PDF](/de/pdf/), [CSV](/de/spreadsheet/csv/), [XLSX](/de/spreadsheet/xlsx/), [TXT](/de/ text-processing/txt/), [HTML](/de/web/html/), [XPS](/de/page-description-language/xps/) und mehrere andere. Das XLS-Dateiformat wurde mit der Veröffentlichung von Microsoft Excel 2007 durch ein offeneres und strukturierteres Format, XLSX, ersetzt. Die neuesten Versionen bieten weiterhin Unterstützung für das Erstellen und Lesen von XLS-Dateien, obwohl XLSX jetzt die erste Wahl ist.

## Kurze Geschichte

XLS wurde von Microsoft für die Verwendung mit Microsoft Excel entwickelt und ist auch als Binary Interchange File Format (BIFF) bekannt. Dieser Dateityp wurde zum ersten Mal eingeführt, indem er 1987 Teil von Excel für Windows wurde. XLS-Dateiformatspezifikationen wurden erstmals im Juni 2008 als Revision 1 veröffentlicht. Danach wurden die Spezifikationen kontinuierlich aktualisiert und die neueste Revision verfügbar ist Stand August 2018, die als Revision 8.0 gekennzeichnet ist. Eine kurze Geschichte der verschiedenen Versionen des XLS-Dateiformats ist wie folgt:

* Version 7.0 (veröffentlicht mit Office 95): Diese Excel-Version war die robusteste und schnellste unter allen Versionen, und interne Stream-Umschreibungen wurden auf 32 Bit aktualisiert.
* Version 8 (freigegeben mit Office 97): VBA wurde als Standardsprache eingeführt und entfernte Labels für natürliche Sprache wurden in dieser Version erstmals integriert. Außerdem wurde erstmals ein Büroklammer-Büroassistent eingeführt.
* Version 9 (freigegeben mit Office 2000): In Version 9 gab es nur geringfügige Änderungen, bei denen der Büroklammer-Büroassistent mehrere Objekte gleichzeitig halten konnte, was zuvor nicht möglich war.
* Version 10 (freigegeben mit Office XP): Diese Version enthielt keine merklichen Verbesserungen.
* Version 11 (freigegeben mit Office 2003): Großes Update in Version 11, Excel 2003 war die Einführung neuer Tabellen.

## Spezifikationen des XLS-Dateiformats ##

Daten werden in einer XLS-Datei als binäre Streams in Form einer zusammengesetzten Datei angeordnet, wie in [MS-CFB] beschrieben. Daten werden in der zusammengesetzten Datei gespeichert, indem Speicher, Streams und Substreams verwendet werden, die Informationen über den Inhalt und die Struktur einer Arbeitsmappe enthalten, einschließlich Arbeitsmappendaten wie Arbeitsblattdefinitionen. Jeder Stream oder Substream enthält eine Reihe von binären Datensätzen. Jeder binäre Datensatz enthält null oder mehr strukturierte Felder, die die Arbeitsmappendaten enthalten. Dieser Abschnitt gibt einen kurzen Überblick über die XLS-Dateistruktur, aber für detaillierte Dateiformatspezifikationen muss man die [XLS File Formation Specifications](https://msdn.microsoft.com/en-us/library/cc313154(v#office .12).aspx) Dokument von Microsoft.

#### Stream und Substream ####

Eine Arbeitsmappe wird durch den Arbeitsmappen-Stream dargestellt. Jedes Arbeitsblatt in einer Arbeitsmappe wird durch Substreams dargestellt. Darüber hinaus verfügt es über einen Diagrammblatt-Substream, Makroblatt-Substream oder Dialogblatt-Substream, der dem globalen Substream folgt. Jeder binäre Stream oder Substream, der Arbeitsmappendaten enthält, MUSS als eine Reihe von binären Datensätzen geschrieben werden.

#### Aufzeichnung ####

Informationen zu Features in einer Arbeitsmappe werden als Datensatz gespeichert, der eine Folge von Bytes variabler Länge ist. Ein binärer Datensatz besteht aus den folgenden drei Komponenten:

**Datensatztyp:** Der Datensatztyp ist eine vorzeichenlose Zwei-Byte-Ganzzahl, die angibt, welche Art von Informationen durch den Datensatz angegeben wird und wie die Struktur der für diesen Datensatz spezifischen Datensatzdaten geordnet und strukturiert ist. Datensatztypwerte MÜSSEN ein Wert aus der Datensatzaufzählung (Abschnitt 2.3) sein oder der Datensatz MUSS die zukünftige Datensatzarchitektur verwenden (Abschnitt 2.1.6).

**Datensatzgröße**: Die Datensatzgröße ist eine vorzeichenlose Zwei-Byte-Ganzzahl, die die Anzahl der Bytes angibt, die die Gesamtgröße der Datensatzdaten angibt. Die Datensatzgröße MUSS größer oder gleich 0 und MUSS kleiner oder gleich 8224 sein.

**Datensatzdaten:** Die Datensatzdatenkomponente enthält Felder, die einem bestimmten Datensatztyp entsprechen und den Rest des Datensatzes umfassen. Die Reihenfolge und Struktur der Felder für einen bestimmten Datensatztyp sind im entsprechenden Abschnitt für diesen Datensatztyp angegeben. Die Größe der Datensatzdatenkomponente MUSS gleich der Datensatzgröße sein. Felder in der Datensatzdatenkomponente können einfache Werte, Arrays von Werten, Strukturen aus mehreren Feldern, Arrays von Feldern und Arrays von Strukturen enthalten.

#### Zellentabelle ####

Zellen sind die grundlegenden Blöcke einer Arbeitsmappe, die den Inhalt der Arbeitsmappe wie Text, Formeln und numerische Daten speichern. Zellen verwalten die Aufzeichnung der gespeicherten Daten über eine Datenstruktur, die Zellentabelle genannt wird. Die Zellentabelle selbst wird in der Folge von Datensätzen gespeichert, die den im Spezifikationsdokument definierten CELLTABLE-Regeln entsprechen. Es besteht aus einer Reihe von Reihenblöcken, wobei die Reihen in Reihenblöcken angeordnet sind. Jeder Zeilenblock enthält Zeilen von der ersten Zeile mit Daten bis zur letzten Zeile mit Daten.

Die Daten- oder Zeilenformatierung wird in einem Zeilendatensatz für jeden Zeilenblock gespeichert. Jede Zelle, die Daten oder individuelle Zellformatierungen enthält, wird durch einen Datensatz dargestellt. Die einer Zelle zugeordnete Formatierung kann von der individuellen Zellenformatierung, Zeilenformatierung, Spaltenformatierung oder dem Standardzellenformat abgeleitet werden. Die Prioritätsreihenfolge für die Formatierung ist die individuelle Zellenformatierung mit der höchsten Priorität, gefolgt von der Zeilenformatierung und dann der Spaltenformatierung und dann dem Standardzellenformat. Zellen, die keine Daten enthalten und keine individuelle Formatierung enthalten, werden nicht gespeichert.

#### Formeln ####

Eine Formel ist eine Folge von Werten, Zellbezügen, Namen, Funktionen oder Operatoren in einer Zelle, die zusammen einen neuen Wert ergeben. Formeln werden in einer tokenisierten Darstellung gespeichert, die als „geparste Ausdrücke“ bekannt ist. Ein geparster Ausdruck wird zur Laufzeit zur Anzeige und Bearbeitung durch den Benutzer in eine Textformel umgewandelt. Zellformeln werden durch den Formeldatensatz angegeben. Array-Formeln werden durch den Array-Datensatz angegeben. Freigegebene Formeln werden durch den ShrFmla-Datensatz angegeben.

#### Diagramme ####

Das Diagrammblatt gibt ein Diagramm, eine Grafik, die Daten oder die Beziehungen zwischen Datensätzen in visueller Form anzeigt, und einen Diagrammdaten-Cache an, eine lokale Kopie der Daten, die in den Diagrammdaten verwendet wird, fehlt oder wenn Links zu externen vorhanden sind Datenquellen sind kaputt. Das Diagramm spezifiziert ein- oder zweiachsige Gruppen, einen Satz von Achsen, gegen die die Diagrammdaten gezeichnet werden, und den Satz von Serien, Trendlinien und Fehlerbalken, die im Diagramm angegeben sind. Jede Achsengruppe gibt eine bis vier Diagrammgruppen an, die den Visualisierungstyp angeben, der zum Anzeigen der Daten verwendet wird. Jede Serie, Trendlinie und Fehlerleiste gibt eine Diagrammgruppe an, der sie zugeordnet ist.

#### Metadaten ####

Metadaten sind zusätzliche Daten, die einer bestimmten Zelle oder ihrem Inhalt zugeordnet sind. Metadaten werden in BIFF8 nur für zukünftige Erweiterbarkeitszwecke aufgezeichnet.

#### Pivot-Tabellen ####

Eine PivotTable ist ein Mechanismus zum Zusammenfassen von Quelldaten, um einen Überblick über die Verteilung dieser Daten zu erhalten. In einer PivotTable werden anwendbare Spalten der Quelldaten zu Feldern, die zum Zusammenfassen von Daten verwendet werden können. Wenn die Quelldaten der PivotTable OLAP-Quelldaten sind, werden OLAP-Hierarchien und einige andere OLAP-Entitäten zu Feldern in der PivotTable.
Eine PivotTable besteht aus zwei Hauptteilen, einem PivotCache und einer PivotTable-Ansicht. Basierend auf einem einzelnen Nicht-OLAP-PivotCache können mehrere PivotTable-Ansichten vorhanden sein.

#### Stile ####

Diese Übersicht beschreibt, wie Formatierungs- und Schutzinformationen für Zellen in einem Blatt (1) angegeben werden. Die Zellenformatierung besteht aus mehreren Sätzen von Eigenschaften:

* Schrifteigenschaften (fett, kursiv, Schriftfarbe, Schriftgröße usw.)
* Fülleigenschaften (Vordergrundfarbe, Hintergrundfarbe, Muster, Verlauf usw.)
* Ausrichtungseigenschaften (linke, zentrierte, rechte Ausrichtung usw.)
* Rahmeneigenschaften (links, rechts, oben, unten, dick oder dünn, Farbe usw.)
* Zahlenformatierungseigenschaften (Datum, Uhrzeit, Anzahl der Dezimalstellen usw.)
* Schutzeigenschaften (gesperrt, versteckt usw.)

Diese Eigenschaften beschreiben insgesamt, wie eine bestimmte Zelle angezeigt und gedruckt wird.

## Verweise ##

* [[MS-XLS] - Struktur des Excel-Binärdateiformats](https://msdn.microsoft.com/en-us/library/cc313154(v#office.12).aspx)
* [[MS-CFB] - Verbunddatei-Binärdateiformat](https://msdn.microsoft.com/en-us/library/dd942138.aspx)

