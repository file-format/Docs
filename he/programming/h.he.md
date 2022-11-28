{
  "date" : "2019-10-11",
  "keywords" :[ "h", ".h","מהו קובץ ah","כיצד לפתוח קובץ h", "הרחבה", "קובץ", "קובץ h","פורמט קובץ h", "סיומת קובץ h", "דוגמה לקובץ H"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"H - C/C++ פורמט קובץ כותרת",
  "description":"למד על פורמט קובץ H וממשקי API שיכולים ליצור ולפתוח קובץ H.",
  "linktitle" : "H",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-07"
}

## מהו קובץ H?

קובץ שנשמר עם **סיומת קובץ h** הוא קובץ כותרת המשמש בקבצי C/C++ כדי לכלול הצהרת משתנים, קבועים ופונקציות. אלה מופנים על ידי קובצי היישום [C++](/he/programming/cpp/) המכילים את היישום בפועל של פונקציות אלה. קובץ כותרת .h יכול לכלול גם מידע נוסף כגון הגדרות מאקרו. קבצי כותרות אלה מוזכרים בקבצי C/C++ באמצעות ההנחיה '#include'.

פרוייקט C++ חדש מכיל בדרך כלל קובץ כותרת מיוחד בשם קובץ **stdafx.h** המהווה נקודת ההתחלה לכל שרשראות ההידור וניתן לכלול את כל קבצי הכותרות בקובץ בודד זה. ניתן לפתוח קובץ .h עם כל עורך טקסט, Eclipse IDE, Microsoft Visual Studio IDE, מהדר Borland C++ ועוד הרבה יישומים אחרים.

## .H פורמט קובץ

קובץ .h הוא קובץ טקסט רגיל שיש לו כללים משלו להגדרת התחביר. קובצי כותרות יכולים להכיל את המידע הבא.

**`משתנים`** - במקרה של תכנות מונחה עצמים (OOP), קובץ כותרת מחלקה מכיל הגדרות של כל משתני רמת המחלקה הנגישים בכל קובצי קוד המקור של היישום
**`הצהרת שיטות`** - כל הצהרות השיטות נכללות בקבצי ה-.h header כדי להיות נגישים על פני מספר קובצי יישום.
**`הגדרות פונקציות שאינן מוטבעות`** - קובצי כותרת יכולים להכיל גם הגדרות של מתודות שאינן מוטבעות.
**`מפות הודעות`** - קובץ כותרת יכול להכיל גם מפות הודעות במקרה של יישום קוד מקור של MFC. במקרה כזה, מפות ההודעות מקושרות ליישום הפונקציונליות המקושר לרכיבי ממשק משתמש כגון כפתור, תיבת סימון, לחצני בחירה וכו'.


### מגני ראשים

קובצי כותרות יכולים להעלות שגיאות מורכבות כאשר מספר הצהרות נכללות באותו קובץ כתוצאה מהוספת קובצי כותרות אחרים. הגדרות כפולות אלו מעלות שגיאות מהדר. ניתן להימנע ממצב בעייתי זה באמצעות מנגנון הנקרא Header guard שהם הנחיות קומפילציה מותנות כפי שמוצג להלן.

```
#ifndef ANY_UNIQUE_NAME_HERE
#define ANY_UNIQUE_NAME_HERE

// your declarations (and certain types of definitions) here

#endif
```
עם כותרת זו, המעבד המקדים בודק אם ה- `ANY_UNIQUE_NAME_HERE` כבר הוגדר. אם הכותרת נכללת שוב ושוב באותו קובץ, יתעלם מתוכן הכותרת.

## H דוגמה לקובץ

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

## הפניות

* [Header Filers - Microsoft](https://docs.microsoft.com/en-us/cpp/cpp/header-files-cpp?view=msvc-160)

