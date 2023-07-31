{
  "date" : "2019-10-11",
  "keywords" :["h", ".h", "what is ah file", "how to open h file", "extension", "file", "h file", "h file format", "h file extension", "مثال ملف H"],
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"تنسيق ملف رأس H - C / C ++" ,
  "description":"تعرف على تنسيق ملف H وواجهات برمجة التطبيقات التي يمكنها إنشاء ملف H. وفتحه." ,
  "linktitle" : "H",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
} ,
  "lastmod" : "2021-05-07"
}

## ما هو ملف H؟

الملف المحفوظ بامتداد الملف ** h ** هو ملف رأس يُستخدم في ملفات C / C ++ ليشمل تعريف المتغيرات والثوابت والوظائف. تتم الإشارة إلى هذه بواسطة ملفات تنفيذ [C++](/ar/programming/cpp/) التي تحتوي على التنفيذ الفعلي لهذه الوظائف. يمكن أن يتضمن ملف الرأس h. أيضًا معلومات إضافية مثل تعريفات الماكرو. تتم الإشارة إلى ملفات الرأس هذه في ملفات C / C ++ باستخدام التوجيه `# include`.

عادةً ما يحتوي مشروع C ++ الجديد على ملف رأس خاص بالاسم ** stdafx.h ** ملف يمثل نقطة البداية لجميع سلاسل الترجمة ويمكن تضمين جميع ملفات الرأس في هذا الملف الفردي. يمكن فتح ملف .h باستخدام أي محرر نصوص و Eclipse IDE و Microsoft Visual Studio IDE و Borland C ++ compiler والعديد من التطبيقات الأخرى.

## تنسيق ملف H.

ملف .h هو ملف نصي عادي له قواعده الخاصة لتعريف بناء الجملة. يمكن أن تحتوي ملفات الرأس على المعلومات التالية.

** `المتغيرات` ** - في حالة البرمجة الموجهة للكائنات (OOP) ، يحتوي ملف رأس الفئة على تعريفات لجميع متغيرات مستوى الفئة التي يمكن الوصول إليها عبر ملفات التعليمات البرمجية المصدر للتنفيذ
** "إعلان الطرق" ** - يتم تضمين كافة إقرارات الطرق في ملفات الرأس .h ليتم الوصول إليها عبر ملفات تنفيذ متعددة.
** `تعريفات الوظائف غير المضمنة` ** - يمكن أن تحتوي ملفات الرأس أيضًا على تعريفات للطرق غير المضمنة.
** "خرائط الرسائل" ** - يمكن أن يحتوي ملف الرأس أيضًا على خرائط رسائل في حالة تنفيذ رمز مصدر MFC. في مثل هذه الحالة ، ترتبط خرائط الرسائل بتنفيذ الوظائف المرتبط بعناصر واجهة المستخدم مثل الزر ومربع الاختيار وأزرار الاختيار وما إلى ذلك.


### حراس الرأس

يمكن أن تؤدي ملفات الرأس إلى أخطاء معقدة حيث يتم تضمين العديد من التعريفات في نفس الملف نتيجة لإضافة ملفات رأس أخرى. هذه التعريفات المكررة تثير أخطاء المترجم. يمكن تجنب هذا الموقف الإشكالي من خلال آلية تسمى header guard وهي عبارة عن توجيهات تجميع مشروطة كما هو موضح أدناه.

```
#ifndef ANY_UNIQUE_NAME_HERE
#define ANY_UNIQUE_NAME_HERE

// your declarations (and certain types of definitions) here

#endif
```
باستخدام هذا الرأس ، يتحقق المعالج المسبق مما إذا كان `ANY_UNIQUE_NAME_HERE` قد تم تعريفه بالفعل. إذا تم تضمين الرأس بشكل متكرر في نفس الملف ، فسيتم تجاهل محتويات الرأس.

## مثال على ملف H

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

## مراجع

* [Header Filers - Microsoft](https://learn.microsoft.com/en-us/cpp/cpp/header-files-cpp؟view=msvc-160)

