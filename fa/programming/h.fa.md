{
  "date": "2019-10-11",
  "keywords": [
"ساعت",
".h",
"فایل ah چیست",
"نحوه باز کردن فایل h",
"افزونه",
"فایل",
"فایل h",
"فرمت فایل h",
"پسوند فایل h",
"نمونه فایل H"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "H - فرمت فایل هدر C/C++",
  "description": "درباره فرمت فایل H و APIهایی که می توانند فایل H را ایجاد و باز کنند، بیاموزید.",
  "linktitle": "H",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming--fah"
}
},
  "lastmod": "2021-05-07"
}

## فایل H چیست؟

یک فایل ذخیره شده با **پسوند فایل h** یک فایل هدر است که در فایل های C/C++ برای شامل اعلان متغیرها، ثابت ها و توابع استفاده می شود. اینها توسط فایلهای پیاده سازی [C++](/programming/cpp/) که شامل اجرای واقعی این توابع هستند ارجاع داده می شوند. یک فایل هدر .h همچنین می تواند شامل اطلاعات اضافی مانند تعاریف ماکرو باشد. این فایل‌های هدر در فایل‌های C/C++ با استفاده از دستور #include ارجاع می‌شوند.

یک پروژه ++C جدید معمولاً حاوی یک فایل هدر ویژه با نام **فایل stdafx.h** است که نقطه شروع همه زنجیره های کامپایل است و همه فایل های هدر را می توان در این فایل واحد گنجاند. یک فایل h را می توان با هر ویرایشگر متنی، Eclipse IDE، Microsoft Visual Studio IDE، کامپایلر Borland C++ و بسیاری از برنامه های کاربردی دیگر باز کرد.

## فرمت فایل .H

یک فایل .h یک فایل متنی ساده است که قوانین خاص خود را برای تعریف نحو دارد. فایل های هدر می توانند حاوی اطلاعات زیر باشند.

**«متغیرها»** - در مورد برنامه نویسی شی گرا (OOP)، یک فایل هدر کلاس شامل تعاریف همه متغیرهای سطح کلاس است که در فایل های کد منبع پیاده سازی قابل دسترسی هستند.
**«اعلام روش‌ها»** - تمام اعلان‌های روش‌ها در فایل‌های هدر .h گنجانده شده‌اند تا در چندین فایل پیاده‌سازی قابل دسترسی باشند.
**تعاریف توابع غیر درون خطی** - فایل های سرصفحه همچنین می توانند شامل تعاریف روش های غیر خطی باشند.
**`نقشه های پیام`** - یک فایل هدر همچنین می تواند حاوی نقشه های پیام در صورت اجرای کد منبع MFC باشد. در چنین حالتی، نقشه‌های پیام به اجرای عملکرد مرتبط می‌شوند که به عناصر UI مانند دکمه، چک باکس، دکمه‌های رادیویی و غیره مرتبط است.


### هدر گارد

فایل‌های هدر می‌توانند به خطاهای پیچیده تبدیل شوند که در آن چندین اعلان در یک فایل در نتیجه اضافه کردن فایل‌های هدر دیگر گنجانده می‌شود. این تعاریف تکراری باعث افزایش خطاهای کامپایلر می شود. این وضعیت مشکل ساز را می توان از طریق مکانیزمی به نام محافظ سرصفحه که دستورالعمل های کامپایل مشروط هستند، اجتناب کرد.

```
#ifndef ANY_UNIQUE_NAME_HERE
#define ANY_UNIQUE_NAME_HERE

// your declarations (and certain types of definitions) here

#endif
```
با این هدر، پیش پردازنده بررسی می کند که آیا «ANY_UNIQUE_NAME_HERE» قبلاً تعریف شده است یا خیر. اگر هدر به طور مکرر در یک فایل قرار داده شود، محتویات هدر نادیده گرفته می شود.

## نمونه فایل H

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

## منابع

* [Header Filers - Microsoft](https://learn.microsoft.com/en-us/cpp/cpp/header-files-cpp?view=msvc-160)


