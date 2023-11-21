{
"Datum": "2023-10-11",
   "keywords":[
"mtl",
"mtl-Datei",
"mtl obj Materialvorlagen-Bibliotheksdatei",
"Wie öffnet man eine MTL-Datei",
"Datei",
"mtl-Dateierweiterung",
"Verlängerung",
"Datei"
],
   "author":{
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc":true,
"title": "MTL-Dateiformat – OBJ-Materialvorlagen-Bibliotheksdatei",
   "description":"Erfahren Sie mehr über das Dateiformat der MTL OBJ Material Template Library und die APIs, mit denen MTL-Dateien erstellt und geöffnet werden können.",
"linktitle": "MTL",
   "menu":{
      "docs":{
         "identifier":"3d-mtl",
"parent": "3d"
}
},
"lastmod": "2023-10-11"
}

## Was ist eine MTL-Datei?

Die MTL-Datei, kurz für **Material Template Library**, ist ein Begleitdateiformat, das in der 3D-Computergrafik und -Modellierung verwendet wird. Es wird häufig mit dem **Wavefront OBJ-Dateiformat** in Verbindung gebracht, einem gängigen Format zum Speichern von 3D-Modellen und den zugehörigen Materialien und Texturen.

## Materialvorlagenbibliothek

Hier finden Sie wichtige Informationen zu MTL-Dateien:

1. **Materialdefinitionen**: Die Datei ".mtl" enthält Definitionen für Materialien, die auf 3D-Objekte in der entsprechenden OBJ-Datei angewendet werden. Jede Materialdefinition spezifiziert verschiedene Eigenschaften wie Farbe, Glanz, Transparenz und Texturkarten.
    





2. **Textbasiertes Format**: ".mtl"-Dateien sind normalerweise reine Textdateien, was bedeutet, dass sie leicht mit einem Texteditor bearbeitet werden können. Jede Materialdefinition besteht aus einer Reihe von Anweisungen, und diese Anweisungen definieren die Materialattribute.
    





3. **Texturzuordnung**: Eine der wesentlichen Funktionen einer ".mtl"-Datei besteht darin, zu definieren, wie Texturen (Bilddateien) auf die Oberflächen des 3D-Modells abgebildet werden. Es gibt den Pfad der Texturdatei an und wie sie umhüllt oder auf das Modell angewendet werden soll.
    





4. **Beispielhafte MTL-Anweisungen**: Hier sind einige Beispielanweisungen, die Sie möglicherweise in einer ".mtl"-Datei finden:
    





- "newmtl MaterialName": Dies definiert neues Material mit dem Namen "MaterialName".
- "Ka rgb": Umgebungsfarbe des Materials, angegeben in RGB-Werten.
- "Kd rgb": Streufarbe des Materials, angegeben in RGB-Werten.
- "Ks rgb": Spiegelfarbe des Materials, angegeben in RGB-Werten.
- "Ns-Wert": Glanz oder Spiegelexponent des Materials.
- "map_Kd texturefile.jpg": Gibt die diffuse Texturkarte für das Material an.
5. **Mehrere Materialien**: Eine OBJ-Datei kann auf mehrere Materialien verweisen und jedes Material ist in der ".mtl"-Datei definiert. Dies ermöglicht komplexe 3D-Modelle mit unterschiedlichen Materialien, die auf verschiedene Teile aufgetragen werden.
    





6. **Kompatibilität**: ".mtl"-Dateien werden von 3D-Modellierungssoftware und Rendering-Engines weitgehend unterstützt und ermöglichen die Übertragung von 3D-Modellen und ihren Materialien zwischen verschiedenen Softwareanwendungen.

## Wie öffne ich eine MTL-Datei?

MTL-Dateien sind textbasierte Dateien und können daher mit jedem Texteditor geöffnet werden

- Notizblock (Windows)
- Notepad++ (Windows)
- Visual Studio-Code
- Erhabener Text
- Atom
- TextEdit (macOS)

Zu den Programmen, die MTL-Dateien öffnen oder darauf verweisen, gehören:

- Adobe Photoshop 2023
- Autodesk Maya 2023
- MeshLab
- Cheetah3D

**SubType:** 3D-Bilddateien

## Verweise
* [Wavefront .obj-Datei](https://en.wikipedia.org/wiki/Wavefront_.obj_file)

