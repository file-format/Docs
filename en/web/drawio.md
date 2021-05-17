{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "DRAWIO - Diagram.net Diagram File Format",
  "description" : "Learn about DRAWIO File Format and APIs to create and open DRAWIO files.",
  "linktitle" : "DRAWIO",
  "menu" : {
    "docs" : {
      "parent" : "web"
    }
  },
  "lastmod" : "2021-05-16"
}

## What is a DRAWIO file?

A file with a .drawio extension is a drawing file created with [diagrams.net](https://www.diagrams.net/)'s draw.io that is an open-source program for working with diagrams. It contains overall information for the content and formatting of the diagram elements such as text, images, layout, shapes and positioning. Diagrams supported by DRAWIO include flowcharts, organization charts, maps, engineering elements, process diagrams, charts and more. DRAWIO files can be exported to several different formats such as [JPG](/image/jpeg/), [PNG](/image/png/), [BMP](/image/bmp/), [XML](/web/xml/), PDF, [HTML](/web/html/) and [VSDX](/image/vsdx/).

## DRAWIO File Format

DRAWIO files are vector image files, stored in the standard XML file format. Developed by diagrams.net, it provides the capability to store diagrams information similar to Microsoft Visio. DrawIO is available as [online app](https://app.diagrams.net/) to create, open and export diagrams to various formats. The app is based on the mxGraph diagramming library that provides interactive graph and charting applications that run in any major browser such as Chrome, Firefox, Edge and Safari.

### DRAWIO Example

The following example is a simple flowchart created with the DRAWIO app.

{{< figure src="../DRAWIO.png" alt="DRAWIO File Format" height="421" width="291">}}

The output XML generated with the export is as shown below.

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

## References ##

* [DRAWIO - Github](https://github.com/jgraph/drawio)
* [DRAWIO - Online App](https://app.diagrams.net/)
* [Diagrams.Net](https://www.diagrams.net/)
