{
  "date" : "2019-10-11",
  "keywords" :[ "h", ".h","vad är ah-fil","hur man öppnar h-fil", "tillägg", "fil", "h-fil","h filformat", "h filtillägg", "H-filexempel"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"H - C/C++ Header File Format",
  "description":"Läs mer om H-filformat och API:er som kan skapa och öppna H-fil.",
  "linktitle" : "H",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-07"
}

## Vad är en H-fil?

En fil sparad med **h filtillägg** är en rubrikfil som används i C/C++-filer för att inkludera deklarationen av variabler, konstanter och funktioner. Dessa refereras av implementeringsfilerna [C++](/sv/programming/cpp/) som innehåller den faktiska implementeringen av dessa funktioner. En .h-huvudfil kan också innehålla ytterligare information som makrodefinitioner. Dessa rubrikfiler hänvisas till i C/C++-filerna med "#include"-direktivet.

Ett nytt C++-projekt innehåller vanligtvis en speciell header-fil med namnet **stdafx.h**-fil som är startpunkten för alla kompileringskedjor och alla header-filer kan inkluderas i denna enda fil. En .h-fil kan öppnas med vilken textredigerare som helst, Eclipse IDE, Microsoft Visual Studio IDE, Borland C++ kompilator och många andra applikationer.

## .H Filformat

En .h-fil är en vanlig textfil som har sina egna regler för att definiera syntaxen. Rubrikfiler kan innehålla följande information.

**`Variables`** - När det gäller objektorienterad programmering (OOP), innehåller en klasshuvudfil definitioner av alla klassnivåvariabler som är tillgängliga över implementeringens källkodsfiler
**`Methods Declaration`** - Alla metoddeklarationer ingår i .h-huvudfilerna för att vara tillgängliga över flera implementeringsfiler.
**`Non-Inline Function Definitions`** - Header-filer kan också innehålla definitioner av icke-inline-metoder.
**`Message Maps`** - En rubrikfil kan också innehålla meddelandekartor vid implementering av en MFC-källkod. I sådana fall är meddelandekartorna länkade till funktionalitetsimplementeringen som är länkad till UI-element som knapp, kryssruta, radioknappar, etc.


### Header Guards

Header-filer kan leda till komplexa fel där flera deklarationer ingår i samma fil som ett resultat av att andra header-filer läggs till. Dessa dubbletter av definitioner ger upphov till kompilatorfel. Denna problematiska situation kan undvikas via en mekanism som kallas header guard som är villkorliga kompileringsdirektiv som visas nedan.

```
#ifndef ANY_UNIQUE_NAME_HERE
#define ANY_UNIQUE_NAME_HERE

// your declarations (and certain types of definitions) here

#endif
```
Med denna rubrik kontrollerar förprocessorn om `ANY_UNIQUE_NAME_HERE` redan har definierats. Om rubriken upprepas inkluderas i samma fil, kommer innehållet i rubriken att ignoreras.

## H Fil Exempel

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

## Referenser

* [Header Filers - Microsoft](https://learn.microsoft.com/en-us/cpp/cpp/header-files-cpp?view=msvc-160)

