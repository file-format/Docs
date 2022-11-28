{
  "date" : "2021-02-25",
  "keywords": [ "ttc file", "ttc file format", "extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TTC - פורמט קובץ TrueType Collection",
  "description":"קובץ TrueType Collection (TTC) משלב מספר גופנים לקובץ אחד. גם אפל וגם מיקרוסופט השתמשו ב-TTF במערכות ההפעלה של Mac ו-Windows.",
  "linktitle" : "TTC",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2021-02-25"
}

## מהו קובץ TTC?
ה-TTC מקוצר בשם TrueType Collection הוא הרחבה של פורמט True Type. קובץ TTC יכול לשלב בתוכו את קובצי הגופן המרובים. קבצים אלה מועילים לשילוב גופנים מרובים החולקים גליפים רבים במשותף. לפני Windows 2000, נעשה שימוש בקבצי TTC בגירסאות סיניות, יפניות וקוריאניות של חלונות, אך מאוחר יותר התמיכה הייתה זמינה בכל האזורים.


## המבנה של קובץ אוסף גופנים
קובץ TTC מורכב מטבלת כותרת TTC, ספריות טבלאות וטבלאות OpenType מרובות. יש למצוא את כותרת ה-TTC בתחילת הקובץ. ספריית טבלה מלאה עבור כל גופן חייבת להיות קיימת. פורמט TableDirectory צריך להיות דומה לזה שהיה קיים בקובץ שאינו אוסף. ספירות הטבלה בכל הספריות בתוך קובץ TTC מחושבות מתחילת קובץ TTC.
הפניה לטבלאות בקובץ TTC דרך ספריית הטבלאות של הגופנים המתאימים. כמה מטבלאות OpenType חייבות להופיע מספר פעמים, פעם אחת עבור כל גופן שנוסף ב-TTC. בעוד שהטבלאות האחרות עשויות להיות משותפות על ידי מספר גופנים בקובץ TTC.

### כותרת TTC
שתי גרסאות של טבלת הכותרות של TTC זמינות עד כה:
- גרסה 1.0 משמשת לקבצי TTC ללא חתימות דיגיטליות.
- ניתן להשתמש בגרסה 2.0 עבור קבצי TTC עם או בלי חתימות דיגיטליות.
להלן טבלאות ה-TTC Header של שתי הגרסאות:

**TTC Header גרסה 1.0:**

|סוג|שם|תיאור|
---|---|---|
|TAG|ttcTag|מחרוזת מזהה אוסף גופנים: 'ttcf' (משמש עבור גופנים עם קווי מתאר CFF או CFF2 וכן קווי מתאר TrueType)|
|uint16|majorVersion|גרסה מרכזית של כותרת TTC, = 1.|
|uint16|minorVersion|גרסה מינורית של כותרת TTC, = 0.|
|uint32|numFonts|מספר גופנים ב-TTC|
|Offset32|tableDirectoryOffsets[numFonts]|מערך של קיזוזים ל-TableDirectory עבור כל גופן מתחילת הקובץ|

**TTC Header גרסה 2.0:**

|סוג|שם|תיאור|
---|---|---|
|TAG|ttcTag |מחרוזת מזהה אוסף גופנים: 'ttcf'|
|uint16| majorVersion |גרסה מרכזית של כותרת TTC, = 2.|
|uint16| minorVersion |גרסה מינורית של כותרת TTC, = 0.|
|uint32| numFonts |מספר גופנים ב-TTC|
|Offset32| tableDirectoryOffsets[numFonts] |מערך של קיזוזים ל-TableDirectory עבור כל גופן מתחילת הקובץ|
|uint32| dsigTag |תג המציין שקיימת טבלת DSIG, 0x44534947 ('DSIG') (null אם אין חתימה)|
|uint32| dsigLength |אורך (בבתים) של טבלת DSIG (null אם אין חתימה)|
|uint32| dsigOffset |ההיסט (בבתים) של טבלת DSIG מתחילת קובץ TTC (null אם אין חתימה)|

## הפניות
* [קובץ הגופן של OpenType](https://docs.microsoft.com/en-us/typography/opentype/spec/otff)
* [TrueType (Wikipedia)](https://en.wikipedia.org/wiki/TrueType)

