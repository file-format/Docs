{
  "date" : "2019-10-11",
  "keywords" :[ "mhtml","קובץ mhtml", "פורמט קובץ mhtml", "סוג קובץ mhtml", "קובץ", "סוג", "מהו קובץ mhtml" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MHTML - MIME HTML File",
  "description":"למד על פורמט קובץ MHTML וממשקי API שיכולים ליצור ולפתוח קובצי MHTML.",
  "linktitle" : "MHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## מהו קובץ MHTML?

קבצים עם סיומת MHTML מייצגים פורמט ארכיון של דפי אינטרנט שניתן ליצור על ידי מספר יישומים שונים. הפורמט ידוע כפורמט ארכיון מכיוון שהוא שומר את קוד האינטרנט **[HTML](/he/web/html/)** ומשאבים משויכים בקובץ בודד. משאבים אלה כוללים כל דבר המקושר לדף האינטרנט כגון תמונות, יישומונים, אנימציות, קובצי אודיו וכן הלאה. ניתן לפתוח קבצי MHTML במגוון יישומים כגון Internet Explorer ו-Microsoft Word. Microsoft Windows משתמש בפורמט קובץ MHTML להקלטת תרחישים של בעיות שנצפו במהלך השימוש בכל יישום ב-Windows המעורר בעיות. פורמט קובץ ה-MHTML מקודד את תוכן העמוד בדומה למפרטים שהוגדרו בהודעה/rfc822 שהוא מפרטים הקשורים למייל טקסט רגיל. המפרטים בפועל של הפורמט הם כמפורט ב-[RFC 2557](https://tools.ietf.org/html/rfc2557).

## פורמט קובץ MHTML

MHTML ידוע גם בשם MIME Encapsulation של מסמכי HTML מצטברים בשל יכולתו לקודד דפי HTML יחד עם המשאבים שלו לארכיון אינטרנט אחד. לפי מפרטי RFC 2557, מסמך מצטבר הוא הודעה מקודדת MIME המכילה משאב שורש (אובייקט) וכן משאבים אחרים המקושרים אליו באמצעות URIs. משאבים אחרים כאלה עשויים להיות ייצוג של תמונות מוטבעות, גיליונות סגנונות, יישומונים וכו'. בנוסף, אלה יכולים להיות השורש של מסמכי מולטימדיה אחרים. מפרטי המסמכים המלאים עבור פורמט קובץ MHTML הם כמפורט ב-[RFC 2557](https://tools.ietf.org/html/rfc2557) ויש להפנות אותם לכל סוג של פיתוח יישומים לקריאה/כתיבה של פורמט קובץ זה. התקן מציין שניתן לזהות את חלקי הגוף שאליהם יש להתייחס או על ידי Content-ID או על ידי Content-Location.

### כותרות תוכן MIME

כותרת תוכן MIME, Content-Location, מוגדרת כדי לפתור הפניות URI למשאבים בחלקי גוף אחרים. כותרת זו יכולה להופיע בכל כותרת הודעה או תוכן.

### כותרת תוכן-מיקום

מיקום תוכן הוא ייצוג של URI המסמן את התוכן של חלק גוף שבו הוא ממוקם. הערך שלו יכול להיות URI מוחלט או יחסי. ניתן להשתמש בו כדי לתייג משאב שאינו ניתן לאחזור על ידי חלק או כל נמעני ההודעה. להודעה בודדת מותר להכיל כותרת Content-Location אחת בלבד. דוגמה למבנה מרובה חלקים/קשורים המכיל חלקי גוף עם תוויות Content-Location וגם Content-ID:

```
Content-Type: multipart/related; boundary#"boundary-example";
                    type#"text/html"

      --boundary-example

      Content-Type: text/html; charset#"US-ASCII"

      ... ... <IMG SRC#"fiction1/fiction2"> ... ...
      ... ... <IMG SRC#"cid:97116092811xyz@foo.bar.net"> ... ...

      --boundary-example
      Content-Type: image/gif
      Content-ID: <97116092511xyz@foo.bar.net>
      Content-Location: fiction1/fiction2

      --boundary-example
      Content-Type: image/gif
      Content-ID: <97116092811xyz@foo.bar.net>
      Content-Location: fiction1/fiction3

      --boundary-example--
```

### URI של אגרגטים MHTML

URI של מצטבר MHTML שונה מזה של URI השורש שלו. שדה הכותרת Content-Location אמור לחול על המצטבר כולו אם הוא משמש בכותרת של כותרת מרובת חלקים/קשורה. באופן דומה, קבוצת המשאבים המאוחזרת יכולה להיות שונה מקבוצת המשאבים שאוחזרה באמצעות מיקומי התוכן של חלקיה כאשר משתמשים ב-URI המתייחס לצבירת MHTML כדי לאחזר את המצטבר הזה. לדוגמה, אחזור מצרפי MHTML עשוי להחזיר גרסה ישנה, בעוד שאחזור URI השורש והאובייקטים המקושרים שלו בשורה עשויה להחזיר גרסה חדשה יותר.

## הפניות

* [Encapsulation MIME של מסמכים מצטברים - RFC 2557](https://tools.ietf.org/html/rfc2557)
* [פורמט קובץ MHTML - מאת ויקיפדיה](https://en.wikipedia.org/wiki/MHTML)

