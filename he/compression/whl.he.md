{
  "date" : "2022-06-29",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"פורמט קובץ WHL - קובץ חבילת גלגל Python",
  "description":"למד על פורמט קובץ WHL וממשקי API שיכולים ליצור ולפתוח קובצי WHL.",
  "linktitle" : "WHL",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-29"
}

## מהו קובץ WHL?

קובץ WHL (גלגל) הוא קובץ חבילת הפצה שנשמר בפורמט הגלגל של Python. זוהי התקנה בפורמט סטנדרטי של הפצות Python ומכילה את כל הקבצים והמטא נתונים הנדרשים להתקנה. קובץ WHL מכיל גם מידע על גרסאות ופלטפורמות Python הנתמכות על ידי קובץ גלגל זה. בדומה לקובץ התקנה [MSI](/he/executable/msi/), פורמט קובץ WHL הוא פורמט מוכן להתקנה המאפשר להפעיל את חבילת ההתקנה מבלי לבנות את הפצת המקור.

## פורמט קובץ WHL

פורמט קובץ WHL הוא ארכיון [ZIP](/he/compression/zip/) (.zip) המכיל את כל קבצי ההתקנה והמטא נתונים הנדרשים על ידי מתקינים לצורך התקנת חבילה. ניתן לחלץ קבצי WHL אלה באמצעות אפשרות unzip או יישומי תוכנה סטנדרטיים לביטול דחיסה כגון WinZIP ו-WinRAR.

### אמנת שמות קובץ WHL

קובץ WHL נקרא לפי המוסכמה הבאה.

```
{dist}-{version}(-{build})?-{python}-{abi}-{platform}.whl
```

דוגמה לשם קובץ WHL היא כדלקמן.

```
cryptography-2.9.2-cp35-abi3-macosx_10_9_x86_64.whl
```

* `קריפטוגרפיה` הוא שם החבילה.
* `2.9.2` היא גרסת החבילה של קריפטוגרפיה. גרסה היא מחרוזת תואמת PEP 440 כגון 2.9.2, 3.4 או 3.9.0.a3.
* `cp35` הוא תג Python ומציין את היישום והגרסה של Python שהגלגל דורש.
* `abi3` הוא תג ABI. ABI ראשי תיבות של ממשק בינארי יישומים.
* `macosx_10_9_x86_64` הוא תג הפלטפורמה, שבמקרה הוא די מלא פה.

## הפניות

* [מהם גלגלי פייתון ולמה צריך לדאוג לך?](https://realpython.com/python-wheels/)
* [גלגל פיתון](https://pypi.org/project/wheel/)
