{
  "date" : "2022-06-20",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"פורמט קובץ FZPZ - קובץ חלקי Fritzing",
  "description":"למד על מהו קובץ FZPZ וממשקי API שיכולים ליצור ולפתוח קובצי FZPZ.",
  "linktitle" : "FZPZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-20"
}

## מהו קובץ FZPZ?

קובץ FZPZ הוא רכיב/חלק המשמש בתכנון מעגלים אלקטרוניים שנוצרו עם אפליקציית אב-טיפוס ועיצוב מעגלים **Fritzing**. זהו ארכיון דחוס המכיל קובץ [FZP](/he/cad/fzp/) וארבע תמונות [SVG](/he/page-description-language/svg/) המתארות את החלק הכולל ב- Fritzing. היתרון בשימוש בקבצים אלה הוא שמשתמשים יכולים לשתף את קבצי ה-FZPZ שלהם עם כל אחד מנקודת מבט של שימוש חוזר. השיתוף של חלקי FZPZ עוזר בשילוב חלקי מעגלים כדי ליצור עיצובי PCB גדולים יותר בצורה מהירה.

## פורמט קובץ FZPZ - מידע נוסף

קבצי FZPZ נשמרים בתקליטור כארכיונים דחוסים [ZIP](/he/compression/zip/). אתה יכול לשנות את שם הסיומת מ-.fzpz ל-.zip ולהשתמש בכל כלי עזר סטנדרטי לביטול דחיסה כגון WinZIP כדי לחלץ את הקבצים מהארכיון.

### מידע על מבנה הקובץ FZPZ

כאמור, קובץ FZPZ הוא קובץ ארכיון המכיל קבצים מרובים לייצוג של חלק המשמש במעגלים מודפסים. ה-FZPZ מכיל את הקבצים הבאים:

* `ארבעה קבצי SVG` - המייצגים את לוח הלחם, הסכימה, ה-PCB והאייקונים של חלק
* `FZP file` - קובץ XML המכיל מידע על מאפייני החלק, המחברים והאוטובוסים של החלק

הקבצים נקראים בדרך כלל כדלקמן.

* part.file.fzp
* svg.breadboard.file.svg
* svg.icon.file.svg
* svg.pbc.file.svg
* svg.schematic.file.svg

## הפניות ##

* [חלקים חדשים עם סיומת fzpz](https://forum.fritzing.org/t/new-parts-with-fzpz-extension/8007/2)

