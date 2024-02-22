{
  "date" : "2023-01-02",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "OSC - OpenStreetMap שנה פורמט קובץ",
  "description":"למד על פורמט קובץ OSC וממשקי API שיכולים ליצור ולפתוח קובצי OSC.",
  "linktitle" : "OSC",
  "menu" : {
    "docs" : {
      "identifier":"gis-osc-he",
      "parent" : "gis"
}
},
  "lastmod" : "2023-01-02"
}

## מהו קובץ OSC?

קובץ OSC הוא תבנית קובץ שינוי המכיל נתוני מפת רחוב שהשתנו עבור מפת רחוב קיימת עם ‎.osm. הוא מכיל מידע על השינויים שייגרמו ל-[OSM file](/gis/osm/). לקובץ OSC יכולים להיות שלושה סוגים אפשריים של פעולות שינוי על נתוני OSM, כלומר 'הכנס', 'שנה' או 'מחק'. קובצי שינוי אלה משמשים בדרך כלל לייצוא נתונים מעורך OSM ויבוא לעורך אחר.

אתה יכול לפתוח קבצי OSC עם תוכנת Merkaartar ו-osmchange.

## פורמט קובץ OSC

קבצי OSC נשמרים בדרך כלל בפורמט קובץ JOSM שבו השינויים מיוצגים על ידי תגים. זה מתחיל בתג 'osmChange' שמציין את תחילת הקובץ. תגי המשנה מציינים אם מדובר בפעולת הוספה, שינוי או מחיקה שיש לבצע בצומת המתאים בקובץ OSM. התוכן של צומת מכיל למעשה את התוכן של תג osm.

### דוגמה לפורמט קובץ OSC

להלן דוגמה לפעולת שינוי בצומת. לכל רכיב חייב להיות מזהה ערכת שינויים ומספר גרסה.

```
<osmChange version="0.6" generator="acme osm editor">
    <modify>
        <node id="1234" changeset="42" version="2" lat="12.1234567" lon="-8.7654321">
            <tag k="amenity" v="school"/>
        </node>
    </modify>
</osmChange>
```

## הפניות

* [פורמט קובץ JOSM](https://wiki.openstreetmap.org/wiki/JOSM_file_format)


