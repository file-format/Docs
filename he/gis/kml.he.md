{
  "date" : "2019-10-11",
  "keywords" :[ "קובץ kml", "מהו קובץ kml", "קובץ", "דוגמה ל-kml", "סיומת קובץ kml","הרחבה", "פורמט" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"KML - Keyhole Markup Language",
  "description":"למד על פורמט קובץ KML וממשקי API שיכולים ליצור ולפתוח קובצי KML.",
  "linktitle" : "KML",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## מהו קובץ KML?

KML, Keyhole Markup Language) מכיל מידע גיאו-מרחבי בסימון XML. ניתן לפתוח קבצים שנשמרו כ-KML ביישומי מערכת מידע גיאוגרפית (GIS) בתנאי שהם תומכים בכך. יישומים רבים החלו לספק תמיכה בפורמט קובץ KML לאחר שהוא אומץ כתקן בינלאומי. KML משתמש במבנה מבוסס תג עם אלמנטים ותכונות מקוננות. כל התגים הם תלויי רישיות וחשוב לעקוב אחר הסדר של תגים אלה, לפי [KML](https://developers.google.com/kml/documentation/kmlreference) הפניה.

## היסטוריה קצרה ##

KML פותחה במקור לשימוש עם Google Earth שהיה ידוע במקור בתור Keyhole Earth Viewer. KLM אומצה כתקן בינלאומי בשנת 2008 על ידי Open Geospatial Consortium בשנת 2008. מאז הפורמט פותח לשימוש עם Google Earth, יש לו את ההבחנה להיות הראשון להציג ולערוך קובצי KML. עם חלוף הזמן, יש כיום יותר ויותר פרויקטים המספקים תמיכה בפורמטים של קבצי KML כולל מספר ממשקי API בשפות שונות.

## מפרטי פורמט קובץ KML ##

ה-KML Reference הוא מדריך שלם להפניה כדי לקבל את מפרטי פורמט הקובץ המלאים. קובץ KML סטנדרטי מורכב מ:

* סימני מקום
* HTML תיאורי בסימני מקום
* שכבות קרקע
* שבילים
* מצולעים

בנוסף לאלה, גרסה מתקדמת של קובץ KML יכולה לכלול:

* סגנונות לגיאומטריה
* סגנונות עבור סמלים מודגשים
* שכבות מסך
* קישורי רשת

לכל אחד ממרכיבי ה-KML יש מידע באורך זמן המאתר גיאוגרפי את המידע הקיים בקובץ. עם זאת, יכולים להיות פרמטרים נוספים כמו כיוון, גובה והטיה.

### סימני מקום ###

הוא משמש לייצוג מיקום על פני כדור הארץ ומזוהה על ידי<Point> אֵלֵמֶנט. להלן דוגמה כיצד סמן מיוצג בקובץ KML.

```

<kml xmlns#"http://www.opengis.net/kml/2.2">
  <Placemark>
    <name>Simple placemark</name>
    <description>Attached to the ground. Intelligently places itself
       at the height of the underlying terrain.</description>
    <Point>
      <coordinates>-122.0822035425683,37.42228990140251,0</coordinates>
    </Point>
  </Placemark>
</kml>
```

### HTML תיאורי בסמנים ###

ניתן לשייך מידע נוסף לסמן שמשפר עוד יותר את הייצוג של הסמן. מידע כזה כולל קישורים, גדלי גופנים, סגנונות וצבעים. בנוסף, הוא כולל גם יישור טקסט וטבלאות שיהיו חלק מהסמן.

```

<kml xmlns#"http://www.opengis.net/kml/2.2">
  <Document>
    <Placemark>
      <name>CDATA example</name>
      <description>
        <![CDATA[
          <h1>CDATA Tags are useful!</h1>
          <p><font color#"red">Text is <i>more readable</i> and
          <b>easier to write</b> when you can avoid using entity
          references.</font></p>
        ]]>
      </description>
      <Point>
        <coordinates>102.595626,14.996729</coordinates>
      </Point>
    </Placemark>
  </Document>
</kml>
```

### שכבות קרקע ###

אלה מייצגים את הריבוד של תמונה על פני כדור הארץ. ה<icon> elment מכיל את הקישור לקובץ תמונת העל.

```

<kml xmlns#"http://www.opengis.net/kml/2.2">
  <Folder>
    <name>Ground Overlays</name>
    <description>Examples of ground overlays</description>
    <GroundOverlay>
      <name>Large-scale overlay on terrain</name>
      <description>Overlay shows Mount Etna erupting
          on July 13th, 2001.</description>
      <Icon>
        <href>https://developers.google.com/kml/documentation/images/etna.jpg</href>
      </Icon>
      <LatLonBox>
        <north>37.91904192681665</north>
        <south>37.46543388598137</south>
        <east>15.35832653742206</east>
        <west>14.60128369746704</west>
        <rotation>-0.1556640799496235</rotation>
      </LatLonBox>
    </GroundOverlay>
  </Folder>
</kml>
```

### נתיבים ###

נתיבים מיוצגים על ידי<LineString> אלמנט שהוא אוסף של זוגות באורך רוחב. באמצעות אלה, ניתן ליצור סוגים רבים ושונים של נתיבים ב-Google Earth.

```

<kml xmlns#"http://www.opengis.net/kml/2.2">
  <Document>
    <name>Paths</name>
    <description>Examples of paths. Note that the tessellate tag is by default
      set to 0. If you want to create tessellated lines, they must be authored
      (or edited) directly in KML.</description>
    <Style id#"yellowLineGreenPoly">
      <LineStyle>
        <color>7f00ffff</color>
        <width>4</width>
      </LineStyle>
      <PolyStyle>
        <color>7f00ff00</color>
      </PolyStyle>
    </Style>
    <Placemark>
      <name>Absolute Extruded</name>
      <description>Transparent green wall with yellow outlines</description>
      <styleUrl>#yellowLineGreenPoly</styleUrl>
      <LineString>
        <extrude>1</extrude>
        <tessellate>1</tessellate>
        <altitudeMode>absolute</altitudeMode>
        <coordinates> -112.2550785337791,36.07954952145647,2357
          -112.2549277039738,36.08117083492122,2357
          -112.2552505069063,36.08260761307279,2357
          -112.2564540158376,36.08395660588506,2357
          -112.2580238976449,36.08511401044813,2357
          -112.2595218489022,36.08584355239394,2357
          -112.2608216347552,36.08612634548589,2357
          -112.262073428656,36.08626019085147,2357
          -112.2633204928495,36.08621519860091,2357
          -112.2644963846444,36.08627897945274,2357
          -112.2656969554589,36.08649599090644,2357
        </coordinates>
      </LineString>
    </Placemark>
  </Document>
</kml>
```

## התייחסות מרחבית בקובץ KML ##

למידע הכלול בכל קובץ גיאוגרפי על מיקומים גיאוגרפיים יכולים להיות משמעויות שונות ללא מידע הפניה מרחבי. כברירת מחדל, ההפניה המרחבית של קובץ KML מוגדרת על ידי World Geodetic System של 1984, WGS84.

## הפניות ##

* [Reference KML](https://developers.google.com/kml/documentation/kmlreference)
* [מדריך למפתחים של Google עבור KML](https://developers.google.com/kml/documentation/kml_tut)
* [פורמט קובץ KML](https://en.wikipedia.org/wiki/Keyhole_Markup_Language)

