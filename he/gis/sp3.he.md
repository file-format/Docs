{
  "date" : "2021-08-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SP3 - NGS SP3 File",
  "description":"למד על פורמט קובץ SP3 וממשקי API שיכולים ליצור ולפתוח קובצי SP3.",
  "linktitle" : "SP3",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-09-29"
}

## מהו קובץ SP3?

קובץ עם סיומת .sp3 הוא פורמט מסלול של סקר גיאודטי לאומי (NGS) לאחסון מידע מסלול. זוהי הרחבה לפורמטים SP1 ו-SP2 של NGS, וכוללת את מידע תיקון השעון לווייני שמחושב בו-זמנית עם המסלולים. הוא מבוסס בעיקר על מיקום ושעון, ואינו כולל מהירויות. הפורמט הוצע ב-Remondi, 1989 ואומץ ב-1991. בנוסף למידע על תיקון שעון לווייני, הוא כולל מידע כגון מעריכים של דיוק מסלול, קווי הערה, שבוע ה-GPS ושניות השבוע הקשורות לעידן הראשון. ניתן לפתוח קבצי SP3 עם Wolfram Research Mathematica.

## פורמט קובץ SP3 - מידע נוסף

קבצי SP3 נשמרים בדיסק בפורמט קובץ ASCII וניתן לפתוח את תוכנו בכל עורך טקסט לצפייה. ניתן לראות את המבנה של קובץ SP3 מהתמונה הבאה.

{{< figure src="../sp3-file-format.png" title="" >}}

## הפניות

* [The Extended Standard Product 3 Orbit Format (SP3-c)](http://epncb.oma.be/ftp/data/format/sp3c.txt#:~:text=The%20SP3%20format%20is%20similar ,מבנה%20יותר%20גמיש%20header%20)
* [הרחבת פורמטים של מסלולי GPS סטנדרטיים ל-National Geodetic Survey](https://beta.ngs.noaa.gov/PUBS_LIB/Extending_the_NGS_Standard_GPS_Orbit_Formats_TR_NOS133_NGS46.pdf)

