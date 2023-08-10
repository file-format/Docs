{
  "date" : "2019-10-11",
  "keywords" :[ ".mel", "Maya Embedded language", "file", "extension", "file format", "Maya 3D", "Programming Guide" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MEL - Maya Embedded Language-Dateiformat",
  "description":"Erfahren Sie mehr über das MEL-Dateiformat und APIs, die MEL-Dateien erstellen und öffnen können.",
  "linktitle" : "MEL",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-03-08"
}

## Was ist eine MEL-Datei?

Eine Datei mit der Erweiterung .mel (Maya Embedded Language) ist eine Skriptsprache, die von Autodesk Maya zum Erstellen grafischer Oberflächen verwendet wird. Damit können Sie die Erstellung grafischer Elemente automatisieren, indem Sie zusätzlich zur grafischen Benutzeroberfläche von Maya ausführbare Skripte verwenden. Mit MEL können Sie grafische Schnittstellen erstellen, ohne Programmierkenntnisse zu erwerben. Dies wird erreicht, indem Makros und benutzerdefinierte Aktionen erstellt werden, die sich wiederholende Aufgaben beschleunigen. Mit diesen Prozeduren und Skripten können Sie benutzerdefinierte Modellierung, Animationen, Dynamik und Task-Rendering erstellen. Autodesk Maya 2020 kann zum Öffnen und Anzeigen des Inhalts einer EML-Datei verwendet werden.

## MEL-Dateiformat – Weitere Informationen

Ein [Referenzhandbuch](https://download.autodesk.com/us/maya/2009help/index.html?url=Glossary_M_.mb_file_format.htm,topicNumber=d0e193865) für Programmierer ist für Entwickler im Dokumentationsbereich von Maya verfügbar. MEL basiert auf Shell-Scripting-Befehlen, ähnlich wie UINX, um Dinge zu erreichen. Die auf Skripten basierenden Befehle machen es für konventionelle und objektorientierte Programmierung (OOP) irrelevant, was dazu führt, dass keine Datenstrukturen verwendet, Funktionen aufgerufen oder OOP wie in anderen Sprachen verwendet werden.

Einige wichtige Punkte zu MEL sind wie folgt.

`Kommentare` - Jede Anweisung in MEL muss mit einem Semikolon (;) enden, auch am Ende eines Blocks.

`Returning Values` - Wenn Sie einen Ausdruck angeben, der einen Wert zurückgibt, wird der Wert nicht automatisch in MEL gedruckt. Stattdessen verursacht es einen Fehler.
```
3 + 5;
// Error: 3 + 5; //
// Error: Syntax error //
print(3+5);
8
```
`Befehle zum Erstellen, Bearbeiten und Löschen` - Derselbe Befehl wird verwendet, um Dinge zu erstellen, Dinge zu bearbeiten oder Informationen über vorhandene Dinge abzufragen. Ein Flag steuert jedoch, was (erstellen, bearbeiten oder abfragen) der Befehl tut.

```
// Create a sphere named "mySphere" with radius 5
sphere -radius 5 -name "mySphere";
// Edit the radius of mySphere
sphere -edit -radius "mySphere";
// Print the radius of mySphere
sphere -query -radius

```
„Rückgabewert von Funktion“ – Die Funktionssyntax gibt automatisch einen Wert zurück. Um einen Rückgabewert mithilfe der Befehlssyntax zu erhalten, müssen Sie den Befehl in Backquotes einschließen.

```
$a = getAttr("mySphere.translateX"); // Function syntax
$b = `getAttr mySphere.translateY`; // Command syntax
```

## Verweise

* [MEL](https://download.autodesk.com/us/maya/2009help/index.html?url=Glossary_M_.mb_file_format.htm,topicNumber=d0e193865)

