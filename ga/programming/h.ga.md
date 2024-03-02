{
  "date": "2019-10-11",
  "keywords": [
"h",
".h",
"cad é comhad ah",
"Conas comhad a oscailt h",
"síneadh",
"comhad",
"h comhad",
"h formáid comhaid",
"h síneadh comhad",
"H Sampla Comhad"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "H - C/C++ Formáid Chomhaid Ceanntásca",
  "description": "Foghlaim faoi fhormáid comhaid H agus APIanna ar féidir leo comhad H a chruthú agus a oscailt.",
  "linktitle": "H",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming--gah"
}
},
  "lastmod": "2021-05-07"
}

## Cad is comhad H ann?

Is comhad ceanntásca é comhad a shábháiltear le **h síneadh comhad** a úsáidtear i gcomhaid C/C++ chun dearbhú athróg, tairisigh agus feidhmeanna a chur san áireamh. Tarchuirtear iad seo ag na comhaid feidhmithe [C++](/programming/cpp/) ina bhfuil cur i bhfeidhm iarbhír na bhfeidhmeanna seo. Is féidir faisnéis bhreise ar nós sainmhínithe Macra a áireamh i gcomhad ceanntásca .h. Déantar tagairt do na comhaid ceanntásc seo sna comhaid C/C++ ag baint úsáide as an treoir `#include`.

De ghnáth bíonn comhad ceanntásca speisialta i dtionscadal C++ nua darb ainm comhad **stdafx.h** arb é an pointe tosaigh do na slabhraí tiomsaithe go léir agus is féidir na comhaid ceanntásc go léir a áireamh sa chomhad singil seo. Is féidir comhad .h a oscailt le haon eagarthóir téacs, Eclipse IDE, Microsoft Visual Studio IDE, tiomsaitheoir Borland C++ agus go leor feidhmchlár eile.

## .H Formáid Chomhaid

Is comhad gnáth-théacs é comhad .h a bhfuil a rialacha féin aige chun an chomhréir a shainiú. Is féidir an fhaisnéis seo a leanas a bheith i gcomhaid cheanntásc.

**`Athróga`** - I gcás Ríomhchláraithe atá Dírithe ar Oibiachtaí (OOP), i gcomhad ceanntásca ranga tá sainmhínithe ar gach athróg leibhéal ranga atá inrochtana ar fud na gcomhad cód foinse feidhmithe
**`Dearbhú Modhanna`** - Tá na dearbhuithe modhanna go léir san áireamh sna comhaid cheannteidil .h chun go mbeidh rochtain orthu thar ilchomhaid cur chun feidhme.
**`Sainmhínithe ar Fheidhm Neamh-Inlíne`** - Is féidir sainmhínithe ar mhodhanna neamhlíne a bheith i gcomhaid ceanntásca freisin.
**`Mapaí Teachtaireachta`** - Is féidir léarscáileanna teachtaireachta a bheith i gcomhad ceanntásc freisin i gcás go gcuirfear cód foinse MFC i bhfeidhm. I gcás den sórt sin, tá na léarscáileanna teachtaireachta nasctha le cur i bhfeidhm feidhmiúlacht atá nasctha le heilimintí Chomhéadain cosúil le cnaipe, ticbhosca, cnaipí raidió, etc.


### Gardaí Ceannteidil

Is féidir earráidí casta a dhéanamh i gcomhaid cheanntásc nuair a áirítear dearbhuithe iolracha sa chomhad céanna mar thoradh ar chomhaid cheanntásc eile a chur leis. Ardaíonn na sainmhínithe dúblacha seo earráidí tiomsaitheora. Is féidir an cás fadhbach seo a sheachaint trí mheicníocht ar a dtugtar garda ceanntásca atá ina dtreoracha tiomsaithe coinníollach mar a thaispeántar thíos.

```
#ifndef ANY_UNIQUE_NAME_HERE
#define ANY_UNIQUE_NAME_HERE

// your declarations (and certain types of definitions) here

#endif
```
Leis an gceanntásc seo, seiceálann an réamhphróiseálaí an bhfuil an `ANY_UNIQUE_NAME_HERE` sainithe cheana. Má chuirtear an ceanntásc san áireamh arís agus arís eile sa chomhad céanna, ní thabharfar aird ar a bhfuil sa cheanntásc.

## H Sampla Comhad

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

## Tagairtí

* [Comhdóirí Ceanntásc - Microsoft](https://learn.microsoft.com/en-us/cpp/cpp/header-files-cpp?view=msvc-160)


