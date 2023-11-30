{
  "date" : "2023-02-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"קובץ ADMX - פורמט קובץ תבנית ניהולי של מדיניות קבוצתית",
  "description":"למד על פורמט קובץ ADMX וכיצד לפתוח קבצי ADMX.",
  "linktitle" : "ADMX",
  "menu" : {
    "docs" : {
      "identifier" : "system-admx",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-14"
}

## מהו קובץ ADMX?

קובץ ADMX הוא קובץ תצורת מדיניות המשמש את תוכנת Microsoft Windows Group Policy המנהלת קבוצת מחשבים בקבוצה. זהו קובץ תבנית ניהול מבוסס XML והוצג עם Windows Vista Service Pack 1. קובצי ADMX מכילים הגדרות תצורה עבור חשבונות משתמש, תצורות מערכת הפעלה ויישומים. קבצי ADMX משמשים לאחסון ופריסה של התצורות לניהול מרכזי של מערכות מחשב רבות.

אתה יכול ליצור או לערוך קובצי ADMX באמצעות כל תואם XML, כל עורך טקסט או עורך אובייקטי מדיניות קבוצתיים של Microsoft.

## פורמט קובץ ADMX - מידע נוסף

קובצי ADMX מאוחסנים בפורמט הקובץ האוניברסלי [XML](/he/web/xml/) הניתן לקריאה אנושית. זהו פורמט קובץ רב לשוני ומאפשר למנהלי מערכת משפות שונות לעבוד עם אותם קבצי ADMX. קובצי ADMX החליפו את פורמט הקובץ הישן [ADM](/he/system/adm/) שהוא פורמט קובץ טקסט בפורמט Unicode. קובצי ADMX מציינים את מפתחות הרישום המשתנים כאשר משתנה הגדרת מדיניות קבוצתית מסוימת.

### מה אני יכול לעשות עם קובץ ADMX?

קובצי ADMX מגדירים אילו פעולות יש לאפשר למחשבי משתמש שהם חלק מקבוצה. המדיניות הקבוצתית כופה את הכללים שנקבעו בשילוב עם תוכנת Active Directory. קבצי ADMX מנוהלים מהחנות המרכזית במערכת ההפעלה Windows שהיא מיקום מרכזי בדומיין.

קובץ ADMX שנפרס בסביבת עבודה יכול לאפשר למנהלי מערכת ליישם מדיניות כגון:

* שליטה בשימוש באינטרנט
* הורדה של סוגים מסוימים של קבצים
* שימוש במכשירים נשלפים במערכות

## הפניות

* [קבצי תבנית ניהול - ADMX](https://learn.microsoft.com/en-us/mem/intune/configuration/administrative-templates-windows)
* [NetIQ - ניהול קבצי תבניות ניהוליות](https://www.netiq.com/documentation/group-policy-administrator-69/grouppolicyadministratoruserguide/data/administrativetemplatefiles.html)
* [SSDT](https://wiki.osdev.org/SSDT)

