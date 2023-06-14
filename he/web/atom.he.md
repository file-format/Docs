{
  "date" : "2022-08-05",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"קובץ ATOM - פורמט הפצת אטום",
  "description" :"למד על מהו קובץ ATOM וממשקי API שיכולים ליצור ולפתוח קבצי ATOM.",
  "linktitle" : "ATOM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-08-05"
}

## מהו קובץ ATOM?

קובץ ATOM הוא פורמט סינדיקציה למבנה של מסמכי הזנה וכניסה של Atom. בדומה לקובצי .RSS, פורמט קובץ ATOM הוא פורמט הפצה מבוסס XML המהווה תקן לפרסום תוכן. קובץ ATOM משמש להזנות אינטרנט המאפשרות לתוכנות לחפש עדכונים המתפרסמים באתר. הוא מכיל ערכים שיכולים להיות מסוגים שונים כגון כותרות, מאמרים בטקסט מלא, קטעים או קישורים לתוכן באתר אינטרנט

יישומים שיכולים **לפתוח קבצי ATOM** כוללים את **Apple Safari**.

## פורמט קובץ ATOM - מידע נוסף

קבצי ATOM מאוחסנים ומתפרסמים בפורמט קובץ XML הפופולרי שהוא פורמט אוניברסלי להחלפת מידע. הוא פותח כחלופה ל-RSS תוך שמירה על המגבלות והפגמים של פורמט קובץ RSS.

### סוגי מסמכי Atom

1. `מסמכי כניסת Atom` - זהו מסמך XML המורכב מפריט מידע בודד, המכונה כניסה, עבור הפיד של Atom. יש לוatom:entry אלמנט המכיל מספר אלמנטים צאצאים. התוכן של ערך Atom יכול להיות טקסט רגיל, HTML, XHTML או סוג אחר של IANA (Internet Assigned Numbers Authority).
1. `Atom Feed Documents` - זהו מסמך XML המספק מטא נתונים על עדכון Atom וערך אחד או יותר עבור הפיד. כאשר לקוח מבקש מידע מהפיד, מסמך הפיד נוצר על ידי השרת הכולל מספר כניסות Atom למילוי הבקשה.
1. `Atom Collection` - זהו סוג מיוחד של מסמך הזנת Atom המכיל את כתובות האתרים של ערכי Atom הזמינים לעריכה.

## הפניות

* [פורמט הפצת Atom - RFC](https://www.rfc-editor.org/rfc/rfc4287.html)
* [סקירה כללית של הזנות Atom - IBM](https://www.ibm.com/docs/en/cics-ts/5.4?topic=support-overview-atom-feeds)
* [Atom - Web Standard](https://en.wikipedia.org/wiki/Atom_(web_standard))

