{
  "date" : "2022-04-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"פורמט קובץ AWK - קובץ סקריפט AWK",
  "description":"למד על פורמט קובץ AWK וממשקי API שיכולים ליצור ולפתוח קובצי AWK.",
  "linktitle" : "AWK",
  "menu" : {
    "docs" : {
      "identifier" : "programming-awk",
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-03"
}

## מהו קובץ AWK?

קובץ AWK הוא קובץ סקריפט שנוצר עבור אפליקציית עיבוד הטקסט **AWK** שמגיע עם מערכות הפעלה Unix ו-Linux. הוא מכיל הוראות הגיוניות לביצוע פעולות על טקסט או תוכן של קובץ כגון התאמה, החלפה והדפסה של טקסט. זה עוזר להפיק דוחות וטקסט מעוצב מקובץ הקלט. כלי השירות awk ממוקם בדרך כלל ב- /usr/bin/awk ברוב ההפצות של לינוקס/יוניקס.

## כיצד ליצור סקריפט AWK?

ניתן ליצור או לפתוח קובץ AWK בכל עורך טקסט ב-Linux/Unix OS. ניתן ליצור קובץ סקריפט חדש של AWK כדלקמן.

```
$ vi script.awk
```

פעולה זו תפתח את קובץ ה-AWK בעורך הטקסט. הזן כמה הצהרות בעורך הטקסט כדלקמן.

```
#!/usr/bin/awk -f
BEGIN { printf "%s\n","Writing my first Awk executable script!" }
```
השורה הראשונה של תוכן טקסט זה מוסברת כדלקמן.

*\#! – המכונה `Shebang`, המציין מתורגמן להוראות בתסריט
* /usr/bin/awk - הוא המתורגמן
* -f - אפשרות מתורגמן, משמשת לקריאת קובץ תוכנית

## כיצד לבצע סקריפט AWK?

שמור את הקובץ והפוך את הסקריפט לניתן להפעלה על ידי הוצאת הפקודה למטה:
```
$ chmod +x script.awk
```

לאחר מכן ניתן להפעיל את הסקריפט כדלקמן.

```
$ ./script.awk
```

שמביא לתוצאה הבאה.

```
Writing my first Awk executable script!
```

## התייחסות ##

* [כתוב סקריפטים באמצעות שפת תכנות Awk](https://www.tecmint.com/write-shell-scripts-in-awk-programming/)

