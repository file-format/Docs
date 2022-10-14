{
  "date" : "2019-10-11",
  "keywords" :[ "c++", "Datei", "Erweiterung", "Dateiformat", "C++", "Programmiersprache" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CPP - C++-Quellcodedatei",
  "description":"Erfahren Sie mehr über das CPP-Dateiformat und APIs, die CPP-Dateien erstellen und öffnen können.",
  "linktitle" :"CPP",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## Was ist eine C++-Datei?

Dateien mit der CPP-Dateierweiterung sind Quellcodedateien für Anwendungen, die in der Programmiersprache C++ geschrieben sind. Ein einzelnes C++-Projekt kann mehr als eine CPP-Datei als Anwendungsquellcode enthalten. Ein solches Projekt besteht aus verschiedenen Dateitypen, von denen die CPP-Dateien als Implementierungsdateien bekannt sind, da sie alle Definitionen der in der Header-Datei (.h) deklarierten Methoden enthalten. Das C++-Projekt als Ganzes ergibt eine ausführbare Anwendung, wenn es als Ganzes kompiliert wird.

## CPP-Dateistruktur

Eine CPP-Dateistruktur ist im Vergleich zu den Header-Dateien einfach. Der Hauptzweck einer solchen Implementierungsdatei besteht darin, die Schnittstelle von der Implementierung zu trennen. Dies führt zu Deklarationen aller Mitgliedsfunktionen in einer Header-Datei und ihren Details in der CPP-Datei. Eine CPP-Implementierungsdatei kann als einfache Datei zum Schreiben einer Anwendung oder als Klassenimplementierung verwendet werden.

### Unabhängige Implementierung

Eine CPP-Datei kann bei Verwendung als unabhängige Anwendung alle darin enthaltenen Implementierungen enthalten, ohne dass eine Methodendeklaration in der Header-Datei erforderlich ist. Eine solche Implementierung besteht aus allen Methoden, die in der Implementierungsdatei definiert sind, wobei der Eintrag der Anwendung durch eine Hauptmethode geregelt wird, die optionale Benutzereingaben als Argumente akzeptiert. Es kann auch beliebige Bibliotheken aus der C++-Standardbibliothek enthalten, die von allen deklarierten Methoden in der Datei verwendet werden sollen.

```
/*
* File: main.cpp
* Author: SomeOne
* Created on November 16, 2018, 4:09 PM
*/

#include <iostream>
using namespace std;

int main()
{
   cout<<"About the CPP file format";
   cout<<std::endl<<"and its very easy";
}
```

### Klassenimplementierung

Bei der objektorientierten Programmierung (OOP) wird eine CPP-Datei als Klassendefinition verwendet. In diesem Fall werden alle Klassendatenmember und Memberfunktionen innerhalb der Header-Datei deklariert. Jede Header-Datei kann wiederum auch auf Standard-Bibliotheksmethoden verweisen. Die Klassendefinitions-CPP-Datei verweist auf die Header-Datei in einer Include-Anweisung am Anfang der Datei. Meistens fügen Softwareentwickler am Anfang einer solchen Klassenimplementierungsdatei Kommentare ein, die Auskunft über den tatsächlichen Inhalt der Datei, Angaben zum Autor und das Implementierungsdatum geben. In solchen Fällen müssen die Header-Implementierungsdateien denselben Namen haben. Ein Beispiel für eine solche Header- und Implementierungsdatei ist wie folgt.

### Header-Datei

```
#include <string>
#include <iostream>

using namespace std;

class MyClass {
public:
   MyClass();     // Constructor
   void add(int i, int j);

private:
   std::string name;
};
```

### CPP-Implementierungsdatei

```
#include "MyClass.h"

MyClass::MyClass(){
   ...
}
void MyClass::add(int i, int j) {
   int result # i + j;
}
```

## Verweise

* [Klassenimplementierung – von Wikipedia](https://en.wikipedia.org/wiki/Class_implementation_file)

