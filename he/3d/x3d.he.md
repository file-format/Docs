{
  "date" : "2019-10-11",
  "keywords" :[ "קובץ x3d", "פורמט קובץ x3d", "מהו קובץ x3d", "קובץ", "דוגמה ל-x3d", "סיומת קובץ x3d", "הרחבה", "פורמט" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"X3D - קובץ תמונה בתלת מימד",
  "description":"למד על פורמט קובץ X3D וממשקי API שיכולים לפתוח וליצור קובצי X3D.",
  "linktitle" : "X3D",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## מהו קובץ X3D?
X3D הוא פורמט קובץ גרפי תלת-ממדי מבוסס [XML](/he/web/xml/) להצגת מידע תלת-ממדי. זהו תקן מודולרי ומוגדר באמצעות מספר מפרטי ISO. הפורמט תומך בגרפיקה וקטורית ורסטר, שקיפות, אפקטים של תאורה והגדרות אנימציה כולל סיבובים, דהויות ותנודות. הוא הפך ליורש של פורמט הקובץ [VRML](/he/3d/vrml/) בשנת 2001. ל-X3D יש את היתרון של קידוד מידע צבע (בניגוד ל-[STL](/he/cad/stl/)) המשמש במהלך הדפסת הדגם על צבע מדפסת תלת מימד. הפורמט כולל הרחבות ל-VRML, המספקות את היכולת לקודד את הסצנה באמצעות תחביר XML, כמו גם תחביר דמוי ממציא פתוח של VRML97 או עיצוב בינארי.

המפרט המופשט עבור X3D (ISO/IEC 19775) אושר לראשונה על ידי ה-ISO בשנת 2004. קידודי ה-XML וה-ClassicVRML עבור X3D (ISO/IEC 19776) אושרו לראשונה בשנת 2005.

## פורמט קובץ X3D

לקבצי סצנה X3D יש מבנה קבצים משותף:

* כותרת קובץ (או XML, ClassicVRML או דחוס בינארי)
* התחלת צומת השורש X3D כולל תכונות גרסה ופרופיל
* קטע ראש עם הצהרות רכיבים ומטא (שניהם אופציונליים)
* גרף X3D Scene וצמתי הצאצא שלו
* סוף צומת השורש X3D

## דוגמה לפורמט קובץ X3D

```
<!-- -------------------- X3D header and X3D root node with profile declaration -->
<!DOCTYPE X3D PUBLIC "ISO//Web3D//DTD X3D 3.2//EN"
                     "http://www.web3d.org/specifications/x3d-3.2.dtd">
<X3D profile#'Immersive' version#'3.2'
     xmlns:xsd#'http://www.w3.org/2001/XMLSchema-instance'
     xsd:noNamespaceSchemaLocation#'http://www.web3d.org/specifications/x3d-3.2.xsd'>

<!-- -------------------- head section with included meta data -->
  <head>
    <meta content#'HelloWorld.x3d' name#'title'/>
    <meta content#'Simple X3D example' name#'description'/>
    <meta content#'30 October 2000' name#'created'/>
    <meta content#'7 August 2010' name#'modified'/>
    <meta content#'Don Brutzman' name#'creator'/>
    <meta content#'http://www.web3D.org' name#'reference'/>
    <meta content#'http://x3dGraphics.com' name#'reference'/>
    <meta content#'http://www.web3d.org/x3d/content/examples/HelloWorld.x3d' name#'identifier'/>
    <meta content#'http://www.web3d.org/x3d/content/examples/HelloWorldTall.png' name#'image'/>
    <meta content#'http://www.web3d.org/x3d/content/examples/license.html' name#'license'/>
    <meta content#'X3D-Edit 3.2, https://savage.nps.edu/X3D-Edit' name#'generator'/>
  </head>

<!-- -------------------- the X3D scene node with X3D nodes -->
  <Scene>
    <!-- Example scene to illustrate X3D nodes and fields (XML elements and attributes) -->
    <Group>
      <Viewpoint centerOfRotation#'0 -1 0' description#'Hello world!' position#'0 -1 7'/>
      <Transform rotation#'0 1 0 3'>
        <Shape>
          <Sphere/>
          <Appearance>
            <Material diffuseColor#'0 0.5 1'/>
            <ImageTexture url#'"earth-topo.png" "earth-topo.jpg" "earth-topo-small.gif"
     "http://www.web3d.org/x3d/content/examples/Basic/earth-topo.png"
     "http://www.web3d.org/x3d/content/examples/Basic/earth-topo.jpg"
     "http://www.web3d.org/x3d/content/examples/Basic/earth-topo-small.gif"'/>
          </Appearance>
        </Shape>
      </Transform>
      <Transform translation#'0 -2 0'>
        <Shape>
          <Text string#'"Hello" "world!"'>
            <FontStyle justify#'"MIDDLE" "MIDDLE"'/>
          </Text>
          <Appearance>
            <Material diffuseColor#'0.1 0.5 1'/>
          </Appearance>
        </Shape>
      </Transform>
    </Group>
  </Scene>

<!-- -------------------- footer, closing X3D toot element -->
</X3D>
```

## הפניות ##

* [X3D - מאת ויקיפדיה](https://en.wikipedia.org/wiki/X3D)
* [אתר האינטרנט הרשמי של קונסורציום Web3D](https://www.web3d.org/)
* [אתר רשמי של X3D](https://www.web3d.org/x3d/what-x3d)

