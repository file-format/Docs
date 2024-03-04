{
  "date": "2019-10-11",
  "keywords": [
"h",
".h",
"kas yra ah failas",
"Kaip atidaryti h failą",
"pratęsimas",
"failą",
"h failą",
"h failo formatas",
"h failo plėtinys",
"H failo pavyzdys"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "H – C/C++ antraštės failo formatas",
  "description": "Sužinokite apie H failo formatą ir API, kurios gali sukurti ir atidaryti H failą.",
  "linktitle": "H",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming--lth"
}
},
  "lastmod": "2021-05-07"
}

## Kas yra H failas?

Failas, įrašytas su **h failo plėtiniu**, yra antraštės failas, naudojamas C/C++ failuose, siekiant įtraukti kintamųjų, konstantų ir funkcijų deklaracijas. Tai nurodo [C++](/programming/cpp/) diegimo failai, kuriuose yra tikrasis šių funkcijų įgyvendinimas. .h antraštės faile taip pat gali būti papildomos informacijos, pvz., makrokomandų apibrėžimų. Šie antraštės failai pateikiami C/C++ failuose, naudojant direktyvą #include.

Naujame C++ projekte paprastai yra specialus antraštės failas pavadinimu **stdafx.h** failas, kuris yra visų kompiliavimo grandinių pradžios taškas ir visi antraštės failai gali būti įtraukti į šį vieną failą. .h failą galima atidaryti naudojant bet kurį teksto rengyklę, Eclipse IDE, Microsoft Visual Studio IDE, Borland C++ kompiliatorių ir daugybę kitų programų.

## .H failo formatas

.h failas yra paprasto teksto failas, turintis savo sintaksės apibrėžimo taisykles. Antraštės failuose gali būti ši informacija.

**`Kintamieji`** – Objektinio programavimo (OOP) atveju klasės antraštės faile yra visų klasės lygio kintamųjų, kurie pasiekiami diegimo šaltinio kodo failuose, apibrėžimai.
**`Metodų deklaracija`** – visos metodų deklaracijos įtrauktos į .h antraštės failus, kad būtų pasiekiami keliuose diegimo failuose.
**Neįdėtos funkcijos apibrėžimai** – antraštės failuose taip pat gali būti netiesioginių metodų apibrėžimų.
**`Pranešimų žemėlapiai`** – antraštės faile taip pat gali būti pranešimų žemėlapių, jei įdiegtas MFC šaltinio kodas. Tokiu atveju pranešimų žemėlapiai yra susieti su funkcijų įgyvendinimu, kuris yra susietas su vartotojo sąsajos elementais, tokiais kaip mygtukas, žymės langelis, radijo mygtukai ir kt.


### Antraštės apsaugai

Antraštės failai gali sukelti sudėtingų klaidų, kai į tą patį failą įtraukiamos kelios deklaracijos dėl kitų antraštės failų pridėjimo. Šie pasikartojantys apibrėžimai sukelia kompiliatoriaus klaidas. Šios probleminės situacijos galima išvengti naudojant mechanizmą, vadinamą antraštės apsauga, kurios yra sąlyginės kompiliavimo direktyvos, kaip parodyta toliau.

```
#ifndef ANY_UNIQUE_NAME_HERE
#define ANY_UNIQUE_NAME_HERE

// your declarations (and certain types of definitions) here

#endif
```
Naudodamas šią antraštę, pirminis procesorius patikrina, ar `ANY_UNIQUE_NAME_HERE` jau apibrėžtas. Jei antraštė pakartotinai įtraukiama į tą patį failą, antraštės turinys bus ignoruojamas.

## H failo pavyzdys

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

## Nuorodos

* [Antraštės failai – „Microsoft“](https://learn.microsoft.com/en-us/cpp/cpp/header-files-cpp?view=msvc-160)


