{
  "date" : "2021-07-28",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"QBL - QuickBooks License File",
  "description":"למד על פורמט קובץ QBL וממשקי API שיכולים ליצור ולפתוח קבצי QBL.",
  "linktitle" : "QBL",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2021-07-28"
}

## מהו קובץ QBL?

קובץ עם סיומת qbl הוא קובץ רישיון QuickBooks המכיל מידע רישוי עבור העותק שנרכש על ידי המשתמש. זה מאוחסן בדרך כלל במערכת מקומית עם השם `license.qbl` לאחר התקנת QuickBooks והמשתמש מזין את פרטי הרישוי בתוכנה כאשר התוכנה מופעלת בפעם הראשונה. QBL היה פורמט הקובץ הקודם ששימש לאחסון מידע רישוי של QuickBooks. זה הוחלף כעת בקובץ 'qbregisteration.dat' של QuickBooks והוא מאוכלס במידע ממייל האישור של המשתמש, מ-DVD שנרכש או באמצעי קנייה אחרים. ניתן לפתוח קבצי QBL בכל עורכי טקסט כגון Windows Notepad, Apple TextEdit, Notepad++, Github Atom עורך ועוד רבים.

## פורמט קובץ QBL - מידע נוסף

קובצי QBL נוצרים ומאוחסנים כקובצי טקסט רגיל. המידע בקבצים אלה ניתן לקריאה אנושית וניתן לערוך/לעדכן כאשר קבצים אלה נפתחים בעורכי טקסט. לאחר מכן ניתן להעתיק מידע על רישוי ורישום משתמש בקובץ זה כדי להתחיל בעבודה עם תוכנת QuickBooks. קבצי QBL מאוחסנים בדרך כלל בספריית Program Files\Intuit\QuickBooks\INET במערכת ההפעלה Windows.

קובץ QBL מכיל שני סוגי מידע.

* `מידע על גרסה של QuickBooks:` מתייחס לגרסה המותקנת של QuickBooks והיא בפורמט כגון xx.x
* `מפתח רישיון:` טקסט בפורמט 000-000 0000-0000-0000-000 000073adbf3f שבו 000-000 0000-0000-0000-000 מוחלף במפתח ה-qbregisteration של המשתמש

## הפניות

* [QuickBooks מאת Intuit](https://quickbooks.intuit.com/)
* [QuickBooks - יצירת קובץ qbregistration.dat](https://quickbooks.intuit.com/learn-support/en-us/license-information/create-or-re-create-the-qbregistration-dat-file/ 00/186082)

