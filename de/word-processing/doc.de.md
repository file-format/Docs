{
  "date" : "2019-12-03",
  "keywords" :[ "doc", "Datei", "Erweiterung", "Dateiformat", "Word", "Dokument" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DOC - Microsoft Word-Dokumentdatei",
  "description":"Erfahren Sie mehr über das DOC-Dateiformat und APIs, die DOC-Dateien erstellen und öffnen können.",
  "linktitle" :"DOC",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2019-12-03"
}

## Was ist eine DOC-Datei?

Dateien mit der Erweiterung .doc stellen Dokumente dar, die von Microsoft Word oder anderen Textverarbeitungsdokumenten im Binärdateiformat generiert wurden. Die Erweiterung wurde ursprünglich für die Klartextdokumentation auf mehreren verschiedenen Betriebssystemen verwendet. Es kann verschiedene Arten von Daten enthalten, z. B. Bilder, formatierten sowie einfachen Text, Grafiken, Diagramme, eingebettete Objekte, Links, Seiten, Seitenformatierung, Druckeinstellungen und vieles mehr. Das Format war beliebt für alle Arten von Dokumentationen, da es den Benutzern eine Vielzahl von Optionen zum Schreiben von Handbüchern, Angeboten, Spezifikationen, Lebensläufen, Artikeln oder ähnlichen Dokumenten bietet. Die aktualisierte Version von DOC ist [DOCX](/de/Word%20Processing/DOCX/), die auf Office OpenXML basiert, dessen Spezifikationen offen verfügbar sind.

## Kurze Geschichte ##

WordPerfect, ein Produkt von [Corel](https://www.corel.com/en/), verwendete DOC als Erweiterung seines proprietären Formats. In den 1980er Jahren blieb WordPerfect aufgrund seiner einfachen Verfügbarkeit, der Konformität mit den meisten Computern und Betriebssystemen die erste Wahl für die Verwendung auf den meisten Computern. WordPerfect erlebte jedoch seinen Niedergang auf Windows-Betriebssystemen, als Microsoft Microsoft Word als sein Produkt für das Dateiformat von Dokumenten einführte und die DOC-Erweiterung für ihr proprietäres Format wählte. Als Microsoft Word immer beliebter wurde, wurde das DOC-Dateiformat von Microsoft Word 97 bis 2003 mehrfach überarbeitet. Es war 2007, als das Standard-DOC-Dateiformat durch das Office Open XML-Format (bekannt als DOCX) und die neuen Versionen von ersetzt wurde Microsoft Word verwendet jetzt diese neue Erweiterung als Standarddateiformat.

## DOC-Dateiformatspezifikationen – Weitere Informationen

Microsoft hat die DOC-Dateiformatspezifikationen lange Zeit bis 2008 nicht veröffentlicht. Im Februar 2008 wurden Formatspezifikationen für das .doc-Dateiformat im Rahmen des Microsoft Open Specification Promise veröffentlicht. Obwohl die Spezifikation nicht alle vom DOC-Format verwendeten Funktionen beschreibt, gibt sie doch umfassende Informationen über das Wissen, das für die Arbeit mit diesem Dateiformat erforderlich ist. Dennoch ist Reverse Engineering erforderlich, um die verfügbaren Informationen zu nutzen. Die Spezifikationen wurden mehrmals aktualisiert und die neueste [Revision](https://msdn.microsoft.com/en-us/library/cc313153(v#office.12).aspx) ist 8.0, die im August 2018 aktualisiert wurde .

### Einige grundlegende Konzepte ###

Bevor wir auf Einzelheiten zu den Dateiformatspezifikationen für DOC eingehen, müssen einige grundlegende Konzepte verstanden werden, um mit diesem Dateiformat arbeiten zu können.

**File Information Base (Fib):** Die Fib-Struktur enthält Informationen über das Dokument und gibt die Dateizeiger auf verschiedene Teile an, aus denen das Dokument besteht.
Die Fib ist eine Struktur mit variabler Länge. Mit Ausnahme des Basisabschnitts, dessen Größe feststeht, geht jedem Abschnitt ein Zählfeld voraus, das die Größe des nächsten Abschnitts angibt.

**Zeichenposition:** CP oder Zeichenposition stellt eine vorzeichenlose 32-Bit-Ganzzahl dar, die als nullbasierter Index eines Zeichens im Dokumenttext dient. Die Position und Größe jedes Zeichens in der Datei kann nicht direkt abgerufen werden und muss mithilfe eines vordefinierten Algorithmus berechnet werden. Zu den Charakteren gehören:

* Text des Dokuments
* Anker von Objekten wie Fußnoten oder Textfeldern
* Steuerzeichen wie Absatzmarken und Tabellenzellenmarken

**SPS:** Die SPS-Struktur ist ein Array von CPs gefolgt von einem Array von Datenelementen. Die Datenelemente für jede SPS müssen die gleiche Größe von null oder mehr Bytes haben, und aus diesem Grund muss die Anzahl der CPs um eins größer sein als die Anzahl der Datenelemente. SPS-Strukturen haben unterschiedliche Typen, wobei jeder Typ angibt, ob doppelte CPs für diesen Typ zulässig sind oder nicht. Eine SPS-Struktur besteht aus:

* **aCP (variable Länge):** Ein Array von CP-Elementen. Jeder Typ von **SPS**-Struktur spezifiziert die Bedeutung der CP-Elemente und den zulässigen Bereich.
* **aData (variable Länge):** Jeder Typ von **SPS**-Struktur spezifiziert die Struktur und Bedeutung der Datenelemente, alle Einschränkungen bezüglich der Anzahl von Datenelementen und alle Einschränkungen bezüglich der darin enthaltenen Daten. Es spezifiziert auch die Beziehung zwischen den Datenelementen und den entsprechenden CPs.

**Gültige Auswahl:** Die .DOC-Dateikonstrukte werden hauptsächlich durch eine Reihe von CPs beschrieben. Es gibt eine Reihe von [Regeln](https://msdn.microsoft.com/en-us/library/dd908861(v#office.12).aspx), die von Microsoft in einem solchen Fall befolgt werden müssen.

**STTB:** Die STTB ist eine Zeichenfolgentabelle, die aus einem Header besteht, dem ein Array von Elementen folgt. Der **cData**-Wert gibt die Anzahl der Elemente an, die im Array enthalten sind.

**Speicherung von Eigenschaften:** Eine Word-Datei kann verschiedene Elemente wie Text, Absätze, Tabellen, Bilder und Abschnitte enthalten, wobei jedes seine eigenen Eigenschaften haben kann. Eigenschaften davon werden in der Word-Datei als Abweichungen vom Standard gespeichert. Solche Unterschiede werden durch PR1 spezifiziert, das aus einem Single Property Modifier (Sprm) und seinem Operanden besteht. Eine Anwendung kann den endgültigen Satz von Eigenschaften durch Anwendung von Listen von **Prl**s bestimmen.

**Passwortschutz:** Word-Dateien können auch passwortgeschützt werden, wofür einer der folgenden Mechanismen verwendet werden kann.

* XOR-Verschleierung
* RC4-Verschlüsselung von Office-Binärdokumenten
* Office-Binärdokument RC4 CryptoAPI-Verschlüsselung

Wenn FibBase.fEncrypted und FibBase.fObfuscation beide 1 sind, wird die Datei mithilfe von XOR-Verschleierung verschleiert.

Wenn FibBase.fEncrypted 1 und FibBase.fObfuscation 0 ist, wird die Datei entweder mit Office Binary Document RC4 Encryption oder Office Binary Document RC4 CryptoAPI Encryption verschlüsselt, wobei der EncryptionHeader in den ersten FibBase.lKey-Bytes des Tabellenstreams gespeichert wird. EncryptionHeader.EncryptionVersionInfo gibt an, welcher Verschlüsselungsmechanismus verwendet wurde, um die Datei zu verschlüsseln.

### Dateistruktur ###

Eine binäre Word-Datei in ihrer Originalität ist eine zusammengesetzte OLE-Datei, die aus mehreren Speichern und Streams besteht. Diese Speicher und Streams haben ihre eigene Struktur und Größe, die die Parameter zum Schreiben und Lesen angeben. Diese sind:

#### WordDocument Stream ####

Dieser Stream enthält den Dokumenttext und andere Informationen, auf die von anderen Teilen der Datei verwiesen wird. Der Stream hat keine vordefinierte Struktur außer der FIB am Anfang, die obligatorisch ist und am Offset 0 stehen sollte. Dieser Stream darf nicht größer als 2147 MB sein.

#### 1TableStream oder 0TableStream ####

Eine binäre Word-Datei kann Tabellenströme enthalten, die als 1Table-Stream oder 0Table-Stream bekannt sind. Mindestens einer davon sollte im Dokument vorhanden sein. Wenn ein Dokument jedoch sowohl 1Table- als auch 0Table-Streams enthält, wird nur der Stream verwendet, auf den base.fWhichTblStm verweist. Der nicht referenzierte Stream MUSS ignoriert werden.
Der Tabellenstrom DARF NICHT größer als 2147 MB sein.

#### Datenstrom ####

Der Datenstrom hat keine vordefinierte Struktur. Es enthält Daten, die von der FIB oder von anderen Teilen der Datei referenziert werden. Dieser Strom muss nicht vorhanden sein, wenn keine Verweise darauf vorhanden sind. Der Datenstrom DARF NICHT größer als 2147 MB sein.

#### Objektpoolspeicher ####

Der Objektpoolspeicher enthält Speicher für eingebettete OLE-Objekte. Dieser Speicher muss nicht vorhanden sein, wenn das Dokument keine eingebetteten OLE-Objekte enthält.

#### Benutzerdefinierter XML-Datenspeicher ####

Der benutzerdefinierte XML-Datenspeicher ist ein optionaler Speicher, dessen Name „MsoDataStore“ lauten MUSS.

#### Zusammenfassender Informationsstrom ####

Der Zusammenfassungsinformationsstrom ist ein optionaler Strom, dessen Name „\005SummaryInformation“ sein MUSS, wobei \005 das Zeichen mit dem Wert 0x0005 und nicht das Zeichenfolgenliteral „\005“ ist.

#### Dokumentzusammenfassung Informationsstrom ####

Der Stream Document Summary Information ist ein optionaler Stream, dessen Name „\005DocumentSummaryInformation“ sein MUSS, wobei \005 das Zeichen mit dem Wert 0x0005 ist, nicht das Zeichenfolgenliteral „\005“.

#### Verschlüsselungsstream ####

Der Verschlüsselungsstrom ist ein optionaler Strom, dessen Name „Verschlüsselung“ lauten MUSS. Dieser Stream DARF NICHT vorhanden sein, es sei denn, die beiden folgenden Bedingungen sind erfüllt:

* Das Dokument ist mit Office Binary Document RC4 CryptoAPI Encryption verschlüsselt.
* Der fDocProps-Wert wird in EncryptionHeader.Flags festgelegt.

#### Makrospeicher ####

Der Makrospeicher ist ein optionaler Speicher, der die Makros für die Datei enthält. Falls vorhanden, MUSS es sich um einen Projektstammspeicher handeln.

#### Speicherung von XML-Signaturen ####

Der XML-Signaturenspeicher ist ein optionaler Speicher, dessen Name „_xmlsignatures“ lauten MUSS.

#### Signaturen-Stream ####

Der Signaturen-Stream ist ein optionaler Stream, dessen Name „_signatures“ lauten MUSS. Dieser Stream enthält digitale Signaturen.

#### Information Rights Management Data Space Storage ####

Der Information Rights Management Data Space-Speicher ist ein optionaler Speicher, dessen Name „\006DataSpaces“ lauten MUSS, wobei \006 das Zeichen mit dem Wert 0x0006 und nicht das Zeichenfolgenliteral „\006“ ist. Wenn dieser Speicher vorhanden ist, MUSS auch der Protected Content Stream vorhanden sein.
Wenn dieser Speicher vorhanden ist, SOLLTEN alle angegebenen Streams und Speicher außer diesem Speicher und dem geschützten Inhaltsstream aus dem geschützten Inhaltsstream gelesen werden, wie in [MS-OFFCRYPTO] angegeben, und wenn einer dieser Streams und Speicher außerhalb des geschützten Inhalts existiert Stream, sie SOLLTEN ignoriert werden.

#### Geschützter Inhaltsstream ####

Der Protected Content Stream ist ein optionaler Stream, dessen Name „\009DRMContent“ sein MUSS, wobei \009 das Zeichen mit dem Wert 0x0009 und nicht das Zeichenfolgenliteral „\009“ ist.
Wenn dieser Stream vorhanden ist, MUSS auch der Information Rights Management Data Space Storage vorhanden sein.

## Verweise ##

* [MS-DOC-Dateiformatspezifikationen](https://msdn.microsoft.com/en-us/library/cc313153(v#office.12).aspx)
* [Doc Computing](https://en.wikipedia.org/wiki/Doc_(computing))

