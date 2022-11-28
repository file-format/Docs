{
  "date" : "2021-05-24",
  "keywords" :["xht", "קובץ", "הרחבה", "פורמט קובץ", "הרחבת קובץ", "שפת סימון היפרטקסט מורחבת"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XHT",
  "description":"למד על פורמט קובץ XHT וממשקי API שיכולים ליצור ולפתוח קובצי XHT.",
  "linktitle" : "XHT",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-24"
}

## מהו קובץ XHT?

קובץ עם סיומת .xht הוא קובץ אינטרנט המשויך לסוג הקובץ [XHTML](/he/web/xhtml/) (Extended Hypertext Markup Language), שהוא עצמו קובץ סימון מבוסס [XML](/he/web/xml/). שני הקבצים הללו דומים ל-HTML אך יש להם תחביר דמוי XML מחמיר יותר. קבצי XHT מתוכננים בצורה מובנים יותר, כוללים פחות סקריפטים והם גנריים בנוסף לשימוש במתקנים הקיימים של XML.

## פורמט קובץ XHT

קובץ XHT נוצר ומאוחסן כקובץ טקסט רגיל עם קידוד UTF-8 כברירת מחדל. הוא מכיל את קוד המקור המלא של מסמך XHTML שניתן לפתוח ולערוך עם כל עורך טקסט התומך בקידוד Unicode. בנוסף לעורכי טקסט, פורמט קובץ XHT מובן לרוב דפדפני האינטרנט המודרניים וניתן לפתוח באמצעותם.

## דוגמה XHT

הדוגמה הבאה של מסמך XHT מגדירה את הצהרות ה-XML.

```
<!DOCTYPE html
     PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"
    "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<html xmlns#"http://www.w3.org/1999/xhtml" xml:lang#"en" lang#"en">
  <head>
    <title>Public Property</title>
  </head>
  <body>
    <p>changed to <a href#"http://sample.com/">sample.com</a>.</p>
  </body>
</html>
```

## הפניות ##

* [היסטוריה של XHTML: משנות ה-90 ועד היום](https://www.brighthub.com/internet/web-development/articles/109224.aspx)

