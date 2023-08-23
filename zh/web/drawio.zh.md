{
  "date" : "2019-10-11",
  "keywords" :["drawio","drawio 文件","drawio 文件格式","drawio 文件类型","文件","类型","什么是 drawio 文件"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DRAWIO - Diagram.net 图表文件格式",
  "description" :"了解 DRAWIO 文件格式和用于创建和打开 DRAWIO 文件的 API。",
  "linktitle" : "DRAWIO",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-16"
}

## 什么是 .drawio 文件？

具有 .drawio 扩展名的文件是使用 [diagrams.net](https://www.diagrams.net/) 的 draw.io 创建的绘图文件，该文件是用于处理图表的开源程序。它包含有关图表元素的内容和格式的整体信息，例如文本、图像、布局、形状和定位。 DRAWIO 支持的图表包括流程图、组织结构图、地图、工程元素、流程图、图表等。 DRAWIO 文件可以导出为多种不同的格式，例如 [JPG](/zh/image/jpeg/)、[PNG](/zh/image/png/)、[BMP](/zh/image/bmp/)、[XML](/zh/web /xml/)、PDF、[HTML](/zh/web/html/) 和 [VSDX](/zh/visio/vsdx/)。

## 绘图文件格式

DRAWIO 文件是矢量图像文件，以标准 XML 文件格式存储。由 diagrams.net 开发，它提供了存储图表信息的能力，类似于 Microsoft Visio。 DrawIO 可作为 [在线应用](https://app.diagrams.net/) 来创建、打开和导出各种格式的图表。该应用程序基于 mxGraph 图表库，该库提供可在任何主流浏览器（如 Chrome、Firefox、Edge 和 Safari）中运行的交互式图形和图表应用程序。

### DRAWIO 示例

以下示例是使用 DRAWIO 应用程序创建的简单流程图。

{{< figure src="../DRAWIO.png" alt="绘图文件格式" height="421" width="291">}}

导出生成的输出 XML 如下所示。

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

## 参考 ＃＃

* [DRAWIO - Github](https://github.com/jgraph/drawio)
* [DRAWIO - 在线应用](https://app.diagrams.net/)
* [图表网](https://www.diagrams.net/)

