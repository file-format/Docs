{
  "date" : "2020-01-10",
  "keywords" :[ "c", ".c", "co to jest plik ac", "jak otworzyć plik c", "rozszerzenie", "plik", "plik c", "format pliku c", "rozszerzenie pliku c"] ,
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Plik Programowania Języka C - C",
  "description":"Poznaj format pliku C i interfejsy API, które mogą tworzyć i otwierać pliki C.",
  "linktitle" : "C",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-01-10"
}

## Czym jest plik C?

Plik zapisany z rozszerzeniem pliku c to plik kodu źródłowego napisany w języku programowania C. **Plik C** zawiera całą implementację funkcjonalności aplikacji w postaci kodu źródłowego. Deklaracja kodu źródłowego jest zapisywana w plikach nagłówkowych zapisywanych z rozszerzeniem [.h](/pl/programming/h/). C++ jest nowoczesną formą języka C i jest obecnie używany do tworzenia większości oprogramowania.

## Krótka historia

Język C powstał w wyniku tworzenia różnych narzędzi dla systemu operacyjnego UNIX. Denis Ritchie, człowiek stojący za stworzeniem tego języka programowania, prace rozpoczęto pierwotnie w latach sześćdziesiątych i wczesnych siedemdziesiątych.

## Format pliku C

Pliki C są zapisywane w formacie zwykłego pliku tekstowego zgodnie ze składnią języka programowania. Typowy plik C będzie miał:

* oświadczenie importu na górze pliku, aby zaimportować dowolne pliki nagłówkowe
* jedną lub więcej metod implementacji pożądanej funkcjonalności

### Import nagłówków

Pliki nagłówkowe z rozszerzeniem .h zawierają niezbędne instrukcje dołączania do włączenia innych plików funkcjonalności do projektu. Dodatkowo zawierają one deklaracje metod zdefiniowanych w pliku implementacyjnym. Pliki nagłówkowe są dołączane przy użyciu instrukcji include, jak pokazano poniżej.

```
#include <filename.h>
```

### Implementacja kodu źródłowego

Rzeczywista implementacja wymagań funkcjonalnych jest zakodowana jako metody w pliku C. Każda metoda w pliku C ma zwracany typ, nazwę metody i może mieć pewne parametry wejściowe. Jeśli typem zwracanym nie jest void, metoda może zwracać jakąś wartość.

### Przykład kodu C
Oto przykładowy program ac:

```
long some_function();
/* int */ other_function();

/* int */ calling_function()
{
    long test1;
    register /* int */ test2;

    test1 = some_function();
    if (test1 > 0)
          test2 = 0;
    else
          test2 = other_function();
    return test2;
}
```



## **Bibliografia** ##

* [Implementacja klas – według Wikipedii](https://en.wikipedia.org/wiki/Class_implementation_file)

