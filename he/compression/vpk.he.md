{
  "date" : "2022-03-01",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"קובץ VPK - פורמט קובץ חבילת יישומים של PlayStation Vita",
  "description":"למד על פורמט קובץ VPK וממשקי API שיכולים ליצור ולפתוח קובצי VPK.",
  "linktitle" : "VPK",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-03-01"
}

## מהו קובץ VPK?

קובץ עם סיומת .vpk הוא קובץ חבילת ארכיון דחוס המשמש להתקנת אפליקציות צד שלישי בקונסולת המשחקים Sony PlayStation Vita. ניתן להתקין קבצים אלה רק ב-Jailbreak Vita PlayStation של HENkaku שאפשרה ל-PS Vita ול-PSTV להשתמש בתוכן מותאם אישית שנוצר על ידי המשתמש. קובץ ארכיון VPK מכיל את כל התוכן המרכיב את המשחק כולל תמונות כגון קבצי [PNG](/he/image/png/), קבצי הגדרות כגון [.bin](/he/disc-and-media/bin/) ו כל תצורות בפורמט קובץ [XML](/he/web/xml/).

## פורמט קובץ VPK

קבצי VPK נשמרים בדיסק כארכיוני [ZIP](/he/compression/zip/) דחוסים סטנדרטיים. אלה עשויים להכיל תיקיות מרובות וקבצים משויכים אחרים עבור אפליקציות צד שלישי שיותקנו ב-Vita Gaming Console. כדי להציג את התוכן של קובץ חבילת VPK, שנה את שם הסיומת שלו מ-.vpu ל-.zip, וחלץ את התוכן באמצעות כלי עזר סטנדרטיים לביטול דחיסה כגון WinZip או WinRAR.

ל-Valvesoftware יש מידע מפורט על [פורמט הקובץ VPK](https://developer.valvesoftware.com/wiki/VPK_File_Format) שניתן להתייחס אליו מנקודת המבט של המפתח.

## כיצד להתקין קבצי VPK?

ניתן להתקין את קבצי ה-VPK משירות שורת הפקודה VPK.exe. במערכת ההפעלה Windows, ניתן להוריד קבצים בקובץ vpk.exe שמחזיר קובץ \*.vpk המכיל את כל הקבצים הארוזים. לחלופין, ניתן להשתמש בכלי שורת הפקודה כדלקמן.

### צור VPK והוסף קבצים

```
vpk <dirname>
```

### חלץ קבצי VPK

```
vpk x <vpkfile> <filename1> <filename2> ...
```

## VPK Viewer

* [VRF VPK Viewer](https://github.com/SteamDatabase/ValveResourceFormat)

## הפניות

* [פורמט קובץ VPK](https://developer.valvesoftware.com/wiki/VPK_File_Format)
* [קבצי VPK](https://developer.valvesoftware.com/wiki/VPK)

