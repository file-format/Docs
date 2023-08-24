{
  "date" : "2019-10-11",
  "keywords" :[ "drawio", "drawio file", "drawio file format", "drawio file type", "file", "type", "cos'è un drawio file" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DRAWIO - Formato file diagramma Diagram.net",
  "description" :"Ulteriori informazioni sul formato file DRAWIO e sulle API per creare e aprire file DRAWIO.",
  "linktitle" : "DRAWIO",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-16"
}

## Che cos'è un file DRAWIO?

Un file con estensione .drawio è un file di disegno creato con draw.io di [diagrams.net](https://www.diagrams.net/) che è un programma open source per lavorare con i diagrammi. Contiene informazioni generali per il contenuto e la formattazione degli elementi del diagramma come testo, immagini, layout, forme e posizionamento. I diagrammi supportati da DRAWIO includono diagrammi di flusso, organigrammi, mappe, elementi ingegneristici, diagrammi di processo, grafici e altro ancora. I file DRAWIO possono essere esportati in diversi formati come [JPG](/it/image/jpeg/), [PNG](/it/image/png/), [BMP](/it/image/bmp/), [XML](/it/web/xml/), PDF, [HTML](/it/web/html/) e [VSDX](/it/visio/vsdx/).

## Formato file DRAWIO

I file DRAWIO sono file di immagini vettoriali, archiviati nel formato di file XML standard. Sviluppato da diagrams.net, offre la possibilità di archiviare informazioni sui diagrammi simili a Microsoft Visio. DrawIO è disponibile come [app online](https://app.diagrams.net/) per creare, aprire ed esportare diagrammi in vari formati. L'app si basa sulla libreria di diagrammi mxGraph che fornisce grafici interattivi e applicazioni di creazione di grafici che vengono eseguite in tutti i principali browser come Chrome, Firefox, Edge e Safari.

### DRAWIO Esempio

L'esempio seguente è un semplice diagramma di flusso creato con l'app DRAWIO.

{{< figure src="../DRAWIO.png" alt="Formato file DRAWIO" height="421" width="291">}}

L'XML di output generato con l'esportazione è mostrato di seguito.

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

## Riferimenti ##

* [DRAWIO - Github](https://github.com/jgraph/drawio)
* [DRAWIO - App online](https://app.diagrams.net/)
* [Diagrams.Net](https://www.diagrams.net/)

