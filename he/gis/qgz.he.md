{
  "date" : "2021-03-18",
  "keywords" :[ "קובץ qgz", "פורמט קובץ qgz", "מהו קובץ qgz", "קובץ", "דוגמה לqgz", "סיומת קובץ qgz","הרחבה", "פורמט" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"QGZ - Quantum GIS Compressed Project",
  "description":"למד על פורמט קובץ QGZ שהוא רק QGS דחוס וממשקי API שיכולים ליצור ולפתוח קבצי QGZ.",
  "linktitle" : "QGZ",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-03-18"
}

## מהו קובץ QGZ?

פורמט הקובץ **QGZ** הוא ארכיון דחוס המכיל קובץ [QGS](https://docs.fileformat.com/gis/qgs/) וקובץ QGD. ואילו קובץ QGD הוא מסד הנתונים sqlite של פרויקט qgis המורכב מנתוני עזר עבור הפרויקט. אם אין נתוני עזר, קובץ QGD יישאר ריק.

## פרטים על פורמט קובץ QGZ

ה-QGZ הוצג כגרסה חדשה של **פורמט קובץ הפרויקט QGIS 3**. פורמט זה הוא מיכל מכווץ עבור קובץ ה-XML של QGS. אם משתמשים בוחרים ב-QGD שהוא פורמט אופציונלי, במקרה זה המכולה מועיל לאחסון מסד הנתונים של האחסון העזר.

במצב קלאסי, מסד הנתונים העזר נשמר כקובץ עם סיומת qgd לאורך קובץ ה-xml. בעת בחירת הקונטיינר הדחוס, קובץ ה-qgd כולל לתוך ה-.qgz, זה פשוט מקל על המשתמשים ללא כל בעיה, המשתמשים לא יכולים למחוק אותו או לשכוח להעתיק אותו בעת שיתוף קבצי פרויקט!


## הפניות

* [QGZ – פורמט חדש של קובץ פרוייקט ברירת מחדל עבור QGIS](https://oslandia.com/en/2018/06/01/qgz-a-new-default-project-file-format-for-qgis/)
* [פורמטי קובץ QGIS](https://docs.qgis.org/3.16/en/docs/user_manual/appendices/qgis_file_formats.html)

