{
  "date" : "2020-08-20",
  "keywords" :[ "קובץ fnt", "פורמט קובץ fnt", "מהו קובץ fnt", "קובץ", "דוגמה ל-fnt", "סיומת קובץ fnt","סיומת", "פורמט" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"FNT - קובץ גופן של Windows",
  "description":"למד על פורמט קובץ FNT וממשקי API שיכולים ליצור ולפתוח קובצי FNT.",
  "linktitle" : "FNT",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-30"
}

## מהו קובץ FNT?

קובץ עם סיומת .fnt הוא קובץ גופנים המאחסן מידע כללי על גופנים במערכות ההפעלה של Windows. קובצי FNT הוחלפו בעיקר בפורמטים של TrueType (.TTF) ו-OpenType (.OTF), והוא פורמט קובץ גופן מיושן נכון לעכשיו. קבצים אלה יכולים לאחסן מדרג יחיד או גופן וקטור. כל מנהלי ההתקנים תומכים בגופני Windows 2.x. עם זאת, לא כל מנהלי ההתקנים
תומך בגרסת Windows 3.0.

## פורמט קובץ FNT

קובצי FNT מסוגלים לאחסן גופן רסטר או וקטור בודד. הפורמטים הווקטוריים נמצאים בשימוש תכוף יותר על ידי GDI בהשוואה לרסטר שבו הגליף של כל אמנה מוגדר באמצעות מפת סיביות קטנה. הסיבה הברורה להחלפת .fnt ב-.ttf ו-.otf היא פורמט הרסטר שלו.

### כותרת קובץ גופן
ההתחלה של קובצי גופן רסטר וגם וקטורים היא נפוצה, ואחריה מידע שונה עבור כל סוג של קובץ. כותרת קובץ הגופן כוללת עבור Windows 3.0 כוללת שישה שדות חדשים כדלקמן אשר מוגדרים לאפס כדי להבטיח תאימות עם גרסאות עתידיות של חלונות.

* דגלים
* dfAspace
* dfBspace
* dfCspace
* dfColorPointer
* dfReserved1

למידע מפורט על הכותרות עבור Windows 3.0 ו-2.0, בקר ב[ארכיון Microsoft KnowledgeBase](https://jeffpar.github.io/kbarchive/kb/065/Q65123/).

## הפניות
* [פורמט קובץ גופן](https://jeffpar.github.io/kbarchive/kb/065/Q65123/)
* [כיצד להתקין או להסיר גופן ב-Windows](https://support.microsoft.com/en-us/windows/how-to-install-or-remove-a-font-in-windows-f12d0657-2fc8 -7613-c76f-88d043b334b8)

