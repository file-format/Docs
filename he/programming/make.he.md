{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"צור קובץ - קובץ סקריפט של Xcode Makefile",
  "description":"למד על XCode MakeFile Format וממשקי API שיכולים ליצור ולפתוח קבצי MakeFile.",
  "linktitle" : "MAKE",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}


## מהו קובץ MAKE?

קובץ MAKE הוא קובץ סקריפט XCode שמארגן קומפילציה של קוד. הוא משמש להדר ולקשר תוכניות ממספר קובצי קוד מקור. עזרה זו להחליט אילו חלקים של יישום גדול נדרשים להידור מחדש כאשר יש לעדכן את היישום. גרמו לקבצים להשתמש בסדרת הוראות להפעלה בהתאם לקבצים שהשתנו.

## דוגמה לפורמט קובץ עשה

התכנים הבאים מבוצעים באמצעות כלי השירות Make והפלטים הם כדלקמן.

```
hello:
	echo "hello world"
```
**צור פלט**

```
$ make
echo "hello world"
hello world
```

## הפניות
* [XCode and Make - Apple Forums](https://developer.apple.com/forums/thread/657458)
* [מדריך אובייקט-C](https://blog.teamtreehouse.com/beginners-guide-objective-c-classes-objects)

