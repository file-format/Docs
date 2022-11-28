{
  "date" : "2021-04-22",
  "keywords": [ "appx file", "extension", "format","how to open appx file","appx file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"APPX - מהו קובץ APPX?",
  "description":"למד על פורמט קובץ APPX וממשקי API שיכולים ליצור ולפתוח קובצי APPX.",
  "linktitle" : "APPX",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-12-16"
}

## מהו קובץ APPX?

קובץ APPX הוא פורמט קובץ חבילה שניתן להפצה המשמש להפצה והתקנה של יישום. זה הוצג עם Windows 8 כדי להתפרסם ב-Microsoft Windows Store. הוא מכיל את כל הקבצים הדרושים להתקנת יישום Windows. אלה כוללים מטא נתונים, קבצים ומידע על אישורים. פורמט קובץ אריזה מודרני יותר הוא MSIX שנמצא כיום בשימוש נפוץ יותר בהשוואה ל-APPX.

## פורמט קובץ APPX - מידע נוסף

קובצי APPX נשמרים כקבצים דחוסים בפורמט קובץ [ZIP](/he/compression/zip/). זה הופך את החבילה כולה לקובץ ארכיון עם גודל קובץ מופחת שקל להעלות אותו ל-Microsoft Store.

## כיצד להציג קבצים בקובץ APPX?

על מנת להציג את התוכן או הקבצים בתוך קובץ APPX, יש לבצע את השלבים הבאים.

1. מכיוון שקובצי APPX מאוחסנים כקובצי ZIP דחוסים, שנה את שם הקובץ לסיומת .zip
1. השתמש בכל כלי ביטול דחיסה כגון 7-Zip, WinZip או WinRAR כדי לחלץ את הקבצים הכלולים בקובץ APPX

## כיצד ליצור קובץ APPX?

ישנן שתי שיטות שניתן להשתמש בהן ליצירת קבצי APPX.

1. שימוש ב-MakeApp.exe - [MakeApp.exe](https://docs.microsoft.com/en-us/windows/msix/package/create-app-package-with-makeappx-tool) משמש ליצירת שניהם חבילות אפליקציות (.msix או .appx) וקבצי חבילת אפליקציות .msixbundle או .appxbundle). בנוסף, הוא יכול לחלץ קבצים מחבילת אפליקציה. MakeApp.exe זמין עם Windows 10 SDK וניתן להשתמש בו משורת הפקודה.
1. שימוש ב-Microsoft Visual Studio - מפתחים בדרך כלל [יוצרים קבצי APPX](https://docs.microsoft.com/en-us/windows/msix/desktop/vs-package-overview) באמצעות Microsoft Visual Studio. לאחר השלמת פיתוח האפליקציה והאפליקציה מוכנה לפרסום, ניתן ליצור קובץ חבילת APPX על ידי פרסומו מתוך Visual Studio.

## הפניות

* [צור חבילה או חבילה של MSIX עם MakeAppx.exe](https://docs.microsoft.com/en-us/windows/msix/package/create-app-package-with-makeappx-tool)
* [צור קובצי APPX באמצעות Microsoft Visual Studio](https://docs.microsoft.com/en-us/windows/msix/desktop/vs-package-overview)

