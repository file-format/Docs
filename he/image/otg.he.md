{
  "date" : "2020-01-10",
  "keywords" :[ "קובץ otg", "פורמט קובץ otg", "מהו קובץ otg", "קובץ", "דוגמה ל-otg", "סיומת קובץ otg","הרחבה", "פורמט" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OTG - OpenDocument Drawing Template File Format",
  "description":"למד על פורמט קובץ OTG וממשקי API שיכולים ליצור ולפתוח קובצי OTG.",
  "linktitle" : "OTG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-01-10"
}

## מהו קובץ OTG?

קובץ OTG הוא תבנית ציור שנוצרת באמצעות תקן OpenDocument העוקב אחר מפרט OASIS Office Applications [1.0 מפרט](https://www.oasis-open.org/committees/download.php/12572/OpenDocument-v1.0-os.pdf). הוא מייצג את ארגון ברירת המחדל של רכיבי ציור עבור תמונה וקטורית שניתן להשתמש בהם כדי לשפר עוד יותר את תוכן הקובץ. קבצי OTF הם כמו כל קבצים אחרים המבוססים על פורמט OpenDocument המבוססים על פורמט XML כדי לייצג את תוכן המסמך. ניתן לצפות בקבצי OTF על ידי פתיחתם בכל עורך טקסט או XML רגיל.

## מפרטי פורמט קובץ OTG ##

פורמט קובץ OTG מבוסס על פורמט OpenDocument XML שיש לו סכימה מבוססת היטב. המבנה של כל רכיב של פורמט OpenDocument מיוצג על ידי אלמנט שיש לו תכונות משויכות ומשותף לכל סוגי המסמכים כגון מסמך טקסט, גיליון אלקטרוני או קובץ ציור. OTG, בהיותה תבנית ציור, עושה שימוש נרחב במפרטי התוכן הגרפי הכוללים:

* תכונות עמוד משופרות עבור יישומים גרפיים
* ציור צורות
* מסגרות
* צורות תלת מימד
* צורה מותאמת אישית
* צורות מצגת
* אנימציות מצגות
* אנימציות מצגות SMIL
* אירועי מצגת
* הצג שדות טקסט
* תוכן מסמך מצגת

### תכונות דף משופרות עבור יישומים גרפיים ###
#### מדריך נדבות ####

רכיב Handout Master הוא תבנית להפקה אוטומטית של דפי המידע עבור יישומים התומכים בהדפסת דפים כאלה.
התכונות שעשויות להיות משויכות ל-`<style:handout-master>` אלמנט הם:

|פריסה|תכונה|תיאור
---|---|---|
|פריסת עמוד מצגת|מצגת:presentation-page-layout-name|קישורים אל `<style:presentation-page-layout>`  תכונה
|פריסת עמוד|`style:page-layout-name` | מציין פריסת עמוד שמכילה את הגדלים, הגבול והכיוון של דף האב של דף המידע.
|סגנון עמוד|`draw:style-name`|מקצה תכונות עיצוב נוספות לדף מאסטר של דף מידע על ידי הקצאת סגנון דף ציור.|
|הצהרת כותרת| `presentation:use-header-name`| מציין את השם של הצהרת שדה הכותרת המשמשת עבור כל שדות הכותרות המוצגים בדף המאסטר של דפי המידע.
|הצהרת כותרת תחתונה| presentation:use-footer-name|מציין את השם של הצהרת שדה הכותרת התחתונה המשמשת עבור כל שדות הכותרת התחתונה המוצגים בדף המאסטר של דפי המידע.
|הצהרת תאריך ושעה|use-date-time-name|מציין את השם של הצהרת שדה התאריך-שעה המשמשת עבור כל שדות התאריך-שעה המוצגים בדף המאסטר של ה-dock.

### ציור צורות ###
פורמט OpenDocument תומך במספר צורות ציור שניתן להשתמש בהן בכל סוג של מסמך.

|צורה|תכונות משויכות| אלמנטים
---|---|---|
מלבן - `<draw:rect> `|מיקום, גודל, סגנון, שכבה, Z-Index, מזהה, כיתוב מזהה, עוגן טקסט, רקע שולחן, מיקום סיום ציור, פינות עגולות|כותרת, תיאור ארוך, מאזיני אירועים, נקודות דבק, טקסט
שורה `<draw:line> `|סגנון, שכבה, Z-Index, ID, כיתוב מזהה ושינוי, עוגן טקסט, רקע טבלה, מיקום סיום ציור, נקודת התחלה, נקודת סיום|כותרת, תיאור ארוך, מאזיני אירועים, נקודות דבק, טקסט
פוליליין `<draw:polyline> `| מיקום, גודל, תיבת תצוגה, סגנון, שכבה, Z-Index, מזהה, מזהה כיתוב ושינוי, עוגן טקסט, רקע טבלה, מיקום סיום ציור, נקודות| כותרת, תיאור ארוך, מאזיני אירועים, נקודות דבק, טקסט
מצולע `<draw:polygon> `|מיקום, גודל, תיבת תצוגה, סגנון, שכבה, Z-Index, מזהה, מזהה כיתוב ושינוי, עוגן טקסט, רקע טבלה, מיקום סיום ציור, נקודות|כותרת, תיאור ארוך, מאזיני אירועים, נקודות דבק, טקסט
|מצולע רגיל `<draw:regular-polygon> `|מיקום, גודל, סגנון, שכבה, Z-Index, מזהה, כיתוב מזהה וטרנספורמציה, עוגן טקסט, רקע טבלה, מיקום סיום ציור, קעור, פינות, חדות|כותרת, תיאור ארוך, מאזיני אירועים, נקודות דבק, טקסט
|פאט `<draw:path> `|מיקום, גודל, תיבת תצוגה, סגנון, שכבה, Z-Index, מזהה, כיתוב מזהה ושינוי, עוגן טקסט, רקע טבלה, מיקום סיום שרטוט, נתוני נתיב| כותרת, תיאור ארוך, מאזיני אירועים, נקודות דבק, טקסט

### מסגרות ###
מסגרת, במסמך ציור היא מיכל מלבני המכיל תיבות טקסט, תמונות או אובייקטים. מסגרות תומכות בתכונות נוספות כגון קווי מתאר, מפות תמונה והיפר-קישורים. מסגרת עשויה להכיל אובייקט וגם תמונה, ובכך לאפשר ביצועים מרובים של אובייקט. היישומים מציגים את הרכיב המתאים על בסיס התמיכה הטובה ביותר.

מסגרות יכולות להכיל:
* תיבות טקסט
* אובייקטים המיוצגים בפורמט OpenDocument או בפורמט בינארי ספציפי לאובייקט
* תמונות
* יישומונים
* פלאגינים
* מסגרות צפות

מסגרת כלולה במסמך כפי שמוצג להלן.

```
<define name="draw-frame">
<element name="draw:frame">
<ref name="common-draw-shape-with-text-and-styles-attlist"/>
<ref name="common-draw-position-attlist"/>
<ref name="common-draw-rel-size-attlist"/>
<ref name="common-draw-caption-id-attlist"/>
<ref name="presentation-shape-attlist"/>
<ref name="draw-frame-attlist"/>
<zeroOrMore>
<choice>
<ref name="draw-text-box"/>
<ref name="draw-image"/>
<ref name="draw-object"/>
<ref name="draw-object-ole"/>
<ref name="draw-applet"/>
<ref name="draw-floating-frame"/><ref name="draw-plugin"/>
</choice>
</zeroOrMore>
<optional>
<ref name="office-event-listeners"/>
</optional>
<zeroOrMore>
<ref name="draw-glue-point"/>
</zeroOrMore>
<optional>
<ref name="draw-image-map"/>
</optional>
<optional>
<ref name="svg-title"/>
</optional>
<optional>
<ref name="svg-desc"/>
</optional>
<optional>
<choice>
<ref name="draw-contour-polygon"/><ref name="draw-contour-path"/>
</choice>
</optional>
</element>
</define>
```

## הפניות ##
* [OASIS Open Document Format עבור יישומי Office](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=office)
* [OpenDocument Format - ויקיפדיה](https://en.wikipedia.org/wiki/OpenDocument)

