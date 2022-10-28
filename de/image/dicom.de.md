{
  "date" : "2019-10-11",
  "keywords" :[ "dicom-Datei", "dicom-Dateiformat", "was ist eine dicom-Datei", "Datei", "dicom-Beispiel", "dicom-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DICOM - Dateiformat für digitale Bildgebung und Kommunikation",
  "description":"Erfahren Sie mehr über das DICOM-Dateiformat und APIs, die DICOM-Dateien erstellen und öffnen können.",
  "linktitle" : "DICOM",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Was ist eine DICOM-Datei?

DICOM ist die Abkürzung für Digital Imaging and Communications in Medicine und gehört zum Gebiet der Medizinischen Informatik. DICOM wird für die Integration von medizinischen Bildgebungsgeräten wie Druckern, Servern, Scannern usw. verschiedener Anbieter verwendet und enthält auch Identifikationsdaten jedes Patienten zur Eindeutigkeit. DICOM-Dateien können zwischen zwei Parteien geteilt werden, wenn sie in der Lage sind, Bilddaten im DICOM-Format zu empfangen. Der Kommunikationsteil von DICOM ist ein Anwendungsschichtprotokoll und verwendet TCP/IP zur Kommunikation zwischen Entitäten. Von Webdiensten unterstützte Versionen sind 1.0, 1.1, 2 oder höher.

## Geschichte ##

DICOM wurde gemeinsam vom American College of Radiology (ACR) und der National Electrical Manufacturers Association (NEMA) für den Austausch und die Anzeige medizinischer Bilder wie MRTs, CT-Scans und Ultraschallbilder entwickelt. Anfangs war es schwierig, die von den Maschinen produzierten Bilder zu entschlüsseln. Daher bildeten ACR und NEMA 1983 zusammen ein Team, das 1985 seinen ersten Standard, ACR/NEMA 300, veröffentlichte. Die zweite Version wurde 1988 veröffentlicht, die bei Anbietern beliebter war, aber bald wurde erkannt, dass auch die zweite Version verbessert werden muss. Die 3. Version des Standards wurde 1993 als "DICOM" veröffentlicht. 3.0 ist immer noch die neueste Version, wurde aber seit 1993 kontinuierlich aktualisiert.

## DICOM-Dateiformat ##

DICOM ist die Kombination aus Dateiformatdefinition und einem Netzwerkkommunikationsprotokoll. DICOM verwendet die Erweiterung .DCM. .DCM gibt es in zwei verschiedenen Formaten, dh Format 1.x und Format 2.x. Das DCM-Format 1.x ist weiterhin in zwei Versionen normal und erweitert verfügbar. Für die Webdienste von DICOM werden HTTP- und HTTPS-Protokolle verwendet.

### Dateikopf ###

Der Dateikopf enthält 128 Byte Dateipräambel und 4 Byte DICOM-Präfix.

**Präambel # 128 Bytes**|**Präfix # 4 Bytes „D, I, C, M**

**Präambel** wird verwendet, um auf die Bilder und andere Daten in der DICOM-Datei zuzugreifen, wodurch die Kompatibilität mit häufig verwendeten Bilddateiformaten gewährleistet wird.

**Präfix** enthält die Zeichenkette „DICM“ als Großbuchstaben.

### Datensatz ###

Jede Datei muss einen einzelnen Datensatz enthalten, der eine SOP-Instanz und eine SOP-Klasse mit zugehörigem IOD darstellt. Datensatz ist die Darstellung von Informationen aus der realen Welt. Der Datensatz enthält Datenelemente und Datenelemente enthalten Werte der Attribute dieses Objekts. Die Struktur der Attribute ist in IODs angegeben. Ein DICOM-Datenobjekt besteht aus einer Reihe von Attributen, einschließlich Elementen wie Name, ID usw., und auch einem speziellen Attribut, das die Bildpixeldaten enthält.

### Datenelemente ###

Datenelement besteht aus Datenelement-Tag, Wertlänge und Wert für das Datenelement. Es gibt 5 Arten von Datenelementen, nämlich Typ 1 Erforderliche Datenelemente, Typ 1C Bedingte Datenelemente, Typ 2 Erforderliche Datenelemente, Typ 2C Bedingte Datenelemente und Typ 3 Optionale Datenelemente. Grundlegende Drei Arten von Datenelementstrukturen sind wie folgt.

**Datenelement mit einem expliziten VR**

|Gruppennummer|Elementnummer|Wertdarstellung|Reserviert|Wertlänge|Wertfeld
---|---|---|---|---|---|
|2 Bytes|2 Bytes|2 Bytes|2 Bytes # 0x00, 0x00|4 Bytes|"Wertlänge Bytes"

**Datenelement mit einem expliziten VR**

|Gruppennummer|Elementnummer|Wertdarstellung|Wertlänge|Wertfeld
---|---|---|---|---|
|2 Bytes|2 Bytes|2 Bytes|2 Bytes|"Wertlänge Bytes"

**Datenelement mit implizitem VR**


|Gruppennummer|Elementnummer|Wertlänge|Wertfeld
---|---|---|---|
|2 Bytes|2 Bytes|4 Bytes|"Wertlänge Bytes"

1. **Datenelement-Tag**: Eine geordnete Ganzzahl, die die Gruppennummer und die Elementnummer darstellt
1. **Wertdarstellung VR**: VR ist eine Zeichenfolge, die die VR des Datenelements darstellt.
1. **Wertlänge**: ist die vorzeichenlose Ganzzahl, die die explizite Länge des Wertfelds darstellt.
1. **Wertfeld**: Beschreibt die Werte der Datenelemente.

## Übertragungssyntax ##

Die Übertragungssyntax ist ein Satz von Regeln für die Codierung, um abstraktere Syntaxen eindeutig darzustellen. Mit Hilfe der Transfersyntax verhandeln kommunizierende Einheiten über gemeinsame Verschlüsselungstechniken, die sie unterstützen.

## SOPs ##

Die Vereinigung von IOD und DIMSE definiert eine SOP-Klasse. Die SOP-Klassendefinition enthält die Regeln und die Semantik, die die Verwendung der Dienste in der DIMSE-Dienstgruppe oder der Attribute des IOD einschränken können. Beispiele für Serviceelemente sind Store, Get, Find, Move usw. Beispiele für Objekte sind CT-Bilder, MR-Bilder, aber auch Zeitplanlisten, Druckwarteschlangen usw.

## Dienstleistungen ##

DICOM bietet verschiedene Dienste an, die sich hauptsächlich auf die Übertragung von Daten beziehen. Jeder wird im Folgenden kurz beschrieben:


**Speichern:** Der DICOM-Speicherdienst sendet Bilder oder andere Objekte an ein Bildarchivierungs- und Kommunikationssystem (PACS) oder einen Server.


**Storage Commitment:** Der Storage Commitment Service wird verwendet, um zu bestätigen, dass ein Bild dauerhaft auf einem Gerät auf einem beliebigen Medientyp gespeichert wurde.


**Abfrage/Abruf:** Dieser Dienst ermöglicht es einer Arbeitsstation, die Listen von Bildern oder anderen Objekten zu finden und sie dann von PACS abzurufen.


**Modalitäts-Arbeitsliste:** Der Modalitäts-Arbeitsliste-Dienst enthält eine Liste von Bildgebungsverfahren, die für die Durchführung durch ein Bilderfassungsgerät geplant wurden.


**Drucken:** Dieser Dienst sendet Bilder an den Drucker.

## Portnummern über IP ##

DICOM verwendet die folgenden TCP- und UDP-Ports:

1. 104
1. 2761
1. 2762
1. 11112

## Verweise ##

* [https://en.wikipedia.org/wiki/DICOM](https://en.wikipedia.org/wiki/DICOM)
* [https://www.leadtools.com/sdk/medical/dicom-spec](https://www.leadtools.com/sdk/medical/dicom-spec)
* [https://www.dicomstandard.org/concepts/](https://www.dicomstandard.org/concepts/)
* [https://www.dicomlibrary.com/dicom/](https://www.dicomlibrary.com/dicom/)

