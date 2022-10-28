{
  "date" : "2019-10-11",
"Schlüsselwörter": [ "M-Datei", "M", "Erweiterung", "Format", "M-Dateiformat" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"M - Matlab-Quellcodedatei",
  "description":"Erfahren Sie mehr über Matlab .m-Quellcodedateien und APIs, die MF-Dateien erstellen und öffnen können.",
  "linktitle" : "M",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

# M - Matlab-Quellcodedateien

## Was ist eine M (Matlab)-Datei?

Eine Datei mit der Erweiterung .m ist eine Quellcodedatei, die von Matlab verwendet wird, einer Programmier- und numerischen Berechnungsplattform, die für Analysen, Algorithmenentwicklung und Simulationsmodellierung verwendet wird. Wie andere Programmierdateiformate enthält eine M-Datei Quellcode, der Matlab-Befehle ausführt, um Diagramme zu zeichnen, Simulationen auszuführen und andere mathematische Operationen auszuführen. Eine einzelne Matlab-Simulation kann sich über mehrere solcher .m-Dateien erstrecken, die die Anwendung in Skripte, Klassen, Funktionen oder Deklarationen klassifizieren können. Matlab M-Dateien können mit jedem Texteditor geöffnet werden.

## Matlab M-Dateiformat - Weitere Informationen

Matlab .m-Dateien sind Textdateien, die Programmiercode in der Programmiersprache Matlab enthalten. Diese können in jedem Texteditor geöffnet und bearbeitet und wieder gespeichert werden, um in der Matlab-Software ausgeführt zu werden. Matlab selbst enthält einen Live-Editor, der zum Erstellen von Skripten verwendet wird, die eine Kombination aus Code, Ausgabe und formatiertem Text sind.

### Matlab-Funktionsdateien

Wie andere Programmiersprachen können Sie eine .m-Datei erstellen, die nur die Definition einer Funktion enthält, die nur eine bestimmte Aufgabe ausführt. Solche Dateien werden auch mit der Erweiterung .m gespeichert und implementieren nur die Funktionalität, die sich auf diese Funktion bezieht.

### Beispiel für eine .M-Datei

Das Folgende ist ein Beispiel für eine Matlab-Funktionsdatei, die die Zeit berechnet, die für ein aus der Höhe h fallen gelassenes Objekt benötigt wird.

```C++
function t= TimeToGround(h)  
  t=sqrt(h/4.9);
end
```

Um diese Funktion aus dem Matlab-Editor oder aus einer anderen .m-Datei aufzurufen, kann der folgende Code verwendet werden.
```C++
TimeToGround(100)
```

## Verweise

* [Matlab - Unterstützte Dateiformate](https://www.mathworks.com/help/matlab/standard-file-formats.html)
* [Mit Matlab] (https://www.maths.unsw.edu.au/sites/default/files/MatlabSelfPaced/lesson0/MatlabLesson0_Mfiles.html)

# M - Objective-C-Implementierungsdatei

## Was ist eine M (Objective-C)-Datei?

Eine M-Datei wird auch als Implementierungsdatei bezeichnet, die den Quellcode einer Klasse enthält, die in der Sprache Objective-C geschrieben ist, einer Programmiersprache, die zum Schreiben von Softwareanwendungen für OS X und iOS verwendet wird. Objective-C ist die wichtigste Programmiersprache, die von den wichtigsten APIs von Apple, Cocoa und Cocoa Touch, für diese Plattformen verwendet wird. Eine einzelne Softwareanwendung, die in dieser Sprache entwickelt wurde, kann mehrere .m-Dateien enthalten, die die Implementierung der Programmklassen enthalten. Diese können mit Apple XCode, jEdit und anderen gängigen Texteditoren geöffnet werden.

## Objective-C M-Dateiformat – Weitere Informationen

Die M-Dateien werden im Klartextformat unter Verwendung der Programmiersyntax von Objective-C geschrieben. Jede Methode einer Klasse muss mit ihrem gesamten notwendigen Code in diesen Implementierungsdateien definiert werden. Diese Implementierungs-M-Dateien können je nach Bedarf eine oder mehrere .h-Header-Dateien importieren. Die import-Anweisung teilt dem Compiler mit, wo er die zu dieser Implementierungsdatei gehörende Header-Datei finden kann. Die import-Anweisung wird wie folgt geschrieben.

```C++
#import "network.h"
```

Jede M-Dateiimplementierung beginnt dann mit der `@implementation`-Direktive, gefolgt vom Dateinamen der Implementierungsklasse. Danach folgen alle Methodenimplementierungen, die in der Header-Datei deklariert sind.

### Beispiel für ein M-Dateiformat

```C++
UrlConnection.m

#import "UrlConnection.h"

@implementation UrlConnection

(void)connect {
    // In here would be code to attempt a connection to the
    // specified URL, while possibly handling connection errors.
    //
}

 + (BOOL)canHandleRequest:(NSString \*)type
                   forUrl:(NSString \*)url {
    //And in here would be code to see if the given URL passed
    // in is capable of handling the HTTP request type specified
    // by the "type" parameter. It will return YES or NO.
 }

 @end
```

## Verweise
* [Über Objective C](https://developer.apple.com/library/archive/documentation/Cocoa/Conceptual/ProgrammingWithObjectiveC/Introduction/Introduction.html#//apple_ref/doc/uid/TP40011210-CH1-SW1)
* [Objekt-C-Anleitung](https://blog.teamtreehouse.com/beginners-guide-objective-c-classes-objects)

