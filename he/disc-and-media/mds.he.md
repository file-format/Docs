{
  "date" : "2023-01-23",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "למד על פורמט קובץ MDS וממשקי API שיכולים ליצור ולפתוח קובצי MDS.",
  "title" : "פורמט קובץ MDS - Media Descriptor Sidecar File",
  "linktitle" : "MDS",
  "menu" : {
    "docs" : {
      "identifier":"disc-and-media-mds-he",
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2023-01-23"
}

## מהו קובץ MDS?

ה-MDS (Media Descriptor Sidecar File) הוא קובץ המשויך לתוכנה Alcohol 120% ו-Daemon Tools, שניהם משמשים ליצירה וניהול של כונני CD ו-DVD וירטואליים. קובץ ה-MDS מכיל מידע על פריסת הנתונים בדיסק, כולל מיקום כל הקבצים ומבנה הדיסק. זה מאפשר לכונן הוירטואלי לחקות את ההתנהגות של דיסק פיזי, כך שהתוכנה יכולה לקרוא את הנתונים בדיסק הוירטואלי כאילו היה דיסק אמיתי.

When you want to mount an image file to a virtual drive, the MDS file is used along with the corresponding image file in a format such as ISO, BIN or CUE. The MDS file contains a description of the layout of the data on the disc, and the virtual drive software uses this information to create a virtual disc. This allows you to use the software as if you were using a physical disc, without having to physically insert the disc into the drive.

## קשר עם אלכוהול 120%

אלכוהול 120% היא תוכנה פופולרית ליצירה וניהול של כונני CD ו-DVD וירטואליים, והיא משתמשת בפורמט הקובץ MDS כדי לשמור ולגשת לתמונות דיסק. פורמט הקובץ MDS הוא קנייני של Alcohol 120% וניתן לפתוח אותו ולהשתמש בו רק על ידי תוכנת Alcohol 120% או תוכנה אחרת התומכת בו.

## איך פותחים קובץ MDS?

כדי לפתוח קובץ MDS ב-Alcohol 120%, תצטרך להתקין את התוכנה במחשב שלך. לאחר התקנת אלכוהול 120%, תוכל לפתוח את קובץ MDS על ידי ביצוע הפעולות הבאות:

1. השקת אלכוהול 120%.
2. לחץ על התפריט קובץ ובחר פתח.
3. נווט אל המיקום של קובץ ה-MDS במחשב ובחר בו.
4. קובץ ה-MDS ייפתח כעת ב-Alcohol 120%, ותתבקש לבחור את קובץ התמונה המתאים (כגון ISO, BIN או CUE).
5. לאחר שתבחר את קובץ התמונה, אלכוהול 120% יעלה את התמונה לכונן וירטואלי.

לחילופין, ניתן גם לפתוח קובץ MDS על ידי לחיצה כפולה עליו, אם אלכוהול 120% מוגדר כתוכנית ברירת המחדל לפתיחת קבצי MDS. אתה יכול גם להשתמש בתוכנות אחרות התומכות בפורמט MDS כמו Daemon Tools, Virtual CloneDrive, Virtual Drive Manager ו-MagicISO.

## הפניות
* [אלכוהול 120% - תוכנת צריבת תקליטורים ו-DVD](https://www.alcohol-soft.com/)


