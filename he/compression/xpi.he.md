{
  "date" : "2022-06-07",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XPI - קובץ חבילת מתקין חוצה פלטפורמות",
  "description":"למד על פורמט קובץ XPI וממשקי API שיכולים ליצור ולפתוח קובצי XPI.",
  "linktitle" : "XPI",
  "menu" : {
    "docs" : {
    "identifier": "compression-xpi",
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-07"
}

## מהו קובץ XPI?

קובץ XPI הוא ארכיון התקנה שנדחס כדי להקטין את גודל הקובץ. הוא משמש יישומי מוזילה להתקנת תוספים וקבצי הרחבות. הוא מכיל סקריפט התקנה או מניפסט בשורש הקובץ יחד עם מספר קבצי נתונים. קובץ XPI עשוי להכיל ערכת נושאים, ערכת כלים או תוספים של Firefox שהמשתמש יכול להתקין כדי להפוך לחלק מדפדפן Firefox, Thunderbird או SeaMonkey.

## פורמט קובץ XPI - מידע נוסף

קובצי XPI נשמרים בדיסק כארכיוני [ZIP](/he/compression/zip/) המשלבים קבצים מרובים לקובץ דחוס אחד. הקבצים בתוך קובץ XPI עשויים לכלול קובץ סקריפט התקנה כגון JS וקובצי אינטרנט כגון [CSS](/he/web/css/), [HTML](/he/web/html/) ו-[JSON](/he/web/json/ ). לפעמים, הוא עשוי להכיל גם קובצי תמונה [PNG](/he/image/png/) שישמשו כסמלים על ידי תוסף.

### כיצד להציג את התוכן של קובץ ה-XPI?

קובץ XPI הוא למעשה ארכיון ZIP שניתן לראות את תוכנו באמצעות השלבים הבאים.

* שנה את סיומת הקובץ מ-XPI ל-ZIP
* חלץ את תוכן הקובץ באמצעות כל כלי עזר סטנדרטי לביטול דחיסה כגון WinZip (Windows, Mac), 7-Zip (Windows) או Apple Archive Utility (Mac).

### התקן את קובץ XPI ב-Firefox Android

בעיקר אנשים סקרנים לדעת אם ניתן להתקין קבצי XPI בפיירפוקס במכשירי אנדרואיד. באנדרואיד, אתה יכול להתקין תוסף מקובץ XPI על ידי איתור הקובץ ופתיחתו עם Firefox.

## הפניות

* [XPIninstall - ויקיפדיה](https://en.wikipedia.org/wiki/XPInstall)
* [כיצד אוכל לפתוח הרחבת קובץ XPI?](https://support.mozilla.org/en-US/questions/1009049)

