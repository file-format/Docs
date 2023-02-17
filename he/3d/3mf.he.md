{
  "date" : "2019-12-09",
  "keywords" :[ "קובץ 3mf", "פורמט קובץ 3mf", "מהו קובץ 3mf", "קובץ", "דוגמה 3mf", "סיומת קובץ 3mf","הרחבה", "פורמט" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"3MF",
  "description":"למד על פורמט קובץ 3MF וממשקי API שיכולים לפתוח וליצור קובצי 3MF.",
  "linktitle" : "3MF",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-12-09"
}

## מהו קובץ 3MF?

3MF, 3D Manufacturing Format, משמש יישומים לעיבוד מודלים של אובייקטים תלת מימדיים למגוון יישומים, פלטפורמות, שירותים ומדפסות אחרים. הוא נבנה כדי למנוע את המגבלות והבעיות בפורמטים אחרים של קבצים תלת-ממדיים, כמו [STL](/he/cad/stl/), לעבודה עם הגרסאות העדכניות ביותר של מדפסות תלת-ממד. 3MF הוא פורמט קובץ חדש יחסית שפותח ופורסם על ידי קונסורציום 3MF. הוא עשיר מספיק כדי לתאר במלואו מודל, תוך שמירה על מידע פנימי, צבע ומאפיינים אחרים שמאפשרים להרחבה לתמיכה בחידושים חדשים בהדפסת תלת מימד. הפורמט ניתן להרחבה, ניתן לאימוץ נרחב וללא בעיות הפוגעות בתבניות קבצים אחרות בשימוש נרחב.

## היסטוריה קצרה של פורמט קובץ 3MF

המגבלות הקיימות בפורמטים תיאוריים של מודלים זמינים, כגון STL ואחרים, מובילות את המותגים המובילים להתכנס ולגבש פורמט קובץ שניתן להרחבה יותר להדפסת תלת מימד. שיקול חשוב היה כיצד יישומים צריכים להעביר נתוני מודל למדפסות תלת מימד. קונסורציום 3MF, מכאן, נוצר כדי לגבות פורמט קובץ תלת מימדי חדש בשם 3MF במטרה להפוך אותו להרחבה מספיק כדי לספק את הצרכים של הדפסת תלת מימד. כמה חברות היו חלק מקונסורציום זה כולל Microsoft, Autodesk, Dassault Systems, Netfabb, SLM, HP ואחרות. מיקרוסופט תרמה את תבנית הקובץ התלת-ממדית שלה בתהליך עבודה כנקודת ההתחלה לפיתוח שיתופי נוסף של קונסורציום 3MF של המפרט.

## פורמט קובץ 3MF - מידע נוסף

3MF הוא פורמט נתונים מבוסס XML - XML דחוס קריא לאדם - הכולל הגדרות לנתונים הקשורים לייצור תלת מימד, כולל הרחבה של צד שלישי לנתונים מותאמים אישית. פורמט הקובץ 3MF תוכנן תוך התחשבות במגבלות ובבעיות העומדות בפני פורמטים אחרים של קבצים תלת מימדיים. זה הוביל לניסוח של פורמט קובץ 3MF שהוא:

* **מלא:** מכיל את כל המידע הנחוץ על הדגם, החומר והרכוש בארכיון אחד
* **ניתן לקריאה לאדם:** שימוש במבנים נפוצים כגון OPC, [ZIP](/he/compression/zip/) ו-XML כדי להקל על הפיתוח
* **פשוט:** מפרט קצר וברור, מה שהופך את הפיתוח לקל ואימות מהיר
* **ניתן להרחבה:** מינוף מרחבי שמות ב-XML מאפשר הרחבות ציבוריות ופרטיות כאחד תוך שמירה על תאימות
* **חד משמעי:** מבחני שפה ברורים והתאמה מבטיחים שקובץ תמיד עקבי מדיגיטלי לפיזי
* **חינם:** גישה ויישום של מפרט 3MF היא ותמיד תהיה ללא תמלוגים, פטנטים ורישוי

המפרטים של פורמט קובץ 3MF מתארחים ב-[Github](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md) לגישה ציבורית ועדכונים מתמשכים. הגרסה המתפרסמת הנוכחית היא 1.2.3 המתארת את קבוצת המוסכמות לשימוש ב-XML ובטכנולוגיות אחרות הזמינות באופן נרחב לתיאור התוכן והמראה של מודל תלת-ממדי אחד או יותר. מפתחים, שרוצים לבנות מערכות לעיבוד פורמטים של קבצים 3MF, יכולים להתייחס למפרטים אלה לצורך יישום.

## מפרטי פורמט קובץ 3MF

פורמט הקובץ 3MF משתמש במפרטי Open Packaging בצורת ארכיון ZIP עבור הדגם הפיזי שלו. הוא כולל קבוצה מוגדרת היטב של חלקים וקשרים הממלאים מטרה מסוימת במסמך. זה גם גורם לפורמט לעקוב אחר תכונת החבילה, כולל חתימות דיגיטליות ותמונות ממוזערות.

### מסמך 3MF - סקירה כללית

מסמך 3MF טיפוסי נראה כך:

![3MF Document Structure](https://github.com/3MFConsortium/spec_core/raw/master/images/figure_2-1.png "3MF Document Structure")

המטען כולל את הסט המלא של החלקים הנדרשים לעיבוד החלק של דגם 3D. כל התוכן שישמש לייצור אובייקט המתואר במטען התלת-ממדי חייב להיות כלול במסמך 3MF. התיאור של כל חלק במסמך יחד עם מצבו כנדרש או כאפשרות הוא כפי שניתן בטבלה הבאה.


|**שם**|**תיאור**|**מקור מערכת יחסים**|**חובה/אופציונלי**
--- | --- | --- | ---
|מודל תלת מימדי|מכיל את התיאור של אובייקט תלת מימדי אחד או יותר לייצור.|חבילה|נדרש
|Core Properties|חלק OPC המכיל מאפייני מסמך שונים.|חבילה|אופציונלי
|מקור חתימה דיגיטלית|חלק ה-OPC שהוא שורש החתימות הדיגיטליות בחבילה.|חבילה|אופציונלי
|חתימה דיגיטלית|חלקי OPC שכל אחד מהם מכיל חתימה דיגיטלית.|מקור חתימה דיגיטלית|אופציונלי
|תעודת חתימה דיגיטלית|חלקי OPC המכילים תעודת חתימה דיגיטלית.|חתימה דיגיטלית|אופציונלי
|PrintTicket|מספק הגדרות לשימוש בעת הוצאת האובייקט(ים) התלת-ממדיים בחלק של דגם תלת-ממד.|דגם תלת-ממדי|אופציונלי
|תמונה ממוזערת|מכילה תמונת JPEG או PNG קטנה המייצגת את האובייקטים התלת מימדיים בחבילה או בחבילה כולה.|חבילה|אופציונלי
|טקסטורה תלת מימדית|מכיל מרקם המשמש להחלת צבע על אובייקט תלת מימדי בחלק של דגם תלת מימד (זמין להרחבות)|דגם תלת מימד|אופציונלי
|חלקים מותאמים אישית|חלקי OPC המשויכים למטא נתונים|חבילה|אופציונלי

[חלקים ויחסים](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-2-parts-and-relationships), [מודלים תלת מימדיים](https:/ /github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-3-3d-models), [Object Resources](https://github.com/3MFConsortium/spec_core/blob/master /3MF%20Core%20Specification.md#chapter-4-object-resources), [משאבי חומר](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-5 -material-resources) ו-[Package Features](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-6-3mf-document-package-features) קטעי מפרטים מסמך מספק מידע מפורט על מסמך 3MF.

## הפניות ##

* [מפרט פורמט קובץ 3MF](https://github.com/3MFConsortium/spec_core)
* [3MF - מאת ויקיפדיה](https://en.wikipedia.org/wiki/3D_Manufacturing_Format)
