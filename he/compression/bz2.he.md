{
  "date" : "2019-10-11",
  "keywords" :[ "קובץ bz2", "פורמט קובץ bz2", "מהו קובץ bz2", "קובץ", "דוגמה של bz2", "סיומת קובץ bz2","הרחבה", "פורמט" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"BZ2 - פורמט קובץ דחוס",
  "description":"למד לדעת מה זה קובץ BZ2 וממשקי API שיכולים ליצור ולפתוח קבצי BZ2.",
  "linktitle" : "BZ2",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2020-09-05"
}

## מהו קובץ BZ2?

BZ2 הם קבצים דחוסים שנוצרו באמצעות שיטת הדחיסה [BZIP2](http://www.bzip.org/) בקוד פתוח, בעיקר במערכת UNIX או Linux. הוא משמש לדחיסת קובץ בודד ואינו מיועד לארכיון של מספר קבצים. זאת בניגוד לפורמט הקובץ TAR באותן פלטפורמות ששומר מספר קבצים לקובץ בודד אך ללא דחיסה. ניתן לפרק קבצים דחוסים כ-BZ2 עם יישומים כמו [WinZip](https://www.winzip.com/win/en/). BZIP2 משתמש באלגוריתם דחיסה של Run-Length Encoding (RLE) או [Burrows-Wheeler](https://en.wikipedia.org/wiki/Burrows%E2%80%93Wheeler_transform) כדי להשיג רמות גבוהות של דחיסה.

## פורמט קובץ BZ2

אין מפרטים רשמיים זמינים עבור פורמט קובץ זה. עם זאת, [מפרט הנדסה לאחור](https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf) לא רשמי מראה שזרם ‎.bz2 מורכב מכותרת של 4 בתים שאחריה עוקבים אחריהם על ידי אפס או יותר בלוקים דחוסים. מיד אחריו מופיע סמן סוף הזרם המכיל CRC של 32 סיביות עבור הטקסט הרגיל שעובד. אין ריפוד בין הבלוקים הדחוסים וכל הבלוקים מיושרים ביט.

## פתח/חלץ קובץ BZ2

אתה יכול לפתוח קובץ BZ2 ב-Windows וב-Mac OS באמצעות תוכנה כמו WinZip. בלינוקס, הפקודה הבאה בטרמינל.

```
bzip2 -d filename.bz2
```

## הפניות

* [מפרטי פורמט BZIP2](https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf)

