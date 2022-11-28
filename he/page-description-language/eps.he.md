{
  "date" : "2019-12-12",
  "keywords" :[ "EPS", "קובץ", "סיומת", "פורמט קובץ", "פריסת עמוד", "PostScript Encapsulated" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"למד על פורמט קובץ EPS וממשקי API שיכולים ליצור ולפתוח קובצי EPS.",
  "title" :"פורמט קובץ EPS - קובץ PostScript מובלע",
  "linktitle" : "EPS",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2019-09-10"
}

## מהו קובץ EPS?

קובץ eps הוא קובץ תמונה שנשמר בתקליטור בפורמט קובץ Encapsulated Postscript. הוא עשוי להכיל כל שילוב של טקסט, גרפיקה ותמונות. קובצי EPS עשויים לכלול גם תמונת תצוגה מקדימה של מפת סיביות מכוסה בפנים לתצוגה על ידי יישומים שיכולים לפתוח קבצים כאלה.

## היסטוריה קצרה של פורמט קובץ EPS

מבט מהיר על פורמט קובץ EPS מנקודת מבט של היסטוריה מגלה את המידע הבא:

* הגרסה הראשונה של EPS שוחררה על ידי Adobe מתישהו בין 1985 ל-1988
* גרסה 2.0 של מפרט ה-EPS פורסמה בינואר 1989
* המפרט לגרסה 3.0 של EPS פורסם כמסמך נפרד בשנת 1992; זו הגרסה האחרונה שפורסמה.

EPS, בשילוב עם מנגנון ההרחבה של Open Structuring Conventions המתואר בסעיף 9 של מפרט ה-PostScript Language Document Structurering Conventions של Adobe, היוו את הבסיס לגרסאות מוקדמות של פורמט הקובץ של Adobe Illustrator Artwork.

## פורמט קובץ EPS

EPS הוא פורמט קנייני אך מתועד בפומבי ומפרטי פורמט קובץ EPS זמינים לציבור לעיון המפתחים. EPS הוא [DSC](https://en.wikipedia.org/wiki/Document_Structuring_Conventions) (אמנת בניית מסמכים) התואם פורמט קובץ ועומד בכל הכללים שנקבעו על ידי DSC. ה-DSC הוא פורמט קובץ מיוחד עבור מסמכי PostScript של Adobe. כל אפליקציה שמתיימרת להיות מסוגלת לקרוא קבצי EPS צריכה להיות תואמת DSC.

קובץ EPS מורכב משני חלקים עיקריים כפי שמוסבר להלן.

### תמונה מקדימה ###

קובץ EPS טיפוסי מכיל תמונת תצוגה מקדימה בפורמט המיועד לשימוש נוח בזרימת עבודה הכוללת מספר מערכות או יישומים. הכוונה של תצוגה מקדימה היא לקבל תמונה בפורמט שרוב יישומי הגרפיקה יכולים לעבד; תצוגה מקדימה היא בדרך כלל ברזולוציה נמוכה יותר, במידות פיקסלים ו/או בעומק סיביות. קובץ התצוגה המקדימה יכול להיות באחד ממספר פורמטים. המפרט עבור EPS_3 מפרט שלושה פורמטים של תצוגה מקדימה "ספציפית למכשיר":

* עבור Apple Macintosh, תמונת PICT כפי שמשמשת את היישום QuickDraw
* עבור מחשבי DOS, מפת סיביות TIFF
* Windows Metafile.

PICT ו-Windows Metafile יכולים לשלב גם נתוני מפת סיביות וגם גרפיקה וקטורית. בנוסף, המפרט מגדיר ייצוג פשוט מאוד ללא תלות בהתקן עבור תמונת תצוגה מקדימה מוטבעת של Bitmap. ייצוג זה ידוע בשם Encapsulated PostScript Interchange Format (EPSI).

תצוגה מקדימה של EPSI היא מפת סיביות המיוצגת כהקסדצימלית ASCII, עטופה בין כמה הערות PostScript לצורך זיהוי ונועדה להיות פשוטה וניתנת להעברה בקלות. על מנת להבחין בין קבצי EPS עם פורמטי התצוגה המקדימה השונים, הומלצו סיומות קבצי DOS וסוגי קבצי מקינטוש שונים במפרט EPS.

### קוד PostScript

לכל הפחות, פורמט הקובץ EPS חייב לכלול את הדברים הבאים:

* הערת כותרת, %!PS-Adobe-3.0 EPSF-3.0
* והערת תיבה תוחמת, %%BoundingBox: llx lly urx ury, המתארת את גבולות האיור. ארבעת הארגומנטים הללו תואמים לפינות השמאלית התחתונה (llx, lly) והפינה הימנית העליונה (urx, ury) של התיבה התוחמת.

קובץ EPS אינו יכול להשתמש באף אחד מהאופרטורים הבאים:

*התקן פס,
* cleardictstack
* עמוד העתק
*מחיקת דף
* שרת יציאה
* מכשיר מסגרת
* grestoreall
*initclip
* איניטגרפיקה
*initmatrix
* להתפטר
* רנדבנדים
* setglobal
* setpagedevice
* סט משותף
* תחילת עבודה.

## המרה של EPS לפורמטים אחרים של קבצים

ניתן להמיר קובצי EPS לפורמטים סטנדרטיים של תמונה כגון [JPG](/he/image/jpeg/), [PNG](/he/image/png/), [TIFF](/he/image/tiff/) ו-[PDF](/he/pdf /) באמצעות יישומים שונים כגון Adobe Illustrator, Photoshop ו- PaintShop Pro.

בגלל [פגיעות אבטחה](https://support.office.com/en-us/article/support-for-eps-images-has-been-turned-off-in-office-a069d664-4bcf-415e- a1b5-cbb0c334a840) בקובצי EPS, Office 2016, Office 2013, Office 2010 ו-Office 365 כיבו את היכולת להכניס קובצי EPS למסמכי Office.

## הפניות

* [Encapsulated PostScript - מאת ויקיפדיה](https://en.wikipedia.org/wiki/Encapsulated_PostScript)

