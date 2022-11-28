{
  "date" : "2019-10-11",
  "keywords" :[ "vb", "קובץ", "סיומת", "פורמט קובץ", "Visual Basic", "מדריך תכנות" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VB - Visual Basic Code File",
  "description":"למד על פורמט קובץ VB וממשקי API שיכולים ליצור ולפתוח קבצי VB.",
  "linktitle" : "VB",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## מהו קובץ VB?

קובץ VB הוא קובץ קוד מקור שנוצר בשפת Visual Basic אשר נוצר על ידי מיקרוסופט לפיתוח יישומי NET. שפה דומה נוספת עם תחביר שונה היא C# שהקבצים שלה נשמרים עם סיומת הקובץ [.CS](/he/programming/cs/). פורמט הקובץ מספק את שפת התכנות ברמה הנמוכה לכתיבת קוד אשר מורכבת כדי ליצור את קובץ הפלט הסופי בצורה של EXE או DLL. ניתן ליצור ולהרכיב אותם עם Microsoft Visual Studio. ניתן להשתמש ב-Microsoft Visual Studio Express גם כדי ליצור ולעדכן קבצים כאלה שהם IDE חינמי. פרויקט פשוט של Visual Studio [פתרון](/he/programming/sln/) שנוצר בשפת VB יכול להכיל קובץ אחד או יותר כאלה. קבצים שסומנו להכללה בהידור מופיעים בקובץ [CSPROJ](/he/programming/csproj/) שהוא חלק מהפרויקט ומורה למהדר להשתמש בקבצים המסומנים.

## פורמט קובץ VB - מידע נוסף

קבצי VB הם פורמטים מבוססי טקסט שניתן לפתוח בכל עורך טקסט לצורך עריכה. עם זאת, כאשר הוא נפתח ב-IDE נתמך עם הדגשת תחביר נכונה, הקוד קל לקריאה ולסדר. קובץ VB פשוט מכיל:

* הצהרת מרחבי שמות - להתייחסות לפונקציונליות מסוימת המוגדרת על ידי אותו מרחב שמות ספציפי
* הצהרת משתנים - להכריז על משתנים ברמת המחלקה עבור היישום המסוים
* הצהרת שיטות - כדי להכריז על הצהרת שיטות עבור הפונקציונליות המסוימת

## דוגמה לפורמט קובץ VB

```
Imports System
Module Module1
   'This program will display Hello World
   Sub Main()
      Console.WriteLine("Hello World")
      Console.ReadKey()
   End Sub
End Module
```



