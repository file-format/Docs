{
  "date" : "2022-04-02",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"פורמט קובץ DDS- DirectDraw Surface Image File",
  "description":"למד על פורמט קובץ DDS וממשקי API שיכולים ליצור ולפתוח קובצי DDS.",
  "linktitle" : "DDS",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2022-04-02"
}

## מהו קובץ DDS?

קובץ DDS הוא קובץ תמונת רסטר המשתמש בפורמט המכולה DirectDraw Surface (DDS). הוא מאחסן מרקמים לא דחוסים ודחוסים (DXTn) ומיישם סוגים שונים לאחסון סוגים שונים של נתונים. זה גם תומך בכמה סוגים שונים של נתונים כמו טקסטורות בשכבה אחת, טקסטורות עם mipmaps, מפות קוביות, מפות נפח ומערכי טקסטורה. זה מאפשר לקבצי DDS לאחסן דגמי יחידות מרקם של משחקי וידאו בנוסף לתמונות דיגיטליות ורקע שולחן העבודה של Windows. פורמט קובץ DDS פותח על ידי מיקרוסופט לשימוש עם DirectX SDK.

## פורמט קובץ DDS

קבצי DDS נשמרים כקבצים בינאריים וניתן להשתמש בהם עם DirectX SDK. הוא מנצל את הכוח של DirectX כדי לפתח יישומי רינדור בזמן אמת כגון משחקי תלת מימד.

### פריסת קובץ DDS

[פריסת הקובץ DDS](https://learn.microsoft.com/en-us/windows/win32/direct3ddds/dx-graphics-dds-pguide#dds-file-layout) תועדה על ידי Microsoft בפירוט. קובץ DDS בינארי מכיל את המידע הבא.

* DWORD (מספר קסם) המכיל את ערך הקוד של ארבעה תווים 'DDS' (0x20534444).
* תיאור הנתונים בקובץ.

ה-DDS_HEADER מתאר את הנתונים וה-DDS_PIXELFORMAT מתאר את פורמט הפיקסלים. שניהם מחליפים את המבנים DDSURFACEDESC2, DDSCAPS2 ו-DDPIXELFORMAT DirectDraw 7 שהוצאו משימוש.

```
DWORD               dwMagic;
DDS_HEADER          header;
```

[מדריך התכנות של פורמט קובץ DDS](https://learn.microsoft.com/en-us/windows/win32/direct3ddds/dx-graphics-dds-pguide) מרחיב עוד יותר את הפרטים הטכניים של פורמט קובץ זה.

## הפניות

* [DDS - מאת ויקיפדיה](https://en.wikipedia.org/wiki/DirectDraw_Surface)
* [מדריך עזר טכני בפורמט קובץ PCX של ZSoft](http://qzx.com/pc-gpe/pcx.txt)

