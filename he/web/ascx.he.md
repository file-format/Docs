{
  "date" : "2019-10-11",
  "keywords" :[ "ascx", "קובץ ascx", "פורמט קובץ ascx", "סוג קובץ ascx", "קובץ", "סוג", "מהו קובץ ascx" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"פורמט קובץ ASCX",
  "description" :"למד על מהו קובץ ASCX וממשקי API שיכולים ליצור ולפתוח קובצי ASCX.",
  "linktitle" : "ASCX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2020-09-10"
}

## מהו קובץ ASCX?

קובץ עם סיומת .ascx הוא פקד משתמש המשמש כרכיב לשימוש חוזר בדפי אינטרנט. מפנה אליו בכל אתר ASP על ידי גרירתו מתיבת הבקרה לדף. בקרות משתמשי ASCX מתווספות לפרויקט כמקור מרכזי, וכתוצאה מכך כל שינוי בבקרת המשתמש יבוא לידי ביטוי בכל האתר. בניגוד לקבצי ASMX המגדירים מנגנון לתקשורת בתוך 2 אובייקטים דרך האינטרנט, קבצי ASCX הם בקרות משתמש להטמעה בדפים או באתר.

## פורמט קובץ ASCX

קובצי ASCX נכתבים בפורמט טקסט רגיל ויכולים להשתמש בקוד מאחורי תכונה כמו דפי אינטרנט המסתיימים ב-.ascx.cs. קוד הסימון של בקרות המשתמש מתחיל בהוראה @Control כפי שמוצג בדוגמה הבאה.

```
<%@ Control Language="VB" AutoEventWireup="false" CodeFile="WebUserControl.ascx.vb" Inherits="WebUserControl" %>
<p>A simple web user control with static HTML only.</p>
```

ניתן לעשות שימוש חוזר בבקרת משתמש אינטרנט זו בדפים רבים כגון כותרת תחתונה, כותרת עליונה או סוג של ניווט באתר. לפקדים של משתמשי אינטרנט יש מאפיינים, שיטות ואירועים כמו כל שליטה אחרת שהופכים אותם לשימושיים בקביעת ההתנהגות החזותית שלהם.

### דוגמה לרישום פקדי משתמש ב-web.config

על מנת להשתמש בפקד משתמש בודד בדפים רבים, ניתן לרשום את בקרת האינטרנט ב-web.config. זה מאפשר להשתמש בשליטה על כל האתר במקום להירשם בכל עמוד בנפרד. הקוד לדוגמה הבא מגדיר כיצד לרשום פקד אינטרנט ב-web.config שיוצג ככותרת תחתונה באתר כולו.

```
<configuration>
  <system.web>
    <pages>
      <controls>
        <add src="Footer.ascx" tagPrefix="bs" tagName="footer" />
      </controls >
    </pages >
  </system.web>
</configuration>
```
## הפניות

* [ASCX לעומת ASMX](https://forums.asp.net/t/1838934.aspx?How+to+work+with+ascx+files+)
* [בקרת משתמש ASCX](http://www.beansoftware.com/ASP.NET-Tutorials/User-Control.aspx)

