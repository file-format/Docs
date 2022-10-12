{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ONE - Microsoft OneNote-Dateiformat",
  "description":"Erfahren Sie mehr über EIN Dateiformat und APIs, mit denen EINE Datei erstellt und geöffnet werden kann.",
  "linktitle" :"EINES",
  "menu" : {
    "docs" : {
      "parent" : "note-taking"
}
},
  "lastmod" : "2019-09-10"
}

## Was ist eine .ONE-Datei? ##

Dateien mit der Erweiterung .ONE werden von der Microsoft OneNote-Anwendung erstellt. Mit OneNote können Sie mithilfe der Anwendung Informationen sammeln, als ob Sie Ihren Zeichenblock zum Aufzeichnen von Notizen verwenden würden. OneNote-Dateien können verschiedene Elemente enthalten, die an nicht festen Positionen auf Dokumentseiten platziert werden können. Diese Elemente können Text, digitalisierte Handschriften und Objekte enthalten, die aus anderen Anwendungen kopiert wurden, darunter Bilder, Zeichnungen und Multimedia-Clips (Audio/Video). Microsoft bietet jetzt eine Online-Version von OneNote als Teil von Office365 an, in der Notizen mit anderen OneNote-Benutzern über das Internet geteilt werden können.

## Spezifikationen des .ONE-Dateiformats ##

Das OneNote-Dateiformat bietet eine effektive Möglichkeit, digitale Notizen als hierarchische Sätze von Abschnitten und Seiten darzustellen. Jede Seite enthält benutzerdefinierte Inhalte in einer bestimmten Struktur zur Darstellung durch das Dateiformat Document Object Model (DOM). Das Datenmodell für dieses Format ist wie unten dargestellt.

### Strukturübersicht ###

Wie im Datenmodell für das OneNote-Dateiformat dargestellt, besteht ein OneNote-Dokument aus verschiedenen Elementen.

#### Abschnitt ####

Ein Abschnitt ist der oberste Container in einer OneNote-Datei, der weitere verschiedene Elemente enthält, wie:

* Seiten
* Metadaten
* Eigenschaften

Zu den Metadaten und Eigenschaften gehören der Abschnittsname, die Identifizierung der Seiten, die in dem Abschnitt enthalten sind, und die Reihenfolge, in der diese Seiten angezeigt werden. Der Begriff „Abschnitt“ bezieht sich auf alle Seiten, die sich in einem Abschnitt befinden, und auf die Darstellung dieser Daten in einer OneNote®-Revisionsspeicherdatei mit der Dateinamenerweiterung „.one“.

#### Buchseite ####

Benutzerdefinierte Inhalte in einem OneNote-Dokument sind auf einer Seite enthalten. Zu den Seiteninformationen gehören Text, Listen, Tabellen, Seitentitel, Bilder und Notiz-Tags. Eine Seite besteht aus Gliederungsobjekten, zu denen die meisten enthaltenen Objekte hinzugefügt werden. Jeder Seite kann zur aussagekräftigen Darstellung ein Name zugewiesen werden und auch Objekte können Seiten direkt hinzugefügt werden. Eine Seite kann ferner Unterseiten in einem hierarchischen System enthalten.

#### Eigenschaften und Eigenschaftssätze ####

OneNote-Inhalte bestehen aus Eigenschaften, Eigenschaftssätzen und Dateidatenobjekten. Ein Eigenschaftssatz ist eine Sammlung von Eigenschaften, die einen Inhaltstyp darstellen. Ein Dateidatenobjekt ist ein Block binärer Daten, der Bilder, eingebettete Dateien oder Audio-/Videoinhalte enthält.

#### OneNote-Notizbuch ####

Ein Notizbuch ist eine Sammlung von Abschnittsdateien, die im selben Verzeichnis gespeichert sind. Eine Sammlung von Eigenschaften wird verwendet, um Einstellungen wie die Reihenfolge der Abschnitte innerhalb des Notizbuchs und die Farbe des Notizbuchs anzugeben.

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

