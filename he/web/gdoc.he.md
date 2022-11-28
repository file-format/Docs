{
  "date" : "2022-01-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"קובץ GDOC - קיצור דרך של Google Docs",
  "description":"למד על מהו קובץ GDOC וממשקי API שיכולים ליצור ולפתוח קבצי GDOC.",
  "linktitle" : "GDOC",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-01-23"
}

## מהו קובץ GDOC?

קובץ GDOC הוא קובץ קיצור המצביע על קובץ שנמצא ב-Google Drive, שירות אחסון מסמכים מבוסס ענן. כאשר לקוח Google Drive מותקן במחשב ונוצר בתוכו מסמך, הכונן יוצר מסמך באחסון הענן המקוון וכותב את [URL](/he/web/url/) של מסמך זה בקובץ GDOC ב-Google המקומית תיקיית Drive. כאשר לוחצים פעמיים על קובץ קיצור זה, דפדפן האינטרנט המוגדר כברירת מחדל פותח את המסמך ממיקום [URL](/he/web/url/). אם קובץ קיצור זה מועבר מתיקיה זו, הקישור למסמך מקוון נשבר.

## פורמט קובץ GDOC - מידע נוסף

קובץ GDOC מכיל קיצור דרך למסמך המקוון שנכתב בפורמט קובץ [JSON](/he/web/json/). הדפדפן הפותח קבצי GDOC קורא את פרטי כתובת האתר ופותח את המסמך המקושר להצגה בתנאי שהמשתמש מחובר לחשבון Google זה שבו המסמך מאוחסן. קבצי GDOC אינם מכילים את תוכן המסמך.

### דוגמה לקובץ GDOC

ניתן לפתוח קובץ GDOC בעורך טקסט והתוכן שלו נראה כמו הבא.

```
{"url": "https://docs.google.com/a/test.com/spreadsheet/ccc?key=01234567898765432123456789&usp=docslist_api", "resource_id": "spreadsheet:0A12345B678HJK9TZPL9078767"}
```

כפי שניתן לראות, התוכן מעוצב ב-JSON עם כתובת URL של מסמך ומזהה המסמך המשויך.

## הפניות

* [Google Docs לא פותח קבצי gdoc או docx](https://support.google.com/docs/thread/8408691/google-docs-not-opening-either-gdoc-or-docx-files?hl=iw )

