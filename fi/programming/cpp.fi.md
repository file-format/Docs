{
  "date": "2019-10-11",
  "keywords": [
"c++",
"tiedosto",
"laajennus",
"tiedosto muoto",
"C++",
"Ohjelmointikieli"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "CPP - C++-lähdekooditiedosto",
  "description": "Lisätietoja CPP-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata CPP-tiedostoja.",
  "linktitle": "CPP",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-cp-fip"
}
},
  "lastmod": "2019-09-10"
}

## Mikä on C++-tiedosto?

CPP-tiedostotunnistetiedostot ovat lähdekooditiedostoja sovelluksille, jotka on kirjoitettu C++-ohjelmointikielellä. Yksi C++-projekti voi sisältää useamman kuin yhden CPP-tiedoston sovelluksen lähdekoodina. Tällainen projekti koostuu erilaisista tiedostotyypeistä, joista CPP-tiedostot tunnetaan toteutustiedostoina, koska ne sisältävät kaikki otsikkotiedostossa (.h) ilmoitettujen menetelmien määritelmät. C++-projekti kokonaisuudessaan johtaa suoritettavaan sovellukseen, kun se käännetään kokonaisuutena.

## CPP-tiedostorakenne

CPP-tiedostorakenne on yksinkertainen verrattuna otsikkotiedostoihin. Tällaisen toteutustiedoston päätarkoitus on jakaa käyttöliittymä toteutuksesta. Tämä johtaa kaikkien otsikkotiedoston jäsentoimintojen ilmoitukseen ja niiden yksityiskohtiin CPP-tiedoston sisällä. CPP-toteutustiedostoa voidaan käyttää yksinkertaisena tiedostona sovelluksen kirjoittamiseen tai luokkatoteutukseen.

### Itsenäinen toteutus

CPP-tiedosto, kun sitä käytetään itsenäisenä sovelluksena, voi sisältää kaikki sen sisällä olevat toteutukset ilman vaatimusta menetelmien määrittelystä otsikkotiedostossa. Tällainen toteutus koostuu kaikista toteutustiedostossa määritellyistä menetelmistä, joissa sovelluksen syöttämistä hallitsee päämenetelmä, joka ottaa valinnaisen käyttäjän syötteen argumentteina. Se voi myös sisältää mitä tahansa kirjastoja C++-standardikirjastosta, joita käytetään millä tahansa tiedostossa määritellyllä menetelmällä.

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

### Luokan toteutus

Object Oriented Programming (OOP) -ohjelmassa CPP-tiedostoa käytetään luokkamäärittelynä. Tässä tapauksessa kaikki luokan datajäsenet ja jäsenfunktiot ilmoitetaan otsikkotiedoston sisällä. Jokaisessa otsikkotiedostossa voi vuorostaan olla viittaus myös vakiokirjastomenetelmiin. Luokkamäärittelyn CPP-tiedosto viittaa otsikkotiedostoon tiedoston alussa olevassa include-lauseessa. Useimmiten ohjelmistokehittäjät lisäävät tällaisen luokan toteutustiedoston alkuun kommentteja, jotka kertovat tiedoston todellisesta sisällöstä, tekijän tiedoista ja toteutuspäivämäärästä. Tällaisissa tapauksissa otsikkototeutustiedostoilla on oltava samat nimet. Esimerkki tällaisesta otsikko- ja toteutustiedostosta on seuraava.

### Otsikkotiedosto

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

### CPP-toteutustiedosto

```
#include "MyClass.h"

MyClass::MyClass(){
   ...
}
void MyClass::add(int i, int j) {
   int result # i + j;
}
```

## Viitteet

* [Luokkien toteutus – Wikipedia](https://en.wikipedia.org/wiki/Class_implementation_file)


