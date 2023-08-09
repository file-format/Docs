{
  "date" : "2022-05-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"למד על פורמט קובץ PYC וממשקי API שיכולים ליצור ולפתוח קובצי PYC.",
  "title" :"פורמט קובץ PYC- קובץ הידור של Python",
  "linktitle" : "PYC",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2022-05-09"
}

## מהו קובץ PYC?

קובץ PYC הוא קובץ פלט מהול שנוצר מקוד מקור שנכתב בשפת התכנות Python. כאשר קובץ PY מופעל באמצעות מתורגמן Python, הוא מומר ל-bytecode לביצוע. במקביל, קוד ה-byte-קומפילציה נשמר גם כקובץ .pyc כדי לעשות שימוש חוזר מהמטמון במועד מאוחר יותר, אם ישים.

## מבנה פורמט קובץ PYC

קובצי PYC נמצאים בקוד בתים ומפרטי פורמט הקובץ שלהם אינם זמינים לציבור. עם זאת, חקירה של מקורות מסוימים מראה ש[מבנה של קובץ PYC](https://nedbatchelder.com/blog/200804/the_structure_of_pyc_files.html) מורכב מ:

* `מספר קסם של ארבעה בתים` - פשוט שני בתים המשתנים עם כל שינוי בקוד ה-Marshalling, ולאחר מכן שני בתים של 0d0a.
* `A four-byte modification timestamp` - חותמת זמן שינוי Unix של קובץ המקור שיצר את ה-.pyc, כך שניתן להידור מחדש אם המקור משתנה.
* `A marshalled code object` - הפלט של marshal.dump של אובייקט הקוד שהוא תוצאה של קומפילציה של קובץ המקור.

## הפניות

* [המבנה של קבצי .pyc](https://nedbatchelder.com/blog/200804/the_structure_of_pyc_files.html)

