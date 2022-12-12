{
  "date" : "2019-10-11",
  "keywords" :[ "h", ".h", "какво е ah файл", "как да отворите h файл", "разширение", "файл", "h файл", "h файлов формат", "h файлово разширение", "Пример за H файл"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"H - C/C++ формат на заглавен файл",
  "description":"Научете за H файловия формат и API, които могат да създават и отварят H файл.",
  "linktitle" : "H",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-07"
}

## Какво е H файл?

Файлът, записан с **h файлово разширение**, е заглавен файл, използван във файлове на C/C++, за да включва декларацията на променливи, константи и функции. Те се препращат от [C++](/bg/programming/cpp/) файловете за изпълнение, които съдържат действителното изпълнение на тези функции. Заглавният файл .h може също да включва допълнителна информация, като дефиниции на макроси. Тези заглавни файлове са посочени в C/C++ файловете с помощта на директивата `#include`.

Нов C++ проект обикновено съдържа специален заглавен файл с името **stdafx.h** файл, който е началната точка за всички вериги на компилация и всички заглавни файлове могат да бъдат включени в този един файл. .h файл може да бъде отворен с всеки текстов редактор, Eclipse IDE, Microsoft Visual Studio IDE, Borland C++ компилатор и много други приложения.

## .H файлов формат

.h файлът е обикновен текстов файл, който има свои собствени правила за дефиниране на синтаксиса. Заглавните файлове могат да съдържат следната информация.

**`Променливи`** - В случай на обектно ориентирано програмиране (ООП), заглавен файл на клас съдържа дефиниции на всички променливи на ниво клас, които са достъпни във файловете с изходен код на изпълнение
**`Декларация на методи`** - Всички декларации на методи са включени в .h заглавните файлове, за да бъдат достъпни в множество файлове за изпълнение.
**`Дефиниции на невградени функции`** - Заглавните файлове могат също да съдържат дефиниции на невградени методи.
**`Карти на съобщенията`** - Заглавният файл може също да съдържа карти на съобщенията в случай на внедряване на изходен код на MFC. В такъв случай картите на съобщенията са свързани с изпълнението на функционалността, което е свързано с елементи на потребителския интерфейс като бутон, квадратче за отметка, радио бутони и др.


### Предпазители на главата

Заглавните файлове могат да доведат до сложни грешки, когато множество декларации са включени в един и същ файл в резултат на добавяне на други заглавни файлове. Тези дублирани дефиниции предизвикват грешки на компилатора. Тази проблемна ситуация може да бъде избегната чрез механизъм, наречен защита на заглавката, които са директиви за условно компилиране, както е показано по-долу.

```
#ifndef ANY_UNIQUE_NAME_HERE
#define ANY_UNIQUE_NAME_HERE

// your declarations (and certain types of definitions) here

#endif
```
С тази заглавка препроцесорът проверява дали `ANY_UNIQUE_NAME_HERE` вече е дефинирано. Ако заглавката се включва многократно в един и същи файл, съдържанието на заглавката ще бъде игнорирано.

## Пример за H файл

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

## Препратки

* [Филери за заглавки - Microsoft](https://docs.microsoft.com/en-us/cpp/cpp/header-files-cpp?view=msvc-160)

