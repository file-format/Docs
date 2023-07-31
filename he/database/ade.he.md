{
  "date" : "2021-08-29",
  "keywords" :[ "ade", "סיומת", "קובץ", "פורמט קובץ", "סוג קובץ מסד נתונים", "תבנית קובץ מסד נתונים", "מיקרוסופט אקסס" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"למד על פורמט קובץ ADE וממשקי API שיכולים ליצור ולפתוח קובצי ADE.",
  "title" :"ADE - Access Project Extension File",
  "linktitle" : "ADE",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-08-29"
}

## מהו קובץ ADE?

קובץ עם סיומת .ade הוא קובץ Microsoft Access Project המכיל את הפלט הקומפילציה של המידע הכלול בקובץ הפרויקט של Microsoft Access ADP. מידע בקובץ פרויקט Access, מלבד Visual Basic for Applications (VBA), זמין בצורה מורכבת בקובצי ADE. הנתונים מאוחסנים בפורמט דחוס בקבצים אלה כדי להקטין את גודל הקובץ ולשפר את הביצועים ב-Access. מכיוון ש-ADE הוא הפלט המהודר של קובץ הפרויקט של Access, כל קוד מקור VBA שהוא חלק מהפרויקט, נשאר מוגן בכך שהוא לא מאפשר לו להיות חלק מהפלט. ניתן לפתוח קבצי ADE ב-Microsoft Access 365.

## פורמט קובץ ADE - מידע נוסף

ADE הם קבצי Access Database מהודרים המאוחסנים בדיסק כקבצים בינאריים. מבנה הקבצים הפנימי של קבצים אלה אינו ידוע.

קבצי ADE יכולים ליצור בעיות בפתיחה בהתבסס על הגרסה של Microsoft Access ששימשה ליצירת קבצים אלה. מסדי נתונים של Access המשתמשים בגירסת 64 סיביות של Microsoft Access 2010 ואשר מורכבים כ-MDE, [ACCDE](/he/database/accde/), או קבצי ADE חייבים להיות מורכבים מחדש ב-Microsoft Access 2021 Service Pack 1 (SP1) כדי לעבוד נכון עם Access 2010 SP1. בעיה זו מתרחשת מכיוון ש-Access 2010 SP1 משתמש בגרסה חדשה יותר של הקובץ VBE7.dll (גרסה 7.00.1619).

## הפניות

* [בעיה עם Access ADE Files](https://learn.microsoft.com/en-us/office/troubleshoot/access/error-run-compiled-mde-accde-ade)
* [באיזה פורמטי קבצים יש להשתמש](https://support.microsoft.com/en-us/office/which-access-file-format-should-i-use-012d9ab3-d14c-479e-b617-be66f9070b41)

