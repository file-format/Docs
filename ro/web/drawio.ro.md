{
  "date" : "2019-10-11",
  "keywords" :[ "drawio","fișier drawio", "format fișier drawio", "tip fișier drawio", "fișier", "tip", "ce este un fișier drawio" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DRAWIO - Diagram.net Diagram File Format",
  "description" :"Aflați despre formatul fișierului DRAWIO și API-urile pentru a crea și deschide fișiere DRAWIO.",
  "linktitle" : "DRAWIO",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-16"
}

## Ce este un fișier DRAWIO?

Un fișier cu extensia .drawio este un fișier de desen creat cu [diagrams.net](https://www.diagrams.net/) draw.io, care este un program open-source pentru lucrul cu diagrame. Conține informații generale pentru conținutul și formatarea elementelor diagramei, cum ar fi text, imagini, aspect, forme și poziționare. Diagramele acceptate de DRAWIO includ diagrame de flux, organigrame, hărți, elemente de inginerie, diagrame de proces, diagrame și multe altele. Fișierele DRAWIO pot fi exportate în mai multe formate diferite, cum ar fi [JPG](/ro/image/jpeg/), [PNG](/ro/image/png/), [BMP](/ro/image/bmp/), [XML](/ro/web /xml/), PDF, [HTML](/ro/web/html/) și [VSDX](/ro/visio/vsdx/).

## Format de fișier DRAWIO

Fișierele DRAWIO sunt fișiere de imagine vectorială, stocate în formatul standard de fișier XML. Dezvoltat de diagrams.net, oferă capacitatea de a stoca informații despre diagrame similare cu Microsoft Visio. DrawIO este disponibil ca [aplicație online](https://app.diagrams.net/) pentru a crea, deschide și exporta diagrame în diferite formate. Aplicația se bazează pe biblioteca de diagrame mxGraph care oferă aplicații interactive de grafice și diagrame care rulează în orice browser major, cum ar fi Chrome, Firefox, Edge și Safari.

### DRAWIO Exemplu

Următorul exemplu este o diagramă simplă creată cu aplicația DRAWIO.

{{< figure src="../DRAWIO.png" alt="Format de fișier DRAWIO" height="421" width="291">}}

Ieșirea XML generată cu exportul este așa cum se arată mai jos.

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

## Referințe ##

* [DRAWIO - Github](https://github.com/jgraph/drawio)
* [DRAWIO - Aplicație online](https://app.diagrams.net/)
* [Diagrams.Net](https://www.diagrams.net/)

