{
  "date" : "2022-01-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"פורמט קובץ CMS - קובץ פרופיל שירות מנהל החיבורים",
  "description":"למד על קבצי CMS וממשקי API שיכולים ליצור ולפתוח קובצי CMS.",
  "linktitle" : "CMS",
  "menu" : {
    "docs" : {
      "identifier": "misc-cms",
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-12"
}

## מהו קובץ CMS?

קובץ CMS הוא קובץ נתונים המכיל מידע פרופיל המשמש את Microsoft Windows Connection Manager. זה מאפשר למשתמשים מרוחקים להתחבר לרשת באמצעות מידע פרופיל זה. מידע המאוחסן בתוך קובץ CMS כולל נתונים על מערכת ההפעלה של המשתמש והרשאות המשמשות ליצירת חיבור בין משתמש מרוחק לרשת. מנהלי מערכת CMS משתמשים ב-Connection Manager Administrator Kit (CMAK) כדי ליצור קובצי CMS.

## פורמט קובץ CMS - מידע נוסף

קבצי CMS אינם נמצאים בדרך כלל במחשבי משתמש. מכיוון שמשתמשים אלה משמשים במיוחד כדי לאפשר למשתמשים מרוחקים לרשת, תמצאו אותם במחשבים המשמשים לחיבור לרשת חברה או למשרד ספציפי מסוים. ברוב המקרים הוא משמש לחיבור לרשת ארגונית כמו Virtual Private Network (VPN) המוקדשת לחברה בלבד. בהיותך מנהל רשת, תגדיר גישה לרשת כזו עם Connection Manager כדי לאפשר לו לגשת לרשת החברה ממקום מרוחק.

### מה זה insdie CMS?

קובץ פרופיל CMS נוצר באמצעות מנהל החיבורים והוא ארוז עם קובצי תצורה אחרים לפני שהוא מסופק למשתמש מרוחק. קבצים נוספים אלה עשויים לכלול קובץ CMP ו- ו-INF שנארזים לצדם בקובץ [EXE](/he/executable/exe/). חבילה מלאה זו מסופקת למשתמש המרוחק לצורך התחברות לרשת.

## הפניות

* [הבנה והגדרה של Windows Connection Manager](https://learn.microsoft.com/en-us/windows-hardware/drivers/mobilebroadband/understanding-and-configuring-windows-connection-manager)

