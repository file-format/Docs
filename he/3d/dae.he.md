{
  "date" : "2019-10-11",
  "keywords" :[ "קובץ dae", "פורמט קובץ dae", "מהו קובץ dae", "קובץ", "דוגמה של dae", "סיומת קובץ dae","סיומת", "פורמט" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"למד על פורמט קובץ DAE וממשקי API שיכולים לפתוח וליצור קובצי DAE.",
  "title" :"DAE - Digital Asset Exchange Format File",
  "linktitle" : "DAE",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## מהו קובץ DAE?

קובץ DAE הוא פורמט קובץ Digital Asset Exchange המשמש להחלפת נתונים בין יישומי תלת מימד אינטראקטיביים. פורמט קובץ זה מבוסס על סכימת ה-XML COLLADA (COLLAborative Design Activity) שהיא סכימת XML סטנדרטית פתוחה להחלפת נכסים דיגיטליים בין יישומי תוכנה גרפית. זה אומץ על ידי ISO כמפרט זמין לציבור, ISO/pAS 17506. ניתן לפתוח קבצי DAE ביישומים כגון Adobe Photoshop, AutoDesk Maya, AutoDesk AutoCAD וממשקי API כגון [Aspose.CAD](https://products.aspose.com/cad/).

## פורמט קובץ DAE

פורמט קובץ ה-DAE מבוסס על [סכימת ה-XML של COLLADA](https://www.khronos.org/files/collada_spec_1_5.pdf) שבה כל הרכיבים מוגדרים כתגי XML. היא מאפשרת כריכה של כלי עיבוד DCC ו-3D מגוונים לצינור ייצור עבור נכסי 3D. יש לו קידוד מקיף של סצנות חזותיות כולל גיאומטריה, אנימציה, הצללות ופיזיקה. הפורמט פתוח, בדרגת ארכיון ושומר על מטא מידע.

### תגיות COLLADA

תג הסכימה של COLLADA הוא כפי שמוצג להלן.
```
<?xml version="1.0"?>
<COLLADA
  xmlns="http://www.collada.org/2005/11/COLLADASchema"
  version="1.4.1"
>
...
</COLLADA>
```
### תג נכס

תג הנכס מתאר את המחבר והסביבה של הקובץ

```
<asset>
  <author>alorino</author>
  <up_axis>Y_UP</up_axis>
</asset>
```

### ספריית מצלמה

נכסי COLLADA נמצאים בתוך ספריות. ספריית המצלמות מכילה באופן לא מפתיע, מצלמות. המצלמות הנפוצות הן פרספקטיבה או אורתוגרפית. תג ספריית המצלמה מוגדר כדלקמן.
```
<library_cameras>
    <camera id="PerspCamera" name="PerspCamera">
      <optics>
        <technique_common>
          <perspective>
            <yfov>37.8493</yfov>
            <aspect_ratio>1</aspect_ratio>
            <znear>10</znear>
            <zfar>1000</zfar>
          </perspective>
        </technique_common>
      </optics>
    </camera>
</library_cameras>
```
### אורות

האורות הנפוצים הם נקודה, נקודה או כיוונית
```
<library_lights>
    </light>
    <light id="pointLightShape1-lib" name="pointLightShape1">
      <technique_common>
        <point>
          <color>1 1 1 </color>
          <constant_attenuation>1</constant_attenuation>
          <linear_attenuation>0</linear_attenuation>
          <quadratic_attenuation>0</quadratic_attenuation>
        </point>
      </technique_common>
    </light>
</library_lights>
```

### מופע חומרים

אפקטי מופע החומרים מוגדרים כדלקמן.
```
<library_materials>
    <material id="Blue" name="Blue">
      <instance_effect url="#Blue-fx"/>
    </material>
</library_materials>
```
### אפקטים נפוצים

אפקטים נפוצים פועלים כמו מצב OpenGL 1 וניתן להגדיר אותם כדלקמן.

```
<library_effects>
    <effect id="Blue-fx">
      <profile_COMMON>
        <technique sid="common">
          <phong>
            <emission>
              <color>0 0 0 1 </color>
            </emission>
            ...
            <index_of_refraction>
              <float>0</float>
            </index_of_refraction>
          </phong>
        </technique>
      </profile_COMMON>
    </effect>
</library_effects>
```

### תכונות גיאומטריה

גיאומטריה מתארת את תכונות OpenGL ומוגדרות כדלקמן.
```
<library_geometries>
    <geometry id="box-lib" name="box">
      <mesh>
        <source id="box-lib-positions" name="position">
        </source>
        <source id="box-lib-normals" name="normal">
        </source>
        ...
        <vertices id="box-lib-vertices">
          <input semantic="POSITION" source="#box-lib-positions"/>
        </vertices>
        <polylist count="6" material="BlueSG">
          <input offset="0" semantic="VERTEX" source="#box-lib-vertices"/>
          <input offset="1" semantic="NORMAL" source="#box-lib-normals"/>
          <vcount>4 4 4 4 4 4 </vcount>
          <p>0 0 2 1 3 2 1 3 0 4 1 5 5 6 4 7 ...</p>
        </polylist>
      </mesh>
    </geometry>
</library_geometries>
```

### סצנות חזותיות

סצנות חזותיות הן כמו סצנות אחדות ומכילות היררכיה של צמתים כדלקמן.
```
<library_visual_scenes>
    <visual_scene id="VisualSceneNode" name="untitled">
        <node id="Camera" name="Camera">
        </node>
        ...
    </visual_scene>
</library_visual_scenes>
```

## הפניות
* [מפרט COLLADA 1.5.0](https://www.khronos.org/files/collada_spec_1_5.pdf)

