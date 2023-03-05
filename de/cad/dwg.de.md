{
  "date" : "2020-03-16",
  "keywords" :[ "DWG", "Dateiformat", "CAD", "Öffnen", "Erstellen" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Erfahren Sie mehr über das DWG-Dateiformat und APIs, die DWG-Dateien erstellen und öffnen können.",
  "title" :"DWG-Dateiformat",
  "linktitle" : "DWG",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2019-09-10"
}

## Was ist eine DWG-Datei?

Dateien mit der Erweiterung DWG stellen proprietäre Binärdateien dar, die zum Enthalten von 2D- und 3D-Konstruktionsdaten verwendet werden. Wie DXF, bei denen es sich um ASCII-Dateien handelt, repräsentiert DWG das binäre Dateiformat für CAD-Zeichnungen (Computer Aided Design). Es enthält Vektorbilder und Metadaten zur Darstellung von Inhalten von CAD-Dateien. Es gibt kostenlose Viewer zum Anzeigen von DWG-Dateien auf Windows-Betriebssystemen, wie z. B. das kostenlose DWG TrueView von Autodesk. Es gibt auch andere Anwendungen von Drittanbietern, die das Erreichen von DWG-Dateien unterstützen. DWG-Dateien enthalten vom Benutzer erstellte Informationen und beinhalten:

* Entwürfe
* Geometrische Daten
* Karten und Fotos

Dieses Format wird häufig von Architekten, Ingenieuren und Designern für verschiedene Designzwecke verwendet.

## Kurze Geschichte ##

Das DWG-Dateiformat hat sich seit seiner formellen Einführung im Jahr 1982 im Laufe der Zeit weiterentwickelt. Nachfolgend ein kurzer Überblick über die vergangenen Ereignisse aus historischer Sicht.

**1982:** Autodesk lizenzierte das DWG-Dateiformat, das 1970 von Mike Riddle entwickelt wurde, als Grundlage für AutoCAD.

**1998:** Mit der Veröffentlichung von AutoCAD R14.01 fügte Autodesk die Dateiüberprüfung durch eine Funktion namens DWGCHECK hinzu, die eine verschlüsselte Prüfsumme und einen Produktcode, von Autodesk WaterMark genannt, in die vom Programm erstellten DWG-Dateien einbettete.

**2006:** Autodesk hat AutoCAD 2007 modifiziert, um die „TrustedDWG-Technologie“ zum Einbetten der Textzeichenfolge „Autodesk DWG. Diese Datei ist eine vertrauenswürdige DWG, die zuletzt von einer Autodesk-Anwendung oder einer von Autodesk lizenzierten Anwendung gespeichert wurde“ in die DWG-Dateien einzufügen. Der Zweck war, Benutzern von Autodesk-Software dabei zu helfen, sicherzustellen, dass diese Dateien von einer Autodesk- oder RealDWG-Anwendung erstellt wurden, was definitiv dazu beitragen sollte, das Risiko von Inkompatibilitäten zu verringern.

## Dateistruktur ##

DWG ist eines der weit verbreiteten Dateiformate von einer Reihe von Anwendungen und hat eine robuste Dateistruktur. Da es sich bei DWG um ein binäres Dateiformat handelt, ist es nicht menschenlesbar wie das reine ASCII-Dateiformat [DXF](/de/cad/dxf/). DWG-Dateien enthalten normalerweise Informationen zu den Bildkoordinaten und allen damit verbundenen Metadaten. Vollständige [Spezifikationen](https://www.opendesign.com/files/guestdownloads/OpenDesign_Specification_for_.dwg_files.pdf) des DWG-Dateiformats stehen zum Download von OpenDesign zur Verfügung. Die Dateistruktur des DWG-Dateiformats wird wie folgt zusammengefasst.

**Header**: Der Dateiheader besteht aus DWG-Header-Variablen und Informationen über Cyclic Redundancy Check (CRC), die zur Fehlererkennung verwendet werden. Jeder Unterabschnitt ist ein spezialisierter Vektor, in dem unterschiedliche Bitlängen verwendet werden, um unterschiedliche Labels darzustellen. Beispielsweise stehen die ersten 6 Bits der DWG-Header-Variablen für den Versionsstring.

**Klassendefinitionen:** Eine DWG-Datei kann je nach Zweck der DWG-Datei zahlreiche Klassen enthalten. Informationen wie Klassenmetadaten, Größe des Klassendatenbereichs, Klassennummer und Prüfsumme sowie andere.

**Vorlage**: Dies ist optional und für R15- und R15-Versionen befindet sich dieser Abschnitt unterhalb des Abschnitts „Objektfreier Speicherplatz“.

**Padding**: Die Metadaten werden mit einer bestimmten Anzahl von Bytes angehängt und nachgestellt, wodurch die älteren AutoCAD-Softwareversionen aufwärtskompatibel mit dem neuen DWG-Dateiformat sind.

**Bilddaten**: Die Metadaten für diesen Abschnitt hängen vom jeweiligen .dwg-Typ ab. Für Benutzer von R14 und R15 ist dieser Abschnitt optional.

**Objektdaten**: Die Objektdaten bestehen aus einer vollständigen Liste von Tabellenentitäten, Wörterbucheinträgen usw., die der bestehenden Liste von Objekten entsprechen.

**Objektkarte**: Die Position jedes Objekts in der Datei wird in diesem Abschnitt der Datei angegeben. Die meisten Metadaten in diesem Abschnitt sind Dateihandles, die bei der Identifizierung und erneuten Wiedergabe des Objekts eine Rolle spielen.

**Objektfreier Speicherplatz**: Dieser Abschnitt ist für alle Benutzer optional

**Zweiter Header**: Ein Duplikat des Dateiheaderabschnitts gegen Ende der DWG-Datei

## Verweise ##

* [DWG-Dateiformatspezifikationen](https://www.opendesign.com/files/guestdownloads/OpenDesign_Specification_for_.dwg_files.pdf)
* [Die DWG-Dateispezifikation](https://www.scan2cad.com/dwg/file-spec/)
* [DWG - Von Wikipedia](https://en.wikipedia.org/wiki/.dwg)

