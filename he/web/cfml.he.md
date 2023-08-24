{
  "date" : "2021-08-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CFML - ColdFusion Markup Language File",
  "description" :"למד על מהו קובץ CFML וממשקי API שיכולים ליצור ולפתוח קובצי CFML.",
  "linktitle" : "CFML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-08-19"
}

## מהו קובץ CFML?

קובץ עם סיומת .cfml הוא קובץ ColdFusion Markup Language המשמש ליצירת דף אינטרנט. זה מתייחס למערכת של כללים המשמשים כדי להגדיר כיצד אפליקציית ColdFusion יפותח על ידי המתכנת. ColdFusion היא שפת תכנות שרגילה ליצור יישומי אינטרנט צדדיים במהירות ועם פחות מטכנולוגיות אחרות כגון [ASP](/he/web/asp/), [PHP](/he/programming/php/) וכו'. מהיישומים שיכולים לפתוח קובצי CML כוללים את Adobe ColdFusion 2018, Adobe ColdFusion Builder ו-Adobe Dreamweaver.

## פורמט קובץ CFML - מידע נוסף

קובצי CFML הם קובצי סימון ומכילים רכיבי אינטרנט בצורה של תגים. אלו קבצי טקסט שניתן לפתוח ולערוך בכל עורך טקסט. קובצי CFML מורכבים ממספר תגים הדומים ל-[HTML](/he/web/html/) ובדרך כלל מורכבים מתג פתיחה ותג סוגר. תגים אלה יכולים להכיל גם תכונה אחת או יותר.

### תחביר תגיות

להלן התחביר הכללי של תגי CFML.

```
<tagname>
  Code/text that is affected by the surrounding tags.
</tagname>
```

רוב התגים מקבלים תכונות ומוגדרות כדלקמן.

```
<tagname attribute="value">
  Code/text that is affected by the surrounding tags.
</tagname>
```

חלק מהתגים הללו מקבלים גם תכונות מרובות עם התחביר הבא.

```
<tagname attribute1="value" attribute2="value">
  Code/text that is affected by the surrounding tags.
</tagname>
```

## דוגמה לקוד CFML

הנה דוגמה שמשתמשת בתג CFML בפועל - תג `cfoutput`:

```
<cfoutput>
  #firstname#
</cfoutput>
```

## הפניות

* [ColdFusion](https://www.quackit.com/coldfusion/tutorial/)

