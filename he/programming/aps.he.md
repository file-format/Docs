{
  "date" : "2021-04-22",
  "keywords": [ "aps file", "visual studio aps file", "extension", "format","aps file visual studio","aps file extension","how to open aps file","APS file format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"APS - Visual C++ Resource File",
  "description":"למד על פורמט קובץ APS עם דוגמה APS וממשקי API שיכולים ליצור ולפתוח קובצי APS.",
  "linktitle" : "APS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-22"
}

## מהו פורמט קובץ APS?
קובץ APS נוצר על ידי Visual C++, יישום פיתוח תוכנה של מיקרוסופט. זה חוסך את הייצוג הבינארי של משאב המשולב בפרויקט וזה מאפשר לאפליקציה לטעון משאבים מהר יותר. אתה יכול למצוא בקלות קבצים אלה עם סיומת הקובץ .aps. למעשה, עורכי המשאבים אינם קוראים ישירות את קבצי resource.h ולכן מהדר המשאבים מרכיב אותם לקבצי .aps הנצרכים על ידי עורכי המשאבים.

## פורמט קובץ APS
פורמט הקובץ APS הוא רק שלב קומפילציה ומאחסן רק נתונים סמליים. המידע הלא סמלי, כגון הערות, נמחק במהלך תהליך ההידור. לדוגמה, בעת שמירה, עורך המשאבים מחליף את קובץ סקריפט המשאב ואת הקובץ resource.h. כל השינויים במשאבים עצמם יישארו משולבים בקובץ סקריפט המשאב, אך הערות תמיד יאבדו ברגע שקובץ סקריפט המשאב יוחלף.


## הפניות

* [קבצי משאבים (C++)](https://learn.microsoft.com/en-us/cpp/windows/resource-files-visual-studio?view=msvc-160)
 


