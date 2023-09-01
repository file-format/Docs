{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OST - Outlook-Speicherdateiformat",
  "description":"Erfahren Sie mehr über das OST-Dateiformat und APIs, die OST-Dateien erstellen und öffnen können.",
  "linktitle" : "OST",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Was ist eine OST-Datei?

OST- oder Offlinespeicherdateien stellen die Postfachdaten des Benutzers im Offlinemodus auf dem lokalen Computer nach der Registrierung bei Exchange Server mit Microsoft Outlook dar. Es wird automatisch bei der ersten Verwendung von Microsoft Outlook nach Verbindung mit dem Server erstellt. Sobald die Datei erstellt ist, werden die Daten mit dem E-Mail-Server synchronisiert, sodass sie auch offline verfügbar sind, falls die Verbindung zum E-Mail-Server unterbrochen wird. OST-Dateien können Postfachelemente wie E-Mails, Kontakte, Kalenderinformationen, Notizen, Aufgaben und andere ähnliche Daten verwenden. Benutzer können E-Mails und andere Datenelemente in der OST-Datei auch ohne Verbindung zum Server erstellen, diese werden jedoch nicht mit dem Server synchronisiert. Sobald die Verbindung hergestellt ist, wird die lokale Datei erneut mit dem Server synchronisiert, sodass sowohl der Server als auch die lokale Kopie auf dem gleichen Informationsstand sind.

## OST-Dateiformat

Das Dateiformat OST (Offline Storage Table) und [PST](/de/email/pst/) (Personal Storage Table) besteht aus dem Format Personal Folder File (PFF), das dem Speichern von E-Mails, Kontakten und Terminen des Benutzers entspricht. Daten in einer PFF-Datei werden in Little-Endian gespeichert, wobei alle Daten und Zeiten als FILETIME in UTC dargestellt werden. [MS-PST] definiert zwei Arten von PFF:

* 32-Bit-ANSI-Format
* 64-Bit-Unicode-Format

PST-Dateiformat [Spezifikationen](https://learn.microsoft.com/en-us/openspecs/office_file_formats/ms-pst/141923d5-15ab-4ef1-a524-6dce75aae546), wie von Microsoft erhältlich, gelten auch für das OST-Dateiformat als kostenlos und unwiderrufliche Patentlizenzierung durch das Open Specification Promise. Es besteht aus folgenden unterscheidbaren Elementen:

* Fle-Header
* Dateikopfdaten
* Index-Zweigknoten
* Indexblattknoten
* (Datei-)Offset-Index
* (Element) Deskriptorindex
* Lokale Deskriptoren
* Artikeltabellentyp

### Header-Informationen

Die HEADER-Struktur der OST-Datei befindet sich ganz am Anfang der Datei bei 0 Offset. Sie enthält Metadateninformationen über die OST-Datei und die ROOT-Informationen für den Zugriff auf die oben beschriebenen NDB-Layer-Datenstrukturen. Die HEADER-Struktur unterscheidet sich für die Unicode- und ANSI-Versionen des OST-Dateiformats.

Der Header beginnt mit einem 4-Byte-Zauberwort **!BDN**, dargestellt durch Bytes (0x21, 0x42, 0x44, 0x4E). Eine weitere magische 2-Byte-Zahl, **SM** (0x53, 0x4D), befindet sich bei Offset 8 vom Anfang der Datei. Versionsinformationen (ANSI oder Unicode) liegen bei einem Offset von 10 vom Anfang der Datei. Der Hex-Wert (0x17) gibt die Unicode-OST-Datei an, während 0x0E oder 0x0F das ANSI-Dateiformat darstellt.

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
|rgnid[]   (128 bytes)|Ein festes Array von 32 NIDs, die jeweils einem der 32 möglichen NID_TYPEs entsprechen (NID_TYPE, NID_TYPE_NORMAL_FOLDER, NID_TYPE_SEARCH_FOLDER, NID_TYPE_NORMAL_MESSAGE, NID_TYPE_ASSOC_MESSAGE)
|qwUnused (8 Bytes)|Unbenutzter Speicherplatz; MUSS auf Null gesetzt werden. Nur Unicode-PST-Dateiformat.
|root (Unicode: 72 Bytes; ANSI: 40 Bytes)|Eine ROOT-Struktur (Abschnitt 2.2.2.5).
|dwAlign (4 Bytes)|Nicht verwendete Ausrichtungsbytes; MUSS auf Null gesetzt werden. Nur Unicode-PST-Dateiformat.
|rgbFM (128 Bytes)|Veraltetes FMap. Diese wird nicht mehr verwendet und MUSS mit 0xFF gefüllt werden. Leser SOLLTEN den Wert dieser Bytes ignorieren.
|rgbFP (128 Bytes)|Veraltete FPMap. Diese wird nicht mehr verwendet und MUSS mit 0xFF gefüllt werden. Leser SOLLTEN den Wert dieser Bytes ignorieren.
|bSentinel (1 Byte)|MUSS auf 0x80 gesetzt werden.
|bCryptMethod (1 Byte)|Gibt an, wie die Daten in der PST-Datei codiert sind. MUSS auf einen der vordefinierten Werte gesetzt werden (NDB_CRYPT_NONE, NDB_CRYPT_PERMUTE, NDB_CRYPT_CYCLIC).
|rgbReserviert (2 Bytes)| Reserviert; MUSS auf Null gesetzt werden.
|bidNextB (8 Bytes)|zeigt den nächsten verfügbaren BID-Wert an. Nur Unicode-PST-Dateiformat.
|bidNextB (NUR Unicode: 8 Bytes)|Nächstes GEBOT. Dieser Wert ist der monotone Zähler, der die für den nächsten zugewiesenen Block zuzuweisende BID anzeigt. BID-Werte rücken in 4er-Schritten vor. Weitere Einzelheiten finden Sie in Abschnitt 2.2.2.2.
|dwCRCFull (4 Bytes)|Der 32-Bit-CRC-Wert der 516 Datenbytes, beginnend von wMagicClient bis einschließlich bidNextB. Nur Unicode-PST-Dateiformat.
|ullReserviert (8 Bytes)|Reserviert; MUSS auf Null gesetzt werden. Nur ANSI-PST-Dateiformat.
|dwReserviert (4 Bytes)|Reserviert; MUSS auf Null gesetzt werden. Nur ANSI-PST-Dateiformat.
|rgbReserved2 (3 Byte)|
|bReserviert (1 Byte) |
|rgbReserved3 (32 Byte) |

## Verweise

* [Outlook Personal Folders (.ost) File Format](https://learn.microsoft.com/en-us/openspecs/office_file_formats/ms-pst/141923d5-15ab-4ef1-a524-6dce75aae546)
* [Dateiformatspezifikationen für persönliche Ordner](https://github.com/libyal/libpff/blob/main/documentation/Personal%20Folder%20File%20(PFF)%20format.asciidoc)

