{
  "date" : "2019-12-12",
  "keywords" :[ "EPUB", "קובץ", "הרחבה", "פורמט", "ספר אלקטרוני", "ספר דיגיטלי" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"למד על פורמט קובץ EPUB וממשקי API שיכולים ליצור ולפתוח קובצי EPUB.",
  "title" :"מהו קובץ EPUB?",
  "linktitle" : "EPUB",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2019-12-12"
}

## מהו קובץ EPUB?

קבצים עם סיומת epub הם פורמט קובץ של ספר אלקטרוני המספק פורמט פרסום דיגיטלי סטנדרטי עבור מפרסמים וצרכנים. הפורמט היה כה נפוץ עד כה שהוא נתמך על ידי קוראי אלקטרוני ויישומי תוכנה רבים. לדוגמה, ב-Mac OS, תוכנת **Books** המותקנת מראש מספקת תמיכה בפתיחת קבצים כאלה. בנוסף, יש הרבה תוכנות תואמות זמינות לסמארטפונים, טאבלטים ומחשבים. תקני קובץ EPUB נשמרים על ידי [פורום הפרסום הדיגיטלי הבינלאומי ](https://idpf.org/epub/30/spec/epub30-publications.html)(IDPF). גרסת EPUB 3 נתמכת גם על ידי קבוצת המחקר של תעשיית הספרים (BISG), איגוד סחר ספרים מוביל לשיטות עבודה מומלצות סטנדרטיות, מחקר, מידע ואירועים, לאריזת תוכן.

## היסטוריה קצרה של פורמט קובץ EPUB

* **אוקטובר 2007** - EPUB 2.0 אושר
* **ספטמבר 2010** - שוחרר עדכון תחזוקה
* **אוקטובר 2011** - מפרטי EPUB 3.0 נכנסו לתוקף
* **יוני 2014** - עדכון תחזוקה קל שוחרר כדי להחליף את גרסת 3.0
* **ינואר 2017** - EPUB 3.1 נכנס לתוקף

## פורמט קובץ EPUB

פורמט קובץ EPUB הוא ארכיון שניתן לשנות את שמו לסיומת [ZIP](/he/compression/zip/) וניתן לצפות בתוכן שלו על ידי חילוץ הארכיון עם כל מחלץ ארכיון. זהו פורמט פתוח מבוסס XML ומורכב מקובצי HTML, תמונות, גיליונות סגנונות CSS ואלמנטים אחרים. ניתן גם להמיר אותו ל-PDF, Mobi ועוד מספר פורמטים של קבצים באמצעות מספר יישומי תוכנה וממשקי API.

{{< figure src="../epub.png" alt="פורמט קובץ EPUB" >}}

**ספר אלקטרוני EPUB נפתח עם יישום Mac OS Books**

פורמט הקובץ EPUB מבוסס על שלושה סטנדרטים פתוחים.

### מבנה ציבורי פתוח (OPS) ###

קובץ EPUB 2.0 משתמש ב-XHTML 1.1 כדי לבנות את התוכן של פרסום. בעצם זה אומר שקובץ EPUB מורכב מדף אינטרנט אחד או יותר. למרות שאתה יכול לכלול את כל התוכן של ספר או עיתון בעמוד אחד, עדיף שקובץ כזה לא יעלה על 300K, הן מטעמי ביצועים והן מטעמי תאימות. בדיוק כמו בדפי אינטרנט רגילים, הסגנון והפריסה מוגדרים באמצעות גיליונות סגנונות מדורגים (CSS). בקבצי EPUB יש להשתמש בתת-קבוצה (סדרה מוגבלת של פקודות) של CSS2. רבים מהתכונות החדשות של CSS3, כגון קופסאות מעוגלות או צלליות, אינן זמינות עדיין. עבור תאימות לאחור, יוצר יכול גם להשתמש ב-DTBook במקום XHTML כדי לקודד את התוכן.

### פורמט אריזה פתוח (OPF) ###

חלק זה של המפרט עוסק במידע מבני כמו מטא נתונים (מי המחבר והמוציא לאור, מהי הכותרת,..), המניפסט (רשימת כל הקבצים בתוך קובץ epub) ותוכן העניינים. הנתונים הללו מוטבעים כולם באמצעות XML.

### פורמט מיכל פתוח (OCF) ###

כפי שהתיאורים לעיל היו צריכים להבהיר, מסמך EPUB מורכב מסדרה של קבצים. מפרטי ה-OCF מגדירים כיצד כל הקבצים האלה בסופו של דבר ארוזים בקובץ מכיל אחד. לשם כך נעשה שימוש בדחיסת ZIP.

## פורמטים נתמכים של קבצי תמונה ##

פורמט הקובץ EPUB תומך בפורמטים הבאים של קובץ התמונה.

* [GIF](/he/image/gif/)
* [JPG](/he/image/jpeg/)
* [PNG](/he/image/png/)
* [SVG](/he/page-description-language/svg/)

## הפניות ##

* [EPUB - מאת ויקיפדיה](https://en.wikipedia.org/wiki/EPUB)
