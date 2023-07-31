{
  "date" : "2020-01-11",
  "keywords" :[ "x file", "x format file", "מהו קובץ x", "קובץ", "x example", "x extension file","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"X - פורמט קובץ DirectX 2.0",
  "description":"למד על פורמט קובץ DirectX X וממשקי API שיכולים לפתוח וליצור קבצי DirectX X.",
  "linktitle" : "X",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2020-01-11"
}

## מהו קובץ X?

קובץ עם סיומת .x מתייחס לפורמט קובץ 3D Graphics מדור קודם [DirectX](https://www.microsoft.com/en-us/download/search.aspx?q=directx) שהוצג עם Microsoft DirectX 2.0. הוא שימש לעיבוד גרפיקה תלת מימדית במשחקים ומציין את המבנים עבור רשתות, טקסטורות, אנימציות ואובייקטים המוגדרים על ידי המשתמש. זה הוצא משימוש מאז 2014 מכיוון שפורמט הקובץ Autodesk FBX משמש טוב יותר כפורמט מודרני יותר. X מונחה תבניות והוא נקי מכל ידע שימוש.

אתה יכול לפתוח קבצי DirectX X באמצעות Microsoft DirectX ועורכי טקסט נפוצים.

## פורמט קובץ X

[הפניה לקובץ X](https://learn.microsoft.com/en-us/windows/win32/direct3d9/dx9-graphics-reference-d3dx-x-file) מכיל מידע התייחסות עבור רכיבי ה-API המשמשים כדי עבודה עם קבצי DirectX .x. הפורמט מספק פרימיטיבים של נתונים ברמה נמוכה המשמשים יישומים אחרים כדי להגדיר פרימיטיבים ברמה גבוהה יותר באמצעות תבניות נתונים. DirectX 6.0 הציגה ממשקים ושיטות המאפשרות קריאה וכתיבה לקבצי .x. DirectX 3.0 הציגה גרסה בינארית של פורמט קובץ זה.

[הפניה לפורמט קובץ X](https://learn.microsoft.com/en-us/windows/win32/direct3d9/dx9-graphics-reference-x-file-format) שהוגדר על ידי DirectX 9 מכיל מידע עזר עבור ‎.x קבצים בקידוד בינארי כמו גם בטקסט.

### קידוד בינארי

[הפורמט הבינארי](https://learn.microsoft.com/en-us/windows/win32/direct3d9/binary-encoding) מגדיר את פורמט DirectX X כייצוג סמלי של פורמט הטקסט. אסימונים אלה יכולים להיות עצמאיים כדי לתת מבנה דקדוקי או יכולים להיות אסימונים נושאי תיעוד המספקים את הנתונים הדרושים.

#### כותרת

ניתן לקרוא ולכתוב את הכותרת הבינארית באמצעות ההגדרות הבאות.

```
#define XOFFILE_FORMAT_MAGIC \
  ((long)'x' + ((long)'o' << 8) + ((long)'f' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_VERSION \
  ((long)'0' + ((long)'3' << 8) + ((long)'0' << 16) + ((long)'2' << 24))

#define XOFFILE_FORMAT_BINARY \
  ((long)'b' + ((long)'i' << 8) + ((long)'n' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_TEXT   \
  ((long)'t' + ((long)'x' << 8) + ((long)'t' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_COMPRESSED \
  ((long)'c' + ((long)'m' << 8) + ((long)'p' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_FLOAT_BITS_32 \
  ((long)'0' + ((long)'0' << 8) + ((long)'3' << 16) + ((long)'2' << 24))

#define XOFFILE_FORMAT_FLOAT_BITS_64 \
  ((long)'0' + ((long)'0' << 8) + ((long)'6' << 16) + ((long)'4' << 24))
```

### קידוד טקסט

קבצי DirectX .x אינם תלויים באופן השימוש בקובץ ואינם ספציפיים לאף יישום. גישה מונחית תבנית זו מאפשרת להשתמש בפורמט קובץ .x על ידי כל יישום לקוח.


#### כותרת

הכותרת באורך משתנה היא חובה וחייבת להיות בתחילת זרם הנתונים. הכותרת מכילה את הנתונים הבאים.

| סוג | סוג משנה | גודל | תוכן | משמעות התוכן |
---|---|---|---|---|
|מספר קסם (חובה)| | 4 בתים |xof |
|מספר גרסה (נדרש) |מספר עיקרי |2 בתים |03 |גרסה עיקרית 3|
| |מספר קטן |2 בתים |02 |גרסה מינורית 2|
|סוג פורמט (חובה)| |4 בתים |"txt " |קובץ טקסט|
| | | |"bin "| קובץ בינארי|
| | | |"tzip"| קובץ טקסט דחוס MSZip|
| | | |"bzip"| MSZip קובץ בינארי דחוס|
|גודל ציפה (חובה)| |4 בתים| 0064| צפים של 64 סיביות|
| | | |0032 |צפים 32 סיביות|


## הפניות

* [X Files Legacy](https://learn.microsoft.com/en-us/windows/win32/direct3d9/x-files--legacy-)
* [הפניה לפורמט קובץ DirectX 9](https://learn.microsoft.com/en-us/windows/win32/direct3d9/dx9-graphics-reference-x-file-format)

