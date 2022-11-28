{
  "date" : "2022-08-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"קובץ CON - פורמט קובץ מקור יישום מושג",
  "description" :"למד על מהו קובץ CON וממשקי API שיכולים ליצור ולפתוח קובצי CON.",
  "linktitle" : "CON",
  "menu" : {
    "docs" : {
      "identifier":"web-con",
      "parent" : "web"
}
},
  "lastmod" : "2022-08-24"
}

## מהו קובץ CON?

קובץ CON הוא קובץ קוד מקור עבור אפליקציה שפותחה עבור **Concept Application Server**. הוא משמש לכתיבת יישומים לחילופי נתונים בין השרת למשתמש. קבצי CON המתארחים בשרת נגישים באמצעות דפדפן אינטרנט בתנאי ש-Concept Client מותקן בקצה המשתמש. קונספט שרת יישומים הוא שרת אינטרנט עם שפת תכנות בקנה מידה קטן שיכול להיות בעל מנוע מסד נתונים [SQL](/he/database/sql/) משנה (TinDB).

קבצי CON יכולים להיפתח/להפעיל עם RadGs Concept Application Server.

## פורמט קובץ CON - מידע נוסף

קבצי CON מתארחים בשרת וניגשים אליהם באמצעות דפדפן אינטרנט במחשב המשתמש. מושג [כתובות אתרים](/he/web/url/) שונות מכתובות URL רגילות של HTTP ומתחילות ב-**concept://**.

### דוגמה של כתובת URL של קובץ CON

ניתן לגשת לקובץ CON המתארח ב-Concept Application Server באמצעות דפדפן אינטרנט באמצעות כתובות URL כגון:

```
concept://domain.server.com/web_application/main.con.
```
## הפניות

* [שרת יישומים קונספט](https://github.com/Devronium/ConceptApplicationServer)

