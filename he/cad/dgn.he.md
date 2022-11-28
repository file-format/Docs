{
  "date" : "2020-01-12",
  "keywords" :[ "DGN", "קובץ", "פורמט", "פתח", "קרא", "API", "MicroStation", "Intergraph Interactive Graphics Design System" ],
  "author" :{
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DGN - MicroStation CAD Design File Format",
  "description" :"למד על פורמט קובץ DGN וממשקי API שיכולים ליצור ולפתוח קובצי DGN.",
  "linktitle" : "DGN",
  "menu" :{
    "docs" :{
      "parent" : "cad"
}
},
  "lastmod" : "2020-01-12"
}

## מהו קובץ DGN?

קובץ עם סיומת .dgn (Design) הוא קובץ ציור שנוצר ונתמך על ידי יישומי CAD כגון MicroStation ו-Intergraph Interactive Graphics Design System. הוא משמש ליצירה ושמירת עיצובים עבור פרויקטי בנייה כגון כבישים מהירים, גשרים ומבנים. הפורמט דומה לפורמט הקובץ [DWG](/he/cad/dwg/) של Autodesk ונחשב למתחרה שלו. ניתן לשמור קבצי DNG כ-Intergraph Standard File Format או V8 DGN. ניתן להמיר DGN למספר פורמטים אחרים כגון DWG, [BMP](/he/image/bmp/), [JPEG](/he/image/jpeg/), [PDF](/he/pdf/), [GIF](/he/image/ gif/) ואחרים. ניתן לפתוח אותו עם Autodesk AutoCAD, Bentley View ו-Bentley Systems MicroStation בנוסף ליישומי תוכנה אחרים כגון Corel PaintShop Photo Pro ו-IMSI TurboCAD Deluxe.

## פורמט קובץ V8 DGN

קובץ MicroStation V8 DGN מורכב מדגם אחד או יותר. דגם הוא מיכל לאלמנטים. ה-V8 DGN מסיר את כל האילוצים המבוססים על פורמט קבצים שהיו בגירסאות קודמות של MicroStation. להלן רשימה של שיפורים בפורמט הקובץ DGN.

* הגבלה על מספר הרמות בקובץ DGN הוסרה, וכל רמה נקראת ומאוחסנת כאלמנט.
* לגודל הפיזי המרבי של קובץ ה-DGN אין כל הגבלה והוא מוגבל רק על ידי מערכת ההפעלה (כגון מגבלת NT היא 4 GB)
* הגודל המרבי של רכיב בודד הוא 128 KB.
* אין הגבלה על הגודל המרבי של תא.
* שמות התאים מוגבלים לכ-500 תווים.
* אין הגבלה על מספר הפניות שניתן לצרף לקובץ DGN.
* מחרוזת קו, צורה או עקומת נקודה יכולה לכלול עד 5000 קודקודים.
* אין הגבלה למספר הרכיבים בשרשרת מורכבת או בצורה מורכבת.
* אין הגבלה למספר הקבוצות הגרפיות בקובץ DGN.
* הגדר מקבילה לנוף בו היא מוצבת.
* שורת טקסט בודדת יכולה להכיל 65,535 תווים.
* אין הגבלה על הגודל המרבי של צומת טקסט.
* אין הגבלה למספר צמתי הטקסט בקובץ DGN.
* לכל אלמנט יש מזהה ייחודי של 64 סיביות שאינו משתנה במהלך מחזור החיים של האלמנט.
* לכל אלמנט יש חותמת זמן המציינת את מועד השינוי האחרון.

## הפניות

* [DNG - מאת ויקיפדיה](https://en.wikipedia.org/wiki/DGN)
* [OpenDNG](http://www.bentley.com/opendgn)
* [פורמט קובץ MicroStation V8 DGN](https://web.archive.org/web/20120713013730/http://docs.bentley.com/ko/MicroStation/ustnhelp47.html)

