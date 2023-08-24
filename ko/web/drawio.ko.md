{
  "date" : "2019-10-11",
  "keywords" :[ "drawio","drawio 파일", "drawio 파일 형식", "drawio 파일 형식", "파일", "유형", "drawio 파일이란" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DRAWIO - Diagram.net 다이어그램 파일 형식",
  "description" :"DRAWIO 파일 형식 및 API를 사용하여 DRAWIO 파일을 만들고 여는 방법에 대해 알아보세요.",
  "linktitle" : "DRAWIO",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-16"
}

## .DRAWIO 파일이란?

확장자가 .drawio인 파일은 다이어그램 작업을 위한 오픈소스 프로그램인 [diagrams.net](https://www.diagrams.net/)의 draw.io로 만든 드로잉 파일입니다. 여기에는 텍스트, 이미지, 레이아웃, 모양 및 위치와 같은 다이어그램 요소의 내용 및 서식에 대한 전체 정보가 포함됩니다. DRAWIO에서 지원하는 다이어그램에는 순서도, 조직도, 지도, 엔지니어링 요소, 프로세스 다이어그램, 차트 등이 포함됩니다. DRAWIO 파일은 [JPG](/ko/image/jpeg/), [PNG](/ko/image/png/), [BMP](/ko/image/bmp/), [XML](/ko/web/xml/), PDF, [HTML](/ko/web/html/) 및 [VSDX](/ko/visio/vsdx/).

## DRAWIO 파일 형식

DRAWIO 파일은 표준 XML 파일 형식으로 저장된 벡터 이미지 파일입니다. diagrams.net에서 개발한 Microsoft Visio와 유사한 다이어그램 정보를 저장할 수 있는 기능을 제공합니다. DrawIO는 [온라인 앱](https://app.diagrams.net/)으로 제공되어 다이어그램을 생성하고 열고 다양한 형식으로 내보낼 수 있습니다. 이 앱은 Chrome, Firefox, Edge 및 Safari와 같은 주요 브라우저에서 실행되는 대화형 그래프 및 차트 작성 응용 프로그램을 제공하는 mxGraph 다이어그램 라이브러리를 기반으로 합니다.

### DRAWIO 예

다음 예제는 DRAWIO 앱으로 만든 간단한 순서도입니다.

{{< figure src="../DRAWIO.png" alt="DRAWIO 파일 형식" height="421" width="291">}}

내보내기로 생성된 출력 XML은 다음과 같습니다.

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

## 참조 ##

* [DRAWIO - Github](https://github.com/jgraph/drawio)
* [DRAWIO - 온라인 앱](https://app.diagrams.net/)
* [Diagrams.Net](https://www.diagrams.net/)

