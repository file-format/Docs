{
  "date" : "2019-12-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"פורמט קובץ ZIM - OpenZIM Archive File",
  "description":"למד על פורמט קובץ ZIM וממשקי API שיכולים ליצור ולפתוח קובצי ZIM.",
  "linktitle" : "ZIM",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2019-12-09"
}

## מהו קובץ ZIM? ##

קבצים עם סיומת .zim הם ארכיונים שנוצרו כדי לאחסן תוכן Wiki במצב לא מקוון. זה נחשב לפורמט הקובץ הפתוח המתאים ביותר לאחסון ויקיפדיה ב-USB. הוא מאחסן את תוכן האתר בפורמט קומפקטי. השם שלו בא מ"Zeno IMproved" שהיה פורמט הקובץ הקודם של Zeno. צים מתוחזקת על ידי פרויקט [openZIM ](https://openzim.org/) אשר ממומן על ידי Wikimedia CH, ונתמך על ידי קרן ויקימדיה. ניתן לפתוח קבצי ZIM באמצעות יישומים כמו Kiwix ו-ZIMReader. פרויקט OpenZIM אירח את היישום של פורמט קובץ ZIM ב-[Github](https://github.com/openzim) עבור תרומה מקהילת OpenSource.

## מפרט פורמט קובץ ZIM

פורמט קובץ ZIM פותח על גבי [פורמט קובץ Zeno](https://openzim.org/wiki/Zeno_file_format) ואינו תואם לאחור. מפרטי הפורמט של פורמט קובץ ZIM הם [זמינים באינטרנט](https://openzim.org/wiki/ZIM_file_format) על ידי openZIM לעיון המפתחים. OpenZIM סיפקה הטמעת קוד פתוח של C++, [LibZim](https://openzim.org/wiki/Zimlib), לקריאה וכתיבה של קובצי ZIM.

פורמט קובץ ZIM משתמש בדחיסת LZMA2 כדי להפוך את התוכן לקומפקטי.

{{< figure src="../ZIM_File_Format.jpeg" alt="פורמט קובץ ZIM" >}}


### כותרת צים

קובץ ZIM מתחיל עם כותרת שנמצאת ב-offset 0. כל המרכיבים מבוססים על little-endian וכל המספרים השלמים הם מספרים שלמים ללא סימנים כלומר uint_16, uint_32, uint_64.

|שם שדה |סוג| קיזוז| אורך| תיאור|
---|---|---|---|---|
|magicNumber| מספר שלם| 0| 4| מספר קסם כדי לזהות את פורמט הקובץ, חייב להיות 72173914 (0x44D495A)|
|majorVersion| מספר שלם| 4| 2| הגרסה העיקרית של פורמט הקובץ ZIM (5 או 6)|
|minorVersion| מספר שלם| 6| 2| גרסה מינורית של פורמט הקובץ ZIM|
|uuid| מספר שלם| 8| 16| מזהה ייחודי של קובץ צים זה|
|ArticleCount| מספר שלם| 24| 4| המספר הכולל של מאמרים|
|ClusterCount| מספר שלם| 28| 4| המספר הכולל של אשכולות|
|urlPtrPos| מספר שלם| 32| 8| מיקום רשימת המצביעים של הספרייה מסודרת לפי כתובת URL|
|titlePtrPos| מספר שלם| 40| 8| מיקום רשימת המצביעים של הספרייה מסודרת לפי כותרת|
|clusterPtrPos| מספר שלם| 48| 8| מיקום רשימת מצביעי האשכולות|
|mimeListPos| מספר שלם| 56| 8| מיקום רשימת סוגי MIME (גם גודל כותרת)|
|העמוד הראשי| מספר שלם| 64| 4| עמוד ראשי או 0xffffffff אם אין עמוד ראשי|
|layoutPage| מספר שלם| 68| 4| דף פריסה או 0xffffffffff אם אין דף פריסה|
|checksumPos| מספר שלם| 72| 8| מצביע ל-md5checksum של קובץ זה ללא ה-checksum עצמו. זה מצביע תמיד 16 בתים לפני סוף הקובץ.|

## הפניות ##

* [OpenZIM](https://openzim.org/)
* [C++ LibZim](https://openzim.org/wiki/Zimlib)

