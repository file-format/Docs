{
  "date" : "2022-03-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"פורמט קובץ CR3 - קובץ תמונה של Canon Raw 3",
  "description":"למד על פורמט קובץ CR3 וממשקי API שיכולים ליצור ולפתוח קובצי CR3.",
  "linktitle" : "CR3",
  "menu" : {
    "docs" : {
      "identifier":"image-cr3",
      "parent" : "image"
}
},
  "lastmod" : "2022-03-26"
}

## מהו קובץ CR3?

קובץ CR3 הוא פורמט קובץ תמונה של Canon RAW שנוצר על ידי מצלמות דיגיטליות נבחרות של Canon. זה הוצג על ידי קנון כדי להחליף את פורמט הקובץ CR2 ומשמש את חלק מהמכשירים הדיגיטליים של קנון. קובצי CR3 מאחסנים את נתוני התמונה המקוריים שאינם מעובדים ללא אובדן שנלכדו על ידי המצלמה. השימוש בתמונות גולמיות אלו מספקות תמונות באיכות גבוהה ומאפשרות שפע של מקום לעריכה לצלמים. בנוסף לנתוני התמונה הראשיים, קבצי CR3 מאחסנים גם מידע מטא נתונים על התמונה.

## פורמט קובץ CR3

קובצי CR3 מאוחסנים בדיסק כקובץ בינארי בפורמט ISO Base Media File (ISO/IEC 14496-12) וכוללים גם [תגי Canon] מותאמים אישית (https://exiftool.org/TagNames/Canon.html#uuid). הוא כולל גם את [Canon 'crx' codec](https://github.com/LibRaw/LibRaw/blob/master/src/decoders/crx.cpp) שהוא שילוב של JPEG-LS (Rice-Golomb + RLE) קידוד) ו-JPEG-2000 (LeGall 5/3 DWT + כימות).

## CR3 תגים מותאמים אישית

קובצי CR3 מכילים תגים מותאמים אישית למטרות שונות. חלק מהתגים הללו הם כדלקמן.

|מזהה תג| שם תג| לכתיבה |ערכים / הערות|
---|---|---|---|
|'CCTP' |CanonCCTP| - |--> תגיות CCTP של Canon|
|'CMT1' |IFD0| - |--> תגיות EXIF|
|'CMT2' |ExifIFD| - |--> תגיות EXIF|
|'CMT3' |MakerNoteCanon| - |--> תגיות קנון|
|'CMT4' |GPSInfo| - |--> תגיות GPS|
|'CNCV' |CompressorVersion| לא| |
|'CNOP' |CanonCNOP| - |--> תגיות Canon CNOP|
|'CNTH' |CanonCNTH| - |--> Canon CNTH Tags|
|'THMB' |תמונה ממוזערת| לא| |

## הפניות

* [פורמט קובץ CR2](http://lclevy.free.fr/cr2/)
* [תגי Canon](https://exiftool.org/TagNames/Canon.html#uuid)

