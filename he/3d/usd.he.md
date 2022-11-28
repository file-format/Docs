{
  "date" : "2021-02-01",
  "keywords" :[ "USD", "USD file", "USd file format", "פורמט קובץ", "קובץ", "סיומת", "3d"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"USD - פורמט תיאור סצנה אוניברסלי",
  "description":"למד על פורמט קובץ USD וממשקי API שיכולים לפתוח וליצור קבצי USD.",
  "linktitle" : "USD",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-02-01"
}

## מהו קובץ USD?

קובץ עם סיומת .usd הוא פורמט קובץ Universal Scene Description המקודד נתונים למטרת החלפת נתונים והגדלה בין יישומי יצירת תוכן דיגיטלי. פותח על ידי Pixar, [USD](https://graphics.pixar.com/usd/docs/Introduction-to-USD.html) מספק את היכולת להחליף נכסים יסודיים (כגון מודלים) או אנימציה.

## פורמט קובץ USD

קבצי USD יכולים להיות בפורמט בינארי (המכונה גם קבצי ארגז) או קבצים מגובי ASCII. שני פורמטי הקבצים הללו ניתנים להחלפה כאשר ההפניות ניתנות לקישור לנכסי ‎.usd מבלי לשנות את המקורות. פורמט קובץ USD מורכב מקבוצה של ספריות C++ עם כריכות Python ל-scripting. זה מאפשר הרכבה וארגון של כל מספר אלמנטים של סצנה תלת מימדית כגון סטים וירטואליים, סצנות וצילומים כדי להעביר אותם מאפליקציה לאפליקציה.

### סוגי נתונים בדולר ארה"ב

סוגי הנתונים הבסיסיים הנתמכים על ידי פורמט הקובץ USD מפורטים בטבלה הבאה.

|אסימון סוג ערך |C++ סוג |תיאור|
---|---|---|
|bool|bool||
|uchar|uint8_t|מספר שלם ללא סימן 8 סיביות|
|int|int32_t|מספר שלם בסימן 32 סיביות|
|uint|uint32_t|מספר שלם ללא סימן 32 סיביות|
|int64|int64_t|מספר שלם בסימן 64 סיביות|
|uint64|uint64_t|מספר שלם ללא סימן 64 סיביות|
|חצי|GfHalf|נקודה צפה 16 סיביות|
|float|float|נקודה צפה 32 סיביות|
|double|double|64 ביט נקודה צפה|
|timecode|SdfTimeCode|כפול המייצג זמן בר פתרון|
|string|std::string|מחרוזת stl|
|token|TfToken|מחרוזת מתמחה עם השוואה מהירה וגיבוב|
|asset|SdfAssetPath|מייצג נתיב בר פתרון לנכס אחר|
|matrix2d|GfMatrix2d|2x2 מטריצה של כפילים|
|matrix3d|GfMatrix3d|3x3 מטריצה של כפילים|
|matrix4d|GfMatrix4d|4x4 מטריצה של כפילים|
|quatd|GfQuatd|קווטרניון עם דיוק כפול|
|quatf|GfQuatf|קווטרניון עם דיוק יחיד|
|quath|GfQuath|קווטרניון בחצי דיוק|
|double2|GfVec2d|וקטור של 2 כפילים|
|float2|GfVec2f|וקטור של 2 מצופים|
|half2|GfVec2h|וקטור של 2 חצאים|
|int2|GfVec2i|וקטור של 2 אינטס|
|double3|GfVec3d|וקטור של 3 כפילים|
|float3|GfVec3f|וקטור של 3 מצופים|
|half3|GfVec3h|וקטור של 3 חצאים|
|int3|GfVec3i|וקטור של 3 אינטס|
|double4|GfVec4d|וקטור של 4 כפילים|
|float4|GfVec4f|וקטור של 4 מצופים|
|half4|GfVec4h|וקטור של 4 חצאים|
|int4|GfVec4i|וקטור של 4 אינטס|

## דוגמה דולר

דוגמה לקובץ USD בפורמט קובץ ASCII רגיל היא כדלקמן.

```
#usda 1.0

class "_class_Planet"
{
    bool has_life = False
}

def Xform "SolarSystem"
{
    def "Earth" (
        references = @./planet.usda@</Planet>
    )
    {
        bool has_life = True
        string color = "blue"
}

    def "Mars" (
        references = @./planet.usda@</Planet>
    )
    {
        string color = "red"
}

    def "Saturn" (
        references = @./planet.usda@</Planet>
        variants = {
            string rings = "with_rings"
    }
    )
    {
        string color = "beige"
}
}
```

```
#usda 1.0

class "_class_Planet"
{
}

def Sphere "Planet" (
    inherits = </_class_Planet>
    kind = "model"
    variantSets = "rings"
    variants = {
        string rings = "none"
}
)
{
    variantSet "rings" = {
        "none" {
            bool has_rings = False
    }
        "with_rings" {
            bool has_rings = True
    }
}

}
```
## הפניות ##

* [מבוא לדולר ארה"ב](https://graphics.pixar.com/usd/docs/Introduction-to-USD.html)
* [USD API Reference](https://graphics.pixar.com/usd/docs/USD-Developer-API-Reference.html)

