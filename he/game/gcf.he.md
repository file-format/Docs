{
  "date" : "2023-01-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"למד על פורמט קובץ GCF וממשקי API שיכולים ליצור ולפתוח קובצי GCF.",
  "title" : "קובץ GCF - Nadeo Game GCF Format",
  "linktitle" : "GCF",
  "menu" : {
    "docs" : {
      "identifier":"game-gcf-he",
      "parent" : "game"
}
},
  "lastmod" : "2023-01-19"
}

## מהו קובץ GCF?

קובץ .gcf הוא קובץ מטמון משחק המשמש את פלטפורמת המשחקים Steam. הוא מכיל נתוני משחק כגון טקסטורות, דגמים וקבצים אחרים המשמשים את המשחק. קבצים אלו מאוחסנים במחשב של המשתמש ומשמשים להפחתת כמות הנתונים שיש להוריד בעת עדכון או התקנה של משחק. ניתן להשתמש בקבצי ה-.gcf גם ליצירת גיבויים של התקנת משחק או להעברת משחק בין מחשבים.

ניתן לקרוא ולכתוב קובצי GCF באמצעות ספריית התכנות C++ בקוד פתוח, **HLLib**.

## פורמט קובץ GCF

קבצי GCF נשמרים בדיסק כקבצים בינאריים. GCF שימש במקור כראשי תיבות של Grid Cache File (שם הקוד המוקדם של Steam היה Grid), אך מאוחר יותר הוא נלקח כקובץ מטמון משחק. קובץ GCF הוא קובץ ארכיון המאחסן משחקי Steam. כל התוכן הרשמי מוורד כקבצי GCF. ניתן לשתף קבצי GCF גם בין משחקים.

הערה: GCF הוא קודמו של [VPK file format](/game/vpk/).
## הפניות

* [תוכנת שסתום](https://www.valvesoftware.com/en/)

* [פורמט קובץ GCF](https://developer.valvesoftware.com/wiki/GCF)

* [HLLib - ספריית תכנות C++ בקוד פתוח לקריאת קבצי GCF](https://developer.valvesoftware.com/wiki/HLlib)


