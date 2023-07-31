{
  "date" : "2021-06-29",
  "keywords" :[ "DLL", "הרחבה", "קובץ", "פורמט", "מערכת", "ספריית קישורים דינמית", "הגדרות", "תוכניות", "מחשב", "אפליקציה" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DLL - ספריית קישורים דינמית",
  "description":"למד על פורמט קובץ DLL וממשקי API שיכולים ליצור ולפתוח קבצי DLL.",
  "linktitle" : "DLL",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-06-29"
}

## מהו קובץ DLL? ##

קובץ DLL או ספריית קישורים דינמית הם סוג של קובץ הפעלה. זהו אחד מקבצי ההרחבה הנפוצים ביותר במכשיר שלך והוא מאוחסן בדרך כלל בתיקיית System32 ב-Windows שלך. קובץ הסיומת DLL פותח על ידי מיקרוסופט והוא נמצא בשימוש עממי על ידם. יש לו דירוג משתמש גבוה בפופולריות. ה-DLL פועל כמדף המכיל את *מנהלי התקנים/נהלים/פונקציות/מאפיינים* שתוכננו ומיושמים עבור תוכנית/יישום על ידי שרת Windows. ניתן גם לשתף קובץ DLL בודד בין תוכניות חלונות שונות. קבצי הרחבות אלו חיוניים להפעלה חלקה של תוכניות Windows במכשיר שלך מכיוון שהם אחראים להפעלת והפעלת פונקציות שונות בתוכנית כגון כתיבה וקריאה של קבצים, התחברות למכשירים אחרים שהם חיצוניים להגדרה שלך.
עם זאת, ניתן לפתוח קבצים אלו רק במכשיר התומך בכל גרסה של Windows (Windows 7/Windows 10/וכו') ולכן לא ניתן לפתוח אותם ישירות במכשיר התומך ב-Mac OS. (אם ברצונך לפתוח קובץ DLL ב-Mac OS, יישומים חיצוניים שונים יכולים לעזור לפתוח אותם.)


## פורמט קובץ DLL ##

קובץ DLL פותח על ידי מיקרוסופט ויש לו את הסיומת ".dll" המייצגת את הסוג. זה היה חלק בלתי נפרד משרת Windows 1.0, ומעבר לכך. זהו סוג קובץ בינארי ונתמך על ידי כל הגירסאות של Microsoft Windows. סוג קובץ זה נוצר כאמצעי ליצירת מערכת ספרייה משותפת בתוך תוכנות Windows, כדי לאפשר עריכות או שינויים נפרדים ועצמאיים בספריות התוכנות ללא צורך בקישור מחדש של התוכנות.


## דוגמה DLL ##

קוד דוגמה לנקודת כניסה DLL ניתן למצוא להלן:

```
BOOL APIENTRY DllMain(
HANDLE hModule,// Handle to DLL module
DWORD ul_reason_for_call,// Reason for calling function
LPVOID lpReserved ) // Reserved
{
    switch ( ul_reason_for_call )
    {
        case DLL_PROCESS_ATTACHED: // A process is loading the DLL.
        break;
        case DLL_THREAD_ATTACHED: // A process is creating a new thread.
        break;
        case DLL_THREAD_DETACH: // A thread exits normally.
        break;
        case DLL_PROCESS_DETACH: // A process unloads the DLL.
        break;
}
    return TRUE;
}

```

## התייחסות ##

* [DLL - Microsoft](https://learn.microsoft.com/en-us/troubleshoot/windows-client/deployment/dynamic-link-library)
