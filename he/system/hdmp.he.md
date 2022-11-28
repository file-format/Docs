{
  "date" : "2022-08-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"קובץ HDMP - Windows Heap Dump Format",
  "description":"למד על פורמט קבצי HDMP וממשקי API שיכולים ליצור ולפתוח קובצי HDMP.",
  "linktitle" : "HDMP",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2022-08-19"
}

## מהו קובץ HDMP?

קובץ HDMP הוא dump זיכרון לא דחוס כאשר יישום או תוכנית קורסים עקב שגיאה. הוא נוצר רק על ידי Windows XP/Vista ומכיל dump של סטטוס היישום כאשר הוא קרס. בהיותם לא דחוסים, קבצי ה-HDMP תופסים יותר מקום בדיסק בהשוואה לקבצי Minidump [MDMP](/he/system/mdmp/) שנדחסים למטרת דיווח.

יישומים שניתן להשתמש בהם כדי **פתיחה** או ניתוח קובצי HDMP כוללים את Microsoft Visual Studio עם כלי ניפוי באגים עבור Windows.

## פורמט קובץ HDMP

קובצי HDMP מאוחסנים בדיסק כקבצים בינאריים ואינם מספקים תועלת אם הם נפתחים ללא יישומים מתאימים. אלה מכילים נתוני מערכת רלוונטיים שנרשמו כאשר התרחשה השגיאה.

### ההבדל בין תבניות קבצים HDMP ו-MDMP

HDMP הם קבצי dump של זיכרון לא דחוסים. לעומת זאת, MDMP הם קבצי מיני dump שנדחסים להקטנת גודל הקובץ ושליחה למיקרוסופט לדיווח על הבעיה.

## התייחסות ##

* [DMP - Microsoft](https://docs.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)

