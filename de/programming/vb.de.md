{
  "date" : "2019-10-11",
  "keywords" :[ "vb", "file", "extension", "file format", "Visual Basic", "Programming Guide" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VB - Visual Basic-Codedatei",
  "description":"Erfahren Sie mehr über das VB-Dateiformat und APIs, die VB-Dateien erstellen und öffnen können.",
  "linktitle" : "VB",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## Was ist eine VB-Datei?

Eine VB-Datei ist eine in Visual Basic-Sprache erstellte Quellcodedatei, die von Microsoft für die Entwicklung von .NET-Anwendungen erstellt wurde. Eine andere ähnliche Sprache mit anderer Syntax ist C#, dessen Dateien mit der Dateierweiterung [.CS](/de/programming/cs/) gespeichert werden. Das Dateiformat stellt die Low-Level-Programmiersprache zum Schreiben von Code bereit, der kompiliert wird, um die endgültige Ausgabedatei in Form einer EXE- oder DLL-Datei zu generieren. Diese können mit Microsoft Visual Studio erstellt und kompiliert werden. Microsoft Visual Studio Express kann auch verwendet werden, um solche Dateien zu erstellen und zu aktualisieren, was eine kostenlose IDE ist. Ein einfaches Visual Studio-Projekt [solution](/de/programming/sln/), das mit der VB-Sprache erstellt wurde, kann aus einer oder mehreren solcher Dateien bestehen. Dateien, die für die Aufnahme in die Kompilierung markiert sind, werden in der Datei [CSPROJ](/de/programming/csproj/) aufgelistet, die Teil des Projekts ist und den Compiler anweist, die markierten Dateien zu verwenden.

## VB-Dateiformat – Weitere Informationen

VB-Dateien sind textbasierte Dateiformate, die in jedem Texteditor zur Bearbeitung geöffnet werden können. Wenn er jedoch in einer unterstützten IDE mit korrekter Syntaxhervorhebung geöffnet wird, ist der Code einfach zu lesen und anzuordnen. Eine einfache VB-Datei enthält:

* Namespaces-Deklaration - Zum Verweisen auf eine bestimmte Funktionalität, die durch diesen bestimmten Namespace definiert ist
* Variablendeklaration - Um Variablen auf Klassenebene für die jeweilige Implementierung zu deklarieren
* Methodendeklaration - Um die Methodendeklaration für die jeweilige Funktionalität zu deklarieren

## Beispiel für ein VB-Dateiformat

```
Imports System
Module Module1
   'This program will display Hello World
   Sub Main()
      Console.WriteLine("Hello World")
      Console.ReadKey()
   End Sub
End Module
```



