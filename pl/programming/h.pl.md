{
  "date" : "2019-10-11",
  "keywords" :[ "h", ".h", "co to jest plik ah", "jak otworzyć plik h", "rozszerzenie", "plik", "plik h", "format pliku h", "rozszerzenie pliku h", "Przykład pliku H"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format pliku nagłówka H - C/C++",
  "description":"Poznaj format pliku H i interfejsy API, które mogą tworzyć i otwierać plik H.",
  "linktitle" : "H",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-07"
}

## Co to jest plik H?

Plik zapisany z **rozszerzeniem pliku h** jest plikiem nagłówkowym używanym w plikach C/C++ do dołączania deklaracji zmiennych, stałych i funkcji. Odwołują się do nich pliki implementacji [C++](/pl/programming/cpp/), które zawierają rzeczywistą implementację tych funkcji. Plik nagłówkowy .h może również zawierać dodatkowe informacje, takie jak definicje makr. Te pliki nagłówkowe są przywoływane w plikach C/C++ przy użyciu dyrektywy `#include`.

Nowy projekt C++ zwykle zawiera specjalny plik nagłówkowy o nazwie **stdafx.h**, który jest punktem wyjścia dla wszystkich łańcuchów kompilacji i wszystkie pliki nagłówkowe mogą być zawarte w tym pojedynczym pliku. Plik .h można otworzyć za pomocą dowolnego edytora tekstu, Eclipse IDE, Microsoft Visual Studio IDE, kompilatora Borland C++ i wielu innych aplikacji.

## Format pliku .H

Plik .h to zwykły plik tekstowy, który ma własne reguły definiowania składni. Pliki nagłówkowe mogą zawierać następujące informacje.

**`Zmienne`** — w przypadku programowania obiektowego (OOP) plik nagłówka klasy zawiera definicje wszystkich zmiennych na poziomie klasy, które są dostępne w plikach kodu źródłowego implementacji
**`Deklaracja metod`** — wszystkie deklaracje metod są zawarte w plikach nagłówkowych .h, aby były dostępne w wielu plikach implementacji.
**`Definicje funkcji nieliniowych`** — pliki nagłówkowe mogą również zawierać definicje metod nieliniowych.
**`Mapy wiadomości`** — plik nagłówkowy może również zawierać mapy wiadomości w przypadku implementacji kodu źródłowego MFC. W takim przypadku mapy komunikatów są powiązane z implementacją funkcjonalności, która jest powiązana z elementami interfejsu użytkownika, takimi jak przycisk, pole wyboru, przyciski radiowe itp.


### Osłony nagłówka

Pliki nagłówkowe mogą powodować złożone błędy, gdy wiele deklaracji jest zawartych w tym samym pliku w wyniku dodania innych plików nagłówkowych. Te zduplikowane definicje powodują błędy kompilatora. Tej problematycznej sytuacji można uniknąć za pomocą mechanizmu zwanego strażnikiem nagłówka, który jest dyrektywą kompilacji warunkowej, jak pokazano poniżej.

```
#ifndef ANY_UNIQUE_NAME_HERE
#define ANY_UNIQUE_NAME_HERE

// your declarations (and certain types of definitions) here

#endif
```
Za pomocą tego nagłówka preprocesor sprawdza, czy `ANY_UNIQUE_NAME_HERE` zostało już zdefiniowane. Jeśli nagłówek jest wielokrotnie dołączany do tego samego pliku, zawartość nagłówka zostanie zignorowana.

## Przykład pliku H

```
// sample.h
#pragma once
#include <vector> // #include directive
#include <string>

namespace N  // namespace declaration
{
    inline namespace P
    {
        //...
}

    enum class colors : short { red, blue, purple, azure };

    const double PI = 3.14;  // const and constexpr definitions
    constexpr int MeaningOfLife{ 42 };
    constexpr int get_meaning()
    {
        static_assert(MeaningOfLife == 42, "unexpected!"); // static_assert
        return MeaningOfLife;
}
    using vstr = std::vector<int>;  // type alias
    extern double d; // extern variable

#define LOG   // macro definition

#ifdef LOG   // conditional compilation directive
    void print_to_log();
#endif

    class my_class   // regular class definition,
    {                // but no non-inline function definitions

        friend class other_class;
    public:
        void do_something();   // definition in my_class.cpp
        inline void put_value(int i) { vals.push_back(i); } // inline OK

    private:
        vstr vals;
        int i;
    };

    struct RGB
    {
        short r{ 0 };  // member initialization
        short g{ 0 };
        short b{ 0 };
    };

    template <typename T>  // template definition
    class value_store
    {
    public:
        value_store<T>() = default;
        void write_value(T val)
        {
            //... function definition OK in template
    }
    private:
        std::vector<T> vals;
    };

    template <typename T>  // template declaration
    class value_widget;
}
```

## Bibliografia

* [Pliki nagłówkowe — Microsoft](https://docs.microsoft.com/en-us/cpp/cpp/header-files-cpp?view=msvc-160)

