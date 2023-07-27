{
  "date" : "2019-10-11",
  "keywords" :[ "tệp x3d", "định dạng tệp x3d", "tệp x3d là gì", "tệp", "ví dụ x3d", "phần mở rộng tệp x3d","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"X3D - Tệp hình ảnh 3D",
  "description":"Tìm hiểu về định dạng tệp X3D và API có thể mở và tạo tệp X3D.",
  "linktitle" : "X3D",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Tệp X3D là gì?
X3D là định dạng tệp đồ họa 3D dựa trên [XML](/vi/web/xml/) để trình bày thông tin 3D. Nó là một tiêu chuẩn mô-đun và được xác định thông qua một số thông số kỹ thuật ISO. Định dạng này hỗ trợ đồ họa vector và raster, độ trong suốt, hiệu ứng ánh sáng và cài đặt hoạt hình bao gồm xoay, mờ dần và thay đổi. Nó trở thành phiên bản kế nhiệm của định dạng tệp [VRML](/vi/3d/vrml/) vào năm 2001. X3D có ưu điểm là mã hóa thông tin màu (không giống như [STL](/vi/cad/stl/)) được sử dụng trong quá trình in mô hình trên một màu máy in 3D. Định dạng này có các phần mở rộng cho VRML, cung cấp khả năng mã hóa cảnh bằng cách sử dụng cú pháp XML cũng như cú pháp giống như Open Inventor của VRML97 hoặc định dạng nhị phân.

Đặc tả trừu tượng cho X3D (ISO/IEC 19775) lần đầu tiên được ISO phê duyệt vào năm 2004. Các mã hóa XML và ClassicVRML cho X3D (ISO/IEC 19776) lần đầu tiên được phê duyệt vào năm 2005.

## Định dạng tệp X3D

Các tệp cảnh X3D có cấu trúc tệp chung:

* Tiêu đề tệp (XML, ClassicVRML hoặc Nhị phân nén)
* Bắt đầu nút gốc X3D bao gồm các thuộc tính phiên bản và cấu hình
* Phần đầu với các câu lệnh Thành phần và Meta (cả hai tùy chọn)
* Biểu đồ X3D Scene và các nút con của nó
* Kết thúc nút gốc X3D

## Ví dụ về định dạng tệp X3D

```
<!-- -------------------- X3D header and X3D root node with profile declaration -->
<!DOCTYPE X3D PUBLIC "ISO//Web3D//DTD X3D 3.2//EN"
                     "http://www.web3d.org/specifications/x3d-3.2.dtd">
<X3D profile#'Immersive' version#'3.2'
     xmlns:xsd#'http://www.w3.org/2001/XMLSchema-instance'
     xsd:noNamespaceSchemaLocation#'http://www.web3d.org/specifications/x3d-3.2.xsd'>

<!-- -------------------- head section with included meta data -->
  <head>
    <meta content#'HelloWorld.x3d' name#'title'/>
    <meta content#'Simple X3D example' name#'description'/>
    <meta content#'30 October 2000' name#'created'/>
    <meta content#'7 August 2010' name#'modified'/>
    <meta content#'Don Brutzman' name#'creator'/>
    <meta content#'http://www.web3D.org' name#'reference'/>
    <meta content#'http://x3dGraphics.com' name#'reference'/>
    <meta content#'http://www.web3d.org/x3d/content/examples/HelloWorld.x3d' name#'identifier'/>
    <meta content#'http://www.web3d.org/x3d/content/examples/HelloWorldTall.png' name#'image'/>
    <meta content#'http://www.web3d.org/x3d/content/examples/license.html' name#'license'/>
    <meta content#'X3D-Edit 3.2, https://savage.nps.edu/X3D-Edit' name#'generator'/>
  </head>

<!-- -------------------- the X3D scene node with X3D nodes -->
  <Scene>
    <!-- Example scene to illustrate X3D nodes and fields (XML elements and attributes) -->
    <Group>
      <Viewpoint centerOfRotation#'0 -1 0' description#'Hello world!' position#'0 -1 7'/>
      <Transform rotation#'0 1 0 3'>
        <Shape>
          <Sphere/>
          <Appearance>
            <Material diffuseColor#'0 0.5 1'/>
            <ImageTexture url#'"earth-topo.png" "earth-topo.jpg" "earth-topo-small.gif"
     "http://www.web3d.org/x3d/content/examples/Basic/earth-topo.png"
     "http://www.web3d.org/x3d/content/examples/Basic/earth-topo.jpg"
     "http://www.web3d.org/x3d/content/examples/Basic/earth-topo-small.gif"'/>
          </Appearance>
        </Shape>
      </Transform>
      <Transform translation#'0 -2 0'>
        <Shape>
          <Text string#'"Hello" "world!"'>
            <FontStyle justify#'"MIDDLE" "MIDDLE"'/>
          </Text>
          <Appearance>
            <Material diffuseColor#'0.1 0.5 1'/>
          </Appearance>
        </Shape>
      </Transform>
    </Group>
  </Scene>

<!-- -------------------- footer, closing X3D toot element -->
</X3D>
```

## Người giới thiệu ##

* [X3D - Theo Wikipedia](https://vi.wikipedia.org/wiki/X3D)
* [Web3D Consortium trang web chính thức](https://www.web3d.org/)
* [Trang web chính thức của X3D](https://www.web3d.org/x3d/what-x3d)

