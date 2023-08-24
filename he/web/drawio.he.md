{
  "date" : "2019-10-11",
  "keywords" :[ "drawio","drawio file", "drawio file format", "drawio file type", "file", "type", "what is drawio file" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DRAWIO - פורמט קובץ דיאגרמה Diagram.net",
  "description" :"למד על פורמט קובץ DRAWIO וממשקי API ליצירה ופתיחה של קבצי DRAWIO.",
  "linktitle" : "DRAWIO",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-16"
}

## מהו קובץ DRAWIO?

קובץ עם סיומת .drawio הוא קובץ ציור שנוצר עם draw.io של [diagrams.net](https://www.diagrams.net/) שהוא תוכנת קוד פתוח לעבודה עם דיאגרמות. הוא מכיל מידע כולל על התוכן והעיצוב של רכיבי הדיאגרמה כגון טקסט, תמונות, פריסה, צורות ומיקום. דיאגרמות הנתמכות על ידי DRAWIO כוללות תרשימי זרימה, תרשימי ארגון, מפות, אלמנטים הנדסיים, דיאגרמות תהליכים, תרשימים ועוד. ניתן לייצא קבצי DRAWIO למספר פורמטים שונים כגון [JPG](/he/image/jpeg/), [PNG](/he/image/png/), [BMP](/he/image/bmp/), [XML](/he/web/xml/), PDF, [HTML](/he/web/html/) ו-[VSDX](/he/visio/vsdx/).

## פורמט קובץ DRAWIO

קבצי DRAWIO הם קובצי תמונה וקטוריים, המאוחסנים בפורמט קובץ XML הסטנדרטי. פותח על ידי diagrams.net, הוא מספק את היכולת לאחסן מידע דיאגרמות בדומה ל-Microsoft Visio. DrawIO זמין כ[אפליקציה מקוונת](https://app.diagrams.net/) כדי ליצור, לפתוח ולייצא דיאגרמות לפורמטים שונים. האפליקציה מבוססת על ספריית הדיאגרמות mxGraph המספקת יישומי גרפים ותרשימים אינטראקטיביים הפועלים בכל דפדפן מרכזי כמו Chrome, Firefox, Edge ו-Safari.

### דוגמה של DRAWIO

הדוגמה הבאה היא תרשים זרימה פשוט שנוצר עם אפליקציית DRAWIO.

{{< figure src="../DRAWIO.png" alt="פורמט קובץ DRAWIO" height="421" width="291">}}

פלט XML שנוצר עם הייצוא הוא כפי שמוצג להלן.

```
<?xml version="1.0" encoding="UTF-8"?>
<mxfile host="app.diagrams.net" modified="2021-05-17T17:18:48.774Z" agent="5.0 (Macintosh; Intel Mac OS X 10_14_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/90.0.4430.93 Safari/537.36" etag="jyk4LjRpkp5MiVdB0UgM" version="14.6.13" type="device">
  <diagram name="Page-1" id="74e2e168-ea6b-b213-b513-2b3c1d86103e">
    <mxGraphModel dx="946" dy="469" grid="1" gridSize="10" guides="1" tooltips="1" connect="1" arrows="1" fold="1" page="1" pageScale="1" pageWidth="1100" pageHeight="850" background="#ffffff" math="0" shadow="0">
      <root>
        <mxCell id="0" />
        <mxCell id="1" parent="0" />
        <mxCell id="IQM8xkm7UoOLgGwT3--F-3" value="" style="edgeStyle=orthogonalEdgeStyle;rounded=0;orthogonalLoop=1;jettySize=auto;html=1;" edge="1" parent="1" source="IQM8xkm7UoOLgGwT3--F-1" target="IQM8xkm7UoOLgGwT3--F-2">
          <mxGeometry relative="1" as="geometry" />
        </mxCell>
        <mxCell id="IQM8xkm7UoOLgGwT3--F-1" value="Jogging Start" style="rounded=0;whiteSpace=wrap;html=1;" vertex="1" parent="1">
          <mxGeometry x="440" y="240" width="120" height="60" as="geometry" />
        </mxCell>
        <mxCell id="IQM8xkm7UoOLgGwT3--F-5" value="" style="edgeStyle=orthogonalEdgeStyle;rounded=0;orthogonalLoop=1;jettySize=auto;html=1;" edge="1" parent="1" source="IQM8xkm7UoOLgGwT3--F-2" target="IQM8xkm7UoOLgGwT3--F-4">
          <mxGeometry relative="1" as="geometry" />
        </mxCell>
        <mxCell id="IQM8xkm7UoOLgGwT3--F-7" value="" style="edgeStyle=orthogonalEdgeStyle;rounded=0;orthogonalLoop=1;jettySize=auto;html=1;" edge="1" parent="1" source="IQM8xkm7UoOLgGwT3--F-2" target="IQM8xkm7UoOLgGwT3--F-6">
          <mxGeometry relative="1" as="geometry" />
        </mxCell>
        <mxCell id="IQM8xkm7UoOLgGwT3--F-2" value="Should Run?" style="rhombus;whiteSpace=wrap;html=1;" vertex="1" parent="1">
          <mxGeometry x="460" y="340" width="80" height="80" as="geometry" />
        </mxCell>
        <mxCell id="IQM8xkm7UoOLgGwT3--F-4" value="Process End" style="rounded=0;whiteSpace=wrap;html=1;" vertex="1" parent="1">
          <mxGeometry x="610" y="350" width="120" height="60" as="geometry" />
        </mxCell>
        <mxCell id="IQM8xkm7UoOLgGwT3--F-9" value="" style="edgeStyle=orthogonalEdgeStyle;rounded=0;orthogonalLoop=1;jettySize=auto;html=1;" edge="1" parent="1" source="IQM8xkm7UoOLgGwT3--F-6" target="IQM8xkm7UoOLgGwT3--F-8">
          <mxGeometry relative="1" as="geometry" />
        </mxCell>
        <mxCell id="IQM8xkm7UoOLgGwT3--F-6" value="Run 10 KM" style="rounded=0;whiteSpace=wrap;html=1;" vertex="1" parent="1">
          <mxGeometry x="440" y="460" width="120" height="60" as="geometry" />
        </mxCell>
        <mxCell id="IQM8xkm7UoOLgGwT3--F-8" value="End Run" style="whiteSpace=wrap;html=1;rounded=0;" vertex="1" parent="1">
          <mxGeometry x="440" y="600" width="120" height="60" as="geometry" />
        </mxCell>
      </root>
    </mxGraphModel>
  </diagram>
</mxfile>

```

## הפניות ##

* [DRAWIO - Github](https://github.com/jgraph/drawio)
* [DRAWIO - אפליקציה מקוונת](https://app.diagrams.net/)
* [Diagrams.Net](https://www.diagrams.net/)

