{
  "date" : "2019-10-11",
  "keywords" :[ "drawio","tệp drawio", "định dạng tệp drawio", "loại tệp drawio", "tệp", "loại", "tệp drawio là gì" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DRAWIO - Định dạng tệp sơ đồ Diagram.net",
  "description" :"Tìm hiểu về Định dạng tệp DRAWIO và API để tạo và mở tệp DRAWIO.",
  "linktitle" : "DRAWIO",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-16"
}

## Tệp DRAWIO là gì?

Tệp có phần mở rộng .drawio là tệp bản vẽ được tạo bằng draw.io của [diagrams.net](https://www.diagrams.net/), một chương trình mã nguồn mở để làm việc với các sơ đồ. Nó chứa thông tin tổng thể về nội dung và định dạng của các thành phần sơ đồ chẳng hạn như văn bản, hình ảnh, bố cục, hình dạng và vị trí. Các sơ đồ được DRAWIO hỗ trợ bao gồm lưu đồ, sơ đồ tổ chức, bản đồ, các yếu tố kỹ thuật, sơ đồ quy trình, biểu đồ, v.v. Các tệp DRAWIO có thể được xuất sang một số định dạng khác nhau như [JPG](/vi/image/jpeg/), [PNG](/vi/image/png/), [BMP](/vi/image/bmp/), [XML](/vi/web/xml/), PDF, [HTML](/vi/web/html/) và [VSDX](/vi/visio/vsdx/).

## Định dạng tệp DRAWIO

Tệp DRAWIO là tệp hình ảnh vector, được lưu trữ ở định dạng tệp XML tiêu chuẩn. Được phát triển bởi diagrams.net, nó cung cấp khả năng lưu trữ thông tin sơ đồ tương tự như Microsoft Visio. DrawIO có sẵn dưới dạng [ứng dụng trực tuyến](https://app.diagrams.net/) để tạo, mở và xuất sơ đồ sang các định dạng khác nhau. Ứng dụng này dựa trên thư viện lập sơ đồ mxGraph cung cấp các ứng dụng biểu đồ và biểu đồ tương tác chạy trong bất kỳ trình duyệt chính nào như Chrome, Firefox, Edge và Safari.

### DRAWIO Ví dụ

Ví dụ sau đây là một lưu đồ đơn giản được tạo bằng ứng dụng DRAWIO.

{{< figure src="../DRAWIO.png" alt="Định dạng tệp DRAWIO" height="421" width="291">}}

XML đầu ra được tạo khi xuất như được hiển thị bên dưới.

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

## Người giới thiệu ##

* [DRAWIO - Github](https://github.com/jgraph/drawio)
* [DRAWIO - Ứng dụng trực tuyến](https://app.diagrams.net/)
* [Diagrams.Net](https://www.diagrams.net/)

