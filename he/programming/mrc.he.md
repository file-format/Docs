{
  "date" : "2021-09-14", 
  "keywords" :[ "mrc", "קובץ", "הרחבה", "פורמט קובץ", "יישום mrc", "מדריך תכנות", "דוגמה לmrc", "mIRC", "שפת סקריפטים של mIRC", "קבצים של INI", " שפת סקריפטים mSL", "שפת mIRC", "סקריפטים mIRC", "שפת סקריפטים" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MRC - קובץ שפת סקריפט mIRC",
  "description":"למד על פורמט קובץ MRC וממשקי API שיכולים ליצור ולפתוח קובצי MRC.",
  "linktitle" : "MRC",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-14"
}

## מהו קובץ MRC?

mIRC היא שפת סקריפטים המוטמעת כלקוח IRC (Internet Relay Chat) במערכת ההפעלה Windows. הוא מספק מתקן של הגנה מפני ספאם לשימוש אישי וערוץ. כדי לספק חוויה טובה יותר של תאימות משתמש, שפת סקריפטים זו של mIRC מאפשרת יצירת חלונות דיאלוג. הקבצים המכילים סקריפטים, לרוב בפורמט טקסט רגיל, מאוחסנים עם סיומת MRC או כקבצים של [INI](/he/system/ini/). פונקציות של שפה זו ידועות כפקודות ומזהים (כאשר הן מחזירות ערך).

שפת mIRC מספקת טעינת קבצי סקריפט מרובים בו-זמנית. מצד שני, קובץ אחד יכול לגרום לכך שהשני לא יהיה בשימוש עוד כשהוא נטען בו זמנית. הפקודות נשמרות והן יכולות להתקיים ב-IRC באופן אוטומטי. הפקודות והכינויים המשמשים בשפה זו אינם מהווים קדימות של אף אחד מהתווים.

נעשה שימוש נרחב ב-mIRC כדי לגרום לבוטים לנהל ערוץ באופן אוטומטי, אך ניתן לשנות אותו גם על ידי שפת הסקריפטים של mSL. זה יכול להציג תכונות חדשות רבות כמו פקודות מאקרו, יכולת ניגון מוזיקה, פקודות מאקרו ופונקציות קטנות, משחקים בסיסיים או הפעלת יישומים קטנים.


## היסטוריה קצרה ##

שפת סקריפטים זו פותחה לראשונה בשנת 1995 על ידי חאלד אדם ביי. עיצוב שפת התסריט נוצר גם על ידי חאליד. היעד של שפה זו היה תכנות מונחה אירועים. בתחילה, סיומת הקובץ ששימשה לקבצים של שפת תכנות זו הייתה .mrc ו-.ini. יתר על כן, הוא פותח ברישיון של תוכנה קניינית.

## מפרט טכני ##

חלק מהפונקציות נכתבו בהתאמה אישית באמצעות שפת mIRC זו והן ידועות ככינויים. כאשר כינויים אלה מחזירים ערכים הם ידועים כמזהים מותאמים אישית. כל המשתנים הכלולים בשפת mIRC זו מוקלדים באופן דינמי. Sigils משמשים את סקריפטי mIRC. תכונה נוספת של שפת סקריפטים זו היא חלונות קופצים. המשתמשים יכולים להתקשר לחלונות קופצים פשוט על ידי בחירתם. שלטים מוגדרים לאירועים מסוימים. השלטים נקראים כאשר האירוע היחסי מתרחש.

אסימוני רווח מופרדים משמשים לשבירת כל שורת קוד של שפה זו. ישנן כמה הרחבות פופולריות אחרות המשמשות עבור קבצי mIRC כגון MDX (mIRC Dialog Extension) ו-DCX (Dialog Control Extension). שני אלה הם הרחבות דיאלוג והם פופולריים יותר באופן יחסי. מבני השפה מתייחסים לפי המינוח של שפת סקריפטים זו. שפת mIRC כוללת היבטים שונים של שפת סקריפטים כגון משתנים מקומיים וגלובליים, משתנים בינאריים, טבלאות גיבוב וטיפול בקבצים.


## דוגמה לפורמט קובץ MRC ##

```

;Defines the alias 'hello' in the remote script

;Note: if this is placed in an alias script,
;the 'alias' part must be removed (result: hello {)
;Usage: /hello

alias hello {

  ;Displays(/he/echo) 'Hello World!' into the active window(-a)
  echo -a Hello World!

}

```

```
;Placed in a remote script

;When a user types Hello! in a channel,
;you answer back: Hello, [nickname]!

on *:TEXT:Hello!:#:{ msg $chan Hello, $nick $+ ! }

;When a user types Hello! in a private message,
;you answer back: Hello, [nickname]!

on *:TEXT:Hello!:?: { msg $nick Hello, $nick $+ ! }

;Here is a script which automatically gives voice to a user
;who joins a particular channel (The Bot or user should have HOP)

on *:JOIN:#?: { mode $chan +v $nick }

;A bad word script

on *:Text:die*:#: { .mode $chan +b $nick | kick $chan $nick Dont say that again }

```

## התייחסות ##

* [MIRC - מאת ויקיפדיה](https://en.wikipedia.org/wiki/MIRC_scripting_language)



