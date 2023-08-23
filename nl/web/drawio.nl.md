{
  "date" : "2019-10-11",
  "keywords" :[ "drawio","drawio-bestand", "drawio-bestandsformaat", "drawio-bestandstype", "bestand", "type", "wat is een drawio-bestand"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DRAWIO - Diagram.net Diagram Bestandsformaat",
  "description" :"Meer informatie over DRAWIO-bestandsindeling en API's om DRAWIO-bestanden te maken en te openen.",
  "linktitle" : "DRAWIO",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-16"
}

## Wat is een DRAWIO-bestand?

Een bestand met de extensie .drawio is een tekenbestand gemaakt met [diagrams.net](https://www.diagrams.net/)'s draw.io, een open-sourceprogramma voor het werken met diagrammen. Het bevat algemene informatie voor de inhoud en opmaak van de diagramelementen zoals tekst, afbeeldingen, lay-out, vormen en positionering. Diagrammen die door DRAWIO worden ondersteund, omvatten stroomdiagrammen, organigrammen, kaarten, technische elementen, procesdiagrammen, grafieken en meer. DRAWIO-bestanden kunnen naar verschillende formaten worden geëxporteerd, zoals [JPG](/nl/image/jpeg/), [PNG](/nl/image/png/), [BMP](/nl/image/bmp/), [XML](/nl/web/xml/), PDF, [HTML](/nl/web/html/) en [VSDX](/nl/visio/vsdx/).

## DRAWIO-bestandsindeling

DRAWIO-bestanden zijn vectorafbeeldingsbestanden, opgeslagen in de standaard XML-bestandsindeling. Het is ontwikkeld door diagrams.net en biedt de mogelijkheid om diagraminformatie op te slaan, vergelijkbaar met Microsoft Visio. DrawIO is beschikbaar als [online app](https://app.diagrams.net/) om diagrammen te maken, openen en exporteren naar verschillende formaten. De app is gebaseerd op de mxGraph-diagrambibliotheek die interactieve grafiek- en diagramtoepassingen biedt die in elke grote browser zoals Chrome, Firefox, Edge en Safari draaien.

### DRAWIO Voorbeeld

Het volgende voorbeeld is een eenvoudig stroomdiagram dat is gemaakt met de DRAWIO-app.

{{< figure src="../DRAWIO.png" alt="DRAWIO-bestandsindeling" height="421" width="291">}}

De uitvoer-XML die met de export wordt gegenereerd, is zoals hieronder weergegeven.

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

## Referenties ##

* [DRAWIO - Github](https://github.com/jgraph/drawio)
* [DRAWIO - Online-app](https://app.diagrams.net/)
* [Diagrams.Net](https://www.diagrams.net/)

