{
  "date" : "2019-10-11",
  "keywords" :[ "h", ".h","co je soubor ah","jak otevřít soubor h", "přípona", "soubor", "soubor h","formát souboru h", "přípona souboru h", "Příklad souboru H"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"H - C/C++ formát souboru záhlaví",
  "description":"Další informace o formátu souboru H a rozhraních API, která mohou vytvořit a otevřít soubor H.",
  "linktitle" : "H",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-07"
}

## Co je soubor H?

Soubor uložený s příponou **h** je hlavičkový soubor používaný v souborech C/C++ k zahrnutí deklarace proměnných, konstant a funkcí. Na ně odkazují implementační soubory [C++](/cs/programming/cpp/), které obsahují skutečnou implementaci těchto funkcí. Soubor záhlaví .h může také obsahovat další informace, jako jsou definice maker. Na tyto hlavičkové soubory se odkazuje v souborech C/C++ pomocí direktivy `#include`.

Nový projekt C++ obvykle obsahuje speciální hlavičkový soubor s názvem **stdafx.h** soubor, který je výchozím bodem pro všechny kompilační řetězce a všechny hlavičkové soubory mohou být zahrnuty do tohoto jediného souboru. Soubor .h lze otevřít pomocí libovolného textového editoru, Eclipse IDE, Microsoft Visual Studio IDE, Borland C++ kompilátoru a mnoha dalších aplikací.

## Formát souboru .H

Soubor .h je prostý textový soubor, který má svá vlastní pravidla pro definování syntaxe. Soubory záhlaví mohou obsahovat následující informace.

**`Proměnné`** – V případě objektově orientovaného programování (OOP) obsahuje soubor záhlaví třídy definice všech proměnných na úrovni třídy, které jsou přístupné napříč soubory zdrojového kódu implementace.
**`Deklarace metod`** - Všechny deklarace metod jsou zahrnuty v hlavičkových souborech .h, aby byly přístupné ve více souborech implementace.
**`Definice neinline funkcí`** - Soubory záhlaví mohou také obsahovat definice neinline metod.
**`Mapy zpráv`** - Soubor záhlaví může také obsahovat mapy zpráv v případě implementace zdrojového kódu MFC. V takovém případě jsou mapy zpráv propojeny s implementací funkčnosti, která je propojena s prvky uživatelského rozhraní, jako je tlačítko, zaškrtávací políčko, přepínače atd.


### Chrániče hlavy

Soubory záhlaví mohou způsobit složité chyby, pokud je do stejného souboru zahrnuto více deklarací v důsledku přidání jiných souborů záhlaví. Tyto duplicitní definice způsobují chyby kompilátoru. Této problematické situaci lze předejít pomocí mechanismu zvaného header guard, což jsou direktivy podmíněné kompilace, jak je ukázáno níže.

```
#ifndef ANY_UNIQUE_NAME_HERE
#define ANY_UNIQUE_NAME_HERE

// your declarations (and certain types of definitions) here

#endif
```
Pomocí této hlavičky preprocesor zkontroluje, zda již bylo definováno `ANY_UNIQUE_NAME_HERE`. Pokud je záhlaví opakovaně zahrnuto do stejného souboru, obsah záhlaví bude ignorován.

## Příklad souboru H

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

## Reference

* [Filery záhlaví – Microsoft](https://learn.microsoft.com/en-us/cpp/cpp/header-files-cpp?view=msvc-160)

