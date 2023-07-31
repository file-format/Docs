{
  "date" : "2022-03-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MSO - Microsoft Office Macro Reference File",
  "description":"למד על קבצי MSO וממשקי API שיכולים ליצור ולפתוח קובצי MSO.",
  "linktitle" : "MSO",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-03-12"
}

## מהו קובץ MSO?

קובץ MSO הוא פורמט של קובץ מיכל נתונים שנוצר כאשר הודעת HTML נשלחת באמצעות Microsoft Outlook. זה קורה בעיקר עם יישומי Microsoft Office 2000. ברוב המקרים, הודעת האימייל מצורפת עם השם **Oledata.mso**. נמען הדוא"ל, כאשר פותח מייל כזה, יכול להציג את הקובץ בצורה נכונה גם אם לא מותקנת אצלו אותה תוכנה. קובצי MSO מתייחסים ל-[Microsoft Compound Document File Format (MCDF)](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-cfb/53989ce4-7b05-4f8d-829b-d08d6148375b).

## פורמט קובץ MSO של מיקרוסופט

קבצי MSO נשמרים ב-Microsoft Compound Document File Format (MCDF) הידוע גם כ-OLE (OLE) או Component Object Model (COM) מובנה של יישום קובץ קובץ בינארי ליישום קובץ מורכב.

### מבנה פורמט קובץ MSO

מבנה פורמט הקובץ הפנימי של פורמט קובץ MSO מוגדר היטב ב-[Structures](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-cfb/28488197-8193-49d7-84d8-dfd692418ccd ) סעיף בתיעוד MCDF. טבלת הקצאת קבצים (FAT) מנהלת את הקצאת הסקטורים ואת שרשראות הסקטורים. הוא מכיל מערך של מספרי סקטור של 32 סיביות. כל אינדקס במערך מייצג מספר מגזר ואילו הערך שלו מייצג את המגזר הבא בשרשרת או ערך מיוחד.

## הפניות

* [אחסון מובנה של COM](https://en.wikipedia.org/wiki/COM_Structured_Storage)
* [פורמט קובץ מסמכים מורכב של מיקרוסופט (MCDF)](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-cfb/53989ce4-7b05-4f8d-829b-d08d6148375b)

