{
  "date" : "2022-04-07",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"פורמט קובץ HAML - קובץ קוד מקור Haml",
  "description":"למד על פורמט קובץ HAML וממשקי API שיכולים ליצור ולפתוח קובץ HAML.",
  "linktitle" : "HAML",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-07"
}

## מהו קובץ HAML?

קובץ HAML הוא קובץ שפת סימון הפשטה של HTML המכיל קוד מקור שנכתב בשפת [Haml](https://haml.info/). זה יכול לשמש כתחליף ל-ERB (סקריפטים של תבנית רובי). קובץ HAML מכיל קוד מקור של תבנית ליצירת HTML של מסמך אינטרנט. ניתן להחליף קבצי ERB פשוט על ידי החלפת קבצים אלה בתיקיית האפליקציה/צפיות להמל על ידי שינוי סיומת הקובץ. ניתן לפתוח קבצי HAML עם כל עורך טקסט כגון Microsoft Notepad, Notepad++, Apple TextEdit,

## פורמט קובץ HAML

קבצי HAML הם קובצי מקור שנשמרו בדיסק כקובצי טקסט רגיל. הוא מכיל קוד שנכתב בתחביר HAML. HAML מחליפה את התגים **<>** בסימן **%** כדי להפוך את הקוד לפשוט וקל יותר. קבצי ERB ניתנים להחלפה על ידי HAML כפי שמוצג בדוגמה הפשוטה הבאה.

```
app/views/account/login.html.erb → app/views/account/login.html.haml
```

### דוגמה HAML

להלן דוגמה של Hello World לדוגמא של HAML.

```
%p{:class => "sample", :id => "welcome"} Hello, World!
%p.sample#welcome Hello, World!
```
אשר מעבד לפלט ה-HTML הבא.

```
<p class="sample" id="welcome">Hello, World!</p>
```

## הפניות

* [HAML - Github](https://github.com/haml/haml)

