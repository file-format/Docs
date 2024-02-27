{
  "date": "2019-10-11",
  "keywords": [
"c++",
"fil",
"udvidelse",
"filformat",
"C++",
"Programmeringssprog"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "CPP - C++ Kildekodefil",
  "description": "Lær om CPP-filformat og API'er, der kan oprette og åbne CPP-filer.",
  "linktitle": "CPP",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-cp-dap"
}
},
  "lastmod": "2019-09-10"
}

## Hvad er en C++ fil?

Filer med CPP filtypenavn er kildekodefiler til programmer skrevet i C++ programmeringssprog. Et enkelt C++-projekt kan indeholde mere end én CPP-fil som applikationskildekode. Et sådant projekt består af forskellige filtyper, hvoraf CPP-filerne er kendt som implementeringsfiler, da de indeholder alle definitionerne af metoderne erklæret i header-filen (.h). C++-projektet som helhed resulterer i en eksekverbar applikation, når det kompileres som en helhed.

## CPP filstruktur

En CPP-filstruktur er enkel sammenlignet med header-filerne. Hovedformålet med en sådan implementeringsfil er at opdele grænsefladen fra implementeringen. Dette resulterer i erklæringer af alle medlemsfunktionerne i en header-fil og deres detaljer i CPP-filen. En CPP implementeringsfil kan bruges som en simpel fil til at skrive en applikation eller som en klasseimplementering.

### Uafhængig implementering

En CPP-fil, når den bruges som en uafhængig applikation, kan indeholde alle implementeringerne i den uden krav om metodedeklaration i header-fil. En sådan implementering består af alle metoder defineret i implementeringsfilen, hvor indtastningen af applikationen er styret af en hovedmetode, der tager valgfri brugerinput som argumenter. Det kan også inkludere alle biblioteker fra C++ Standard Library, der skal bruges af alle erklærede metoder i filen.

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

### Klasseimplementering

I Object Oriented Programming (OOP) bruges en CPP-fil som en klassedefinition. I sådanne tilfælde er alle klassedatamedlemmer og medlemsfunktioner erklæret inde i header-filen. Hver header-fil kan også have reference til standard biblioteksmetoder. Klassedefinitionen CPP-filen refererer til header-filen i en include-sætning i starten af filen. For det meste inkluderer softwareudviklere kommentarer i starten af en sådan klasseimplementeringsfil, der giver information om det faktiske indhold af filen, forfatterens detaljer og implementeringsdatoen. I sådanne tilfælde skal headerimplementeringsfilerne have de samme navne. Et eksempel på en sådan header og implementeringsfil er som følger.

### Overskriftsfil

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

### CPP-implementeringsfil

```
#include "MyClass.h"

MyClass::MyClass(){
   ...
}
void MyClass::add(int i, int j) {
   int result # i + j;
}
```

## Referencer

* [Klasseimplementering - af Wikipedia](https://en.wikipedia.org/wiki/Class_implementation_file)


