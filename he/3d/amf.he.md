{
  "date" : "2019-10-11",
  "keywords" :[ "amf", "קובץ amf", "פורמט קובץ amf", "פורמט קובץ", "3d"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"למד על פורמט קובץ AMF וממשקי API שיכולים לפתוח וליצור קובצי AMF.",
  "title" :"AMF - Additive Manufacturing File",
  "linktitle" : "AMF",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## מהו קובץ AMF?
קובץ AMF מורכב מהנחיות לתיאור אובייקטים על מנת שישמשו בתהליכי ייצור תוסף. הוא מכיל פתח<amf> תג XML ומסתיים בא</amf> אֵלֵמֶנט. קודמת לכך שורת הצהרת XML המציינת את גרסת ה-XML והקידוד של הקובץ. ההצהרות יכולות לכלול מידע על יחידות מדידה, ובהיעדר מידע כזה, מילימטרים משמשים כיחידת ברירת מחדל.


## פורמט קובץ AMF

פורמט קובץ ייצור תוסף (**AMF**) מגדיר סטנדרטים פתוחים לתיאור אובייקטים על מנת לנצל אותם על ידי תהליכי ייצור תוספים כגון הדפסת תלת מימד. תוכניות CAD משתמשות בפורמט הקובץ AMF על ידי שימוש במידע כגון גיאומטריה, צבע וחומר של האובייקטים. AMF שונה מפורמט STL מכיוון שהצדדי אינו תומך בצבע, חומרים, סריג וקבוצות כוכבים.

### אלמנטים של קובץ AMF

חמשת האלמנטים ברמה העליונה המוגדרים עם ה-<AMF> התגים הם כמפורט להלן. נוכחות של רכיב אובייקט בודד היא חובה עבור קובץ AMF מתפקד במלואו.

`<object> ` - רכיב האובייקט מגדיר נפח או נפחים של חומר, שכל אחד מהם משויך למזהה חומר להדפסה. לפחות רכיב אובייקט אחד חייב להיות קיים בקובץ. אובייקטים נוספים הם אופציונליים.

`<material> ` - רכיב החומר האופציונלי מגדיר חומר אחד או יותר להדפסה עם מזהה חומר משויך. אם לא נכלל רכיב מהותי, ההנחה היא חומר ברירת מחדל יחיד.

`<texture> ` - אלמנט הטקסטורה האופציונלי מגדיר תמונה או טקסטורה אחת או יותר למיפוי צבע או טקסטורה, לכל אחד מהם מזהה מרקם משויך.

`<constellation> ` - אלמנט קונסטלציה האופציונלי משלב באופן היררכי אובייקטים וקבוצות כוכבים אחרות לתבנית יחסית להדפסה.

`<metadata> ` - רכיב המטא נתונים האופציונלי מציין מידע נוסף על האובייקט/ים והאלמנטים הכלולים בקובץ.

## דוגמה ל-AMF

להלן דוגמה לקובץ AMF שניתן להעתיק לקובץ [טקסט](/he/עיבוד תמלילים/txt/) ולשמור כקובץ [zip](/he/compression/zip/) דחוס לפתיחה.
```
<?xml version="1.0" encoding="utf-8"?>
<amf unit="inch" version="1.1">
  <metadata type="name">Split Pyramid</metadata>
  <metadata type="author">John Smith</metadata>
  <object id="1">
    <mesh>
      <vertices>
        <vertex><coordinates><x>0</x><y>0</y><z>0</z></coordinates></vertex>
        <vertex><coordinates><x>1</x><y>0</y><z>0</z></coordinates></vertex>
        <vertex><coordinates><x>0</x><y>1</y><z>0</z></coordinates></vertex>
        <vertex><coordinates><x>1</x><y>1</y><z>0</z></coordinates></vertex>
        <vertex><coordinates><x>0.5</x><y>0.5</y><z>1</z></coordinates></vertex>
      </vertices>
      <volume materialid="2">
        <metadata type="name">Hard side</metadata>
        <triangle><v1>2</v1><v2>1</v2><v3>0</v3></triangle>
        <triangle><v1>0</v1><v2>1</v2><v3>4</v3></triangle>
        <triangle><v1>4</v1><v2>1</v2><v3>2</v3></triangle>
        <triangle><v1>0</v1><v2>4</v2><v3>2</v3></triangle>
      </volume>
      <volume materialid="3">
        <metadata type="name">Soft side</metadata>
        <triangle><v1>2</v1><v2>3</v2><v3>1</v3></triangle>
        <triangle><v1>1</v1><v2>3</v2><v3>4</v3></triangle>
        <triangle><v1>4</v1><v2>3</v2><v3>2</v3></triangle>
        <triangle><v1>4</v1><v2>2</v2><v3>1</v3></triangle>
      </volume>
    </mesh>
  </object>
  <material id="2">
    <metadata type="name">Hard material</metadata>
    <color><r>0.1</r><g>0.1</g><b>0.1</b></color>
  </material>
  <material id="3">
    <metadata type="name">Soft material</metadata>
    <color><r>0</r><g>0.9</g><b>0.9</b><a>0.5</a></color>
  </material>
</amf>
```
## הפניות

* [AMF - ויקיפדיה](https://en.wikipedia.org/wiki/Additive_manufacturing_file_format)
* [מפרטי AMF על ISO](https://www.iso.org/standard/67472.html)

