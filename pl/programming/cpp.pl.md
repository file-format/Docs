{
  "date" : "2019-10-11",
  "keywords" :["c++", "plik", "rozszerzenie", "format pliku", "C++", "Język programowania" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CPP - Plik kodu źródłowego C++",
  "description":"Poznaj format pliku CPP i interfejsy API, które mogą tworzyć i otwierać pliki CPP.",
  "linktitle" : "CPP",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## Co to jest plik C++?

Pliki z rozszerzeniem pliku CPP to pliki kodu źródłowego aplikacji napisanych w języku programowania C ++. Pojedynczy projekt C++ może zawierać więcej niż jeden plik CPP jako kod źródłowy aplikacji. Taki projekt składa się z różnych typów plików, z których pliki CPP nazywane są plikami implementacyjnymi, ponieważ zawierają wszystkie definicje metod zadeklarowanych w pliku nagłówkowym (.h). Projekt C++ jako całość daje wykonywalną aplikację, gdy jest skompilowany jako całość.

## Struktura plików CPP

Struktura plików CPP jest prosta w porównaniu z plikami nagłówkowymi. Głównym celem takiego pliku implementacji jest oddzielenie interfejsu od implementacji. Powoduje to deklaracje wszystkich funkcji składowych w pliku nagłówkowym i ich szczegóły w pliku CPP. Plik implementacji CPP może służyć jako prosty plik do napisania aplikacji lub jako implementacja klasy.

### Niezależna implementacja

Plik CPP używany jako niezależna aplikacja może zawierać wszystkie implementacje w nim zawarte bez wymogu deklaracji metod w pliku nagłówkowym. Taka implementacja składa się ze wszystkich metod zdefiniowanych w pliku implementacji, gdzie wpis aplikacji jest zarządzany przez główną metodę, która przyjmuje opcjonalne dane wejściowe użytkownika jako argumenty. Może również zawierać dowolne biblioteki ze standardowej biblioteki C++, które mają być używane przez dowolne metody zadeklarowane w pliku.

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

### Implementacja klasy

W programowaniu zorientowanym obiektowo (OOP) plik CPP jest używany jako definicja klasy. W takim przypadku wszystkie składowe danych klasy i funkcje składowe są deklarowane w pliku nagłówkowym. Każdy plik nagłówkowy może z kolei mieć odniesienia do standardowych metod bibliotecznych. Plik definicji klasy CPP odwołuje się do pliku nagłówkowego w instrukcji include na początku pliku. Najczęściej twórcy oprogramowania umieszczają na początku takiego pliku implementacji klasy komentarze, które dostarczają informacji o faktycznej zawartości pliku, danych autora i dacie implementacji. W takich przypadkach pliki implementacji nagłówka muszą mieć takie same nazwy. Przykład takiego pliku nagłówka i implementacji jest następujący.

### Plik nagłówkowy

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

### Plik implementacji CPP

```
#include "MyClass.h"

MyClass::MyClass(){
   ...
}
void MyClass::add(int i, int j) {
   int result # i + j;
}
```

## Bibliografia

* [Implementacja klas – według Wikipedii](https://en.wikipedia.org/wiki/Class_implementation_file)

