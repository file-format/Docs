{
  "date": "2019-10-11",
  "keywords": [
"h",
".h",
"kas ir ah fails",
"kā atvērt h failu",
"pagarinājumu",
"failu",
"h failu",
"h faila formātā",
"h faila paplašinājums",
"H Faila piemērs"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "H — C/C++ galvenes faila formāts",
  "description": "Uzziniet par H faila formātu un API, kas var izveidot un atvērt H failu.",
  "linktitle": "H",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming--lvh"
}
},
  "lastmod": "2021-05-07"
}

## Kas ir H fails?

Fails, kas saglabāts ar **h faila paplašinājumu**, ir galvenes fails, ko izmanto C/C++ failos, lai iekļautu mainīgo, konstantu un funkciju deklarāciju. Uz tiem atsaucas [C++](/programming/cpp/) ieviešanas faili, kas satur šo funkciju faktisko ieviešanu. .h galvenes fails var ietvert arī papildu informāciju, piemēram, makro definīcijas. Uz šiem galvenes failiem ir atsauces C/C++ failos, izmantojot direktīvu #include.

Jauns C++ projekts parasti satur īpašu galvenes failu ar nosaukumu **stdafx.h** fails, kas ir sākumpunkts visām kompilācijas ķēdēm, un visus galvenes failus var iekļaut šajā vienā failā. .h failu var atvērt ar jebkuru teksta redaktoru, Eclipse IDE, Microsoft Visual Studio IDE, Borland C++ kompilatoru un daudzām citām lietojumprogrammām.

## .H faila formāts

.h fails ir vienkārša teksta fails, kuram ir savi sintakses definēšanas noteikumi. Galvenes faili var saturēt šādu informāciju.

**`Mainīgie`** — objektorientētas programmēšanas (OOP) gadījumā klases galvenes failā ir visu klases līmeņa mainīgo definīcijas, kas ir pieejamas ieviešanas avota koda failos.
**`Metožu deklarācija`** — visas metožu deklarācijas ir iekļautas .h galvenes failos, lai tās būtu pieejamas vairākos ieviešanas failos.
**`Neiekļautās funkciju definīcijas`** — galvenes faili var saturēt arī neiekļauto metožu definīcijas.
**`Ziņojumu kartes`** — MFC pirmkoda ieviešanas gadījumā galvenes failā var būt arī ziņojumu kartes. Šādā gadījumā ziņojumu kartes ir saistītas ar funkcionalitātes ieviešanu, kas ir saistīta ar lietotāja interfeisa elementiem, piemēram, pogai, izvēles rūtiņai, radio pogām utt.


### Galvenes sargi

Galvenes faili var radīt sarežģītas kļūdas, ja vienā failā ir iekļautas vairākas deklarācijas, pievienojot citus galvenes failus. Šīs dublētās definīcijas rada kompilatora kļūdas. No šīs problemātiskās situācijas var izvairīties, izmantojot mehānismu, ko sauc par galvenes aizsargu, kas ir nosacījuma kompilācijas direktīvas, kā parādīts tālāk.

```
#ifndef ANY_UNIQUE_NAME_HERE
#define ANY_UNIQUE_NAME_HERE

// your declarations (and certain types of definitions) here

#endif
```
Izmantojot šo galveni, priekšapstrādātājs pārbauda, vai ANY_UNIQUE_NAME_HERE jau ir definēts. Ja galvene tiek atkārtoti iekļauta vienā failā, galvenes saturs tiks ignorēts.

## H Faila piemērs

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

## Atsauces

* [Header Filers — Microsoft](https://learn.microsoft.com/en-us/cpp/cpp/header-files-cpp?view=msvc-160)


