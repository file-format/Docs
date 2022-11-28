{
  "date" : "2021-04-22",
  "keywords": [ "msix file", "extension", "format","how to open msix file","msix file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MSIX - מהו קובץ MSIX?",
  "description":"למד על קבצי MSIX וממשקי API שיכולים ליצור ולפתוח קובצי MSIX.",
  "linktitle" : "MSIX",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-12-16"
}

## מהו קובץ MSIX?

קובץ MSIX הוא פורמט אריזה של אפליקציות Windows המשמש ליצירה והפצה של יישומים ב-Windows 10. זהו פורמט קובץ החבילה המודרני בהשוואה ל-[APPX](/he/programming/appx/) ו-MSI שיופסקו סופית. לפורמט הקובץ החדש הזה. ניתן להשתמש בו לפריסה של אפליקציות Win32, WPF ו-Windows Forms. קבצי MSIX הם אמינים ומטרתם אופטימיזציה של שטחי רשת ודיסק. מפתחים משתמשים בהם כדי להפיץ תוכניות למשתמשי קצה דרך חנות Microsoft (שנודעה בעבר כ-Windows Store).

## פורמט קובץ MSIX - מידע נוסף

קבצי MSIX דחוסים [ZIP](/he/compression/zip/), כאשר כל הקבצים כלולים בתוך הקובץ הארוז. בנוסף לקבצים הקשורים לאפליקציה, קובץ MSIX מכיל [.xml](/he/web/xml/) קובצי תצורה המכילים מידע הקשור להתקנת האפליקציה.

## מה יש בתוך חבילת MSIX?

חבילת MSIX מורכבת מהקבצים הבאים.

* `AppxBlockMap.xml` - המכונה קובץ מפת בלוק החבילה, זהו מסמך XML המכיל רשימה של קבצי האפליקציה עם אינדקסים ו-hashs קריפטוגרפיים עבור כל בלוק נתונים המאוחסן בחבילה.
* `AppxManifest.xml` - מסמך XML המכיל את המידע הנדרש לפריסה, תצוגה ועדכון של אפליקציית MSIX. מידע זה כולל זהות חבילה, תלות בחבילה, יכולות נדרשות, אלמנטים חזותיים ונקודות הרחבה.
* `AppxSignature.p7x` - קובץ שנוצר כאשר החבילה נחתמת. כל חבילות MSIX נדרשות להיות חתומות לפני ההתקנה. עם AppxBlockmap.xml, הפלטפורמה מסוגלת להתקין את החבילה ולקבל אימות.

## הפניות

* [סקירה כללית של MSIX](https://docs.microsoft.com/en-us/windows/msix/overview)
* [צור קובצי APPX באמצעות Microsoft Visual Studio](https://docs.microsoft.com/en-us/windows/msix/desktop/vs-package-overview)

