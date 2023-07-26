{
  "date" : "2022-03-02",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"קובץ TGZ - קובץ טאר Gzipped",
  "description":"למד על פורמט קובץ TGZ וממשקי API שיכולים ליצור ולפתוח קובצי TGZ.",
  "linktitle" : "TGZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-03-02"
}

## מהו קובץ TGZ?

קובץ עם סיומת .tgz הוא קובץ ארכיון TAR, המורכב ממספר קבצים ותיקיות, שנדחס באמצעות תוכנת הדחיסה Gnu Zip (gzip). קובץ [TAR](/he/compression/tar/) משלב בדרך כלל מספר קבצים לקובץ אחד לגיבוי או הפצה דרך האינטרנט. זהו קובץ Uncompress עד שהוא נדחס באמצעות תוכנת gzip ולאחר מכן הוא הופך לקובץ TGZ. קבצי TGZ, בהיותם קבצים דחוסים, תופסים פחות מקום בדיסק וניתנים להעברה בקלות באמצעות האינטרנט באמצעות דואר אלקטרוני. יישומים מסוימים שיכולים לפתוח קבצי TGZ כוללים WinZip, Apple Archive Utility, 7-Zip ו-WinRAR. קבצי TGZ משמשים בעיקר במערכת UNIX ולינוקס.

## פורמט קובץ TGZ

קבצי TGZ נשמרים כקבצים בינאריים דחוסים באמצעות אלגוריתם הדחיסה [GZ](/he/compression/gz/).

## כיצד לפרוק קובץ tgz ב-Linux

במערכת ההפעלה Linux/Unix, ניתן להשתמש בפקודה הבאה כדי לפרוק קבצי TGZ משורת הפקודה.

```
tar zxvf tgzCompressedFile.tgz
```

הפקודה לעיל משחררת את קובץ ה-TGZ הדחוס ומחלצת את הקבצים שלו מארכיון TAR לדיסק.
## הפניות ##

* [TGS](https://core.telegram.org/stickers#animated-stickers)
* [gzip - ויקיפדיה](https://en.wikipedia.org/wiki/Gzip)

