{
  "date" : "2022-07-21",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"פורמט קובץ HDR - מהו קובץ תמונה HDR?",
  "description":"למד על פורמט קבצי HDR וממשקי API שיכולים ליצור ולפתוח קובצי HDR.",
  "linktitle" : "HDR",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2022-07-21"
}

## מהו קובץ HDR?

קובץ HDR הוא פורמט של תמונת רסטר גבוהה (HDR) לאחסון תמונות ממצלמה דיגיטלית. זה מאפשר לעורכי תמונות לשפר את הצבע והבהירות של תמונות דיגיטליות בעלות טווח דינמי מוגבל. שינוי זה יכול לשפר את הבהירות מסביב לפינות, וכתוצאה מכך תמונה קרובה לטבעית. קבצי HDR נשמרים בדרך כלל כתמונות רסטר של 32 סיביות. Adobe Photoshop יכולה ליצור ולפתוח קובצי HDR.

קבצי HDR ידועים גם בשם HDRI.

## פורמט קובץ HDR - מידע נוסף

פורמט הקובץ HDR מבוסס על פורמט הקובץ המקורי של Radiance Picture (.pic). נתוני הפיקסלים של קובץ HDR מאוחסנים בדרך כלל לא דחוסים, אך במקרים מסוימים הם נדחסים באמצעות מערכת קידוד באורך ריצה פשוטה.

### מבנה קובץ HDR

קובץ תמונת HDR מורכב משלושת החלקים הבאים:

* **כותרת:** קובץ HDR מזוהה לפי הבייטים הראשונים בקובץ התמונה, כלומר "#?RADIANCE".
* **מחרוזת רזולוציה:** הכותרת מלווה בשורת רזולוציה אחת המורכבת מ-4 ערכים; תווית X ו-Y כל אחת ואחריה ערך מספר שלם. סדר ה-X וה-Y מציין סיבוב. השילוב של X ו-Y עם ערכים חיוביים ושליליים מכסה את כל כיוון התמונה והסיבובים האפשריים.
* **נתוני פיקסלים:** נתוני הפיקסלים של קובץ HDR אינם דחוסים או דחוסים באמצעות קידוד באורך ריצה סטנדרטי.

## ממשקי API של HDR/HDRI בקוד פתוח

* **[imageinfo](https://github.com/xiaozhuai/imageinfo )** - ספריית כותרות בודדות [C++](/he/programming/cpp/) סופר מהירה בפלטפורמות כדי לקבל גודל ופורמט תמונה ללא טעינה/פענוח.
* **[imgaeinfo-rs](https://github.com/xiaozhuai/imageinfo-rs)** - ספריית חלודה לקבלת גודל ופורמט תמונה ללא טעינה/פענוח. תומך ב-[.avif](/he/image/avif/), [.bmp](/he/image/bmp), [.cur](/he/image/cur/), [.dds](/he/image/dds/), [. gif](/he/image/gif/), hdr (pic), [heic (heif)](/he/image/heic/), [.icns](/he/image/icns/), [.ico](/he/image/ico /), [.jp2](/he/image/jp2/), [jpeg (jpg)](/he/image/jpeg/), [jpx](/he/image/jpx/), ktx, [png](/he/image/png /), [psd](/he/image/psd/), qoi, tga, tiff (tif) ו-webp.
* **[HdrHistogram](https://github.com/HdrHistogram/HdrHistogram)** - יישום Java של HdrHistogram.

## הפניות

* [Radiance HDR](http://paulbourke.net/dataformats/pic/)
* [imageinfo](https://github.com/xiaozhuai/imageinfo )

