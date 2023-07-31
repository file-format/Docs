{
  "date" : "2020-08-20",
  "keywords" :[ "קובץ cff", "פורמט קובץ cff", "מהו קובץ cff", "קובץ", "דוגמה של cff", "סיומת קובץ cff","הרחבה", "פורמט" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CFF - פורמט קובץ גופן קומפקטי",
  "description":"למד על פורמט קובץ CFF וממשקי API ליצירה ופתיחה של קובצי CFF.",
  "linktitle" : "CFF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-21"
}

## מהו קובץ CFF?

קובץ עם סיומת .cff הוא פורמט גופן קומפקטי והוא ידוע גם בשם PostScript Type 1, או CIDFont. CFF פועל כמיכל לאחסון גופנים מרובים יחד ביחידה אחת המכונה FontSet. העיצוב של גופני CFF מאפשר הטמעת קוד שפת PostScript המאפשר גמישות נוספת והרחבה של הפורמט לשימוש עם סביבות מדפסת. ניתן לפתוח ולהמיר קובצי גופן CFF באמצעות ממשקי API כגון [Aspose.Font](https://products.aspose.com/font).

## פורמט קובץ CFF

קבצי CFF הם קבצים בינאריים המכילים פריסת נתונים מובנית, בעלי סוגי נתונים מוגדרים, כותרת, ארגון גליפים ומילוני טבלה. פרטים נוספים על אלה ניתן למצוא ב[מפרט פורמט גופן קומפקטי](https://learn.microsoft.com/en-us/typography/opentype/spec/cff).

### פריסת נתונים
פריסת הנתונים של פורמט קובץ CFF היא כפי שמוצג להלן.

|כניסה|הערות|
---|---|
|כותרת|–|
|NameINDEX|–|
|Top DICT INDEX|–|
|String INDEX|–|
|Global Subr INDEX|–|
|קידודים–תווים|–|
|FDSelect|CIDfonts בלבד|
|CharStrings INDEX|לגופן|
|גופן DICT INDEX|לגופן, CIDfonts בלבד|
|DICT פרטי|לגופן|
|Local Subr INDEX|לגופן או לכל DICT פרטי עבור CIDFonts|
|הודעות זכויות יוצרים וסימנים מסחריים|–|

### סוגי מידע

סוגי נתוני CFF הם כפי שמוצג בטבלה הבאה.

|שם|טווח|תיאור|
---|---|---|
|Card8|0 –255|1-byte מספר ללא סימן|
|Card16|0 – 65535|2-byte מספר לא חתום|
|היסט|משתנה|היסט של 1, 2, 3 או 4 בתים (מצוין בשדה OffSize)|
|OffSize|1–4|מספר ללא סימן של 1 בתים מציין את הגודל של שדה או שדות Offset|
|SID|0 – 64999|מזהה מחרוזת 2 בתים|

### כותרת

הנתונים הבינאריים מתחילים בכותרת בעלת הפורמט המוצג בטבלה הבאה.

|סוג|שם|תיאור|
---|---|---|
|Card8|major|פורמט גרסה עיקרית (החל מ-1)|
|Card8|minor|פורמט גרסה משנית (החל מ-0)|
|כרטיס8|גודל hdr| גודל כותרת (בתים)|
|OffSize|offSize|היסט מוחלט (0) גודל|

## הפניות

* [טבלת פורמט גופנים קומפקטי](https://learn.microsoft.com/en-us/typography/opentype/spec/cff)
* [פורמט קובץ CFF](https://adobe-type-tools.github.io/font-tech-notes/pdfs/5176.CFF.pdf)
* [CFF2 Chartset](https://learn.microsoft.com/en-us/typography/opentype/spec/cff2charstr)

