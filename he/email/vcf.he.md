{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VCF - קובץ איש קשר וירטואלי",
  "description":"למד על פורמט קובץ VCF וממשקי API שיכולים ליצור ולפתוח קובצי VCF.",
  "linktitle" : "VCF",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## מהו קובץ VCF?

VCF (פורמט כרטיס וירטואלי) או vCard הוא פורמט קובץ דיגיטלי לאחסון פרטי איש קשר. הפורמט נמצא בשימוש נרחב להחלפת נתונים בין יישומי חילופי מידע פופולריים. רוב מערכות ההפעלה כגון Windows ו-MacOS מגיעות עם יישומי ברירת מחדל ליצירה ופתיחה של קבצים אלה. קובץ VCF יחיד יכול להכיל מידע ליצירת קשר עבור איש קשר אחד או מרובים. קובץ VCF מכיל בדרך כלל מידע כמו שם איש קשר, כתובת, מספר טלפון, דואר אלקטרוני, יום הולדת, תמונות ואודיו בנוסף למספר שדות נוספים. בהיותך נתמך על ידי לקוחות ושירותי דוא"ל, אין אובדן נתונים במהלך העברת אנשי הקשר באמצעות שימוש בפורמט vCard. סוג המדיה עבור פורמט קובץ VCF הוא טקסט/vcard.

## פורמט קובץ VCF

קובצי VCF הם טקסטואליים מטבעם וניתנים לקריאה על ידי אדם. ניתן לפתוח אותם בעורכי טקסט כגון Notepad ב-Microsoft Windows ו-TextEdit ב-MacOS. אם יש תמונה בקובץ, לעומת זאת, היא לא תוצג בעורך הטקסט.

[Microsoft Outlook](https://support.office.com/en-us/article/send-and-save-contacts-as-vcards-vcf-files-94a17a6f-105f-46c7-9308-33658c1c2690) מספק תמיכה עבור פתיחת קבצי VCF וכן המרה למספר פורמטים אחרים כגון הפורמט הפופולרי [MSG](/he/email/msg/). פורמט קובץ VCF משופר עם הזמן מגרסה 2.1 ל-4.0 ומוסיף מידע מפורט לפורמט הקובץ. הפורמט משמש גם לייצוא אנשי קשר בטלפון ויבוא מאוחר יותר במכשיר אחר.

{{< figure src="../VCF.png" alt="פורמט קובץ VCF" >}}

### VCF 2.1 דוגמה

להלן דוגמה לגרסה 2.1.

```
BEGIN:VCARD
VERSION:2.1
N:Gump;Forrest;;Mr.
FN:Forrest Gump
ORG:Bubba Gump Shrimp Co.
TITLE:Shrimp Man
PHOTO;GIF:http://www.example.com/dir_photos/my_photo.gif
TEL;WORK;VOICE:(111) 555-1212
TEL;HOME;VOICE:(404) 555-1212
ADR;WORK;PREF:;;100 Waters Edge;Baytown;LA;30314;United States of America
LABEL;WORK;PREF;ENCODING#QUOTED-PRINTABLE;CHARSET#UTF-8:100 Waters Edge#0D#
 #0ABaytown\, LA 30314#0D#0AUnited States of America
ADR;HOME:;;42 Plantation St.;Baytown;LA;30314;United States of America
LABEL;HOME;ENCODING#QUOTED-PRINTABLE;CHARSET#UTF-8:42 Plantation St.#0D#0A#
 Baytown, LA 30314#0D#0AUnited States of America
EMAIL:forrestgump@example.com
REV:20080424T195243Z
END:VCARD
```

### VCF 3.0 דוגמה

להלן דוגמה לגרסה 3.0.

```
BEGIN:VCARD
VERSION:3.0
N:Gump;Forrest;;Mr.;
FN:Forrest Gump
ORG:Bubba Gump Shrimp Co.
TITLE:Shrimp Man
PHOTO;VALUE#URI;TYPE#GIF:http://www.example.com/dir_photos/my_photo.gif
TEL;TYPE#WORK,VOICE:(111) 555-1212
TEL;TYPE#HOME,VOICE:(404) 555-1212
ADR;TYPE#WORK,PREF:;;100 Waters Edge;Baytown;LA;30314;United States of America
LABEL;TYPE#WORK,PREF:100 Waters Edge\nBaytown\, LA 30314\nUnited States of America
ADR;TYPE#HOME:;;42 Plantation St.;Baytown;LA;30314;United States of America
LABEL;TYPE#HOME:42 Plantation St.\nBaytown\, LA 30314\nUnited States of America
EMAIL:forrestgump@example.com
REV:2008-04-24T19:52:43Z
END:VCARD
```

### VCF 4.0 דוגמה

להלן דוגמה לגרסה 4.0.

```
BEGIN:VCARD
VERSION:4.0
N:Gump;Forrest;;Mr.;
FN:Sheri Nom
ORG:Sheri Nom Co.
TITLE:Ultimate Warrior
PHOTO;MEDIATYPE#image/gif:http://www.sherinnom.com/dir_photos/my_photo.gif
TEL;TYPE#work,voice;VALUE#uri:tel:+1-111-555-1212
TEL;TYPE#home,voice;VALUE#uri:tel:+1-404-555-1212
ADR;TYPE#WORK;PREF#1;LABEL#"Normality\nBaytown\, LA 50514\nUnited States of America":;;100 Waters Edge;Baytown;LA;50514;United States of America
ADR;TYPE#HOME;LABEL#"42 Plantation St.\nBaytown\, LA 30314\nUnited States of America":;;42 Plantation St.;Baytown;LA;30314;United States of America
EMAIL:sherinnom@example.com
REV:20080424T195243Z
x-qq:21588891
END:VCARD
```

## הפניות

* [VCF - מאת ויקיפדיה](https://en.wikipedia.org/wiki/VCard)

