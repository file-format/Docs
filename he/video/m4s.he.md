{
  "date" : "2022-07-18",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"קובץ M4S - מהו קובץ M4S?",
  "description":"למד על פורמט קובץ M4S וממשקי API שיכולים ליצור ולפתוח קובצי M4S.",
  "linktitle" : "M4S",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2022-07-18"
}

## מהו קובץ M4S?

קובץ M4S הוא קטע קטן של סרטון שמוזרם דרך האינטרנט באמצעות טכניקת הסטרימינג **MPEG-DASH**. הוא מכיל קטע וידאו בצורה של נתונים בינאריים. האפליקציה המקבלת (בדרך כלל דפדפן אינטרנט או נגני מדיה) מנגנת את הקטעים האלה בסדר קבלתם. קטע M4S הראשון מזוהה על ידי נתוני האתחול שהוא מכיל. ב**סיכום**, קבצי M4S הם קטעי מדיה בודדים קטנים של קובץ שלם.

## פורמט קובץ M4S

קובצי M4S מבוססים על [פורמט ISO Base Media File (ISOBMFF)](https://www.w3.org/TR/mse-byte-stream-format-isobmff/). ניתן להוריד מקטעים קטנים אלו של קובץ גדול באופן עצמאי באמצעות HTTP. לפיכך, אם יש לך קובץ סרט [MP4](/he/video/mp4/) גדול, ניתן להזרים אותו באמצעות טכניקת MPEG-DASH (Dynamic Adaptive Streaming over HTTP) על ידי פילוחו כקובצי מקטע M4S. אם קובץ הסרט הגדול הזה ירד לדיסק בתור M4S, יורידו קבצי M4S מרובים. אם כל מקטעי ה-.m4s הללו משורשרים, נוצר קובץ שלם שניתן לשחק בו. נגני המדיה לא יכולים להפעיל את הקובץ אלא אם קטע האתחול הראשון זמין גם עם הקובץ.

## על הזרמת MPEG-DASH

MPEG-DASH משתמש בטכניקת הזרמת קצב סיביות אדפטיבית המאפשרת להזרים תוכן מדיה באיכות גבוהה דרך האינטרנט. זה נעשה על ידי פירוק התוכן לרצף של קטעים קטנים המוזרמים ב-HTTP. ניתן להזרים קבצי מדיה גדולים כגון סרטים, פודקאסטים או שידור חי של אירוע ספורט בדרך זו. מקטעים אלה מקודדים בקצבי סיביות שונים. נגני המדיה התומכים ב-MPEG-DASH בוחרים אוטומטית את הקטע עם קצב הסיביות הגבוה ביותר באמצעות אלגוריתם התאמת קצב סיביות. זה ימנע השבתה או חציצה מחדש של אירועים בהשמעה.

### API של קוד פתוח עבור קבצי M4S

ישנם ממשקי API זמינים בקוד פתוח שניתן להשתמש בהם כדי לקרוא ולהמיר קבצי M4S.

* [libdash](https://github.com/bitmovin/libdash) - .NET API עבור קבצי M4S
* [dash.js](https://github.com/Dash-Industry-Forum/dash.js) - לקוח Javascript עבור קובץ M4S
* [Go Library ליצירת קבצי Dash](https://github.com/zencoder/go-dash)

### API של קוד פתוח להמרת M4S ל-MP4

* [MFourStoMp4](https://github.com/muri11o/mfourstomp4)

## הפניות ###

* [פורמט ISO Base Media File (ISOBMFF)](https://www.w3.org/TR/mse-byte-stream-format-isobmff/)
* [זרימה דינמית אדפטיבית על HTTP - MPEG-DASH](https://en.wikipedia.org/wiki/Dynamic_Adaptive_Streaming_over_HTTP)

