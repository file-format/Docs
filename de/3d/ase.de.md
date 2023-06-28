{
  "date" : "2021-01-22",
  "keywords" :[ "ASE","Datei", "Format", "Dateityp", "Erweiterung","Was ist eine ASE-Datei?" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Erfahren Sie mehr über das ASE-Dateiformat und APIs, die ASE-Dateien öffnen und erstellen können.",
  "title" :"ASE - Autodesk ASCII-Szenen-Exportdatei",
  "linktitle" : "ASE",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-01-22"
}

## Was ist eine ASE-Datei?

Eine Datei mit der Erweiterung .ase ist ein Autodesk-ASCII-Szenenexport-Dateiformat, das eine ASCII-Darstellung einer Szene ist, die 2D- oder 3D-Informationen enthält, während Szenendaten mit Autodesk exportiert werden. Autodesk bietet Optionen zum Einbeziehen von Szenenkomponenten beim Exportieren von Szenendaten. Sie können die Mesh-Definition zusammen mit Eckpunkt- und Flächeninformationen, Materialbeschreibung, Transformationsanimationsdaten für die Objekte, vollständige Mesh-Definition aller n Frames, Animationsdaten für Kameras und Lichter und IK-Gelenkeinstellungen einbeziehen.

## ASE-Dateiformat – Weitere Informationen

ASE-Dateien sind im ASCII-Format gespeicherte Textdateien, die in jedem Texteditor geöffnet werden können. Eine ASE-Datei kann die folgenden Arten von Informationen enthalten, die von Autodesk bereitgestellt werden.

### Ausgabeoptionen

* „Netzdefinition“ – Exportiert die Definition jedes Netzes, einschließlich Vertex- und Flächeninformationen für geometrische Objekte. Darüber hinaus werden durch Aktivieren dieser Option die Elemente im Gruppenfeld Mesh-Optionen aktiviert, die unten beschrieben werden.
* „Materialien“ – Enthält die Materialbeschreibung. Wenn einem Objekt kein Material zugewiesen ist, wird seine Drahtgitterfarbe exportiert. Alle Ebenen eines Materialbaums sind enthalten, daher kann dies viel Text erzeugen.
* `Transform Animation Keys` - Beinhaltet die Transformationsanimationsdaten für die Objekte. Wenn das Objekt eine Zielkamera oder ein Scheinwerfer ist, enthält dies Zielanimationsdaten.
* `Animated Mesh` - Exportiert eine vollständige Mesh-Definition aller n Frames. Die Frequenz wird durch das unten beschriebene Zahlenauswahlfeld „Controller-Ausgang“ angegeben. Jeder Block enthält dieselben Informationen, die im Gruppenfeld Netzoptionen angegeben sind, wie unten beschrieben. Wenn Sie dies aktivieren, kann dies selbst bei kleinen Szenen zu einer riesigen Datei führen.
* „Animierte Kamera-/Lichteinstellungen“ – Exportiert die Animationsdaten für Kameras und Lichter, wie Farbe, Intensität, Falloff, Kartenverzerrung und so weiter. Gibt alle n Frames einen Block aus, wie im Zahlenauswahlfeld "Controller-Ausgabe" angegeben.
* `Inverse Kinematic Joints` - Exportiert die IK-Gelenkeinstellungen in den Hierarchiezweig.

### Objekttypen

Mit den Elementen hier können Sie angeben, welche Objektkategorie in die Ausgabe aufgenommen werden soll. Sie können geometrische Objekte, Formen, Kameras, Lichter und Hilfsobjekte einbeziehen.

* Geometrisch
* Formen
* Kameras
* Beleuchtung
* Helfer

### Mesh-Optionen

* `Mesh Normals` - Exportiert die Flächen- und Vertex-Normalen. Die Normale des Gesichts wird zuerst aufgelistet, gefolgt von den Normalen der drei Eckpunkte, die das Gesicht stützen. Das Einschalten führt zu einer viel größeren Datei.
* „Mapping Coordinates“ – Exportiert eine Liste von Mapping-Scheitelpunkten und -Flächen gemäß den im 3ds Max Software Development Kit beschriebenen TVert- und TVFace-Strukturen. Wenn ein Objekt Face-Mapping verwendet, wird eine Face-Map-Liste exportiert, die UVW-Koordinaten für jedes Gesicht enthält.
* `Scheitelpunktfarben` - Exportiert Scheitelpunktfarben.

### Controller-Ausgang

* `Use Keys` - Exportiert Schlüsselwerte. Wenn der Controller keine Schlüssel verwendet, wird die Force-Sample-Methode verwendet. Bei Transformations-Controllern funktioniert die Option Keys verwenden nur, wenn alle Transformations-Controller entweder Linear/TCB oder Bezier sind. Wenn eine der Transformationsspuren einen anderen Controllertyp verwendet, wird die Force-Sample-Methode für alle Transformationsspuren verwendet.
* `Force Samples` - Samplet Controller-Werte basierend auf der Frequenz, die im Frames per Sample Controller angegeben ist.

## Verweise

* [Autodesk – Exportieren in ASCII](https://help.autodesk.com/view/3DSMAX/2020/ENU/?guid=GUID-98B2388D-A3A7-4096-8E81-888A3F9D6069)

