{
  "date" : "2019-10-11",
  "keywords" :[ "h", ".h", "wat is ah-bestand", "hoe h-bestand te openen", "extensie", "bestand", "h-bestand", "h-bestandsformaat", "h-bestandsextensie", "H-bestandsvoorbeeld"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"H - C/C++ Header-bestandsindeling",
  "description":"Meer informatie over H-bestandsindeling en API's die H-bestanden kunnen maken en openen.",
  "linktitle" : "H",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-07"
}

## Wat is een H-bestand?

Een bestand dat is opgeslagen met de **h-bestandsextensie** is een headerbestand dat in C/C++-bestanden wordt gebruikt om de declaratie van variabelen, constanten en functies op te nemen. Hiernaar wordt verwezen door de [C++](/nl/programming/cpp/) implementatiebestanden die de daadwerkelijke implementatie van deze functies bevatten. Een .h-headerbestand kan ook aanvullende informatie bevatten, zoals macrodefinities. Naar deze header-bestanden wordt verwezen in de C/C++-bestanden met behulp van de `#include`-richtlijn.

Een nieuw C++-project bevat meestal een speciaal header-bestand met de naam **stdafx.h**-bestand dat het startpunt is voor alle compilatieketens en alle header-bestanden kunnen in dit enkele bestand worden opgenomen. Een .h-bestand kan worden geopend met elke teksteditor, Eclipse IDE, Microsoft Visual Studio IDE, Borland C++-compiler en vele andere toepassingen.

## .H-bestandsindeling

Een .h-bestand is een bestand met platte tekst dat zijn eigen regels heeft voor het definiëren van de syntaxis. Headerbestanden kunnen de volgende informatie bevatten.

**'Variabelen'** - In het geval van Object Oriented Programming (OOP), bevat een klasse-headerbestand definities van alle variabelen op klasseniveau die toegankelijk zijn via de broncodebestanden van de implementatie
**'Methods Declaration'** - Alle methodedeclaraties zijn opgenomen in de .h-headerbestanden om toegankelijk te zijn voor meerdere implementatiebestanden.
**'Niet-inline functiedefinities'** - Headerbestanden kunnen ook definities van niet-inline-methoden bevatten.
**`Message Maps`** - Een header-bestand kan ook message maps bevatten in het geval van een MFC-broncode-implementatie. In een dergelijk geval zijn de berichtenkaarten gekoppeld aan de functionaliteitsimplementatie die is gekoppeld aan UI-elementen zoals knop, selectievakje, keuzerondjes, enz.


### Header Guards

Headerbestanden kunnen complexe fouten veroorzaken wanneer meerdere declaraties in hetzelfde bestand zijn opgenomen als gevolg van het toevoegen van andere headerbestanden. Deze dubbele definities veroorzaken compilerfouten. Deze problematische situatie kan worden vermeden via een mechanisme genaamd header guard dat voorwaardelijke compilatierichtlijnen zijn, zoals hieronder weergegeven.

```
#ifndef ANY_UNIQUE_NAME_HERE
#define ANY_UNIQUE_NAME_HERE

// your declarations (and certain types of definitions) here

#endif
```
Met deze header controleert de preprocessor of de `ANY_UNIQUE_NAME_HERE` al is gedefinieerd. Als de header herhaaldelijk in hetzelfde bestand wordt opgenomen, wordt de inhoud van de header genegeerd.

## H-bestandsvoorbeeld

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

## Referenties

* [Header Files - Microsoft](https://docs.microsoft.com/en-us/cpp/cpp/header-files-cpp?view=msvc-160)

