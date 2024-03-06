{
  "date": "2019-10-11",
  "keywords": [
"c++",
"failu",
"pagarinājumu",
"faila formātā",
"C++",
"Programmēšanas valoda"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "CPP — C++ avota koda fails",
  "description": "Uzziniet par CPP failu formātu un API, kas var izveidot un atvērt CPP failus.",
  "linktitle": "CPP",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-cp-lvp"
}
},
  "lastmod": "2019-09-10"
}

## Kas ir C++ fails?

Faili ar CPP faila paplašinājumu ir pirmkoda faili lietojumprogrammām, kas rakstītas C++ programmēšanas valodā. Viens C++ projekts var saturēt vairāk nekā vienu CPP failu kā lietojumprogrammas avota kodu. Šāds projekts sastāv no dažādiem failu tipiem, no kuriem CPP faili ir zināmi kā ieviešanas faili, jo tie satur visas galvenes (.h) failā deklarēto metožu definīcijas. C++ projekts kopumā rada izpildāmu lietojumprogrammu, kad tas tiek apkopots kopumā.

## CPP faila struktūra

CPP faila struktūra ir vienkārša, salīdzinot ar galvenes failiem. Šāda ieviešanas faila galvenais mērķis ir sadalīt saskarni no ieviešanas. Tā rezultātā tiek deklarētas visas dalībnieka funkcijas galvenes failā un to informācija CPP failā. CPP ieviešanas failu var izmantot kā vienkāršu failu lietojumprogrammas rakstīšanai vai kā klases implementāciju.

### Neatkarīga ieviešana

CPP fails, ja to izmanto kā neatkarīgu lietojumprogrammu, var saturēt visas tajā esošās implementācijas bez metožu deklarācijas prasības galvenes failā. Šāda ieviešana sastāv no visām ieviešanas failā definētajām metodēm, kurās lietojumprogrammas ievadi regulē galvenā metode, kas kā argumentus izmanto lietotāja izvēles ievadi. Tas var ietvert arī visas bibliotēkas no C++ standarta bibliotēkas, kas jāizmanto ar jebkuru failā deklarēto metodi.

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

### Klases ieviešana

Object Oriented Programming (OOP) CPP fails tiek izmantots kā klases definīcija. Šādā gadījumā visi klases datu dalībnieki un dalībnieku funkcijas tiek deklarētas galvenes failā. Katram galvenes failam savukārt var būt atsauce arī uz standarta bibliotēkas metodēm. Klases definīcijas CPP fails attiecas uz galvenes failu iekļaušanas priekšrakstā faila sākumā. Pārsvarā programmatūras izstrādātāji iekļauj komentārus šāda klases ieviešanas faila sākumā, kas sniedz informāciju par faila faktisko saturu, autora informāciju un ieviešanas datumu. Šādos gadījumos galvenes ieviešanas failiem ir jābūt vienādiem nosaukumiem. Šādas galvenes un ieviešanas faila piemērs ir šāds.

### Galvenes fails

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

### CPP ieviešanas fails

```
#include "MyClass.h"

MyClass::MyClass(){
   ...
}
void MyClass::add(int i, int j) {
   int result # i + j;
}
```

## Atsauces

* [Klases ieviešana — Wikipedia](https://en.wikipedia.org/wiki/Class_implementation_file)


