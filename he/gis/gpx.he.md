{
  "date" : "2019-10-11",
  "keywords" :[ "קובץ gpx", "מהו קובץ gpx", "קובץ", "דוגמה ל-gpx", "סיומת קובץ gpx","הרחבה", "פורמט" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GPX - GPX Exchange Format File",
  "description":"למד על פורמט קבצי GPX וממשקי API שיכולים ליצור ולפתוח קובצי GPX.",
  "linktitle" : "GPX",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## מהו קובץ GPX?

קבצים עם סיומת GPX מייצגים פורמט GPS Exchange להחלפה של נתוני GPS בין יישומים ושירותי אינטרנט באינטרנט. זהו פורמט קובץ XML קל משקל המכיל נתוני GPS, כלומר נקודות ציון, מסלולים ומסלולים לייבוא ואדום על ידי תוכניות מרובות. פורמט קובץ GPX פתוח ונתמך על ידי מגוון יישומים ומכשירי GPS. ניתן לטעון נתוני GPS מקבצים כאלה להצגה ביישומי מיפוי למטרות גיאו-מרחביות.

## פורמט קובץ GPX ##

קובץ GPX מורכב מנתוני מיקום של קווי רוחב וקו אורך, ערכי גובה ומידע תיאורי אחר. נתוני המיקום מבוטאים במעלות עשרוניות והגובה מתבטא במטרים. הזמן בקובץ GPX הוא בזמן אוניברסלי מתואם (UTC) בפורמט ISO 8601. היתרונות של שימוש בקובץ GPX הם כדלקמן:

* GPX מאפשר לך להחליף נתונים עם רשימה הולכת וגדלה של תוכניות עבור Windows, MacOS, Linux, Palm ו-PocketPC.
* ניתן להפוך את GPX לפורמטים אחרים של קבצים באמצעות דף אינטרנט פשוט או תוכנית ממיר.
* GPX מבוסס על תקן XML, כך שרבות מהתוכנות החדשות שבהן אתה משתמש (Microsoft Excel, למשל) יכולות לקרוא קבצי GPX.
* GPX מקל על כל אחד באינטרנט לפתח תכונות חדשות שיעבדו באופן מיידי עם התוכניות המועדפות עליך.

[GPX Schema](https://www.topografix.com/GPX/1/1/gpx.xsd) מציגה את הייצוג של פורמט קובץ GPX לעיון.

### נתונים חיוניים ###

להלן נתונים חיוניים המהווים חלק מקובץ GPX לייצוג נתוני GPS.

* **נקודות ציון**: נקודת ציון היא קואורדינטות WGS84 (GPS) של נקודה ומייצגות שכבת תכונות מסוג OGR wkbPoint
* **מסלולים**: מייצגים שכבה של תכונות של wkbLineString מסוג OGR. הוא כולל רשימה של נקודות מסלול, שהן נקודות ציון המציגות פנייה או נקודות במה המובילות ליעד
* **מסלולים**: רצועות מייצגות שכבת תכונות של wkbMultiLineString מסוג OGR. הוא מורכב מקטע אחד לפחות המכיל נקודות ציון ברשימה מסודרת של נקודות המתארות נתיב. הוא מורכב מרשימה של נקודות מסלול המייצגות מסלול GPS רציף.

### קובץ GPX לדוגמה ###

קובץ ה-GPX הבא מציג את הארגון של נתוני GPS בקובץ GPX ויכול לתת מושג טוב לגבי התוכן של קובץ GPX.

```
<gpx xmlns#"http://www.topografix.com/GPX/1/1" xmlns:gpxx#"http://www.garmin.com/xmlschemas/GpxExtensions/v3" xmlns:gpxtpx#"http://www.garmin.com/xmlschemas/TrackPointExtension/v1" creator#"Oregon 400t" version#"1.1" xmlns:xsi#"http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation#"http://www.topografix.com/GPX/1/1 http://www.topografix.com/GPX/1/1/gpx.xsd http://www.garmin.com/xmlschemas/GpxExtensions/v3 http://www.garmin.com/xmlschemas/GpxExtensionsv3.xsd http://www.garmin.com/xmlschemas/TrackPointExtension/v1 http://www.garmin.com/xmlschemas/TrackPointExtensionv1.xsd">
  <metadata>
    <link href#"http://www.garmin.com">
      <text>Garmin International</text>
    </link>
    <time>2009-10-17T22:58:43Z</time>
  </metadata>
  <trk>
    <name>Example GPX Document</name>
    <trkseg>
      <trkpt lat#"47.644548" lon#"-122.326897">
        <ele>4.46</ele>
        <time>2009-10-17T18:37:26Z</time>
      </trkpt>
      <trkpt lat#"47.644548" lon#"-122.326897">
        <ele>4.94</ele>
        <time>2009-10-17T18:37:31Z</time>
      </trkpt>
      <trkpt lat#"47.644548" lon#"-122.326897">
        <ele>6.87</ele>
        <time>2009-10-17T18:37:34Z</time>
      </trkpt>
    </trkseg>
  </trk>
</gpx>
```

## הפניות ##

* [פורמט קובץ GPX](http://www.topografix.com/gpx.asp)
* [GPX - מאת ויקיפדיה](https://en.wikipedia.org/wiki/GPS_Exchange_Format)

