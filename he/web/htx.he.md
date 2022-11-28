{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"קובץ HTX - פורמט קובץ הרחבת HTML",
  "description" :"מדריך פורמט הקבצים שלך כדי ללמוד מהו קובץ HTX וממשקי API שיכולים ליצור ולפתוח קובץ HTX.",
  "linktitle" : "HTX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## מהו קובץ HTX?

קובץ HTX הוא למעשה קובץ HTML המכיל משתני נתונים להצגת תוצאות שאילתת מסד הנתונים כדף אינטרנט. נוצרו לרוב עם תוכנת פיתוח האינטרנט של Microsoft FrontPage, קובצי HTX נשמרים כדי לשמור באותה תיקיה כמו הקובץ המתאים למחבר מסד הנתונים באינטרנט (.IDC).

ניתן לפתוח קבצי HTX עם יישומים כגון Microsoft FrontPage וכל עורך טקסט כגון Notepad, TextEdit או Atom.

## פורמט קובץ HTX

קבצי HTX נשמרים כקובץ טקסט רגיל עם קוד לאחזור נתונים ממסד נתונים ושמירה במשתנים לתצוגה.


### דוגמה לקובץ HTX

דוגמה לקובץ HTX היא כדלקמן המגדיר כותרת עמוד להצגת הגבלת השאילתה והמסמכים המוצגים בעמוד להצגה למשתמש.

```
<H4>
<%if CiMatchedRecordCount eq 0%>
No documents matched the query "<%EscapeHTMLCiRestriction%>".</H4>
<%else%>
<H4>Documents <%CiFirstRecordNumber%> to <%CiLastRecordNumber%> of
<%if CiMatchedRecordCount eq CiMaxRecordsInResultSet%>
the first
<%endif%>
<%CiMatchedRecordCount%> matching the query
"<%EscapeHTMLCiRestriction%>".
<%endif%>
</H4>
```

הפלט של קוד לדוגמה זה הוא כדלקמן.

```
Documents 1 to 10 of the first 150 matching the query "cache".
```

כפי שניתן לראות, קובץ ה-HTX הוא תבנית שמעצבת את אופן החזרת התוצאות ומוצגות למשתמשי הקצה. זה כתוב בפורמט HTML עם כמה הרחבות IIS ושירות אינדקס. הרחבות אלו כוללות שמות משתנים וקודים אחרים לעיבוד תוצאות.

## הפניות

* [עיצוב התוצאות בקובץ Htx](https://learn.microsoft.com/en-us/previous-versions/windows/desktop/indexsrv/formatting-the-results--htx-file-)

