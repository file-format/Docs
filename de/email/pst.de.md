{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PST - Outlook Personal Information Store-Dateiformat",
  "description":"Erfahren Sie mehr über das PST-Dateiformat und APIs, die PST-Dateien erstellen und öffnen können.",
  "linktitle" : "PST",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Was ist eine PST-Datei?

Dateien mit der Erweiterung .pst stellen persönliche Outlook-Speicherdateien (auch als persönliche Speichertabelle bezeichnet) dar, die verschiedene Benutzerinformationen speichern. Benutzerinformationen werden in Ordnern unterschiedlicher Art gespeichert, darunter E-Mails, Kalendereinträge, Notizen, Kontakte und mehrere andere Dateiformate. PST-Dateien werden zum Offline-Archivieren von E-Mail-Daten verwendet, die später in verschiedenen Anwendungen geladen und angezeigt werden können.

## PST-Dateiformatspezifikationen

PST-Dateiformat [Spezifikationen](https://learn.microsoft.com/en-us/openspecs/office_file_formats/ms-pst/141923d5-15ab-4ef1-a524-6dce75aae546) sind von Microsoft als kostenlose und unwiderrufliche kostenlose Patentlizenzierung über das Open Specification Promise erhältlich .

### Art der PST-Formate

PST-Dateiformate werden basierend auf der Kodierung des Dateityps in zwei Typen eingeteilt. ANSI-codierte PST-Dateien sind ältere Dateiformate und werden nur von Outlook 2002 und früheren Versionen unterstützt. Solche Dateien haben eine maximale Größe von 2 GB (2^^31^^ Bytes) und unterstützen kein Unicode. Ein modernerer Dateiformattyp, der auf Unicode-Codierung basiert, hebt die Beschränkung der Dateigröße auf und kann eine maximale Datengröße von 50 GB erreichen.

### Logische Organisation des PST-Dateiformats

An der Basis des PST-Dateiformats liegt B-Tree, das Daten sortiert hält und Suchen, sequenziellen Zugriff, Einfügungen, Löschungen usw. in logarithmischer Zeit ermöglicht. Die Gesamtstruktur einer PST-Datei ist in drei Schichten organisiert.

![Logical layers of a PST file](/de/email/PST-1.png "Logical layers of a PST file")

„Knotendatenbank (NDB)-Schicht“ – Die Knotendatenbankschicht liegt auf der unteren Ebene einer PST-Datei und enthält eine Knotendatenbank. Diese Knoten stellen tatsächlich untergeordnete Speichereinrichtungen des PST-Dateiformats dar. Die NDB-Schicht umfasst Header, Dateizuordnungsinformationen, Blöcke und BTrees (Node BTree und Block BTree) aus Speichersicht. Knoten und Blöcke der NDB-Schicht sind über die Daten-BID verknüpft, die eine der vier Eigenschaften der Knotenreferenz ist, dh NID (Knoten-ID), Eltern-NID, Daten-BID (Block-BID) und Unterknoten-BID.

„Layer für Listen, Tabellen und Eigenschaften“ – Der LTP-Layer bietet das logische Verständnis von Konzepten auf höherer Ebene über NDB. Neben anderen Elementen besteht die LTP-Schicht hauptsächlich aus Property Context (PC) und Table Context (TC). PC ist eine Sammlung von Eigenschaften, während TC eine zweidimensionale Matrix aus Sammlung von Eigenschaften vs. deren Vorhandensein darstellt. Effiziente Implementierung von PCs und TCs, die LTP-Schicht verwendet die folgenden zwei Arten von Datenstrukturen auf dem NDB-Knoten:

* Heap On Node (HN) - ermöglicht die Unterteilung des Datenstroms eines Knotens in kleine Fragmente variabler Größe.
* BTree on Heap (BTH) – BTH bietet eine bequeme und praktische Möglichkeit zum Durchsuchen von Daten. PCs, die oben beschrieben wurden, sind als BTHs implementiert, und deshalb wird es implementiert, indem es innerhalb einer HN-Struktur aufgebaut wird.

"Messaging Layer" - Auf dieser Ebene werden Regeln und Geschäftslogik auf höherer Ebene für die Arbeit mit PST-Dateien implementiert. Die logische Ausgabe dieser Schicht ergibt sich als Ordnerobjekte, Nachrichtenobjekte, Anhangsobjekte und Eigenschaften, was durch die Kombination von LTP- und NDB-Schichten ermöglicht wird. Auf dieser Ebene werden auch Regeln und Anforderungen definiert, die bei der Änderung der PST-Inhalte zu beachten sind.

### Physische Organisation des PST-Dateiformats

Die hohe Ebene der Dateiorganisation der PST-Datei ist in der folgenden Abbildung dargestellt. Dies ist nur ein Überblick über verschiedene Konzepte von logischen Elementen der PST-Datei.

![Physical organization of the PST file format](/de/email/PST-2.png "Physical organization of the PST file format")


#### PST-Header-Informationen

Die HEADER-Struktur der PST-Datei befindet sich ganz am Anfang der Datei bei 0 Offset. Es enthält Metadateninformationen über die PST-Datei und die ROOT-Informationen für den Zugriff auf die oben beschriebenen NDB-Layer-Datenstrukturen. Die HEADER-Struktur unterscheidet sich für die Unicode- und ANSI-Versionen des PST-Dateiformats.

Der Header beginnt mit einem 4-Byte-Zauberwort **!BDN**, dargestellt durch Bytes (0x21, 0x42, 0x44, 0x4E). Eine weitere magische 2-Byte-Zahl, **SM** (0x53, 0x4D), befindet sich bei Offset 8 vom Anfang der Datei. Versionsinformationen (ANSI oder Unicode) liegen bei einem Offset von 10 vom Anfang der Datei. Der Hex-Wert (0x17) gibt die Unicode-PST-Datei an, während 0x0E oder 0x0F das ANSI-Dateiformat darstellt.

|Feld|Beschreibung
---|---|
|dwMagic (4 Bytes)|MUSS "{ 0x21, 0x42, 0x44, 0x4E } ("!BDN")" sein
|dwCRCPartial (4 Byte)|Der 32-Bit-CRC-Wert der 471 Datenbyte ab wMagicClient (0ffset 0x0008)
|wMagicClient (2 Bytes)|MUSS "{ 0x53, 0x4D }" sein.
|wVer (2 Bytes)|Version des Dateiformats. Dieser Wert MUSS 14 oder 15 sein, wenn die Datei eine ANSI-PST-Datei ist, und MUSS 23 sein, wenn die Datei eine Unicode-PST-Datei ist.
|wVerClient (2 Bytes)|Version des Client-Dateiformats. Die Version, die dem in diesem Dokument beschriebenen Format entspricht, ist 19. Ersteller einer neuen PST-Datei, die auf diesem Dokument basiert, SOLLTEN diesen Wert auf 19 initialisieren.
|bPlatformCreate (1 Byte)|Dieser Wert MUSS auf 0x01 gesetzt werden.
|bPlatformAccess (1 Byte)|Dieser Wert MUSS auf 0x01 gesetzt werden.
|dwReserviert (8 Byte)|
|bidUnused (nur 8 Byte Unicode)|Unused padding hinzugefügt, als das Unicode-PST-Dateiformat erstellt wurde.
|bidNextP (Unicode: 8 Bytes; ANSI: 4 Bytes)|Nächste Seite BID. Seiten haben einen speziellen Zähler für die Zuordnung von bidIndex-Werten. Der Wert von bidIndex für BIDs für Seiten wird von diesem Zähler zugewiesen.
|bidNextB (nur 4 Bytes ANSI): |Nächstes BID. Dieser Wert ist der monotone Zähler, der die für den nächsten zugewiesenen Block zuzuweisende BID anzeigt. BID-Werte rücken in 4er-Schritten vor. Weitere Einzelheiten finden Sie in Abschnitt 2.2.2.2.
|dwUnique (4 Bytes)|Dies ist ein monoton ansteigender Wert, der jedes Mal geändert wird, wenn die HEADER-Struktur der PST-Datei geändert wird. Die Funktion dieses Werts besteht darin, einen eindeutigen Wert bereitzustellen und sicherzustellen, dass die HEADER-CRCs nach jeder Header-Modifikation unterschiedlich sind.
|rgnid[](128 bytes)|Ein festes Array von 32 NIDs, die jeweils einem der 32 möglichen NID_TYPEs entsprechen (NID_TYPE, NID_TYPE_NORMAL_FOLDER, NID_TYPE_SEARCH_FOLDER, NID_TYPE_NORMAL_MESSAGE, NID_TYPE_ASSOC_MESSAGE)
|qwUnused (8 Bytes)|Unbenutzter Platz; MUSS auf Null gesetzt werden. Nur Unicode-PST-Dateiformat.
|root (Unicode: 72 Bytes; ANSI: 40 Bytes)|Eine ROOT-Struktur (Abschnitt 2.2.2.5).
|dwAlign (4 Bytes)|Nicht verwendete Ausrichtungsbytes; MUSS auf Null gesetzt werden. Nur Unicode-PST-Dateiformat.
|rgbFM (128 Bytes)|Veraltetes FMap. Diese wird nicht mehr verwendet und MUSS mit 0xFF gefüllt werden. Leser SOLLTEN den Wert dieser Bytes ignorieren.
|rgbFP (128 Bytes)|Veraltete FPMap. Diese wird nicht mehr verwendet und MUSS mit 0xFF gefüllt werden. Leser SOLLTEN den Wert dieser Bytes ignorieren.
|bSentinel (1 Byte)|MUSS auf 0x80 gesetzt werden.
|bCryptMethod (1 Byte)|Gibt an, wie die Daten in der PST-Datei codiert sind. MUSS auf einen der vordefinierten Werte gesetzt werden (NDB_CRYPT_NONE, NDB_CRYPT_PERMUTE, NDB_CRYPT_CYCLIC).
|rgbReserviert (2 Byte)| Reserviert; MUSS auf Null gesetzt werden.
|bidNextB (8 Bytes)|zeigt den nächsten verfügbaren BID-Wert an. Nur Unicode-PST-Dateiformat.
|bidNextB (NUR Unicode: 8 Bytes)|Nächstes GEBOT. Dieser Wert ist der monotone Zähler, der die für den nächsten zugewiesenen Block zuzuweisende BID anzeigt. BID-Werte rücken in 4er-Schritten vor. Weitere Einzelheiten finden Sie in Abschnitt 2.2.2.2.
|dwCRCFull (4 Bytes)|Der 32-Bit-CRC-Wert der 516 Datenbytes, beginnend von wMagicClient bis einschließlich bidNextB. Nur Unicode-PST-Dateiformat.
|ullReserviert (8 Bytes)|Reserviert; MUSS auf Null gesetzt werden. Nur ANSI-PST-Dateiformat.
|dwReserviert (4 Byte)|Reserviert; MUSS auf Null gesetzt werden. Nur ANSI-PST-Dateiformat.
|rgbReserved2 (3 Byte)|
|bReserviert (1 Byte) |
|rgbReserved3 (32 Byte) |

### Datenschutz ###

Aus Sicherheitsgründen können PST-Dateien auch passwortgeschützt werden, was erfordert, dass die ladende Anwendung ein Passwort anwendet, bevor sie angezeigt werden können. Das auf die PST-Datei angewendete Passwort wird im Nachrichtenspeicher gespeichert. Dies bietet jedoch keinen starken Datenschutz, da das Passwort durch verfügbare Tools entfernt werden kann. Außerdem wird das vom Benutzer angegebene Passwort nicht als Teil des Schlüssels zum Codieren und Decodieren von Verschlüsselungsalgorithmen verwendet. Daher besteht kein Vorteil darin, Daten zu schützen, auf die nicht autorisierte Parteien zugreifen können. Die Speicherung des Passworts als CRC-32-Hash der ursprünglichen Zeichenfolge macht es auch zu einer schwachen Methode für die Datensicherheit gegen Brute-Force-Ansätze.

## Verweise ##

* [Outlook-Dateiformat für persönliche Ordner (.pst)](https://learn.microsoft.com/en-us/openspecs/office_file_formats/ms-pst/141923d5-15ab-4ef1-a524-6dce75aae546)
* [Dateiformatspezifikationen für persönliche Ordner](https://github.com/libyal/libpff/blob/main/documentation/Personal%20Folder%20File%20(PFF)%20format.asciidoc)

