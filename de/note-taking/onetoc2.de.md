{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ONETOC2 - Microsoft OneNote-Dateiformat",
  "description":"Erfahren Sie mehr über das ONETOC2-Dateiformat und APIs, die ONETOC2-Dateien erstellen und öffnen können.",
  "linktitle" : "ONETOC2",
  "menu" : {
    "docs" : {
      "parent" : "note-taking"
}
},
  "lastmod" : "2019-09-10"
}

## Was ist ONETOC2? ##

Diejenigen, die mit der Anwendung [Microsoft OneNote](https://products.office.com/en-us/onenote/digital-note-taking-app) gearbeitet haben, haben möglicherweise das Vorhandensein von .onetoc2-Dateien im Notizbuchordner bemerkt. Microsoft OneNote erstellt eine binäre .onetoc2-Datei als Inhaltsverzeichnis, um einen Index über die Reihenfolge der verschiedenen Notizabschnitte in einem Notizbuch zu führen. Ein Notizbuch ist eine Sammlung von Abschnittsdateien, die im selben Verzeichnis gespeichert sind. Die .onetoc2-Datei verwendet eine Sammlung von Eigenschaften, um Einstellungen wie die Reihenfolge der Abschnitte innerhalb des Notizbuchs und die Farbe des Notizbuchs anzugeben.

Wenn Sie ein Notizbuch in OneNote 2016 erstellen, wird es automatisch im neuen Dateiformat 2010–2016 gespeichert. Sie benötigen dieses Format, wenn Sie möchten, dass alle Features in OneNote 2016 wie mathematische Gleichungen und verknüpfte Notizen ordnungsgemäß funktionieren.

## ONETOC2-Dateiformat ##

Das .onetoc2-Dateiformat wird als OneNote-Revisionsspeicherdateiformat dargestellt und ist eine Sammlung von Strukturen, die einen Revisionsspeicher angeben, der in Objektbereichen mit Querverweisen organisiert ist, Objekte mit Eigenschaftssätzen enthält und ein Transaktionsprotokoll enthält, um die Dateiintegrität über asynchrone Vorgänge hinweg sicherzustellen schreibt. Vollständige Spezifikationen für das .onetoc2-Dateiformat sind [online] verfügbar (https://msdn.microsoft.com/en-us/library/dd951288(v#office.12).aspx) und können für die Entwicklung von Anwendungen herangezogen werden .

### Dateistruktur ###

Eine Revisionsspeicherdatei MUSS mit einer **Header**-Struktur beginnen. Der Rest der Datei wird in Byteblöcke partitioniert, wobei die Größe und Struktur jedes Blocks durch das Feld angegeben wird, das darauf verweist. Ein Block ist erreichbar, wenn er von der **Header**-Struktur referenziert wird oder wenn er von einem Feld in einem anderen erreichbaren Block referenziert wird. Daten außerhalb der **Header**-Struktur und alle erreichbaren Blöcke MÜSSEN ignoriert werden.

Alle Strukturen sind auf 1-Byte-Grenzen ausgerichtet. Alle Ganzzahlen sind vorzeichenbehaftet, sofern nicht anders angegeben. Alle Felder sind [little-endian](https://msdn.microsoft.com/en-us/library/dd773246(v#office.12).aspx#gt_079478cb-f4c5-4ce5-b72b-2144da5d2ce7), sofern nicht anders angegeben.

#### Header ####

Der Header der .ONE-Datei besteht aus Chunks, die verschiedene eindeutige IDs und Felder zur Darstellung von Dateiinformationen wie folgt enthalten:

`guidFileType (16 Bytes):` Eine GUID, die den Typ der Revisionsspeicherdatei angibt. MUSS einer der Werte aus der folgenden Tabelle sein.

|Dateiformat|Wert
--- | --- |
|.one|{7B5C52E4-D88C-4DA7-AEB1-5378D02996D3}
|.onetoc2|{43FF2FA1-EFD9-4C76-9EE2-10EA5722765F}

`guidFile (16 bytes):` Eine GUID, die die Identität dieser Revisionsspeicherdatei angibt. SOLLTE weltweit einzigartig sein.

`guidLegacyFileVersion (16 bytes):` MUSS "{00000000-0000-0000-0000-000000000000}" sein und MUSS ignoriert werden.

`guidFileFormat (16 Bytes):` Eine GUID, die angibt, dass die Datei eine Revisionsspeicherdatei ist. MUSS "{109ADD3F-911B-49F5-A5D0-1791EDC8AED8}" lauten.

`ffvLastCodeThatWroteToThisFile (4 Bytes):` Eine Ganzzahl ohne Vorzeichen. MUSS je nach Dateityp einer der Werte in der folgenden Tabelle sein.

|Dateiformat|Wert
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

`ffvOldestCodeThatHasWrittenToThisFile (4 Bytes):` Eine Ganzzahl ohne Vorzeichen. MUSS einer der Werte in der folgenden Tabelle sein, abhängig vom Dateiformat dieser Datei.


|Dateiformat|Wert
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

`ffvNewestCodeThatHasWrittenToThisFile (4 Bytes):` Eine Ganzzahl ohne Vorzeichen. MUSS einer der Werte in der folgenden Tabelle sein, abhängig vom Dateiformat dieser Datei.
:


|Dateiformat|Wert
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

`ffvOldestCodeThatMayReadThisFile (4 Bytes):` Eine Ganzzahl ohne Vorzeichen. MUSS einer der Werte in der folgenden Tabelle sein, abhängig vom Dateiformat dieser Datei.


|Dateiformat|Wert
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

## Verweise ##

* [[MS-ONESTORE] - OneNote-Dateiformat](https://msdn.microsoft.com/en-us/library/dd951288(v#office.12).aspx)
* [Microsoft OneNote – Wikipedia](https://en.wikipedia.org/wiki/Microsoft_OneNote#References)

