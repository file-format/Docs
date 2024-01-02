{
"Datum": "15.05.2023",
  "keywords": [
"csx-Datei",
"Was ist eine CSX-Datei",
"Was enthält die CSX-Datei",
"Was ist das Format der CSX-Datei?",
"Datei",
"csx-Dateierweiterung",
"Verlängerung"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "CSX-Dateiformat – Visual C#-Skript",
  "description":"Erfahren Sie mehr über das CSX-Format und APIs, mit denen CSX-Dateien erstellt und geöffnet werden können.",
"linktitle": "CSX",
  "menu": {
    "docs": {
      "identifier": "programming-csx",
"parent": "Programmierung"
}
},
"lastmod": "2023-05-15"
}

## Was ist eine CSX-Datei?

Visual C# Script (auch bekannt als CSX) ist ein Dateiformat, das von der Roslyn-Skript-Engine im .NET-Ökosystem von Microsoft verwendet wird. CSX-Dateien enthalten C#-Code, der direkt ausgeführt werden kann, ohne dass ein separater Kompilierungsschritt erforderlich ist.

Das CSX-Format ist spezifisch für das Microsoft-Ökosystem und kein weit verbreitetes Dateiformat in der allgemeinen Programmierung. CSX-Dateien werden häufig in Szenarien verwendet, in denen schnelle Prototyping- oder Skriptfunktionen erforderlich sind. Sie ermöglichen Ihnen das Erstellen und Ausführen von C#-Programmen auf einfachere Weise als beim Erstellen einer vollwertigen kompilierten Anwendung.

Zum Ausführen von CSX-Dateien können Sie Tools wie .NET Interactive Notebooks verwenden, die eine interaktive Umgebung zum Ausführen von C#-Code bereitstellen. Visual Studio Code mit der C#-Erweiterung und .NET Core SDK kann auch zum Arbeiten mit CSX-Dateien verwendet werden.

## Was enthält die CSX-Datei?

Eine CSX-Datei (C#-Skript) enthält C#-Code, der direkt ausgeführt werden kann. Es kann jeden gültigen C#-Code wie Variablendeklarationen, Funktionen, Klassen und andere Programmierkonstrukte enthalten.

Hier ist ein Beispiel dafür, was eine CSX-Datei enthalten könnte:

```
using System;

// Define a class
public class MyClass
{
    public void Greet(string name)
    {
        Console.WriteLine("Hello, " + name + "!");
}
}

// Create an instance of the class and call a method
var myObject = new MyClass();
myObject.Greet("John");

```

CSX-Dateien können auch Importanweisungen, externe Bibliotheksverweise und andere C#-Sprachfunktionen enthalten, um die Funktionalität des Codes zu unterstützen. Der Code wird im laufenden Betrieb interpretiert und ausgeführt, ohne dass eine Kompilierung erforderlich ist, wodurch er sich für Skripterstellung und schnelle Prototyping-Aufgaben eignet.

## Was ist das Format der CSX-Datei?

Das CSX-Format (C#-Skript) folgt einem einfachen textbasierten Format. Normalerweise hat es die Dateierweiterung .csx, um es von regulären C#-Quellcodedateien (.cs) zu unterscheiden.

CSX-Dateien können mit jedem Texteditor oder jeder integrierten Entwicklungsumgebung (IDE) bearbeitet werden, die C#-Syntaxhervorhebung unterstützt. Sobald die CSX-Datei fertig ist, kann sie mit Tools wie .NET Interactive Notebooks, der .NET Core-Befehlszeilenschnittstelle (CLI) oder einer IDE mit C#-Skriptunterstützung ausgeführt werden.

## Verweise
* [C#-Programmierung mit Visual Studio Code](https://code.visualstudio.com/docs/languages/csharp)

