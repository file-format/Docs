{
  "date" : "2019-10-11",
  "keywords" :[ "drawio","drawio dosyası", "drawio dosya formatı", "drawio dosya türü", "dosya", "tür", "drawio dosyası nedir" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DRAWIO - Diagram.net Diyagram Dosya Formatı",
  "description" :"DRAWIO Dosya Biçimi ve DRAWIO dosyaları oluşturmak ve açmak için API'ler hakkında bilgi edinin.",
  "linktitle" : "DRAWIO",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-16"
}

## DRAWIO dosyası nedir?

.drawio uzantılı bir dosya, diyagramlarla çalışmak için açık kaynaklı bir program olan [diagrams.net](https://www.diagrams.net/)'nin draw.io'su ile oluşturulan bir çizim dosyasıdır. Metin, resimler, düzen, şekiller ve konumlandırma gibi diyagram öğelerinin içeriği ve biçimlendirmesi için genel bilgileri içerir. DRAWIO tarafından desteklenen diyagramlar arasında akış şemaları, organizasyon şemaları, haritalar, mühendislik öğeleri, süreç şemaları, çizelgeler ve daha fazlası bulunur. DRAWIO dosyaları [JPG](/tr/image/jpeg/), [PNG](/tr/image/png/), [BMP](/tr/image/bmp/), [XML](/tr/web) gibi birkaç farklı formatta dışa aktarılabilir. /xml/), PDF, [HTML](/tr/web/html/) ve [VSDX](/tr/visio/vsdx/).

## DRAWIO Dosya Biçimi

DRAWIO dosyaları, standart XML dosya biçiminde saklanan vektör görüntü dosyalarıdır. diagrams.net tarafından geliştirilmiş olup, Microsoft Visio'ya benzer diyagram bilgilerini depolama yeteneği sağlar. DrawIO, diyagramları oluşturmak, açmak ve çeşitli biçimlerde dışa aktarmak için [çevrimiçi uygulama](https://app.diagrams.net/) olarak mevcuttur. Uygulama, Chrome, Firefox, Edge ve Safari gibi herhangi bir büyük tarayıcıda çalışan etkileşimli grafik ve çizelgeleme uygulamaları sağlayan mxGraph diyagram kitaplığına dayanmaktadır.

### DRAWIO Örneği

Aşağıdaki örnek, DRAWIO uygulamasıyla oluşturulmuş basit bir akış şemasıdır.

{{< figure src="../DRAWIO.png" alt="DRAWIO Dosya Biçimi" height="421" width="291">}}

Dışa aktarma ile oluşturulan çıktı XML'i aşağıda gösterildiği gibidir.

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

## Referanslar ##

* [DRAWIO - Github](https://github.com/jgraph/drawio)
* [DRAWIO - Çevrimiçi Uygulama](https://app.diagrams.net/)
* [Diagrams.Net](https://www.diagrams.net/)

