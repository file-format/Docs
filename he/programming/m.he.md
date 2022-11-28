{
  "date" : "2019-10-11",
  "keywords": [ "M file", "M", "extension", "format", "M file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"M - קובץ קוד מקור של Matlab",
  "description":"למד על קובצי קוד מקור וממשקי API של Matlab .m שיכולים ליצור ולפתוח קובצי MF.",
  "linktitle" : "M",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

# M - קבצי קוד מקור של Matlab

## מהו קובץ M (Matlab)?

קובץ עם סיומת .m הוא קובץ קוד מקור המשמש את Matlab, פלטפורמת תכנות וחישוב מספרי המשמשת לניתוח, פיתוח אלגוריתמים ומודלים של סימולציה. כמו פורמטים אחרים של קבצי תכנות, קובץ M מכיל קוד מקור שמבצע פקודות Matlab כדי לשרטט גרפים, להפעיל סימולציות ופעולות מתמטיות אחרות. הדמיית Matlab בודדת יכולה להשתרע על פני מספר קובצי .m כאלה שיכולים לסווג את היישום בסקריפטים, מחלקות, פונקציות או הצהרות. ניתן לפתוח קבצי Matlab M עם כל עורך טקסט.

## פורמט קובץ Matlab M - מידע נוסף

קבצי Matlab .m הם קבצי טקסט המכילים קוד תכנות בשפת התכנות Matlab. ניתן לפתוח ולערוך אותם בכל עורך טקסט, ולשמור אותם בחזרה לביצוע בתוכנת Matlab. Matlab עצמו מכיל עורך Live המשמש ליצירת סקריפטים שהוא שילוב של קוד, פלט וטקסט מעוצב.

### קבצי פונקציית Matlab

כמו שפות תכנות אחרות, אתה יכול ליצור קובץ .m המכיל רק את ההגדרה של פונקציה שמבצעת משימה ספציפית בלבד. קבצים כאלה נשמרים גם עם סיומת .m ומיישמים את הפונקציונליות הקשורה לפונקציה זו בלבד.

### דוגמה לקובץ .M

להלן דוגמה לקובץ פונקציית Matlab המחשבת את הזמן שלוקח לאובייקט שנפל מגובה h.

```C++
function t= TimeToGround(h)  
  t=sqrt(h/4.9);
end
```

כדי לקרוא לפונקציה זו מעורך Matlab או מקובץ .m אחר, ניתן להשתמש בקוד הבא.
```C++
TimeToGround(100)
```

## הפניות

* [Matlab - פורמטי קבצים נתמכים](https://www.mathworks.com/help/matlab/standard-file-formats.html)
* [שימוש ב-Matlab](https://www.maths.unsw.edu.au/sites/default/files/MatlabSelfPaced/lesson0/MatlabLesson0_Mfiles.html)

# M - קובץ יישום Objective-C

## מהו קובץ M (Objective-C)?

קובץ M מכונה גם קובץ יישום המכיל קוד מקור של מחלקה שנכתבה בשפת Objective-C, שפת תכנות המשמשת לכתיבת יישומי תוכנה עבור OS X ו- iOS. Objective-C היא שפת התכנות העיקרית המשמשת את ממשקי ה-API העיקריים של אפל, Cocoa ו-Cocoa Touch, עבור פלטפורמות אלה. יישום תוכנה יחיד שפותח בשפה זו עשוי להכיל מספר קובצי .m, המכילים את היישום של מחלקות התוכנית. ניתן לפתוח אותם באמצעות Apple XCode, jEdit ועורכי טקסט נפוצים אחרים.

## פורמט קובץ Objective-C M - מידע נוסף

קבצי M נכתבים בפורמט טקסט רגיל תוך שימוש בתחביר התכנות של Objective-C. כל שיטה של מחלקה חייבת להיות מוגדרת עם כל הקוד הדרוש לה בקבצי היישום הללו. קבצי M ליישום אלה יכולים לייבא קובץ כותרת .h אחד או יותר לפי הדרישות. הצהרת import אומרת לקומפיילר היכן למצוא את קובץ ה-header ששייך לקובץ היישום הזה. הצהרת הייבוא כתובה כדלקמן.

```C++
#import "network.h"
```

כל מימוש של קובץ M מתחיל עם ההנחיה `@implementation`, ואחריו שם קובץ מחלקת המימוש. לאחר מכן, כל יישום השיטות המוצהרות בקובץ הכותרות.

### דוגמה לפורמט קובץ M

```C++
UrlConnection.m

#import "UrlConnection.h"

@implementation UrlConnection

(void)connect {
    // In here would be code to attempt a connection to the
    // specified URL, while possibly handling connection errors.
    //
}

 + (BOOL)canHandleRequest:(NSString \*)type
                   forUrl:(NSString \*)url {
    //And in here would be code to see if the given URL passed
    // in is capable of handling the HTTP request type specified
    // by the "type" parameter. It will return YES or NO.
 }

 @end
```

## הפניות
* [על מטרה C](https://developer.apple.com/library/archive/documentation/Cocoa/Conceptual/ProgrammingWithObjectiveC/Introduction/Introduction.html#//apple_ref/doc/uid/TP40011210-CH1-SW1)
* [מדריך אובייקט-C](https://blog.teamtreehouse.com/beginners-guide-objective-c-classes-objects)