|Dateiformat|Wert
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

`ffvOldestCodeThatMayReadThisFile (4 Bytes):` Eine Ganzzahl ohne Vorzeichen. MUSS einer der Werte in der folgenden Tabelle sein, abhängig vom Dateiformat dieser Datei.

|Dateiformat|Wert
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

`fcrLegacyFreeChunkList (8 Bytes):` Eine **FileChunkReference32**-Struktur, die den Wert "fcrZero" haben MUSS.

`fcrLegacyTransactionLog (8 Bytes):` Eine **FileChunkReference32**-Struktur, die "fcrNil" sein MUSS.

`cTransactionsInLog (4 Bytes):` Eine Ganzzahl ohne Vorzeichen, die die Anzahl der Transaktionen im Transaktionsprotokoll angibt. DARF NICHT Null sein.

`cbLegacyExpectedFileLength (4 Bytes):` Eine Ganzzahl ohne Vorzeichen, die Null sein MUSS und ignoriert werden MUSS.

`rgbPlaceholder (8 Bytes):` Eine Ganzzahl ohne Vorzeichen, die Null sein MUSS und ignoriert werden MUSS.

`fcrLegacyFileNodeListRoot (8 Bytes):` Eine **FileChunkReference32**-Struktur, die "fcrNil" sein MUSS.

`cbLegacyFreeSpaceInFreeChunkList (4 Bytes):` Eine Ganzzahl ohne Vorzeichen, die Null sein MUSS und ignoriert werden MUSS.

`fNeedsDefrag (1 Byte):` MUSS ignoriert werden.

`fRepairedFile (1 Byte):` MUSS ignoriert werden.

`fNeedsGarbageCollect (1 Byte):` MUSS ignoriert werden.

`fHasNoEmbeddedFileObjects (1 Byte):` Eine Ganzzahl ohne Vorzeichen, die Null sein MUSS und ignoriert werden MUSS.

`guidAncestor (16 bytes):` Eine GUID, die das Feld **Header.guidFile** der Inhaltsverzeichnisdatei angibt, die in der folgenden Tabelle angegeben ist:


|Format der Inhaltsverzeichnisdatei|Speicherort der Inhaltsverzeichnisdatei
--- | --- |
|Abschnittsdatei - .One|Inhaltsverzeichnisdatei befindet sich im selben Verzeichnis wie diese Datei.
|Inhaltsverzeichnisdatei - .onetoc2|Inhaltsverzeichnisdatei befindet sich im übergeordneten Verzeichnis dieser Datei.

Wenn die GUID {00000000-0000-0000-0000-000000000000} ist, verweist dieses Feld nicht auf eine Inhaltsverzeichnisdatei.

`crcName (4 Bytes):` Eine Ganzzahl ohne Vorzeichen, die den CRC-Wert des Namens dieser Revisionsspeicherdatei angibt. Der Name ist die Unicode-Darstellung des Dateinamens mit seiner Erweiterung und einem zusätzlichen Nullzeichen am Ende. Dieser CRC wird immer mit dem CRC-Algorithmus für die .one-Datei berechnet, unabhängig von diesem Dateiformat des Revisionsspeichers.

`fcrHashedChunkList (12 Bytes):` Eine **FileChunkReference64x32**-Struktur, die einen Verweis auf das erste **FileNodeListFragment** in einer gehashten Chunk-Liste angibt. Wenn der Wert der **FileChunkReference64x32**-Struktur "fcrZero" oder "fcrNil" ist, ist die gehashte Chunk-Liste nicht vorhanden.

„fcrTransactionLog (12 Bytes):“ Eine **FileChunkReference64x32**-Struktur, die einen Verweis auf die erste **TransactionLogFragment**-Struktur in einem Transaktionsprotokoll angibt. Der Wert des Feldes **fcrTransactionLog** DARF NICHT „fcrZero“ und DARF NICHT „fcrNil“ sein.

