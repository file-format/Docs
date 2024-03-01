{
  "date": "2019-10-11",
  "keywords": [
"h",
".h",
"mikä on ah-tiedosto",
"kuinka avata h-tiedosto",
"laajennus",
"tiedosto",
"h tiedosto",
"h tiedostomuoto",
"h tiedostopääte",
"H Tiedostoesimerkki"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "H - C/C++-otsikkotiedostomuoto",
  "description": "Opi H-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata H-tiedoston.",
  "linktitle": "H",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming--fih"
}
},
  "lastmod": "2021-05-07"
}

## Mikä on H-tiedosto?

Tiedosto, joka on tallennettu tunnisteella **h, on otsikkotiedosto, jota käytetään C/C++-tiedostoissa muuttujien, vakioiden ja funktioiden määrittelyyn. Näihin viittaavat [C++](/programming/cpp/)-toteutustiedostot, jotka sisältävät näiden toimintojen todellisen toteutuksen. .h-otsikkotiedosto voi sisältää myös lisätietoja, kuten makromääritelmiä. Näihin otsikkotiedostoihin viitataan C/C++-tiedostoissa käyttämällä #include-komentoa.

Uusi C++-projekti sisältää yleensä erityisen otsikkotiedoston nimeltä **stdafx.h**-tiedosto, joka on kaikkien käännösketjujen lähtökohta ja kaikki otsikkotiedostot voidaan sisällyttää tähän yhteen tiedostoon. .h-tiedoston voi avata millä tahansa tekstieditorilla, Eclipse IDE:llä, Microsoft Visual Studio IDE:llä, Borland C++ -kääntäjällä ja monilla muilla sovelluksilla.

## .H-tiedostomuoto

.h-tiedosto on pelkkä tekstitiedosto, jolla on omat sääntönsä syntaksin määrittämiseksi. Otsikkotiedostot voivat sisältää seuraavat tiedot.

**`Muuttujat`** – Object Oriented Programming (OOP) -ohjelmoinnin tapauksessa luokan otsikkotiedosto sisältää määritelmät kaikista luokkatason muuttujista, jotka ovat käytettävissä toteutuksen lähdekooditiedostoissa.
**`Methode Declaration`** - Kaikki menetelmäilmoitukset sisältyvät .h-otsikkotiedostoihin, jotta niitä voidaan käyttää useissa toteutustiedostoissa.
**`Non-inline Function Definitions`** - Otsikkotiedostot voivat sisältää myös ei-inline-menetelmien määritelmiä.
**`Viestikartat`** - Otsikkotiedosto voi sisältää myös viestikarttoja MFC-lähdekoodin toteutuksen tapauksessa. Tällöin viestikartat on linkitetty toiminnallisuuden toteutukseen, joka on linkitetty käyttöliittymäelementteihin, kuten painike, valintaruutu, valintanapit jne.


### Yläsuojat

Otsikkotiedostot voivat aiheuttaa monimutkaisia virheitä, jos samaan tiedostoon sisältyy useita ilmoituksia muiden otsikkotiedostojen lisäämisen seurauksena. Nämä kaksoismääritykset aiheuttavat kääntäjävirheitä. Tämä ongelmallinen tilanne voidaan välttää otsikkovartijaksi kutsutulla mekanismilla, jotka ovat ehdollisia käännösdirektiivejä, kuten alla on esitetty.

```
#ifndef ANY_UNIQUE_NAME_HERE
#define ANY_UNIQUE_NAME_HERE

// your declarations (and certain types of definitions) here

#endif
```
Tämän otsikon avulla esiprosessori tarkistaa, onko ANY_UNIQUE_NAME_HERE jo määritetty. Jos otsikko sisällytetään toistuvasti samaan tiedostoon, otsikon sisältö ohitetaan.

## H Tiedostoesimerkki

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

## Viitteet

* [Otsikkotiedostot – Microsoft](https://learn.microsoft.com/en-us/cpp/cpp/header-files-cpp?view=msvc-160)


