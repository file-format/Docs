{
  "date" : "2019-10-11",
  "keywords" :[ "dcm-Datei", "dcm-Dateiformat", "was ist eine dcm-Datei", "Datei", "dcm-Beispiel", "dcm-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DCM-Dateiformat - Digitale medizinische Informationsdatei",
  "description":"Erfahren Sie mehr über das DCM-Dateiformat und APIs, die DCM-Dateien erstellen und öffnen können.",
  "linktitle" : "DCM",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-07-03"
}

## Was ist eine DCM-Datei?

Dateien mit der Erweiterung .dcm stellen digitale Bilder dar, die medizinische Informationen von Patienten wie MRTs, CT-Scans und Ultraschallbilder speichern. DCM-Dateien verwenden das Bilddateiformat [DICOM](/de/image/dicom/) (Digital Imaging and Communications in Medicine) und können Patienteninformationen als Referenz enthalten. Es wurde von der [National Electrical Manufacturers Association](https://en.wikipedia.org/wiki/National_Electrical_Manufacturers_Association) (NEMA) entwickelt und sollte das Bilddateiformat für die Verteilung und Anzeige medizinischer Bilder standardisieren.

## DCM-Dateiformat

DCM-Dateien speichern Informationen im DICOM-Bildformat. Diese Dateien speichern den Datensatz, bei dem es sich um reale Informationen handelt, die eine SOP-Instanz in Bezug auf ein DICOM IOD darstellen. DICOM-Datei-Metainformationen werden in der Datei gespeichert, gefolgt vom Bytestrom des eigentlichen Datensatzes.

### DICOM-Datei-Metainformationen ##

Jede DICOM-Datei enthält einen Identifikationsinformations-Header für den eingekapselten Datensatz, der aus Folgendem besteht:
* Eine 128-Byte-Dateipräambel
* 4-Byte-DICOM-Präfix
* Datei-Meta-Elemente

Dieser Header ist ein Muss für jede DICOM-Datei.

### Datei-Meta-Elemente ###
|Attributname|Tag|Typ| Attributbeschreibung
---|---|---|---|
|Dateipräambel|Keine Tag- oder Längenfelder|1|Ein festes 128-Byte-Feld, das für das Anwendungsprofil oder die von der Implementierung festgelegte Verwendung verfügbar ist. Wenn sie nicht von einem Anwendungsprofil oder einer bestimmten Implementierung verwendet werden, müssen alle Bytes auf 00H gesetzt werden. Dateisatzleser oder -aktualisierer dürfen sich nicht auf den Inhalt dieser Präambel verlassen, um festzustellen, ob diese Datei eine DICOM-Datei ist oder nicht.
|DICOM-Präfix|Keine Tag- oder Längenfelder|1|Vier Bytes, die die Zeichenfolge "DICM" enthalten. Dieses Präfix soll verwendet werden, um zu erkennen, ob diese Datei eine DICOM-Datei ist oder nicht.
|Länge der Datei-Meta-Informationsgruppe|(0002,0000)|1|Anzahl der Bytes nach diesem Datei-Meta-Element (Ende des Wertfeldes) bis einschließlich des letzten Datei-Meta-Elements der Datei-Meta-Informationen der Gruppe 2
|Datei-Meta-Informations-Version|(0002,0001)|1|Dies ist ein Zwei-Byte-Feld, in dem jedes Bit eine Version dieses Datei-Meta-Informations-Headers identifiziert. In Version 1 ist der erste Bytewert 00H und der zweite Bytewert 01H. Implementierungen, die Dateien mit Metainformationen lesen, bei denen dieses Attribut Bit 0 (lsb) des zweiten Bytes auf 1 gesetzt hat, können die Dateimetainformationen wie hier angegeben interpretieren Version von PS3.10. Alle anderen Bits sollen nicht geprüft werden.
|Media Storage SOP Class UID|(0002,0002)|1|Identifiziert eindeutig die dem Datensatz zugeordnete SOP-Klasse. Für die Medienspeicherung zulässige SOP-Klassen-UIDs sind in PS3.4 – Anwendungsprofile für Medienspeicherung angegeben.
|Medienspeicher-SOP-Instanz-UIID|(0002,0003)|1|Identifiziert eindeutig die SOP-Instanz, die dem in der Datei platzierten Datensatz zugeordnet ist und den Datei-Metainformationen folgt.
|Übertragungssyntax-UID|(0002,0010)|1|Identifiziert eindeutig die Übertragungssyntax, die zum Codieren des folgenden Datensatzes verwendet wird. Diese Übertragungssyntax gilt nicht für die Datei-Metainformationen.
|Implementierungsklassen-UID|(0002,0012)|1|Identifiziert eindeutig die Implementierung, die diese Datei und ihren Inhalt geschrieben hat. Es bietet eine eindeutige Identifizierung des Implementierungstyps, der die Datei zuletzt bei Austauschproblemen geschrieben hat.
|Name der Implementierungsversion|(0002,0013)|3|Identifiziert eine Version für eine Implementierungsklassen-UID (0002,0012) unter Verwendung von bis zu 16 Zeichen des Repertoires.
|Titel der Quellanwendungsentität|(0002,0016)|3|Der Titel der DICOM-Anwendungsentität (AE) der AE, die den Inhalt dieser Datei geschrieben (oder zuletzt aktualisiert) hat. Bei Verwendung ermöglicht es die Rückverfolgung der Fehlerquelle bei Medienaustauschproblemen.
|UID des Erstellers der privaten Informationen|(0002,0100)|3|Die UID des Erstellers der privaten Informationen (0002,0102).
|Private Informationen|(0002,0102)|1C|Enthält private Informationen, die in den Datei-Metainformationen platziert sind. Der Ersteller soll in (0002,0100) identifiziert werden. Erforderlich, wenn Private Information Creator UID (0002,0100) vorhanden ist.

### Datensatzkapselung ###

Eine DICOM-Datei enthält einen einzelnen Datensatz, der eine einzelne SOP-Instanz darstellt, die sich auf eine einzelne SOP-Klasse bezieht. Die Übertragungssyntax-UID der DICOM-Datei-Metainformationen definiert die Übertragungssyntax, die zum Codieren des Datensatzes verwendet wird.

### Unterstützung für Dateiverwaltungsinformationen ###

Die Medienformatebene stellt die folgenden Dateiverwaltungsinformationen bereit, falls dies für ein bestimmtes DICOM-Anwendungsprofil erforderlich ist.

* Identifizierung des Eigentümers von Dateiinhalten

* Dateizugriffsstatistiken (z. B. Datum und Uhrzeit der Erstellung)

* Zugriffskontrolle für Anwendungsdateien

* Zugriffskontrolle auf physische Medien (z. B. Schreibschutz)

## Verweise ##
* [DICOM-Standard](https://www.dicomstandard.org/current/)
* [DICOM-Dateiformat](https://dicom.nema.org/dicom/2013/output/chtml/part10/chapter_7.html)

