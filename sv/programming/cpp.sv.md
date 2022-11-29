{
  "date" : "2019-10-11",
  "keywords" :[ "c++", "fil", "tillägg", "filformat", "C++", "Programmeringsspråk" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CPP - C++ källkodsfil",
  "description":"Läs mer om CPP-filformat och API:er som kan skapa och öppna CPP-filer.",
  "linktitle" : "CPP",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är en C++ fil?

Filer med filändelsen CPP är källkodsfiler för applikationer skrivna i programmeringsspråket C++. Ett enda C++-projekt kan innehålla mer än en CPP-fil som applikationskällkod. Ett sådant projekt består av olika filtyper, varav CPP-filerna är kända som implementeringsfiler eftersom de innehåller alla definitioner av metoderna som deklareras i header-filen (.h). C++-projektet som helhet resulterar i en körbar applikation när den kompileras som en helhet.

## CPP-filstruktur

En CPP-filstruktur är enkel jämfört med rubrikfilerna. Huvudsyftet med en sådan implementeringsfil är att dela upp gränssnittet från implementeringen. Detta resulterar i deklarationer av alla medlemsfunktioner i en rubrikfil och deras detaljer i CPP-filen. En CPP-implementeringsfil kan användas som en enkel fil för att skriva en applikation eller som en klassimplementering.

### Oberoende implementering

En CPP-fil när den används som en oberoende applikation kan innehålla alla implementeringar inuti den utan krav på metoddeklaration i huvudfilen. En sådan implementering består av alla metoder definierade i implementeringsfilen där inmatningen av applikationen styrs av en huvudmetod som tar valfri användarinmatning som argument. Det kan också inkludera alla bibliotek från C++ Standard Library som ska användas av alla deklarerade metoder i filen.

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

### Klassimplementering

I Object Oriented Programming (OOP) används en CPP-fil som klassdefinition. I sådana fall deklareras alla klassdatamedlemmar och medlemsfunktioner inuti rubrikfilen. Varje rubrikfil kan i sin tur också ha referens till standardbiblioteksmetoder. Klassdefinitionen CPP-filen refererar till rubrikfilen i en include-sats i början av filen. Oftast inkluderar mjukvaruutvecklare kommentarer i början av en sådan klassimplementeringsfil som ger information om det faktiska innehållet i filen, författarens detaljer och implementeringsdatum. I sådana fall måste headerimplementeringsfilerna ha samma namn. Ett exempel på en sådan header och implementeringsfil är följande.

### Rubrikfil

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

## Referenser

* [Klassimplementering - av Wikipedia](https://en.wikipedia.org/wiki/Class_implementation_file)

