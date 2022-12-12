{
  "date" : "2019-10-11",
  "keywords" :[ "h", ".h", "що таке файл ah", "як відкрити файл h", "розширення", "файл", "файл h", "формат файлу h", "розширення файлу h", "Приклад файлу H"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"H - C/C++ формат файлу заголовка",
  "description":"Дізнайтеся про формат файлу H та API, які можуть створювати та відкривати файл H.",
  "linktitle" : "H",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-07"
}

## Що таке файл H?

Файл, збережений із **розширенням h**, є файлом заголовка, який використовується у файлах C/C++ для включення оголошення змінних, констант і функцій. На них посилаються файли реалізації [C++](/uk/programming/cpp/), які містять фактичну реалізацію цих функцій. Файл заголовка .h також може містити додаткову інформацію, наприклад визначення макросів. На ці файли заголовків посилаються у файлах C/C++ за допомогою директиви `#include`.

Новий проект C++ зазвичай містить спеціальний файл заголовків під назвою **stdafx.h**, який є відправною точкою для всіх ланцюжків компіляції, і всі файли заголовків можуть бути включені в цей єдиний файл. Файл .h можна відкрити будь-яким текстовим редактором, Eclipse IDE, Microsoft Visual Studio IDE, компілятором Borland C++ і багатьма іншими програмами.

## Формат файлу .H

Файл .h — це звичайний текстовий файл із власними правилами визначення синтаксису. Файли заголовків можуть містити таку інформацію.

**`Змінні`** – у випадку об’єктно-орієнтованого програмування (ООП) файл заголовка класу містить визначення всіх змінних рівня класу, які доступні у файлах вихідного коду реалізації.
**`Оголошення методів`** – усі оголошення методів включені у файли заголовків .h, щоб бути доступними для кількох файлів реалізації.
**`Визначення невбудованих функцій`** - файли заголовків також можуть містити визначення невбудованих методів.
**`Карти повідомлень`** - файл заголовка також може містити карти повідомлень у разі реалізації вихідного коду MFC. У такому випадку карти повідомлень пов’язані з реалізацією функціональності, яка пов’язана з елементами інтерфейсу користувача, такими як кнопки, прапорці, перемикачі тощо.


### Захист голови

Файли заголовків можуть призвести до складних помилок, якщо в один файл включено кілька декларацій у результаті додавання інших файлів заголовків. Ці повторювані визначення викликають помилки компілятора. Цієї проблемної ситуації можна уникнути за допомогою механізму, що називається захистом заголовка, який є директивами умовної компіляції, як показано нижче.

```
#ifndef ANY_UNIQUE_NAME_HERE
#define ANY_UNIQUE_NAME_HERE

// your declarations (and certain types of definitions) here

#endif
```
За допомогою цього заголовка препроцесор перевіряє, чи вже визначено `ANY_UNIQUE_NAME_HERE`. Якщо заголовок неодноразово включається в той самий файл, вміст заголовка ігноруватиметься.

## Приклад файлу H

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

## Список літератури

* [Файли заголовків – Microsoft](https://docs.microsoft.com/en-us/cpp/cpp/header-files-cpp?view=msvc-160)

