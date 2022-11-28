{
  "date" : "2021-02-25",
  "keywords" :[ "קובץ bdf", "פורמט קובץ bdf", "מהו קובץ bdf", "קובץ", "דוגמה ל-bdf", "סיומת קובץ bdf","הרחבה", "פורמט" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"BDF - פורמט הפצת מפת סיביות של Glyph",
  "description":"למד על פורמט קבצי BDF וממשקי API שיכולים ליצור ולפתוח קובצי BDF.",
  "linktitle" : "BDF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2021-02-25"
}

## מהו קובץ BDF?
קבצי BDF הם צורה קריא אנושית ומופצים בדרך כלל בקידוד ASCII. הקובץ מתחיל במידע גלובלי הרלוונטי לגופן המלא, ואחריו המידע ומפות הסיביות עבור הגליפים של הפרט. הנתונים בו מוצגים עבור הגופן עבור כיוון בגודל יחיד. המדדים לשימוש ביותר מכיוון אחד עשויים להיות מורכבים בקובץ בודד. בקובץ BDF, כל פריט כלול בשורת טקסט נפרדת בקובץ. רווחים משמשים להפרדה בין הפריטים בשורה.

## פורמט קובץ BDF
מכנס BDF לפורמט הפצת מפת סיביות של Glyph; בבעלות Adobe הוא פורמט קובץ לשמירת גופנים מסוג Bitmap. התוכן לובש צורה של קובץ טקסט המיועד להיות קריא במחשב כמו גם לאדם. ה-BDF משמש במיוחד בסביבות Unix X Window. הוא הוחלף באופן נרחב בפורמט הגופן PCF שאמור להיות יעיל יותר, ובגופני OpenType ו-TrueType.
### מבנה קובץ BDF
קובץ גופן BDF מורכב משלושה חלקים:

- סעיף גלובלי שחל על כל הגליפים בגופן.
- קטע עם ערך נפרד לכל גליף.
- הצהרת ENDFONT.

## דוגמא
להלן גופן לדוגמה המכיל גליף אחד, עבור ASCII רישיות 'A'. ההצהרות הגלובליות שלה מתחילות בקו "STARTFONT" ומסתיימות בקו "CHARS".
```
STARTFONT 2.1
FONT -gnu-unifont-medium-r-normal--16-160-75-75-c-80-iso10646-1
SIZE 16 75 75
FONTBOUNDINGBOX 16 16 0 -2
STARTPROPERTIES 2
FONT_ASCENT 14
FONT_DESCENT 2
ENDPROPERTIES
CHARS 1
STARTCHAR U+0041
ENCODING 65
SWIDTH 500 0
DWIDTH 8 0
BBX 8 16 0 -2
BITMAP
00
00
00
00
18
24
24
42
42
7E
42
42
42
42
00
00
ENDCHAR
ENDFONT
```



## הפניות
* [פורמט הפצת מפת סיביות של Glyph](https://en.wikipedia.org/wiki/Glyph_Bitmap_Distribution_Format)
* [מפרט תבנית הפצת מפת סיביות של Glyph (BDF)](https://adobe-type-tools.github.io/font-tech-notes/pdfs/5005.BDF_Spec.pdf)

