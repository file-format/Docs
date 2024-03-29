{
  "date" : "2020-08-20",
  "keywords" :[ "קובץ cff2", "פורמט קובץ cff2", "מהו קובץ cff2", "קובץ", "דוגמה cff2", "סיומת קובץ cff2","הרחבה", "פורמט" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CFF2 - פורמט קובץ גופן קומפקטי גרסה 2",
  "description":"למד על פורמט קובץ CFF2 וממשקי API ליצירה ופתיחה של קבצי CFF2.",
  "linktitle" : "CFF2",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-21"
}

## מהו קובץ CFF2?

פורמט הקובץ CFF2 הוא גרסה 2.0 של פורמט הקובץ CFF ומאפשר אחסון יעיל של קווי מתאר גליפים ומטא נתונים בדומה לפורמט הקובץ CFF. CFF2 שונה מ-CFF בכך שהוא נועד לשמש בהקשר של גופן OpenType כטבלת 'sfnt' עם התג CFF2. לא ניתן להשתמש בה כתוכנית עצמאית והיא תלויה בנתונים בטבלאות OpenType אחרות.

## פורמט קובץ CFF2

[מפרט פורמט הקובץ CFF2](https://learn.microsoft.com/en-us/typography/opentype/spec/cff2) מכיל פרטים על פריסת נתונים פנימית, סוגי נתונים, טבלאות ומידע פנימי אחר על פורמט הקובץ. ניתן להפנות אותו לעיון המפתח. חלק מהפרטים על אלה הם כדלקמן.

### פריסת נתונים

הנתונים הבינאריים של פורמט קובץ CFF2 מאורגנים באופן הגיוני כמספר מבני נתונים נפרדים. הפריסה בתוך הנתונים הבינאריים היא כפי שמוצג בטבלה הבאה.

|כניסה |הערות|
---|---|
|כותרת |מיקום קבוע|
|Top DICT| מיקום קבוע|
|Global Subr INDEX| מיקום קבוע|
|וריאציה |חנות|
|FDSelect |הצג רק אם יש יותר מ- Font DICT אחד ב- Font DICT INDEX.|
|פונט DICT INDEX ||
|מערך גופנים DICT| כלול ב- Font DICT INDEX.|
|DICT פרטי| אחד לכל גופן DICT.|

רק שלושת המבנים הראשונים מבוססים על מיקומים קבועים. הנותרים מגיעים באמצעות קיזוז, וניתן לשנות את הסדר שלהם.

### סוגי מידע

פורמט הקובץ CFF2 משתמש בסוגי הנתונים הבאים.

|שם |טווח |תיאור|
---|---|---|
|uint8 |0 עד 255 |מספר ללא סימן של 8 סיביות|
|uint16 |0 עד 65535| מספר 16 סיביות לא חתום|
|uint32 |0 עד 4294967295| מספר 32 סיביות לא חתום|
|היסט |משתנה| קיזוז של 1, 2, 3 או 4 בתים (מצוין בשדה OffSize בטבלת אינדקס)|
|OffSize |1 עד 4| מספר 1-byte ללא סימן מציין את הגודל של שדה או שדות Offset|

הוא מאחסן את כל הנתונים מספריים מרובים בתים ושדות היסט בסדר בתים גדולים. פורמט CFF2 נקי מבייט ריפוד מכיוון שהוא אינו מכבד כל מגבלות יישור.

### נתוני DICT

קבצי CFF2 מכילים את נתוני מילון הגופנים כצמדי מפתח-ערך בפורמט אסימון קומפקטי. מפתחות מילון מקודדים כאופרטורים של 1 או 2 בתים וערכי מילון מקודדים כאופרנדים מספריים בגודל משתנה. ישנם שלושה מבנים המשתמשים בפורמט DICT Data: `Top DICT`, `Font DICT` ו-`Private DICT`. מוגדרים מספר סוגי אופרנדים שלמים בגדלים שונים ומקודדים כפי שמוצג בטבלה הבאה (הבית הראשון של האופרנד הוא b0, השני הוא b1 וכן הלאה).

|גודל |טווח b0 |טווח ערכים |חישוב ערך|
---|---|---|---|
|1 |32 עד 246| -107 עד +107 |b0 - 139|
|2 |247 עד 250| +108 עד +1131 |(b0 - 247) * 256 + b1 + 108|
|2 |251 עד 254| -1131 עד -108| -(b0 - 251) * 256 - b1 - 108|
|3 |28| -32768 ל-+32767| b1 << 8 | b2|
|5 |29| -(2^31) עד +(2^31 - 1)| b1 << 24 \| b2 << 16 \| b3 << 8 \| b4|

### כותרת

הנתונים הבינאריים מתחילים בכותרת בעלת הפורמט המוצג בטבלה למטה.

|הקלד |שם |תיאור|
---|---|---|
|uint8| majorVersion| פורמט גרסה עיקרית. הגדר ל-2.|
|uint8| minorVersion| פורמט גרסה משנית. הגדר לאפס.|
|uint8| headerSize| גודל כותרת (בתים).|
|uint16| topDictLength| אורך מבנה ה-DICT העליון בבתים.|

## הפניות

* [פורמט קובץ CFF2](https://learn.microsoft.com/en-us/typography/opentype/spec/cff2)

