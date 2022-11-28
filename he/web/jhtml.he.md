{
  "date" : "2019-10-11",
  "keywords" :[ "jhtml","קובץ jhtml", "פורמט קובץ jhtml", "סוג קובץ jhtml", "קובץ", "סוג", "מהו קובץ jhtml" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JHTML - קובץ Java HTML",
  "description":"למד על פורמט קובץ JHTML וממשקי API שיכולים ליצור ולפתוח קובצי JHTML.",
  "linktitle" : "JHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-09"
}

## מהו קובץ JHTML?

קובץ עם סיומת jhtml הוא קובץ [HTML](/he/web/html/) עם קוד [Java](/he/programming/java/) המופעל בשרת כאשר לקוח מבקש דף זה בדפדפן. השרת מעבד את הבקשות, מבצע את פונקציות ה-Java הכלולות בפונקציה ומחזיר את העמוד לדפדפן של הלקוח. אובייקטי Java המוטמעים בדפי JHTML פועלים בשרת כדי לטפל בבקשות לדפים מסוג זה. קובצי JHTML יכולים גם לגשת למידע ממסד הנתונים באמצעות חיבור JDBC (קישוריות Java [Database](/he/database/)). ניתן לפתוח קובצי JHTML בכל עורך טקסט ולהציג אותם בדפדפני אינטרנט כגון Google Chrome, Firefox ו-Safari.

## פורמט קובץ JHTML

JHTML היא טכנולוגיה קניינית של ATG וניתן ליצור אותה באמצעות ATG (Art Technology Group) Dynamo Document Editor. קובצי JHTML נכתבים בפורמט קובץ טקסט פשוט באמצעות קוד HTML ו-Java הסטנדרטיים. אלה מכילים תגי HTML סטנדרטיים בנוסף לתגיות קנייניות המתייחסות לאובייקטי Java. כאשר דף כזה מתבקש על ידי המשתמש, שרת ה-HTTP מעביר את הבקשה לשרת יישומי Java. דף ה-JHTML מומר תחילה לקובץ .java וקומפילציה כדי ליצור קובץ [.class](/he/programming/class/) המופעל כ-servlet. זה יוצר זרם של נתוני HTTP ו-HTML סטנדרטיים המוחזרים לדפדפן המבקש להצגה למשתמש. זה מועיל כדי להפעיל שאילתות הקשורות למסד נתונים בשרת ולהחזיר את התוצאה המצטברת הסופית לדפדפן של הלקוח.

## הפניות

* [המבנה הגלובלי של מסמך HTML](https://www.w3.org/TR/html401/struct/global.html#h-7.5.4)

