{
  "date" : "2019-12-09",
  "keywords" :[ "Zip-Datei", "ZIP-Dateiformat", "Was ist eine ZIP-Datei", "Datei", "Zip-Beispiel", "Zip-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"POSTLEITZAHL",
  "description":"Was ist eine ZIP-Datei und APIs, die ZIP-Dateien erstellen und öffnen können.",
  "linktitle" : "ZIP",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2019-12-09"
}

## Was ist eine ZIP-Datei? ##

Eine Datei mit der Erweiterung .zip ist ein Archiv, das eine oder mehrere Dateien oder Verzeichnisse enthalten kann. Das Archiv kann auf die enthaltenen Dateien komprimiert werden, um die Größe der ZIP-Datei zu reduzieren. Das ZIP-Dateiformat wurde bereits im Februar 1989 von Phil Katz veröffentlicht, um die Archivierung von Dateien und Ordnern zu erreichen. Das Format wurde Teil des Dienstprogramms [PKZIP](https://www.pkware.com/pkzip), das von PKWARE, Inc. erstellt wurde. Unmittelbar nach der Verfügbarkeit von [verfügbaren Spezifikationen](https://pkware.cachefly.net/ webdocs/casestudies/APPNOTE.TXT) haben viele Unternehmen das ZIP-Dateiformat zu einem Teil ihrer Softwareprogramme gemacht, darunter Microsoft (seit Windows 7), Apple (Mac OS X) und viele andere.

## Kurze Geschichte des ZIP-Dateiformats

Die Geschichte des ZIP-Dateiformats geht zurück auf die Klage von System Enhancement Associates (SEA) gegen PKWARE wegen der Verwendung seines ARC-Dienstprogramms ohne Genehmigungen für seine Marke und die Urheberrechte des Erscheinungsbilds und der Benutzeroberfläche des Produkts. Zuvor hatte Phil Katz den Quellcode von SEA neu geschrieben und PKXARC, einen ARC-Extraktor, und PKARC, einen Dateikomprimierer, als Freeware für MS-DOS-basierte Systeme veröffentlicht. Als PKWARE den Rechtsstreit verlor, konnte es nichts mehr verwenden, was mit ARC zu tun hatte. Hier entstand die Erstellung einer neuen Dateikomprimierung namens ZIP, die Teil des PKZIP-Dienstprogramms bei PKWARE, Inc. wurde.

Katz veröffentlichte die Spezifikationen des ZIP-Dateiformats für die Öffentlichkeit, behielt jedoch die Eigentumsrechte an seinem Komprimierungs- und Extraktionsprogramm, dh PKZIP. Das ZIP-Komprimierungssystem war (und ist) in der Lage, Dateien in einem Ordner mithilfe eines 32-Bit-Algorithmus zur zyklischen Redundanzprüfung ([CRC](http://en.wikipedia.org/wiki/Cyclic_redundancy_check)) zu archivieren, um die Datei zu komprimieren Größen. Im Gegensatz zu ARC enthielten .ZIP-Ordner eine Verzeichnisdatei, die die Rolle eines Codebuchs eines Kryptografen spielte und die Informationen enthielt, die zum Rendern der komprimierten Dateien erforderlich waren.

## Unterstützte Komprimierungsmethoden in ZIP

Gemäß den Spezifikationen des .ZIP-Dateiformats werden die folgenden Komprimierungsmethoden unterstützt.

* Store - impliziert keine Komprimierung
* Schrumpfen
* Reduktion (Dies impliziert Kompressionsfaktoren von Stufe 1 bis Stufe 4)
* Implodieren
* Entleeren
* Deflat64
* BZIP2
* LZMA (EFS)
* WavPack
* PPMd-Version I, Rev 1

DEFLATE ist die häufig verwendete Komprimierungsmethode, bei der es sich um einen verlustfreien Datenkomprimierungsalgorithmus handelt, der eine Kombination aus LZ77- und Huffman-Codierung verwendet und in [RFC 1951](https://tools.ietf.org/html/rfc1951) detailliert beschrieben wird.

## ZIP-Dateiformatspezifikationen

ZIP-Dateien können mehrere Dateien mit unterschiedlichen Komprimierungstechniken speichern und gleichzeitig das Speichern einer Datei ohne Komprimierung unterstützen. Jede Datei wird einzeln gespeichert/komprimiert, was hilft, sie zu extrahieren oder neue hinzuzufügen, ohne das gesamte Archiv zu komprimieren oder zu dekomprimieren.

### Allgemeines ZIP-Dateiformat

Jede Zip-Datei ist folgendermaßen aufgebaut:


|ZIP-Dateiformat
---|
|Lokaler Dateikopf 1
|Dateidaten 1
|Datendeskriptor 1
|Lokaler Dateikopf 2
|Dateidaten 2
|Datendeskriptor 2
| ....
| ....
|Lokaler Dateikopf N
|Dateidaten N
|Datendeskriptor N
|Entschlüsselungs-Header archivieren
|Extradatensatz archivieren
|Zentrales Verzeichnis

Das ZIP-Dateiformat verwendet einen 32-Bit-CRC-Algorithmus für Archivierungszwecke. Zum Rendern der komprimierten Dateien enthält ein ZIP-Archiv an seinem Ende ein Verzeichnis, das den Eintrag der enthaltenen Dateien und deren Speicherort in der Archivdatei enthält. Es spielt somit die Rolle der Codierung zum Einkapseln von Informationen, die zum Rendern der komprimierten Dateien erforderlich sind. ZIP-Leser verwenden das Verzeichnis, um die Liste der Dateien zu laden, ohne das gesamte ZIP-Archiv zu lesen. Das Format speichert doppelte Kopien der Verzeichnisstruktur, um einen besseren Schutz vor Datenverlust zu bieten.

Jede Datei in einem ZIP-Archiv wird als einzelner Eintrag dargestellt, wobei jeder Eintrag aus einem lokalen Dateikopf gefolgt von den komprimierten Dateidaten besteht. Das Verzeichnis am Ende des Archivs enthält die Verweise auf alle diese Dateieinträge. ZIP-Dateileser sollten vermeiden, die lokalen Dateikopfzeilen zu lesen, und alle Arten von Dateilisten sollten aus dem Verzeichnis gelesen werden. Dieses Verzeichnis ist die einzige Quelle für gültige Dateieinträge im Archiv, da Dateien auch gegen Ende des Archivs angehängt werden können. Wenn ein Lesegerät lokale Kopfzeilen eines ZIP-Archivs von Anfang an liest, liest es daher möglicherweise auch ungültige (gelöschte) Einträge, die nicht Teil des Verzeichnisses sind, das aus dem Archiv gelöscht wird.

Die Reihenfolge der Dateieinträge im zentralen Verzeichnis muss nicht mit der Reihenfolge der Dateieinträge im Archiv übereinstimmen.

### ZIP-Dateieinträge

Die Einträge in der ZIP-Datei sind hintereinander angeordnet, wobei jeder Eintrag besteht aus:

* Lokaler Dateikopf
* Optionale zusätzliche Datenfelder
* Benutzerdaten (optional komprimiert/optional verschlüsselt)

Der Local File Header jedes Eintrags enthält Informationen über die Datei, wie z. B. Kommentar, Dateigröße und Dateiname. Die zusätzlichen Datenfelder (optional) können Informationen für Erweiterungsoptionen des ZIP-Formats aufnehmen.

#### Lokaler Dateikopf

Der Local File Header hat eine spezifische Feldstruktur, die aus Multi-Byte-Werten besteht. Alle Werte werden in Little-Endian-Byte-Reihenfolge gespeichert, wobei die Feldlänge die Länge in Bytes zählt. Alle Strukturen in einer ZIP-Datei verwenden 4-Byte-Signaturen für jeden Dateieintrag. Das Ende der zentralen Verzeichnissignatur ist 0x06054b50 und kann anhand einer eigenen eindeutigen Signatur unterschieden werden. Es folgt die Reihenfolge der im Local File Header gespeicherten Informationen.


|Offset|Bytes|Beschreibung
---|---|---|
|0|4|Lokale Datei-Header-Signatur # 0x04034b50 (als Little-Endian-Zahl gelesen)
|4|2|Zum Extrahieren benötigte Version (Minimum)
|6|2|Allzweck-Bit-Flag
|8|2|Komprimierungsverfahren
|10|2|Zeitpunkt der letzten Änderung der Datei
|12|2|Datum der letzten Änderung der Datei
|14|4|CRC-32
|18|4|Komprimierte Größe
|22|4|Unkomprimierte Größe
|26|2|Dateinamenlänge (n)
|28|2|Zusätzliche Feldlänge (m)
|30|n|Dateiname
|30+n|m|Zusätzliches Feld

#### Header der zentralen Verzeichnisdatei


|Offset|Bytes|Beschreibung
---|---|---|
|0|4|Header-Signatur der zentralen Verzeichnisdatei # 0x02014b50
|4|2|Version erstellt von
|6|2|Zum Extrahieren benötigte Version (mindestens)
|8|2|Allzweck-Bit-Flag
|10|2|Komprimierungsverfahren
|12|2|Zeitpunkt der letzten Änderung der Datei
|14|2|Datum der letzten Änderung der Datei
|16|4|CRC-32
|20|4|Komprimierte Größe
|24|4|Unkomprimierte Größe
|28|2|Dateinamenlänge (n)
|30|2|Zusätzliche Feldlänge (m)
|32|2|Dateikommentarlänge (k)
|34|2|Plattennummer, wo die Datei beginnt
|36|2|Interne Dateiattribute
|38|4|Externe Dateiattribute
|42|4|Relativer Offset des lokalen Dateiheaders. Dies ist die Anzahl von Bytes zwischen dem Beginn der ersten Platte, auf der die Datei vorkommt, und dem Beginn des lokalen Dateiheaders. Dadurch kann Software, die das zentrale Verzeichnis liest, die Position der Datei innerhalb der ZIP-Datei finden.
|46|n|Dateiname
|46+n|m|Zusätzliches Feld
|46+n+m|k|Dateikommentar

#### Ende des zentralen Verzeichniseintrags


|Offset|Bytes|Beschreibung
---|---|---|
|0|4|Ende der zentralen Verzeichnissignatur # 0x06054b50
|4|2|Nummer dieser Festplatte
|6|2|Festplatte, auf der das zentrale Verzeichnis beginnt
|8|2|Anzahl der zentralen Verzeichniseinträge auf dieser Platte
|10|2|Gesamtzahl der Einträge im zentralen Verzeichnis
|12|4|Größe des zentralen Verzeichnisses (Bytes)
|16|4|Offset des Beginns des zentralen Verzeichnisses, relativ zum Beginn des Archivs
|20|2|Kommentarlänge (n)
|22|n|Kommentar

## Verweise

* [PKWARE ZIP-Dateiformatspezifikationen](https://pkware.cachefly.net/webdocs/casestudies/APPNOTE.TXT)
* [Struktur der PKZip-Datei](https://users.cs.jmu.edu/buchhofp/forensics/formats/pkzip-printable.html)

