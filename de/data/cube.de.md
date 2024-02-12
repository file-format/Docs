{
  "date" : "2024-01-25",
  "author" : {
    "display_name" : "Shakeel Faiz"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "CUBE-Datei – Gaußsche Cube-Datei – Was ist eine .cube-Datei und wie öffnet man sie?",
  "description" : "Erfahren Sie mehr über die Gaussian Cube-Datei und wie Sie sie öffnen.",
  "linktitle" : "CUBE",
  "menu" : {
    "docs" : {
      "identifier" : "data-de-cube",
      "parent" : "data"
    }
  },
  "lastmod" : "2024-01-25"
}

## Was ist eine CUBE-Datei?

Das CUBE-Dateiformat, auch bekannt als Gaussian Cube-Datei (.cube), wird in der Computerchemie zum Speichern molekularer Daten verwendet, insbesondere von Informationen zur Elektronendichte, die aus quantenchemischen Berechnungen resultieren. Dieses Format wird üblicherweise mit dem **Gaußschen Softwarepaket** in Verbindung gebracht, das häufig für die Durchführung von Ab-initio-Berechnungen der elektronischen Struktur verwendet wird.

Gaußsche Würfeldateien speichern dreidimensionale Daten, die typischerweise die Elektronendichte oder andere Eigenschaften von Molekülen darstellen und durch quantenchemische Berechnungen gewonnen werden. Die Datei enthält einen Kopfabschnitt mit Metadaten (z. B. Ursprung, Anzahl der Datenpunkte entlang jeder Achse und Abstand), gefolgt von einem Raster mit numerischen Werten, die die interessierende Eigenschaft (z. B. Elektronendichte) an jedem Rasterpunkt im Raum darstellen.

Die Gaussian-Cube-Datei (.cube) ist eine Nur-Text-Datei mit spezifischer Struktur. Der Header enthält Informationen über das molekulare System und das Datengitter, und die Datenwerte sind im dreidimensionalen Gitterformat angeordnet. Gaußsche Würfeldateien werden häufig zur Visualisierung molekularer Eigenschaften mithilfe molekularer Visualisierungssoftware verwendet. Programme wie **VMD (Visual Molecular Dynamics)** oder **PyMOL** können Gaußsche Würfeldateien lesen, um molekulare Oberflächen, Elektronendichte oder andere berechnete Eigenschaften anzuzeigen.

## Vereinfachtes Beispiel einer Gaussian-Cube-Datei:

„
Cubefile-Beispiel
Erzeugt von Gauß
   0 1 0 0 0 0 0 0 0 0
   0,0000000000000000E+00 0,0000000000000000E+00 0,0000000000000000E+00
  50 0,1000000000000000E+01 0,0000000000000000E+00 0,0000000000000000E+00
  50 0,0000000000000000E+00 0,1000000000000000E+01 0,0000000000000000E+00
  50 0,0000000000000000E+00 0,0000000000000000E+00 0,1000000000000000E+01
    0,123456789E+02 0,123456789E+02 0,123456789E+02 0,123456789E+02 0,123456789E+02
    ... (Datenwerte für die Elektronendichte an jedem Gitterpunkt)
„

## Über Gauß

Gaussian ist eine Suite von Softwareanwendungen für Quantenchemie und Computerchemie. Der Hauptschwerpunkt von Gaussian liegt auf Ab-initio-Methoden der Quantenchemie, bei denen es sich um hochpräzise, aber rechenintensive Ansätze zur Untersuchung der elektronischen Struktur von Molekülen handelt. Die Software wird in der Forschung und im akademischen Umfeld häufig für verschiedene Anwendungen eingesetzt, darunter die Vorhersage molekularer Eigenschaften, die Untersuchung von Reaktionsmechanismen und die Erforschung molekularer Strukturen.

## Über NWChem

NWChem ist eine Open-Source-Software für computergestützte Chemie, die für Hochleistungssimulationen der Quantenchemie entwickelt wurde. Es verwendet Ab-initio-Methoden wie Hartree-Fock und Dichtefunktionaltheorie, unterstützt paralleles Rechnen für effiziente Berechnungen auf Clustern und findet Anwendungen in verschiedenen wissenschaftlichen Bereichen, einschließlich Computerchemie, Biochemie und Materialwissenschaften. NWChem ist bekannt für seine Vielseitigkeit, die es Forschern ermöglicht, verschiedene chemische Systeme zu untersuchen, und sein Open-Source-Charakter fördert Community-Beiträge und Anpassungsmöglichkeiten.

## Über VMD

VMD, das für Visual Molecular Dynamics steht, ist ein leistungsstarkes und weit verbreitetes Programm zur molekularen Visualisierung zum Anzeigen, Analysieren und Animieren von Trajektorien der Molekulardynamik (MD) sowie statischen Molekülstrukturen. Besonders beliebt ist es in den Bereichen Computerchemie, Molekularbiologie und strukturelle Bioinformatik. VMD zeichnet sich durch die Visualisierung molekularer Strukturen aus und liefert hochwertige 3D-Renderings von Molekülen und Molekülkomplexen. Es unterstützt verschiedene molekulare Dateiformate.

## Über PyMOL

PyMOL ist ein molekulares Visualisierungssystem und Softwaretool zur dreidimensionalen Visualisierung molekularer Strukturen. Besonders beliebt ist es in den Bereichen Strukturbiologie, Bioinformatik und Computerchemie. PyMOL bietet hochwertige 3D-Renderings molekularer Strukturen und ermöglicht es Benutzern, Formen, Oberflächen und Wechselwirkungen biologischer Makromoleküle zu visualisieren und zu erkunden.

## Wie öffne ich eine CUBE-Datei?

Die CUBE-Datei kann mit den folgenden Programmen geöffnet und referenziert werden.

- **NWChem** (Kostenlos) für (Windows, MAC, Linux)

## Verweise
* [Gaußsches Würfeldateiformat](https://paulbourke.net/dataformats/cube/)
