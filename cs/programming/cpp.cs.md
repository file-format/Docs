{
  "date" : "2019-10-11",
  "keywords" :[ "c++", "soubor", "přípona", "formát souboru", "C++", "Programovací jazyk" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Soubor zdrojového kódu CPP - C++",
  "description":"Další informace o formátu souboru CPP a rozhraních API, která mohou vytvářet a otevírat soubory CPP.",
  "linktitle" : "CPP",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor C++?

Soubory s příponou CPP jsou soubory zdrojového kódu pro aplikace napsané v programovacím jazyce C++. Jeden projekt C++ může obsahovat více než jeden soubor CPP jako zdrojový kód aplikace. Takový projekt se skládá z různých typů souborů, z nichž soubory CPP jsou známé jako implementační soubory, protože obsahují všechny definice metod deklarovaných v souboru záhlaví (.h). Výsledkem projektu C++ jako celku je spustitelná aplikace, když je zkompilován jako celek.

## Struktura souboru CPP

Struktura souboru CPP je ve srovnání se soubory záhlaví jednoduchá. Hlavním účelem takového implementačního souboru je oddělit rozhraní od implementace. Výsledkem jsou deklarace všech členských funkcí v záhlaví souboru a jejich podrobnosti v souboru CPP. Implementační soubor CPP lze použít jako jednoduchý soubor pro psaní aplikace nebo jako implementaci třídy.

### Nezávislá implementace

Soubor CPP, pokud je použit jako nezávislá aplikace, může obsahovat všechny implementace v něm bez požadavku na deklaraci metod v záhlaví souboru. Taková implementace se skládá ze všech metod definovaných v implementačním souboru, kde je vstup aplikace řízen hlavní metodou, která bere volitelný uživatelský vstup jako argumenty. Může také zahrnovat libovolné knihovny ze standardní knihovny C++, které mají být použity jakýmikoli deklarovanými metodami v souboru.

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

### Implementace třídy

V objektově orientovaném programování (OOP) se jako definice třídy používá soubor CPP. V takovém případě jsou všechny datové členy třídy a členské funkce deklarovány uvnitř souboru záhlaví. Každý hlavičkový soubor může mít také odkaz na standardní metody knihovny. Soubor CPP s definicí třídy odkazuje na soubor záhlaví v příkazu include na začátku souboru. Vývojáři softwaru většinou na začátek takového souboru implementace třídy zahrnou komentáře, které poskytují informace o skutečném obsahu souboru, podrobnostech o autorovi a datu implementace. V takových případech musí mít soubory implementace záhlaví stejná jména. Příklad takového souboru záhlaví a implementace je následující.

### Soubor záhlaví

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

### Soubor implementace CPP

```
#include "MyClass.h"

MyClass::MyClass(){
   ...
}
void MyClass::add(int i, int j) {
   int result # i + j;
}
```

## Reference

* [Implementace třídy – podle Wikipedie](https://en.wikipedia.org/wiki/Class_implementation_file)

