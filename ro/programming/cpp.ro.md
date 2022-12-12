{
  "date" : "2019-10-11",
  "keywords" :[ "c++", "fișier", "extensie", "format fișier", "C++", "Limbaj de programare"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CPP - Fișier cod sursă C++",
  "description":"Aflați despre formatul de fișier CPP și despre API-urile care pot crea și deschide fișiere CPP.",
  "linktitle" : "CPP",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este un fișier C++?

Fișierele cu extensia de fișier CPP sunt fișiere de cod sursă pentru aplicații scrise în limbajul de programare C++. Un singur proiect C++ poate conține mai multe fișiere CPP ca cod sursă al aplicației. Un astfel de proiect constă din diferite tipuri de fișiere, dintre care fișierele CPP sunt cunoscute ca fișiere de implementare deoarece conțin toate definițiile metodelor declarate în fișierul antet (.h). Proiectul C++ în ansamblu are ca rezultat o aplicație executabilă atunci când este compilată ca întreg.

## Structura fișierului CPP

O structură a fișierelor CPP este simplă în comparație cu fișierele antet. Scopul principal al unui astfel de fișier de implementare este de a împărți interfața de implementare. Acest lucru are ca rezultat declararea tuturor funcțiilor membre într-un fișier antet și detaliile acestora în fișierul CPP. Un fișier de implementare CPP poate fi folosit ca fișier simplu pentru scrierea unei aplicații sau ca implementare de clasă.

### Implementare independentă

Un fișier CPP atunci când este utilizat ca aplicație independentă poate conține toate implementările din interiorul său fără a necesita declararea metodelor în fișierul antet. O astfel de implementare constă din toate metodele definite în fișierul de implementare în care intrarea aplicației este guvernată de o metodă principală care ia ca argumente intrarea opțională a utilizatorului. Poate include, de asemenea, orice biblioteci din Biblioteca standard C++ pentru a fi utilizate de orice metode declarate în fișier.

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

### Implementarea clasei

În programarea orientată pe obiecte (OOP), un fișier CPP este folosit ca definiție de clasă. În acest caz, toți membrii datelor de clasă și funcțiile membre sunt declarate în fișierul antet. Fiecare fișier antet poate avea, la rândul său, referință la metodele standard de bibliotecă. Fișierul CPP cu definiția clasei se referă la fișierul antet într-o instrucțiune include la începutul fișierului. De cele mai multe ori, dezvoltatorii de software includ comentarii la începutul unui astfel de fișier de implementare a clasei care oferă informații despre conținutul real al fișierului, detaliile autorului și data implementării. În astfel de cazuri, fișierele de implementare antet trebuie să aibă aceleași nume. Un exemplu de astfel de antet și fișier de implementare este următorul.

### Fișier antet

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

### Fișier de implementare a CPP

```
#include "MyClass.h"

MyClass::MyClass(){
   ...
}
void MyClass::add(int i, int j) {
   int result # i + j;
}
```

## Referințe

* [Implementarea clasei - Prin Wikipedia](https://en.wikipedia.org/wiki/Class_implementation_file)

