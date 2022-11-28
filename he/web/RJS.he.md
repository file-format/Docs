{
  "date" : "2021-05-24",
  "keywords" :["rjs", "קובץ", "הרחבה", "פורמט קובץ", "סיומת קובץ", "RJS", "קובץ רובי Javascript"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RJS - Ruby Javascript File",
  "description":"למד על פורמט קובץ RJS וממשקי API שיכולים ליצור ולפתוח קובצי RJS.",
  "linktitle" : "RJS",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-24"
}

## מהו קובץ RJS?

קובץ עם סיומת rjs הוא שילוב של קוד Ruby ו-JavsScript המאפשר למפתחי Rails להשתמש ברובי כדי לייצר קוד JavaScript דינמי. קוד רובי מוטבע בפונקציות של ג'אווה והוא מורכב בשרת האינטרנט שדורש ש-Ruby Engine יפעל על השרת. RJS דומה ל-[RHTML](/he/web/rhtml/); ההבדל היחיד הוא שה-lateral מכיל קוד Ruby ב-[HTML](/he/web/html/) בעוד שהוא מכיל קוד Ruby בפונקציות Javascript.

## פורמט קובץ RJS

קבצי RJS מקודדים בטקסט רגיל כמו כל שפת סקריפטים או תכנות אחרת. כאשר דף כזה מתבקש על ידי הלקוח, קוד Ruby מופעל בשרת, ורק קוד HTML ו-Javascript מוחזרים לדפדפן של הלקוח. התחביר של קובץ RJS דומה לזה של שילוב של תחביר Ruby ו-JavaScript כך שרק קוד Ruby מוטבע בפונקציות JavaScript.

### דוגמה ל-RJS

הדוגמה הבאה מציגה קוד רובי פשוט באופן עצמאי ולאחר מכן מוטבע בפונקציית JavaScript.

```Ruby
### Default Ruby Functions

def foo
  "bar"
end
```

```JavaScript
# JS style which looks like JS

foo = -> { return "bar" }
```
והנה RubyJS:
```Ruby
# here you go!

foo = -> { "bar" }
```
## הפניות

* [RJS](https://github.com/makevoid/rjs)

