{
  "date" : "2019-10-11",
  "keywords" :[ "קובץ psd", "פורמט קובץ psd", "מהו קובץ psd", "קובץ", "דוגמה ל-psd", "סיומת קובץ psd","הרחבה", "פורמט" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PSD - פורמט קובץ תמונה של Photoshop",
  "description":"למד על פורמט קובץ PSD וממשקי API שיכולים ליצור ולפתוח קובצי PSD.",
  "linktitle" : "PSD",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## מהו קובץ PSD?

PSD, Photoshop Document, מייצג את פורמט הקובץ המקורי של Adobe Photoshop המשמש לעיצוב ופיתוח גרפיקה. קובצי PSD עשויים לכלול שכבות תמונה, שכבות התאמה, מסכות שכבות, הערות, מידע על קבצים, מילות מפתח ואלמנטים אחרים הספציפיים לפוטושופ. לקובצי פוטושופ יש סיומת ברירת מחדל כ-.PSD ויש להם גובה ורוחב מרביים של 30,000 פיקסלים, ומגבלת אורך של שני גיגה-בייט.

## מפרטי פורמט קובץ PSD ##

נתונים בקובץ PSD מאוחסנים בסדר בתים גדול אנדיאן. זה מרמז על החלפת המספרים השלמים הקצרים והארוכים בעת קריאה או כתיבה בפלטפורמת Windows. פורמט הקובץ Photoshop מחולק לחמישה חלקים עיקריים. יש לו סמני אורך רבים שניתן להשתמש בהם כדי לעבור מקטע אחד למשנהו. סמני האורך מרופדים בדרך כלל בבתים כדי לעגל למרווח הקרוב ביותר של 2 או 4 בתים. חמשת החלקים העיקריים הם:

* כותרת הקובץ
* נתוני מצב צבע
* משאבי תמונה
* מידע על שכבות ומסכות
* נתוני תמונה

לצורך התאמה, יש לכתוב נתונים לכל השדות הללו בקטע, מכיוון שפוטושופ עשויה לנסות לקרוא את הקטע כולו. זה גם מרמז שאפסים ייכתבו לשדות שדילג עליהם בזמן כתיבה לקובץ. יש להשתמש בשדה האורך בקטעים המופרדים לאורך כדי להחליט מתי להפסיק לקרוא. ברוב המקרים, שדה האורך מציין את מספר הבתים, לא הרשומות, שאחריו. יש לזכור את הנקודות הבאות בעת קריאת קובץ.

* הערכים בעמודה "אורך" בכל הטבלאות הם בבתים.
* כל הערכים המוגדרים כמחרוזת Unicode מורכבים מ:
* שדה באורך 4 בתים, המייצג את מספר התווים במחרוזת (לא בתים).
* מחרוזת ערכי Unicode, שני בייטים לכל תו.

### כותרת הקובץ ###

כותרת הקובץ מכילה את המאפיינים הבסיסיים של התמונה.

|אורך|תיאור
---|---|
|4|חתימה: תמיד שווה ל-'8BPS' . אל תנסה לקרוא את הקובץ אם החתימה אינה תואמת לערך זה.
|2|גרסה: תמיד שווה ל-1. אל תנסה לקרוא את הקובץ אם הגרסה אינה תואמת לערך זה. (~*~*PSB~*~* גרסה 2.)
|6|שמור: חייב להיות אפס.
|2|מספר הערוצים בתמונה, כולל ערוצי אלפא כלשהם. הטווח הנתמך הוא 1 עד 56.
|4|גובה התמונה בפיקסלים. הטווח הנתמך הוא 1 עד 30,000.
|4|רוחב התמונה בפיקסלים. הטווח הנתמך הוא 1 עד 30,000.
|2|עומק: מספר הביטים לכל ערוץ. הערכים הנתמכים הם 1, 8, 16 ו-32.
|2|מצב הצבע של הקובץ. הערכים הנתמכים הם: Bitmap # 0; גווני אפור מס' 1; באינדקס מס' 2; RGB # 3; CMYK # 4; רב ערוצי מס' 7; דואוטון מס' 8; מעבדה מס' 9.

### מדור נתוני מצב צבע ###

קטע נתוני מצב הצבע בנוי באופן הבא:


|אורך|תיאור
---|---|
|4|אורך נתוני הצבע הבאים
|משתנה|נתוני הצבע

נתוני מצב צבע זמינים רק עבור צבע ודואוטון שנוספו לאינדקס כפי שהוגדרו בשדה המצב במקטע כותרת הקובץ. עבור כל המצבים האחרים, קטע זה מיוצג על ידי ערכים מאופסים של 4 בתים. עבור תמונות צבע עם אינדקס, האורך הוא 768 ונתוני הצבע מכילים את טבלת הצבעים של התמונה, בסדר לא שזור. עבור תמונות Duotone, נתוני הצבע מכילים את מפרט הדואוטון (שפורמטו אינו מתועד). יישומים אחרים שקוראים קובצי פוטושופ יכולים להתייחס לתמונה דואוטונית כתמונה אפורה, ופשוט לשמר את תוכן המידע הדואוטוני בעת קריאה וכתיבת הקובץ.

### מדור משאבי תמונה ###

החלק השלישי של הקובץ מכיל משאבי תמונה. זה מתחיל בשדה אורך, ואחריו סדרה של בלוקים של משאבים.


|אורך|תיאור
---|---|
|4|אורך קטע משאב התמונה. האורך עשוי להיות אפס.
|משתנה|משאבי תמונה (בלוקים של משאבי תמונה)

משאבי תמונה משמשים לאחסון נתונים שאינם פיקסל המשויכים לתמונות כגון נתיבי כלי עט. הם מכונים בלוקי משאבים מכיוון שהם מכילים נתונים שאוחסנו במשאב של מקינטוש בגרסאות מוקדמות של Photoshop. המבנה הבסיסי של בלוקי משאבי תמונה הוא כפי שמוצג להלן:


|אורך|תיאור
---|---|
|4|חתימה: '8BIM'
|2|מזהה ייחודי למשאב. מזהי משאבי תמונה מכילים רשימה של מזהי משאבים המשמשים את Photoshop.
|משתנה|שם: מחרוזת פסקל, מרופדת כדי להפוך את הגודל לאחיד (שם ריק מורכב משני בתים של 0)
|4|הגודל האמיתי של נתוני המשאבים הבאים
|משתנה|נתוני המשאב, המתוארים בסעיפים על סוגי המשאבים הבודדים. הוא מרופד כדי להפוך את הגודל לאחיד.

משאבי תמונה משתמשים במספר מספרי זהות סטנדרטיים.

### מידע על שכבה ומסכה ###

החלק הרביעי של קובץ Photoshop מכיל מידע על שכבות ומסכות כגון מספר שכבות, ערוצים בשכבות, טווחי מיזוג, מקשי שכבת התאמה, שכבות אפקטים ופרמטרים של מסכה. אם אין שכבות או מסיכות, קטע זה מיוצג על ידי שדה מאפס של 4 בתים. יש להקדיש תשומת לב מיוחדת לאורך הקטעים בעת קריאת הסעיף הזה בשל הערכים המאפסים. הסידור של קטע שכבה ומסכה הוא כדלקמן:


|אורך|תיאור
---|---|
|4|אורך קטע מידע שכבה ומסכה. (אורך ה-PSB הוא 8 בתים.)
|משתנה|מידע על שכבה
|משתנה|מידע על מסכת שכבה גלובלית
|משתנה|סדרת בלוקים מתויגים המכילים סוגים שונים של נתונים.

#### מידע על שכבה ####

הטבלה הבאה מציגה את הארגון ברמה גבוהה של מידע השכבה.


|אורך|תיאור
---|---|
|4|אורך מקטע מידע השכבות, מעוגל כלפי מעלה לכפולה של 2. (אורך ה-PSB הוא 8 בתים.)
|2|ספירת שכבות. אם מדובר במספר שלילי, הערך המוחלט שלו הוא מספר השכבות וערוץ האלפא הראשון מכיל את נתוני השקיפות של התוצאה הממוזגת.
|משתנה|מידע על כל שכבה. ראה רשומות שכבה מתאר את המבנה של מידע זה עבור כל שכבה.
|משתנה|נתוני תמונת ערוץ. מכיל רשומה אחת או יותר של נתוני תמונה עבור כל שכבה. השכבות נמצאות באותו סדר כמו במידע השכבה

### נתוני תמונה ###

נתוני פיקסל התמונה כלולים בקטע נתוני תמונה של הקובץ. סידור הנתונים בקטע נתוני תמונה הוא בסדר מישור כלומר קודם כל הנתונים האדומים, אחר כך כל הנתונים הירוקים וכו'. כל מישור מאוחסן בסדר קו סריקה, ללא בתים של משטח, קטע נתוני התמונה מסודר בפורמט כפי שמוצג בטבלה הבאה.

|אורך|תיאור
---|---|
|2|שיטת דחיסה: *0 = נתוני תמונה גולמיים * 1 = RLE דחוסים נתוני התמונה מתחילים עם ספירת הבתים עבור כל שורות הסריקה (שורות * ערוצים), כאשר כל ספירה מאוחסנת כערך שני בתים. לאחר מכן הנתונים הדחוסים של RLE, כאשר כל קו סריקה דחוס בנפרד. הדחיסה של RLE היא אותו אלגוריתם דחיסה המשמש את ה-PackBits השגרתי של Macintosh ROM ותקן TIFF. *2 = ZIP ללא חיזוי *3 = ZIP עם חיזוי.
|משתנה|נתוני התמונה. סדר מישור = RRR GGG BBB וכו'.

## הפניות ##

* [מפרט פורמט קובץ PSD - מאת Adobe](https://www.adobe.com/devnet-apps/photoshop/fileformatashtml/#50577409_pgfId-1030196)
* [פורמט קובץ Adobe Photoshop](https://en.wikipedia.org/wiki/Adobe_Photoshop#File_format)
