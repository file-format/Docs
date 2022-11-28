{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CDF - פורמט הגדרת ערוץ",
  "description" :"למד על מהו קובץ CDF וממשקי API שיכולים ליצור ולפתוח קובצי CDF.",
  "linktitle" : "CDF",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-08-18"
}

## מהו קובץ CDF?

קובץ עם סיומת .cdf הוא פורמט קובץ הפצת מידע מבוסס XLM ששימש לפרסום עדכונים תכופים כ"ערוצים". המידע מתפרסם מכל שרת אינטרנט ומועבר אוטומטית למחשבים עם תוכנות קבלה תואמות כגון דפדפני אינטרנט. משתמשים נרשמים לערוצים פעילים ומקבלים עדכונים מתוזמנים לשולחן העבודה שלהם.
קובצי CDF שימשו קודם לכן בשילוב עם הטכנולוגיות Active Channel, Active Desktop ו-Smart Offline Favorites של מיקרוסופט.

## פורמט קובץ CDF

קבצי CDF נשמרים כקבצי XML שהם פורמט קובץ אינטרנט גנרי להחלפת מידע. פורמט קובץ CDF הוא פורמט ישן כעת ומעולם לא אומץ באופן נרחב. בהשוואה לזה, ה-RSS של נטסקייפ היה מפורסם יותר והיה בשימוש נרחב יותר.

### דוגמה לפורמט קובץ CDF

להלן דוגמה כללית לפורמט הקובץ CDF.

```
<?xml version="1.0" encoding="UTF-8"?>
<CHANNEL HREF="http://domain/folder/pageOne.extension"
BASE="http://domain/folder/"
LASTMOD="1998-11-05T22:12"
PRECACHE="כן"
LEVEL="0">
<TITLE>שם הערוץ</TITLE>
<ABSTRACT>תקציר תכני הערוץ.</ABSTRACT>
<SCHEDULE>
<INTERVALTIME DAY="14"/>
</SCHEDULE>
<LOGO HREF="wideChannelLogo.gif" STYLE="IMAGE-WIDE"/>
<LOGO HREF="imageChannelLogo.gif" STYLE="IMAGE"/>
<LOGO HREF="iconChannelLogo.gif" STYLE="ICON"/>
<ITEM HREF="pageTwo.extension"
    LASTMOD="1998-11-05T22:12"
    PRECACHE="כן"
LEVEL="1">
<TITLE>הכותרת של עמוד שני</TITLE>
<ABSTRACT>תקציר התוכן של עמוד שני.</ABSTRACT>
<LOGO HREF="pageTwoLogo.gif" STYLE="IMAGE"/>
<LOGO HREF="pageTwoLogo.gif" STYLE="ICON"/>
</ITEM>
</CHANNEL>
```

## הפניות

* [פורמט הגדרת ערוץ - מאת ויקיפדיה](https://en.wikipedia.org/wiki/Channel_Definition_Format)

