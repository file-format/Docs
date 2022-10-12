{
  "date" : "2019-10-11",
  "keywords" :[ "cs", "Datei", "Erweiterung", "Dateiformat", "CSharp", "Programmiersprache" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CS - CSharp-Codedatei",
  "description":"Erfahren Sie mehr über das CS-Dateiformat und APIs, die CS-Dateien erstellen und öffnen können.",
  "linktitle" :"KS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## Was ist eine CS-Datei?

Dateien mit der Erweiterung .cs sind Quellcodedateien für die Programmiersprache C#. Das Dateiformat wurde von Microsoft zur Verwendung mit .NET Framework eingeführt und stellt die Low-Level-Programmiersprache zum Schreiben von Code bereit, der kompiliert wird, um die endgültige Ausgabedatei in Form einer EXE- oder DLL-Datei zu generieren. Diese können mit Microsoft Visual Studio erstellt und kompiliert werden. Microsoft Visual Studio Express kann auch verwendet werden, um solche Dateien zu erstellen und zu aktualisieren, was eine kostenlose IDE ist. CS-Dateien werden für die Anwendungsentwicklung verwendet, die von einfachen Desktop-Anwendungen bis hin zu komplexeren Programmen reichen kann. Ein einfaches Visual Studio-Projekt [solution](/de/programming/sln/), das mit der Sprache C# erstellt wurde, kann aus einer oder mehreren solcher Dateien bestehen. Dateien, die für die Aufnahme in die Kompilierung markiert sind, werden in der Datei [CSPROJ](/de/programming/csproj/) aufgelistet, die Teil des Projekts ist und den Compiler anweist, die markierten Dateien zu verwenden.

## CS-Dateiformat ##

CS-Dateien sind textbasierte Dateiformate, die in jedem Texteditor zur Bearbeitung geöffnet werden können. Wenn er jedoch in einer unterstützten IDE mit korrekter Syntaxhervorhebung geöffnet wird, ist der Code einfach zu lesen und anzuordnen. Eine einfache CS-Datei enthält:

* Namespaces-Deklaration - Zum Verweisen auf eine bestimmte Funktionalität, die durch diesen bestimmten Namespace definiert ist
* Variablendeklaration - Um Variablen auf Klassenebene für die jeweilige Implementierung zu deklarieren
* Methodendeklaration - Um die Methodendeklaration für die jeweilige Funktionalität zu deklarieren

### Syntax ###

* Semikolons werden verwendet, um das Ende einer Anweisung zu kennzeichnen.
* Geschweifte Klammern werden verwendet, um Anweisungen zu gruppieren. Anweisungen werden üblicherweise in Methoden (Funktionen), Methoden in Klassen und Klassen in Namespaces gruppiert.
* Variablen werden mit einem Gleichheitszeichen zugewiesen, aber mit zwei aufeinanderfolgenden Gleichheitszeichen verglichen.
* Eckige Klammern werden bei Arrays verwendet, sowohl um sie zu deklarieren als auch um einen Wert an einem bestimmten Index in einem von ihnen zu erhalten.

### Beispiel ###

```
using System;

class Program
{
    static void Main()
    {
        Console.WriteLine("Hello, world!");
}
}
```

