{
  "date" : "2019-10-11",
  "keywords" :[ "קובץ tbz", "פורמט קובץ tbz", "מהו קובץ tbz", "קובץ", "דוגמה tbz", "סיומת קובץ tbz","הרחבה", "פורמט" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TBZ - Bzip Compressed Tar Archive",
  "description":"למד על פורמט קובץ TBZ וממשקי API שיכולים ליצור ולפתוח קבצי TBZ.",
  "linktitle" : "TBZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-05"
}

## מהו קובץ TBZ?

קובץ עם סיומת .tbz הוא ארכיון דחוס המשתמש בדחיסת BZIP להקטנת גודל קבצי התוכן. קבצי TBZ הם למעשה קבצי UNIX [TAR](/he/compression/tar/) בארכיון שנדחסים עם BZIP אז. הדחיסה העדכנית ביותר ברמה השנייה היא [BZIP2](/he/compression/bz2/) שהחליפה את BZIP. פורמט קובץ TBZ מתאים להעברת קבצים גדולים. ניתן לפתוח/לחלץ קבצי TBZ באמצעות יישומי תוכנה כגון 7-Zip, PeaZip ו-jZip. משתמשי לינוקס ו-macOS יכולים גם לפתוח TBZ עם הפקודה BZIP2 מחלון מסוף.

## פורמט קובץ TBZ

קבצי TBZ הם למעשה ארכיונים דחוסים שנוצרו עם דחיסת BZIP/[BZIP2](/he/compression/bz2). אין מפרטים רשמיים זמינים עבור פורמט קובץ זה. עם זאת, [מפרט הנדסה לאחור] (https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf) לא רשמי מראה שזרם ‎.bz2 מורכב מכותרת של 4 בתים שאחריה עוקבים אחריהם על ידי אפס או יותר בלוקים דחוסים.

## הפניות ##

* [מפרטי פורמט BZIP2](https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf)

