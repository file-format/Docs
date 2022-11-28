{
  "date" : "2021-09-08",
  "keywords" :[ "קובץ pcc", "פורמט קובץ pcc", "מהו קובץ pcc", "קובץ", "דוגמה ל-pcc", "סיומת קובץ pcc","הרחבה", "פורמט" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"למד על פורמט קבצי Mass Effect PCC וממשקי API שיכולים ליצור ולפתוח קובצי PCC.",
  "title" :"PCC - Mass Effect Package File",
  "linktitle" : "PCC",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## מהו קובץ PCC?

קובץ עם ‎.pcc הוא קובץ [Mass Effect Game](https://www.ea.com/games/mass-effect/mass-effect-3) המכיל נתוני משחק לשינוי תוכן משחק כגון דגמים, מרקמים ו חדרים. Mass Effect 2 ו-3 הם משחקי יריות ראשונים המבוססים על מנוע המשחקים Unreal Engine 3. המשחק פותח בתחילה על ידי [Bioware](https://www.bioware.com/about/) ששמר את רוב משאבי המשחק בפורמט הקובץ הקנייני שלהם PCC. Bioware נרכשה על ידי Electronic Arts, מוציאה לאור עולמית מובילה בתחום הבידור האינטראקטיבי.

## פורמט קובץ PCC - מידע נוסף

קבצי PCC מכילים מבנים דחוסים ו/או לא דחוסים התורמים לארגון הקבצים הכולל.

### מבנה PCC דחוס

קובץ PCC דחוס מורכב מטבלאות ונתונים המחולקים לנתחים. כל נתח מכיל מספר משתנה של בלוקים דחוסים.

* `Chunks Header` - כותרת משותפת של 16 בתים, המכילה מידע על הנתחים.
* `Chunk Header` - כותרת בת 16 בתים המכילה מידע על הנתונים הדחוסים הגולמיים הכלולים בטופס הבלוק.

### מבנה PCC לא דחוס

קבצי PCC לא דחוסים מחולקים לחמישה חלקים הבאים.

* `Header` - מכיל מידע בסיסי על מבנה קובץ PCC.
* `Name Table` - מכיל שם שנמצא בתוך החבילה כולל מחלקות ייבוא, ייצוא ומאפייני ייצוא.
* `ייבוא טבלה` - מכיל את כל המחלקות והאובייקטים המיובאים על ידי ה-PCC.
* `ייצוא טבלה` - מכיל את כל האובייקטים המאוחסנים בחבילה. כל ייצוא יכול להשתנות בגודלו.

## הפניות

* [Me3Explorer - פורמט קובץ PCC](https://me3explorer.fandom.com/wiki/PCC_File_Format)
* [משחק Mass Effect](https://www.ea.com/games/mass-effect/mass-effect-3)
* [Bioware](https://www.bioware.com/about/)

