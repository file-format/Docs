{
  "date" : "2022-03-15",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"תבנית קובץ EGG - קובץ הפצה של Python",
  "description":"למד על פורמט קובץ EGG וממשקי API שיכולים ליצור ולפתוח קובצי EGG.",
  "linktitle" : "EGG",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-03-15"
}

## מהו קובץ EGG?

קובץ EGG, הידוע גם בשם Python eggs, הוא תבנית הפצה ישנה יותר של פייתון הפצות. זהו ארכיון דחוס [ZIP](/he/compression/zip/) עם סיומת .egg ומכיל את קבצי המקור של אפליקציית Python יחד עם מטא מידע על ההפצה. קובצי EGG הם חלופיים לקובץ [EXE](/he/executable/exe/) של Windows להפעלה, אך הם חוצה פלטפורמות. פורמט ישן יותר זה להפצות Python הוחלף בפורמט הקובץ החדש יותר Wheel (WHL) בתחילת 2010.

## פורמט קובץ EGG

קבצי EGG נשמרים כארכיוני ZIP דחוסים. המשמעות היא שאם תחליף את סיומת .egg ב-.zip, תוכל לפתוח אותה עם כלי עזר סטנדרטיים לביטול דחיסה כגון Corel WinZIP, Microsoft Explorer או RARLAB WinRAR.

ניתן ליצור קובצי EGG באמצעות חבילת **distutils** הזמינה על ידי Python. כלי נוסף שיכול ליצור ולפתוח קובצי EGG הוא **SetupTools**. ניתן להתקין קבצי EGG כחבילה באמצעות **easy_install**.

`הערה - פורמט קובץ EGG התיישן לטובת פורמט הקובץ WHL החדש של הגלגל.`

## התייחסות ##

* [Python EGGs](https://python101.pythonlibrary.org/chapter38_eggs.html)

