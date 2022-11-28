{
  "date" : "2019-10-11",
  "keywords" :[ "קובץ xpm", "פורמט קובץ xpm", "מהו קובץ xpm", "קובץ", "דוגמה ל-xpm", "סיומת קובץ xpm","הרחבה", "פורמט" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XPM - X PixMap Format File",
  "description":"למד על פורמט קובץ XPM וממשקי API שיכולים ליצור ולפתוח קובצי XPM.",
  "linktitle" : "XPM",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## מהו קובץ XPM?

קובץ עם סיומת .xpm הוא פורמט קובץ תמונה ששימש את מערכת X Windows. הוא תומך בפיקסלים שקופים ובדרך כלל מכוון ליצירת מפות פיקסלים של אייקונים. הוא תומך בנתוני pixmap מונוכרום, בקנה מידה גרא ובצבע. אלה תוכננו כך שניתן לערוך אותם ביד וניתן לכלול אותם בקוד [C](/he/programming/c/). למטרה זו, קבצי XPM הם בפורמט קובץ טקסט רגיל ועוקבים אחר תחביר שפת התכנות C. ניתן לפתוח קבצי XPM עם מגוון אפליקציות לצפייה בתמונות כגון
CorelDRAW Graphics Suite 2020, Corel PaintShop Pro, IrfanView ו-Canvas X.

## פורמט קובץ XPM

פורמט הקובץ XPM משתמש בתחביר C על מנת שהם ישולבו בתוכנות C ו-C++. הוא מורכב מששת החלקים השונים הבאים.

*\<Values>
*\<Colors>
*\<Pixels>
*\<Extensions>

הקטעים הם למעשה מערך של מחרוזות כדלקמן.

```
/* XPM */
static char*<variable_name>[] = {
  <Values>
  <Colors>
  <Pixels>
  <Extensions>
};
```
להלן הפרטים של כל סעיף.

`<Values> ` - קטע זה הוא מחרוזת המכילה ארבעה או שישה מספרים שלמים שנמצאים בבסיס 10 ומתאימים ל:

* רוחב וגובה pixmap
*מספר צבעים
* מספר תווים לכל פיקסל
* קואורדינטות נקודה חמה אופציונליים ותג XPMEXT

`<Colors> ` - החלק הזה מכיל מחרוזות רבות כמו שיש צבעים. כל מחרוזת היא כדלקמן:

```
<chars>{<key><color> }+
```
`<Pixels> ` - חלק זה מורכב מ<height> מחרוזות ו<width> \*<chars_per_pixel> תווים. כֹּל<chars_per_pixel> מחרוזת אורך צריכה להיות אחת מהקבוצות שהוגדרו קודם לכן ב-<Colors> סָעִיף.

`<Extension> ` - יש לסמן את קטע ההרחבה, אם הוא אינו ריק, ב-<Values> סָעִיף. זה עשוי להיות מורכב מכמה<Extension> תת-סעיפים שעשויים להיות משני הסוגים הבאים:

* מחרוזת אחת עצמאית המורכבת באופן הבא: XPMEXT<extension-name><extension-data>
* או בלוק המורכב מכמה מחרוזות:XPMEXT<extension-name><related extension-data composed of several strings>

## הפניות

* [XPM - ויקיפדיה](https://en.wikipedia.org/wiki/X_PixMap)
* [מדריך XPM](http://www.xfree86.org/current/xpm.pdf)

