{
  "date" : "2022-06-06",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"פורמט קובץ TPSR - קובץ דוח הפעלות פיילוט של TeamViewer",
  "description":"למד על פורמט קובץ TPSR וממשקי API שיכולים ליצור ולפתוח קבצי TPSR.",
  "linktitle" : "TPSR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-06"
}

## מהו קובץ TPSR?

TPSR הוא קובץ פרוטוקול חיבור המשמש את TeamViewer Assist AR (שנודע בעבר בשם TeamViewer Pilot). מידע המאוחסן בקובץ TPSR מאוחסן בפורמט קובץ [ZIP](/he/compression/zip/) דחוס. TPSR מכיל היסטוריה מפורטת של חיבור TeamViewer בין מומחה לטכנאי לפתרון בעיה ומטרת סקירה. המידע הכלול בקובץ TPSR כולל סוג מכשיר, שם, מזהה AR Assist, מזהה מומחה, תאריך ושעה ומשך החיבור. נתונים אלה מאוחסנים בקובץ [JSON](/he/web/json/) בתוך ארכיון TPSR הדחוס.

## פורמט קובץ TPSR

קובץ TPSR מאוחסן על דיסק בפורמט קובץ ארכיון ZIP שבו התוכן מאוחסן בתוך קובץ JSON. הוא נוצר אוטומטית לאחר השלמת חיבור ה-Assist AR בתנאי שאפשרות דיווח החיבור מופעלת ב-TeamViewer.

TeamViewer Assist AR מאפשר למומחים להתחבר לטכנאים כדי לקבל עדכון LIVE של הקצה המרוחק באמצעות המצלמה הניידת. הם יכולים לסייע לטכנאים בפתרון הבעיה בטלפון.

## פתח את קבצי TPSR

אתה יכול לפתוח קבצי TPSR באמצעות גרסת שולחן העבודה של תוכנת TeamViewer. אם מותקן במחשב שלך, לחיצה כפולה על קובץ TPSR תפתח אותו בתוכנת TeamViewer. ניתן לייצא קבצי TPSR לקבצי [PDF](/he/pdf/) גם כן, או שניתן להדפיס אותם כדי לקבל עותק מודפס של קובץ הפרוטוקול.

## הפניות ##

* [TPSR](https://community.teamviewer.com/English/kb/articles/46456-using-teamviewer-assist-ar)

