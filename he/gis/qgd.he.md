{
  "date" : "2021-03-18",
  "author" : {
    "display_name" : "Muhammad Umar",
	"keywords" :[ "QGD", "Sqlite Database של פרויקט QGIS", "הרחבה", "פורמט", "QGIS", "Auxilary Database", "מהו קובץ QGD"]
},
  "draft" : "false",
  "toc" : true,
  "title" :"QGD - Sqlite Database של פרויקט QGIS",
  "description":"למד על QGD שהוא מסד נתונים sqlite של פרויקט QGIS וממשקי API שיכולים ליצור ולפתוח קבצי QGD.",
  "linktitle" : "QGD",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-03-18"
}

## מהו קובץ QGD?

הקובץ עם סיומת קובץ QGD הוא למעשה מסד הנתונים sqlite המשויך לפרויקט **QGIS** שמכיל את נתוני העזר לפרויקט. קובץ QGD יישאר ריק, אם לא יהיו נתוני עזר לפרויקט.

## פרטים על פורמט קובץ QGD

במצב קלאסי, מסד הנתונים העזר נשמר כקובץ עם סיומת qgd לאורך קובץ ה-xml. מערכת **Auxiliary Database** מאפשרת לקרוא ולכתוב נתונים במערכת כדרך חלופית. בעת יצירת ה-QGZ שהוא מיכל מכווץ, קובץ ה-qgd כולל את ה-.qgz.

## מהו מסד נתונים עזר?
מאגר הנתונים העזר הוא למעשה מערכת db המתנה שנוצרת כתגובה לשכפול של מסד הנתונים היעד. מסד הנתונים העזר הוא למעשה מקרה של מסד נתונים משוכפל יהיה מסד הנתונים שאליו אתה משכפל. לדוגמה, אם אתה מגדיר מסד נתונים המתנה באמצעות מסד נתונים כפול, מסד הנתונים של המקור יהיה היעד ומסד הנתונים של ההמתנה ייקרא עזר.


## הפניות

* [QGZ – פורמט חדש של קובץ פרוייקט ברירת מחדל עבור QGIS](https://oslandia.com/en/2018/06/01/qgz-a-new-default-project-file-format-for-qgis/)
* [פורמטי קובץ QGIS](https://docs.qgis.org/3.16/en/docs/user_manual/appendices/qgis_file_formats.html)

