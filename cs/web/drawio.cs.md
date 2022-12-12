{
  "date" : "2019-10-11",
  "keywords" :[ "drawio","soubor drawio", "formát souboru drawio", "typ souboru drawio", "soubor", "typ", "co je soubor drawio" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DRAWIO - Formát souboru diagramu Diagram.net",
  "description" :"Další informace o formátu souborů DRAWIO a rozhraních API pro vytváření a otevírání souborů DRAWIO.",
  "linktitle" : "DRAWIO",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-16"
}

## Co je soubor DRAWIO?

Soubor s příponou .drawio je soubor výkresu vytvořený pomocí draw.io [diagrams.net](https://www.diagrams.net/), což je open-source program pro práci s diagramy. Obsahuje celkové informace o obsahu a formátování prvků diagramu, jako je text, obrázky, rozvržení, tvary a umístění. Diagramy podporované aplikací DRAWIO zahrnují vývojové diagramy, organizační diagramy, mapy, technické prvky, procesní diagramy, diagramy a další. Soubory DRAWIO lze exportovat do několika různých formátů, například [JPG](/cs/image/jpeg/), [PNG](/cs/image/png/), [BMP](/cs/image/bmp/), [XML](/cs/web /xml/), PDF, [HTML](/cs/web/html/) a [VSDX](/cs/image/vsdx/).

## Formát souboru DRAWIO

Soubory DRAWIO jsou soubory vektorových obrázků uložené ve standardním formátu souboru XML. Vyvinul jej diagrams.net a poskytuje možnost ukládat informace o diagramech podobně jako Microsoft Visio. DrawIO je k dispozici jako [online aplikace](https://app.diagrams.net/) pro vytváření, otevírání a export diagramů do různých formátů. Aplikace je založena na knihovně diagramů mxGraph, která poskytuje interaktivní grafy a aplikace pro vytváření grafů, které běží v jakémkoli hlavním prohlížeči, jako je Chrome, Firefox, Edge a Safari.

### Příklad DRAWIO

Následující příklad je jednoduchý vývojový diagram vytvořený pomocí aplikace DRAWIO.

{{< figure src="../DRAWIO.png" alt="Formát souboru DRAWIO" height="421" width="291">}}

Výstupní XML generované exportem je znázorněno níže.

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

## Reference ##

* [DRAWIO – Github](https://github.com/jgraph/drawio)
* [DRAWIO – online aplikace](https://app.diagrams.net/)
* [Diagrams.Net](https://www.diagrams.net/)

