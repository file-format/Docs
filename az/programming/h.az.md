{
  "date": "2019-10-11",
  "keywords": [
"h",
".h",
"ah faylı nədir",
"h faylını necə açmaq olar",
"uzadılması",
"fayl",
"h faylı",
"h fayl formatı",
"h fayl uzantısı",
"H fayl nümunəsi"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "H - C/C++ Başlıq Fayl Formatı",
  "description": "H faylı yarada və aça bilən H fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "H",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming--azh"
}
},
  "lastmod": "2021-05-07"
}

## H faylı nədir?

**h fayl uzantısı** ilə saxlanılan fayl dəyişənlərin, sabitlərin və funksiyaların bəyannaməsini daxil etmək üçün C/C++ fayllarında istifadə olunan başlıq faylıdır. Bunlara bu funksiyaların real icrasını ehtiva edən [C++](/programming/cpp/) icra faylları istinad edilir. .h başlıq faylına Makro tərifləri kimi əlavə məlumat da daxil ola bilər. Bu başlıq fayllarına `#include` direktivindən istifadə etməklə C/C++ fayllarında istinad edilir.

Yeni C++ layihəsi adətən bütün kompilyasiya zəncirləri üçün başlanğıc nöqtəsi olan **stdafx.h** adlı xüsusi başlıq faylını ehtiva edir və bütün başlıq faylları bu tək fayla daxil edilə bilər. .h faylı istənilən mətn redaktoru, Eclipse IDE, Microsoft Visual Studio IDE, Borland C++ kompilyatoru və bir çox başqa proqramlarla aça bilər.

## .H Fayl Formatı

.h faylı sintaksisi müəyyən etmək üçün öz qaydaları olan düz mətn faylıdır. Başlıq faylları aşağıdakı məlumatları ehtiva edə bilər.

**`Dəyişənlər`** - Obyekt yönümlü proqramlaşdırma (OOP) vəziyyətində, sinif başlıq faylı həyata keçirmə mənbə kodu faylları vasitəsilə əldə edilə bilən bütün sinif səviyyəli dəyişənlərin təriflərini ehtiva edir.
**`Metod Bəyannaməsi`** - Bütün metodlar bəyannamələri çoxsaylı icra faylları arasında əlçatan olmaq üçün .h başlıq fayllarına daxil edilmişdir.
**`Qeyri-sətirli Funksiya Tərifləri`** - Başlıq fayllarında qeyri-sətirli metodların tərifləri də ola bilər.
**`Mesaj Xəritələri`** - MFC mənbə kodunun tətbiqi zamanı başlıq faylında mesaj xəritələri də ola bilər. Bu halda, mesaj xəritələri düymə, onay qutusu, radio düymələri və s. kimi UI elementləri ilə əlaqəli funksionallıq tətbiqi ilə əlaqələndirilir.


### Başlıq Mühafizəçiləri

Başlıq faylları digər başlıq fayllarının əlavə edilməsi nəticəsində eyni fayla çoxsaylı bəyannamələrin daxil edildiyi mürəkkəb xətalara səbəb ola bilər. Bu dublikat təriflər kompilyator xətalarını artırır. Bu problemli vəziyyətin qarşısını aşağıda göstərildiyi kimi şərti tərtib direktivləri olan başlıq mühafizəsi adlı mexanizm vasitəsilə almaq olar.

```
#ifndef ANY_UNIQUE_NAME_HERE
#define ANY_UNIQUE_NAME_HERE

// your declarations (and certain types of definitions) here

#endif
```
Bu başlıqla preprosessor `ANY_UNIQUE_NAME_HERE`-nin artıq müəyyən edilib-edilmədiyini yoxlayır. Başlıq təkrar-təkrar eyni fayla daxil edilərsə, başlığın məzmunu nəzərə alınmayacaq.

## H fayl nümunəsi

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

## İstinadlar

* [Başlıq Filers - Microsoft](https://learn.microsoft.com/en-us/cpp/cpp/header-files-cpp?view=msvc-160)


