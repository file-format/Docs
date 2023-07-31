{
  "date" : "2019-10-11",
  "keywords" :[ "h", ".h", "mi az ah fájl", "h fájl megnyitása", "kiterjesztés", "fájl", "h fájl", "h fájlformátum", "h fájl kiterjesztése", "H fájl példa"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"H - C/C++ fejlécfájl formátum",
  "description":"További információ a H fájlformátumról és az API-król, amelyek létrehozhatnak és megnyithatnak H fájlt.",
  "linktitle" : "H",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-07"
}

## Mi az a H fájl?

A **h fájlkiterjesztéssel** mentett fájl a C/C++ fájlokban használt fejlécfájl, amely tartalmazza a változók, konstansok és függvények deklarációját. Ezekre hivatkoznak a [C++](/hu/programming/cpp/) implementációs fájlok, amelyek ezen függvények tényleges megvalósítását tartalmazzák. A .h fejlécfájl további információkat is tartalmazhat, például makródefiníciókat. Ezekre a fejlécfájlokra hivatkoznak a C/C++ fájlok az "#include" direktíva használatával.

Egy új C++ projekt általában tartalmaz egy speciális fejlécfájlt **stdafx.h** néven, amely az összes fordítási lánc kiindulópontja, és az összes fejlécfájl belefoglalható ebbe az egyetlen fájlba. A .h fájl bármilyen szövegszerkesztővel, Eclipse IDE-vel, Microsoft Visual Studio IDE-vel, Borland C++ fordítóval és sok más alkalmazással megnyitható.

## .H fájlformátum

A .h fájl egyszerű szöveges fájl, amelynek saját szabályai vannak a szintaxis meghatározásához. A fejlécfájlok a következő információkat tartalmazhatják.

**`Változók`** – Objektumorientált programozás (OOP) esetén az osztályfejléc fájl tartalmazza az összes olyan osztályszintű változó definícióját, amely elérhető a megvalósítási forráskódfájlokon keresztül.
**`Methods Declaration`** – Az összes metódusdeklaráció szerepel a .h fejlécfájlokban, hogy több megvalósítási fájlon keresztül is elérhető legyen.
**`Non-line Function Definitions`** - A fejlécfájlok nem soron belüli metódusok definícióit is tartalmazhatják.
**`Üzenetleképezések`** - A fejlécfájl üzenetleképezéseket is tartalmazhat MFC forráskód megvalósítása esetén. Ebben az esetben az üzenettérképek a funkcionalitás megvalósításához kapcsolódnak, amely olyan felhasználói felület elemekkel van összekapcsolva, mint a gomb, jelölőnégyzet, rádiógombok stb.


### Fejlécvédők

A fejlécfájlok összetett hibákat okozhatnak, ha több deklaráció is szerepel ugyanabban a fájlban más fejlécfájlok hozzáadása következtében. Ezek az ismétlődő definíciók fordítóhibákat okoznak. Ez a problémás helyzet elkerülhető egy fejlécvédő mechanizmussal, amelyek feltételes fordítási direktívák, amint az alább látható.

```
#ifndef ANY_UNIQUE_NAME_HERE
#define ANY_UNIQUE_NAME_HERE

// your declarations (and certain types of definitions) here

#endif
```
Ezzel a fejléccel az előfeldolgozó ellenőrzi, hogy az `ANY_UNIQUE_NAME_HERE` már meghatározásra került-e. Ha a fejléc többször is szerepel ugyanabban a fájlban, a fejléc tartalma figyelmen kívül marad.

## H fájl példa

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

## Hivatkozások

* [Header Filers – Microsoft](https://learn.microsoft.com/en-us/cpp/cpp/header-files-cpp?view=msvc-160)

