{
  "date" : "2019-10-11",
  "keywords" :[ "c++", "bestand", "extensie", "bestandsformaat", "C++", "Programmeertaal"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CPP - C++ broncodebestand",
  "description":"Meer informatie over CPP-bestandsindeling en API's die CPP-bestanden kunnen maken en openen.",
  "linktitle" : "CPP",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## Wat is een C++-bestand?

Bestanden met de CPP-bestandsextensie zijn broncodebestanden voor toepassingen die zijn geschreven in de programmeertaal C++. Een enkel C++-project kan meer dan één CPP-bestand als toepassingsbroncode bevatten. Een dergelijk project bestaat uit verschillende bestandstypen, waarvan de CPP-bestanden bekend staan als implementatiebestanden omdat ze alle definities bevatten van de methoden die in het headerbestand (.h) zijn gedeclareerd. Het C++-project als geheel resulteert in een uitvoerbare toepassing wanneer het als geheel wordt gecompileerd.

## CPP-bestandsstructuur

Een CPP-bestandsstructuur is eenvoudig in vergelijking met de headerbestanden. Het belangrijkste doel van een dergelijk implementatiebestand is om de interface van de implementatie te splitsen. Dit resulteert in declaraties van alle lidfuncties in een headerbestand en hun details in het CPP-bestand. Een CPP-implementatiebestand kan worden gebruikt als een eenvoudig bestand voor het schrijven van een toepassing of als een klassenimplementatie.

### Onafhankelijke implementatie

Een CPP-bestand kan, wanneer het als een onafhankelijke applicatie wordt gebruikt, alle implementaties erin bevatten zonder de vereiste van de declaratie van methoden in het headerbestand. Een dergelijke implementatie bestaat uit alle methoden die zijn gedefinieerd in het implementatiebestand waarbij de invoer van de toepassing wordt bepaald door een hoofdmethode die optionele gebruikersinvoer als argumenten neemt. Het kan ook alle bibliotheken uit de C++ Standard Library bevatten die door alle gedeclareerde methoden in het bestand kunnen worden gebruikt.

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

### Class-implementatie

In Object Oriented Programming (OOP) wordt een CPP-bestand gebruikt als klassedefinitie. In dat geval worden alle klassegegevensleden en lidfuncties gedeclareerd in het headerbestand. Elk headerbestand kan op zijn beurt ook verwijzen naar standaardbibliotheekmethoden. Het CPP-bestand met klassedefinitie verwijst naar het headerbestand in een include-instructie aan het begin van het bestand. Meestal voegen softwareontwikkelaars opmerkingen toe aan het begin van zo'n klasse-implementatiebestand dat informatie geeft over de feitelijke inhoud van het bestand, de details van de auteur en de implementatiedatum. In dergelijke gevallen moeten de header-implementatiebestanden dezelfde namen hebben. Een voorbeeld van zo'n header- en implementatiebestand is als volgt.

### Koptekstbestand

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

### CPP-implementatiebestand

```
#include "MyClass.h"

MyClass::MyClass(){
   ...
}
void MyClass::add(int i, int j) {
   int result # i + j;
}
```

## Referenties

* [Klasse-implementatie - door Wikipedia](https://en.wikipedia.org/wiki/Class_implementation_file)

