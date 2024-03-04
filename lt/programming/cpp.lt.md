{
  "date": "2019-10-11",
  "keywords": [
"c++",
"failą",
"pratęsimas",
"Dokumento formatas",
"C++",
"Programavimo kalba"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "CPP – C++ šaltinio kodo failas",
  "description": "Sužinokite apie CPP failo formatą ir API, kurios gali kurti ir atidaryti CPP failus.",
  "linktitle": "CPP",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-cp-ltp"
}
},
  "lastmod": "2019-09-10"
}

## Kas yra C++ failas?

Failai su CPP failo plėtiniu yra šaltinio kodo failai, skirti programoms, parašytoms C++ programavimo kalba. Viename C++ projekte gali būti daugiau nei vienas CPP failas kaip programos šaltinio kodas. Tokį projektą sudaro skirtingi failų tipai, iš kurių CPP failai yra žinomi kaip įgyvendinimo failai, nes juose yra visi antraštės (.h) faile nurodytų metodų apibrėžimai. C++ projektas, kaip visuma, sukuria vykdomąją programą, kai sukompiliuojama kaip visuma.

## CPP failo struktūra

CPP failo struktūra yra paprasta, palyginti su antraštės failais. Pagrindinis tokio diegimo failo tikslas yra atskirti sąsają nuo diegimo. Tai lemia visų narių funkcijų deklaracijas antraštės faile ir jų informaciją CPP faile. CPP diegimo failas gali būti naudojamas kaip paprastas failas programai rašyti arba kaip klasės įgyvendinimas.

### Nepriklausomas įgyvendinimas

CPP faile, kai jis naudojamas kaip nepriklausoma programa, gali būti visi jame esantys diegimai, nereikalaujant metodų deklaravimo antraštės faile. Toks diegimas susideda iš visų metodų, apibrėžtų diegimo faile, kur programos įvedimą valdo pagrindinis metodas, kuris pasirenka neprivalomą vartotojo įvestį kaip argumentus. Tai taip pat gali apimti bet kokias C++ standartinės bibliotekos bibliotekas, kurios bus naudojamos bet kokiais faile nurodytais metodais.

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

### Klasės įgyvendinimas

Objektiniame programavime (OOP) CPP failas naudojamas kaip klasės apibrėžimas. Tokiu atveju visi klasės duomenų nariai ir narių funkcijos yra deklaruojamos antraštės faile. Kiekvienas antraštės failas taip pat gali turėti nuorodą į standartinius bibliotekos metodus. Klasės apibrėžimo CPP failas nurodo antraštės failą įtraukimo sakinyje failo pradžioje. Dažniausiai programinės įrangos kūrėjai tokio klasės diegimo failo pradžioje įtraukia komentarus, kuriuose pateikiama informacija apie tikrąjį failo turinį, autoriaus duomenis ir diegimo datą. Tokiais atvejais antraštės įgyvendinimo failai turi turėti tuos pačius pavadinimus. Tokios antraštės ir įgyvendinimo failo pavyzdys yra toks.

### Antraštės failas

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

### CPP diegimo failas

```
#include "MyClass.h"

MyClass::MyClass(){
   ...
}
void MyClass::add(int i, int j) {
   int result # i + j;
}
```

## Nuorodos

* [Klasės įgyvendinimas – pagal Vikipediją](https://en.wikipedia.org/wiki/Class_implementation_file)


