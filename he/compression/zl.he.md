{
  "date" : "2019-12-09",
  "keywords" :[ "קובץ zl", "פורמט קובץ zl", "מהו קובץ zl", "קובץ", "דוגמה zl", "סיומת קובץ zl","הרחבה", "פורמט" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ZL - פורמט קובץ דחוס ZLIP",
  "description":"למד על פורמט קובץ ZL וממשקי API שיכולים ליצור ולפתוח קבצי ZL.",
  "linktitle" : "ZL",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-14"
}

## מהו קובץ ZL?

קובץ עם סיומת .zl הוא פורמט קובץ דחוס ZLIP המשתמש בגרסה של אלגוריתם דחיסה DEFLATE לדחיסת קבצים. זה לא תלוי בסוג המעבד, מערכת ההפעלה, מערכת הקבצים וקבוצת התווים, ולכן ניתן להשתמש בו להחלפת מידע. מפרטים טכניים של דחיסת ZLIP זמינים ב[אתר IETF](https://tools.ietf.org/html/rfc1950) וניתן להתייחס אליהם מנקודת המבט של המפתח.

## פורמט קובץ ZL

לזרם zlib יש את המבנה הבא:

* `CMF (שיטת דחיסה ודגלים)` - בייט זה מחולק לשיטת דחיסה של 4 סיביות ושדה מידע של 4 סיביות בהתאם לשיטת הדחיסה.
```
bits 0 to 3  CM     Compression method
bits 4 to 7  CINFO  Compression info
```
* `CM (שיטת דחיסה)` - זה מזהה את שיטת הדחיסה בשימוש בקובץ. הערכים ושיטת הדחיסה המתאימה שלו הם כדלקמן.

| ערך CM| דחיסה|
|---|---|
|CM = 8|DEFLATE עם גודל חלון של עד 32K|
|CM = 15|שמורה|

* `CINFO (מידע דחיסה)` - עבור CM = 8, CINFO הוא לוגריתם הבסיס-2 של גודל החלון LZ77, מינוס שמונה (CINFO=7 מציין גודל חלון של 32K).

* `FLG (FLaGs)` - בייט הדגל הזה מחולק באופן הבא:
```
  bits 0 to 4  FCHECK  (check bits for CMF and FLG)
  bit  5       FDICT   (preset dictionary)
  bits 6 to 7  FLEVEL  (compression level)
````

## הפניות ##

* [מפרט פורמט קובץ Zlib](https://tools.ietf.org/html/rfc1950)

