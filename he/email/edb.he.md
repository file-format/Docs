{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"פורמט קובץ EDB - קובץ מסד נתונים של דואר של Exchange",
  "description":"למד על פורמט קובץ EDB וממשקי API שיכולים ליצור ולפתוח קובצי EDB.",
  "linktitle" : "EDB",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2020-09-16"
}

## מהו קובץ EDB?

קובץ עם סיומת קובץ .edb הוא מסד נתונים של תיבת דואר שנוצר על ידי Microsoft Exchange Server כדי לאחסן נתונים הקשורים לדואר. EDB, Exchange Database, מאחסן הודעות שנמצאות בתהליך ולא SMTP. EDB ידועים גם בתור Extensible Storage Engine (ESE) קבצי מסד נתונים וקבצי אחסון באמצעות מבנה b-tree. בהיותם קבצי אחסון, ניתן להמיר קבצי EDB לפורמטים אחרים של קבצי אחסון דואר כגון [PST](/he/email/pst/) ו-[OST](/he/email/ost/).

## פורמט קובץ EDB

אין מפרטי פורמט קובץ EDB רשמיים/פתוחים שניתן לעיין בהם. חלה התקדמות מסוימת עבור הנדסה לאחור של פורמט הקובץ, וכתוצאה מכך פענוח מפרטים חלקי. לפי אלה, קובץ EDB מורכב מ:
* כותרת קובץ - מכיל מידע על כותרת קובץ מסד הנתונים
* עמודים בגודל קבוע - מכיל את מסד הנתונים הכולל טבלאות ואינדקסים

### כותרת קובץ מסד נתונים
כותרת קובץ מסד הנתונים נמצאת בעמוד מסד הנתונים הראשון והיא 668 בתים לפחות. כותרת הקובץ מכילה 'גרסת פורמט קובץ' ו'סוג קובץ' בנוסף לשדות אחרים.

#### סוגי קבצים
|סוג|תיאור
---|---|
|0| מסד נתונים|
|1| סטרימינג|

`הערה:` מזהים לסוגים אלו אינם ידועים.

#### גרסת פורמט קובץ
הפורמט המקורי של EDB החל באפריל 1997 והמשיך להתפתח לשינויים לאחר מכן.

|תאריך גרסה|גרסה|גרסה|תיאור
---|---|---|---|
|אפריל 1997| 0x00000620|0x00000000| פורמט ביתא מקורי של מערכת ההפעלה.|
|מאי 1997 |0x00000620|0x00000001| הוסף עמודות בקטלוג לאינדקס מותנה ו-OLD.|
|יוני 1997|0x00000620|0x00000002|הוסף את הדגל fLocalizedText ב-IDB.|
|אוקטובר 1997|0x00000620|0x00000003|הוסף SPLIT_BUFFER לדפי שורש של עץ החלל.|
|ינואר 1998|0x00000620|0x00000002|החזר גרסה כדי ש-ESE97 יישאר תואם קדימה.|
||0x00000620|0x00000003|הוסף עמודות מתויגות חדשות לקטלוג ("CallbackData" ו-"CallbackDependencies").|
|מאי 1998|0x00000620|0x00000004|תמיכה ב-Super Long Value (SLV): signSLV, fSLVExists in dbheader.|
|מאי 1998|0x00000620|0x00000005|עץ שטח SLV חדש.|
|אוקטובר 1998|0x00000620|0x00000006|מפת חלל SLV.|
|בדצמבר 1998|0x00000620|0x00000007|4-בתים IDXSEG.|
|ינואר 1999|0x00000620|0x00000008|תבנית עמודה חדשה של תבנית.|
|יוני 1999|0x00000620|0x00000009|עמודות תבנית ממוינות. בשימוש ב-Windows XP SP3|
||0x00000620|0x0000000b|מכיל את כותרת העמוד עם ה-ECC checksumUsed in Exchange|
||0x00000620|0x0000000c|בשימוש ב-Windows Vista (SP0)|
||0x00000620|0x00000011|תמיכה בדפים של 2 KiB, 16 KiB ו-32 KiB. כותרת עמוד מורחבת עם סכומי בדיקה נוספים של ECC. דחיסה של עמודות. רמזים למרחב. בשימוש ב-Windows 7 (SP0)|
|מאי 1999|0x00000623|0x00000000|מנהל שטח חדש.|

### קבצי מסד נתונים

קובץ מסד הנתונים של EDB מכיל את הסכימה של כל הטבלאות במסד הנתונים. בנוסף, הוא כולל גם רשומות עבור כל טבלאות מסד הנתונים ואינדקסים עבור הטבלאות. מיקומו נקבע על ידי המזהים הבאים.

* JetCreateDatabase
* JetCreateDatabase2
* JetAttachDatabase
* JetAttachDatabase2

על סמך אלה, ניתן להעריך את מצב מסד הנתונים כדלקמן.

|ערך|מזהה|תיאור
---|---|---|
|1|JET_dbstateJustCreated|מסד הנתונים נוצר זה עתה.|
|2|JET_dbstateDirtyShutdown|מסד הנתונים דורש שחזור קשה או רך כדי להיות שמיש או להזזה. לא צריך לנסות להעביר מסדי נתונים במצב זה.|
|3|JET_dbstateCleanShutdown|מסד הנתונים נמצא במצב נקי. ניתן לצרף את מסד הנתונים ללא כל קבצי יומן.|
|4|JET_dbstateBeingConverted|מסד הנתונים עובר שדרוג.|
|5|JET_dbstateForceDetachInternal|ערך זה מוצג ב-WindowsXP|
 

## הפניות
* [מפרטי קובץ מסד נתונים של מנוע אחסון להרחבה (ESE) (EDB)](https://github.com/libyal/libesedb/tree/master/documentation)
