{
  "date" : "2019-10-11",
  "keywords": [ "sh file", ".sh file", "extension", "format", "sh file example", "sh file format", "how to run sh file" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SH - Bash Shell Script File",
  "description":"למד על פורמט קובץ SH וממשקי API שיכולים ליצור ולפתוח קובצי SH.",
  "linktitle" : "SH",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-21"
}

## מהו קובץ SH?

קובץ עם סיומת .sh הוא קובץ פקודות בשפת סקריפט המכיל תוכנת מחשב שתופעל על ידי מעטפת Unix. זה יכול להכיל סדרה של פקודות הפועלות ברצף כדי לבצע פעולות כגון עיבוד קבצים, ביצוע של תוכניות ומשימות אחרות כאלה. אלה מבוצעים מממשק שורת הפקודה על ידי משתמש או באצווה כדי לבצע מספר פעולות בו זמנית. ניתן לפתוח קבצי סקריפט בעורכי טקסט כמו Notepad, Notepad++, Vim, Apple Terminal ויישומים דומים אחרים ב-Windows, MacOS ו-Linux OS.

## פורמט קובץ SH

קבצי SH נכתבים בטקסט רגיל בעקבות התחביר שהוגדר. קבצי סקריפט אלה תומכים:

* `תגובות` - הערות מתחילות ב-# והקליפה מתעלמת מהן.
* `קיצורי דרך` - ניתן להשתמש בהם כדי לשנות שם של פקודה לביצוע קצר וקל.
* 'עבודות אצווה' - ניתן לבצע מספר פקודות באופן אוטומטי שאחרת היה צריך להזין אותן באופן ידני. זה מסיר את הצורך להמתין עד שהמשתמש יפעיל כל שלב ברצף.
* `הכללה` - באמצעות לולאות פשוטות, מושגת הרבה יותר הכללה עבור פעולות כמו המרת תמונות מפרומט אחד לאחר.

## דוגמה לקובץ SH

```
$ echo '#!/bin/sh' > my-script.sh
$ echo 'echo Hello World' >> my-script.sh
$ cat my-script.sh
#!/bin/sh
echo Hello World
$ chmod 755 my-script.sh
$ ./my-script.sh
Hello World
```
## כיצד להפעיל קובץ SH?
קבצי ה-SH בדרך כלל פועלים על לינוקס, אפילו ב-Windows צריך להתחבר למסוף לינוקס באמצעות תוכנות כמו Putty כדי להפעיל את קבצי ה-sh. להלן השלבים להפעלת קובץ SH במסוף לינוקס.

1. פתחו את מסוף לינוקס ועברו לספרייה שבה נמצא קובץ ה-SH.
2. על ידי שימוש בפקודה `chmod`, הגדר הרשאת ביצוע בסקריפט שלך (אם לא הוגדר כבר).
3. הפעל סקריפט באמצעות אחד מהאפשרויות הבאות
1. `./filename.sh`
2. `sh filename.sh`
3. `bash script-name-here.sh`

## הפניות

* [Bashscripting למתחילים](https://help.ubuntu.com/community/Beginners/BashScripting)
* [Shellscript](https://www.shellscript.sh/)

