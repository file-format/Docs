{
"תאריך":"2023-09-21",
   "keywords":[
"ips",
"קובץ ips",
"קובץ תיקון מערכת תיקון פנימי של ips",
"מהו קובץ ips",
"איך פותחים קובץ ips",
"סיומת קובץ ips",
"סיומת",
"קוֹבֶץ"
],
   "author":{
"display_name":"שייק פאיז"
},
"draft": "false",
"toc":true,
"title": "פורמט קובץ IPS - קובץ תיקון מערכת תיקון פנימי",
   "description":"למד על פורמט IPS וממשקי API שיכולים ליצור ולפתוח קובצי IPS.",
   "linktitle":"IPS",
   "menu":{
      "docs":{
         "identifier":"game-ips",
         "parent":"game"
}
},
"lastmod":"2023-09-21"
}

## מהו קובץ IPS?

"קובץ IPS" מתייחס בדרך כלל ל"קובץ תיקון מערכת תיקון פנימי". IPS הוא קיצור של "International Patching System", והוא פורמט קובץ המשמש ליצירה והחלת תיקונים לקבצי ROM (זיכרון לקריאה בלבד), לעתים קרובות בהקשר של אמולציית משחקי וידאו ופריצת ROM.

הנה איך זה עובד:

- **ROM מקורי:** אתה מתחיל עם קובץ ROM מקורי, שהוא בעצם עותק של משחק וידאו או תוכנה המאוחסנים בפורמט ROM. קובץ זה הוא בדרך כלל לקריאה בלבד, כלומר אינך יכול לשנות אותו ישירות.

- **קובץ תיקון IPS:** קובץ תיקון IPS מכיל את השינויים שברצונך להחיל על ה-ROM המקורי. שינויים אלה יכולים להיות תיקוני באגים, תרגומים או שינויים אחרים.

- **יישום תיקון:** כדי להחיל את השינויים, אתה צריך כלי שירות או תוכנית שיכולים לקרוא את קובץ התיקון של IPS ולהחיל אותו על ה-ROM המקורי. תהליך זה בעצם "מתקן" את קובץ ה-ROM המקורי עם השינויים שצוינו בקובץ ה-IPS, ויוצר קובץ ROM שונה.

- ** ROM שונה:** התוצאה היא ROM שונה המשלב את השינויים מקובץ התיקון של IPS. לאחר מכן ניתן להשתמש ב-ROM ששונה זה באמולטור או בחומרה תואמת כדי לשחק במשחק עם השינויים הרצויים.

טלאים אלה משמשים בדרך כלל לביצוע שינויים או שיפורים במשחקים, והם יכולים להכיל שינויים שונים, כולל שינויים בגרפיקה, דגמים ונתוני משחקים אחרים. קבצי IPS מתאימים במיוחד לטלאים קטנים יחסית, בדרך כלל בגודל של פחות מ-16 מגה-בייט.

בסעיף הבא, נחקור את יישומי התוכנה המשויכים לקבצי IPS.

## ירח IPS

Lunar IPS הוא כלי עזר פופולרי וידידותי המשמש ליצירה והחלה של תיקוני IPS (Internal Patching System) לקבצי ROM. להלן כמה מאפיינים ומידע מרכזיים על Lunar IPS:

- **יצירת תיקונים:** Lunar IPS מאפשרת למשתמשים ליצור תיקוני IPS על ידי ציון השינויים שהם רוצים לבצע בקובץ ROM מקורי. אתה יכול לבחור את ה-ROM המקורי ואת הגרסה ששונתה, ו-Lunar IPS יפיק קובץ תיקון IPS על סמך ההבדלים בין שני הקבצים.

- **יישום תיקון:** ברגע שיש לך קובץ תיקון IPS, Lunar IPS מאפשר לך להחיל אותו על ROM מקורי. תהליך זה בעצם "מתקן" את ה-ROM עם השינויים שצוינו בקובץ ה-IPS, ויוצר ROM שונה.

- **קל משקל:** Lunar IPS היא תוכנית קטנה וקלת משקל, מה שאומר שהיא לא צורכת משאבי מערכת רבים ומהירה להורדה והרצה.

## IPSWin

IPSWin הוא כלי עזר המיועד בעיקר למשתמשי Windows המאפשר יצירה ויישום של תיקוני IPS (מערכת תיקון פנימית) לקבצי ROM. זהו כלי פשוט וידידותי למשתמש, מתאים למי שמחפש לתקן ROM בקלות. הנה קצת מידע על IPSWin:

- **יצירת תיקונים:** IPSWin מאפשרת למשתמשים ליצור תיקוני IPS על ידי השוואת שני קבצי ROM: ה-ROM המקורי וה-ROM שהשתנה. הוא מזהה את ההבדלים בין שני הקבצים ומייצר קובץ תיקון IPS המכיל את השינויים הללו.

- **יישום תיקון:** כלי זה גם מאפשר למשתמשים להחיל קבצי תיקון קיימים של IPS על ROM מקוריים. על ידי בחירת תיקון ה-IPS המתאים וה-ROM המקורי, IPSWin תמזג את השינויים לקובץ ROM חדש, וייצור גרסה מתוקנת.

## איך פותחים קובץ IPS?

תוכניות הפותחות קבצי IPS כוללות

- ירח IPS
- IPSWin
- MultiPatch

## קבצי IPS אחרים

להלן סוגי קבצים נוספים המשתמשים בסיומת הקובץ **.ips**.

- [IPS - סרטון פלייסטיישן 2 במשחק](/he/game/ips-ps2/)
- [IPS - נתוני iOS Analytics](/he/misc/ips/)

## הפניות
* [Lunar IPS](https://www.romhacking.net/utilities/240/)