`fcrFileNodeListRoot (12 Bytes):` Eine **FileChunkReference64x32**-Struktur, die einen Verweis auf eine Stammdatei-Knotenliste angibt. Der Wert des **fcrFileNodeListRoot**-Feldes DARF NICHT „fcrZero“ und DARF NICHT „fcrNil“ sein.

`fcrFreeChunkList (12 Bytes):` Eine **FileChunkReference64x32**-Struktur, die einen Verweis auf die erste **FreeChunkListFragment**-Struktur angibt. Wenn der Wert der **FileChunkReference64x32**-Struktur "fcrZero" oder "fcrNil" ist, dann existiert die freie Chunk-Liste nicht.

`cbExpectedFileLength (8 Bytes):` Eine Ganzzahl ohne Vorzeichen, die die Größe dieser Revisionsspeicherdatei in Bytes angibt.

`cbFreeSpaceInFreeChunkList (8 Bytes):` Eine vorzeichenlose Ganzzahl, die die Größe des freien Speicherplatzes in Bytes angeben SOLLTE, der von der Liste der freien Chunks angegeben wird.

`guidFileVersion (16 Bytes):` Eine GUID. Wenn entweder der Wert des Felds **cTransactionsInLog** oder des Felds **guidDenyReadFileVersion** geändert wird, MUSS **guidFileVersion** in eine neue GUID geändert werden.

`nFileVersionGeneration (8 Bytes):` Eine Ganzzahl ohne Vorzeichen, die angibt, wie oft sich die Datei geändert hat. MUSS inkrementiert werden, wenn sich das Feld **guidFileVersion** ändert.

`guidDenyReadFileVersion (16 Byte):` Eine GUID. Wenn der vorhandene Inhalt der Datei geändert wird, mit Ausnahme der **Header**-Struktur der Datei und nicht verwendeter Speicherblöcke, MUSS **guidDenyReadFileVersion** in eine neue GUID geändert werden.

`grfDebugLogFlags (4 Bytes):` MUSS Null sein. MUSS ignoriert werden.

`fcrDebugLog (12 Bytes):` Eine **FileChunkReference64x32**-Struktur, die einen Wert "fcrZero" haben MUSS. MUSS ignoriert werden.

`fcrAllocVerificationFreeChunkList (12 Bytes):` Eine **FileChunkReference64x32**-Struktur, die "fcrZero" sein MUSS. MUSS ignoriert werden.

`bnCreated (4 Bytes):` Eine Ganzzahl ohne Vorzeichen, die die Build-Nummer der Anwendung angibt, die diese Revisionsspeicherdatei erstellt hat. SOLLTE ignoriert werden.

`bnLastWroteToThisFile (4 Bytes):` Eine Ganzzahl ohne Vorzeichen, die die Build-Nummer der Anwendung angibt, die zuletzt in diese Revisionsspeicherdatei geschrieben hat. SOLLTE ignoriert werden.

`bnOldestWritten (4 Bytes):` Eine Ganzzahl ohne Vorzeichen, die die Build-Nummer der ältesten Anwendung angibt, die in diese Revisionsspeicherdatei geschrieben hat. SOLLTE ignoriert werden.

`bnNewestWritten (4 Bytes):` Eine Ganzzahl ohne Vorzeichen, die die Build-Nummer der neuesten Anwendung angibt, die in diese Revisionsspeicherdatei geschrieben hat. SOLLTE ignoriert werden.

`rgbReserved (728 bytes):` MUSS Null sein. MUSS ignoriert werden.

## Verweise ##

* [[MS-ONESTORE] - OneNote-Dateiformat](https://msdn.microsoft.com/en-us/library/dd951288(v#office.12).aspx)
* [Microsoft OneNote – Wikipedia](https://en.wikipedia.org/wiki/Microsoft_OneNote#References)

