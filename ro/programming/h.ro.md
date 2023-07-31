{
  "date" : "2019-10-11",
  "keywords" :[ "h", ".h","ce este fișierul ah","cum se deschide fișierul h", "extensia", "fișierul", "fișierul h","formatul fișierului h", "extensia fișierului h", "Exemplu de fișier H"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"H - Format fișier antet C/C++",
  "description":"Aflați despre formatul de fișier H și despre API-urile care pot crea și deschide fișierul H.",
  "linktitle" : "H",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-07"
}

## Ce este un fișier H?

Un fișier salvat cu **extensia de fișier h** este un fișier antet utilizat în fișierele C/C++ pentru a include declararea variabilelor, constantelor și funcțiilor. Acestea sunt menționate de fișierele de implementare [C++](/ro/programming/cpp/) care conțin implementarea efectivă a acestor funcții. Un fișier antet .h poate include, de asemenea, informații suplimentare, cum ar fi definițiile Macro. Aceste fișiere antet sunt menționate în fișierele C/C++ folosind directiva `#include`.

Un nou proiect C++ conține de obicei un fișier antet special cu numele fișierului **stdafx.h** care este punctul de plecare pentru toate lanțurile de compilare și toate fișierele antet pot fi incluse în acest fișier unic. Un fișier .h poate fi deschis cu orice editor de text, Eclipse IDE, Microsoft Visual Studio IDE, compilator Borland C++ și multe alte aplicații.

## .H Format de fișier

Un fișier .h este un fișier text simplu care are propriile reguli pentru definirea sintaxei. Fișierele antet pot conține următoarele informații.

**`Variabile`** - În cazul programării orientate pe obiecte (OOP), un fișier antet de clasă conține definiții ale tuturor variabilelor la nivel de clasă care sunt accesibile prin fișierele codului sursă de implementare
**`Declarația metodelor`** - Toate declarațiile metodelor sunt incluse în fișierele antet .h pentru a fi accesibile prin mai multe fișiere de implementare.
**`Non-Inline Function Definitions`** - Fișierele antet pot conține, de asemenea, definiții ale unei metode non-inline.
**`Hărți de mesaje`** - Un fișier antet poate conține și hărți de mesaje în cazul implementării unui cod sursă MFC. În acest caz, hărțile de mesaje sunt legate de implementarea funcționalității care este legată de elementele UI, cum ar fi butonul, caseta de selectare, butoanele radio etc.


### Gărzi de antet

Fișierele antet pot duce la erori complexe în cazul în care mai multe declarații sunt incluse în același fișier ca urmare a adăugării altor fișiere antet. Aceste definiții duplicat generează erori ale compilatorului. Această situație problematică poate fi evitată printr-un mecanism numit header guard care sunt directive de compilare condiționată, așa cum se arată mai jos.

```
#ifndef ANY_UNIQUE_NAME_HERE
#define ANY_UNIQUE_NAME_HERE

// your declarations (and certain types of definitions) here

#endif
```
Cu acest antet, preprocesorul verifică dacă „ANY_UNIQUE_NAME_HERE” a fost deja definit. Dacă antetul este inclus în mod repetat în același fișier, conținutul antetului va fi ignorat.

## H Exemplu de fișier

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

## Referințe

* [Filere antet - Microsoft](https://learn.microsoft.com/en-us/cpp/cpp/header-files-cpp?view=msvc-160)

