{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"פורמט קובץ XFDF - מהו קובץ XFDF?",
  "description":"למד על קבצי XFDF וממשקי API שיכולים ליצור ולפתוח קובצי XFDF.",
  "linktitle" : "XFDF",
  "menu" : {
    "docs" : {
      "parent" : "pdf"
}
},
  "lastmod" : "2019-09-10"
}

## מהו קובץ XFDF?

קובץ עם סיומת .xfdf הוא פורמט נתונים של XML Forms שנוצר עם תוכנת Adobe Acrobat. כמו [FDF](/he/pdf/fdf/), XFDF מכיל תיאור של רכיבי טופס והערכים שלהם בפורמט XML. זה יכול לכלול את השמות והערכים של שדות טקסט בטופס PDF. XFDF נשמרים בפורמט הניתן לקריאה אנושית וניתן לקרוא אותם באופן פרוגרמטי באמצעות שפות תכנות כגון C#.

## פורמט קובץ XFDF - מידע נוסף

קבצי XFDF נשמרים בפורמט קובץ XML שהוא פורמט אוניברסלי המשמש לייבוא וייצוא של נתונים. מבנה קובץ XFDF מורכב מכותרת, ואחריה ערכי שדות ונתוני אלמנטים כפי שמוצג להלן.

|אלמנט|תכונה|תוכן|
---|---|---|
|\<XFDF> ||האלמנט העליון|
|\<fields> ||כל ערכי השדות עבור תבנית זו|
|<field (T)> |שם |שם שדה|
|<value (V)> |value |ערך שדה|

## הפניות

* [תמיכה בפורמט FDF מאת Acrobat](https://helpx.adobe.com/coldfusion/developing-applications/working-with-documents-charts-and-reports/assembling-pdf-documents/fdf-format-support-for-acroforms.html)
* [משאבי מפתחים של Adobe](https://opensource.adobe.com/dc-acrobat-sdk-docs/)

