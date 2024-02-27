{
  "date": "2019-10-11",
  "keywords": [
"h",
".h",
"hvad er ah fil",
"hvordan man åbner filen h",
"udvidelse",
"fil",
"h fil",
"h filformat",
"h filtypenavn",
"H Fil Eksempel"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "H - C/C++ Header-filformat",
  "description": "Lær om H filformat og API'er, der kan oprette og åbne H fil.",
  "linktitle": "H",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming--dah"
}
},
  "lastmod": "2021-05-07"
}

## Hvad er en H-fil?

En fil gemt med **h filtypenavn** er en header-fil, der bruges i C/C++-filer til at inkludere erklæringen af variabler, konstanter og funktioner. Disse henvises til af [C++](/programming/cpp/) implementeringsfilerne, der indeholder den faktiske implementering af disse funktioner. En .h-headerfil kan også indeholde yderligere oplysninger såsom makrodefinitioner. Der henvises til disse header-filer i C/C++-filerne ved hjælp af `#include`-direktivet.

Et nyt C++-projekt indeholder normalt en speciel header-fil med navnet **stdafx.h**-fil, som er udgangspunktet for alle kompileringskæder, og alle header-filerne kan inkluderes i denne enkelte fil. En .h-fil kan åbnes med enhver teksteditor, Eclipse IDE, Microsoft Visual Studio IDE, Borland C++ compiler og en masse andre programmer.

## .H Filformat

En .h-fil er en almindelig tekstfil, der har sine egne regler for at definere syntaksen. Header-filer kan indeholde følgende oplysninger.

**`Variables`** - I tilfælde af objektorienteret programmering (OOP) indeholder en klasseheader-fil definitioner af alle klasseniveauvariabler, der er tilgængelige på tværs af implementeringskildekodefilerne
**`Methods Declaration`** - Alle metodedeklarationerne er inkluderet i .h header-filerne for at være tilgængelige på tværs af flere implementeringsfiler.
**`Non-inline funktionsdefinitioner`** - Header-filer kan også indeholde definitioner af en ikke-inline-metode.
**`Message Maps`** - En header-fil kan også indeholde meddelelseskort i tilfælde af en MFC-kildekodeimplementering. I sådanne tilfælde er meddelelseskortene knyttet til funktionalitetsimplementeringen, som er knyttet til UI-elementer såsom knap, afkrydsningsfelt, radioknapper osv.


### Hovedbeskyttere

Header-filer kan føre til komplekse fejl, hvor flere erklæringer er inkluderet i den samme fil som et resultat af tilføjelse af andre header-filer. Disse dublerede definitioner rejser compilerfejl. Denne problematiske situation kan undgås via en mekanisme kaldet header guard, som er betingede kompileringsdirektiver som vist nedenfor.

```
#ifndef ANY_UNIQUE_NAME_HERE
#define ANY_UNIQUE_NAME_HERE

// your declarations (and certain types of definitions) here

#endif
```
Med denne header kontrollerer præprocessoren, om `ANY_UNIQUE_NAME_HERE` allerede er defineret. Hvis headeren gentagne gange inkluderes i den samme fil, vil indholdet af headeren blive ignoreret.

## H Fil Eksempel

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

## Referencer

* [Header Filers - Microsoft](https://learn.microsoft.com/en-us/cpp/cpp/header-files-cpp?view=msvc-160)


