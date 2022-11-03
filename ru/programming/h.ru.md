{
  "date" : "2019-10-11",
  "keywords" :[ "h", ".h", "что такое файл ah", "как открыть файл h", "расширение", "файл", "файл h", "формат файла h", "расширение файла h", "Пример H-файла"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"H - Формат файла заголовка C/C++",
  "description":"Узнайте о формате файла H и API-интерфейсах, которые могут создавать и открывать файл H.",
  "linktitle" : "H",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-07"
}

## .H вариант №

Файл, сохраненный с расширением **h**, представляет собой заголовочный файл, используемый в файлах C/C++ для включения объявлений переменных, констант и функций. На них ссылаются файлы реализации [C++](/ru/programming/cpp/), которые содержат фактическую реализацию этих функций. Файл заголовка .h также может содержать дополнительную информацию, например определения макросов. На эти заголовочные файлы ссылаются в файлах C/C++ с помощью директивы `#include`.

Новый проект C++ обычно содержит специальный заголовочный файл с именем **stdafx.h**, который является отправной точкой для всех цепочек компиляции, и все заголовочные файлы могут быть включены в этот единственный файл. Файл .h можно открыть в любом текстовом редакторе, Eclipse IDE, Microsoft Visual Studio IDE, компиляторе Borland C++ и многих других приложениях.

## Формат файла .H

Файл .h — это обычный текстовый файл, который имеет свои собственные правила для определения синтаксиса. Заголовочные файлы могут содержать следующую информацию.

**`Переменные`** — в случае объектно-ориентированного программирования (ООП) файл заголовка класса содержит определения всех переменных уровня класса, которые доступны в файлах исходного кода реализации.
**`Объявление методов`** — все объявления методов включены в файлы заголовков .h, чтобы быть доступными для нескольких файлов реализации.
**`Определения невстроенных функций`** — заголовочные файлы также могут содержать определения невстроенных методов.
**`Карты сообщений`** — файл заголовка также может содержать карты сообщений в случае реализации исходного кода MFC. В таком случае карты сообщений связаны с реализацией функциональности, которая связана с элементами пользовательского интерфейса, такими как кнопка, флажок, переключатель и т. д.


### Защита заголовка

Файлы заголовков могут привести к сложным ошибкам, когда несколько объявлений включены в один и тот же файл в результате добавления других файлов заголовков. Эти повторяющиеся определения вызывают ошибки компилятора. Этой проблемной ситуации можно избежать с помощью механизма, называемого защитой заголовка, который представляет собой директивы условной компиляции, как показано ниже.

```
#ifndef ANY_UNIQUE_NAME_HERE
#define ANY_UNIQUE_NAME_HERE

// your declarations (and certain types of definitions) here

#endif
```
С помощью этого заголовка препроцессор проверяет, было ли уже определено ANY_UNIQUE_NAME_HERE. Если заголовок повторно включен в один и тот же файл, содержимое заголовка будет проигнорировано.

## Пример H-файла

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

## использованная литература

* [Файлы заголовков — Microsoft] (https://docs.microsoft.com/en-us/cpp/cpp/header-files-cpp?view=msvc-160)

