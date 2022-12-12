{
  "date" : "2019-10-11",
  "keywords" :[ "tệp kml", "tệp kml là gì", "tệp", "ví dụ kml", "phần mở rộng tệp kml","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"KML - Ngôn ngữ đánh dấu lỗ khóa",
  "description":"Tìm hiểu về định dạng tệp KML và các API có thể tạo và mở tệp KML.",
  "linktitle" : "KML",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Tệp KML là gì?

KML, Ngôn ngữ đánh dấu lỗ khóa) chứa thông tin không gian địa lý ở dạng ký hiệu XML. Các tệp được lưu dưới dạng KML có thể được mở trong các ứng dụng Hệ thống Thông tin Địa lý (GIS) miễn là chúng hỗ trợ. Nhiều ứng dụng đã bắt đầu cung cấp hỗ trợ cho định dạng tệp KML sau khi nó được chấp nhận làm tiêu chuẩn quốc tế. KML sử dụng cấu trúc dựa trên thẻ với các phần tử và thuộc tính lồng nhau. Tất cả các thẻ đều phân biệt chữ hoa chữ thường và thứ tự của các thẻ này, theo Tham chiếu [KML](https://developers.google.com/kml/documentation/kmlreference), là điều quan trọng cần tuân theo.

## Lược Sử ##

KML ban đầu được phát triển để sử dụng với Google Earth, ban đầu được gọi là Keyhole Earth Viewer. KLM đã được Open Geospatial Consortium chấp nhận làm tiêu chuẩn quốc tế vào năm 2008. Vì định dạng này được phát triển để sử dụng với Google Earth nên nó có điểm khác biệt là định dạng đầu tiên xem và chỉnh sửa các tệp KML. Cùng với thời gian, ngày càng có nhiều dự án cung cấp hỗ trợ cho các định dạng tệp KML bao gồm một số API bằng các ngôn ngữ khác nhau.

## Thông số kỹ thuật định dạng tệp KML ##

Tài liệu tham khảo KML là một hướng dẫn đầy đủ để tham khảo nhằm có các thông số định dạng tệp đầy đủ. Một tệp KML tiêu chuẩn bao gồm:

* Dấu vị trí
* Dấu vị trí HTMLin mô tả
* Lớp phủ mặt đất
* Đường dẫn
* Đa giác

Ngoài những thứ này, phiên bản nâng cao của tệp KML có thể có:

* Phong cách cho Hình học
* Kiểu cho các biểu tượng được đánh dấu
* Lớp phủ màn hình
* Liên kết mạng

Mỗi phần tử KML có thông tin thời gian trễ định vị địa lý thông tin có trong tệp. Tuy nhiên, có thể có các tham số bổ sung cũng như tiêu đề, độ cao và độ nghiêng.

### Dấu vị trí ###

Nó được sử dụng để đại diện cho một vị trí trên bề mặt Trái đất và được xác định bởi<Point> yếu tố. Sau đây là ví dụ về cách dấu vị trí được thể hiện trong tệp KML.

```

<kml xmlns#"http://www.opengis.net/kml/2.2">
  <Placemark>
    <name>Simple placemark</name>
    <description>Attached to the ground. Intelligently places itself
       at the height of the underlying terrain.</description>
    <Point>
      <coordinates>-122.0822035425683,37.42228990140251,0</coordinates>
    </Point>
  </Placemark>
</kml>
```

### HTML mô tả trong Dấu vị trí ###

Thông tin bổ sung có thể được liên kết với một dấu vị trí giúp nâng cao hơn nữa tính đại diện của dấu vị trí. Những thông tin như vậy bao gồm các liên kết, cỡ chữ, kiểu dáng và màu sắc. Ngoài ra, nó cũng bao gồm căn chỉnh văn bản và bảng để trở thành một phần của dấu vị trí.

```

<kml xmlns#"http://www.opengis.net/kml/2.2">
  <Document>
    <Placemark>
      <name>CDATA example</name>
      <description>
        <![CDATA[
          <h1>CDATA Tags are useful!</h1>
          <p><font color#"red">Text is <i>more readable</i> and
          <b>easier to write</b> when you can avoid using entity
          references.</font></p>
        ]]>
      </description>
      <Point>
        <coordinates>102.595626,14.996729</coordinates>
      </Point>
    </Placemark>
  </Document>
</kml>
```

### Lớp phủ mặt đất ###

Chúng đại diện cho lớp của một hình ảnh trên bề mặt Trái đất. Các<icon> phần tử chứa liên kết đến tệp hình ảnh lớp phủ.

```

<kml xmlns#"http://www.opengis.net/kml/2.2">
  <Folder>
    <name>Ground Overlays</name>
    <description>Examples of ground overlays</description>
    <GroundOverlay>
      <name>Large-scale overlay on terrain</name>
      <description>Overlay shows Mount Etna erupting
          on July 13th, 2001.</description>
      <Icon>
        <href>https://developers.google.com/kml/documentation/images/etna.jpg</href>
      </Icon>
      <LatLonBox>
        <north>37.91904192681665</north>
        <south>37.46543388598137</south>
        <east>15.35832653742206</east>
        <west>14.60128369746704</west>
        <rotation>-0.1556640799496235</rotation>
      </LatLonBox>
    </GroundOverlay>
  </Folder>
</kml>
```

### Đường dẫn ###

Đường dẫn được đại diện bởi<LineString> phần tử là một tập hợp các cặp lat-long. Sử dụng những thứ này, nhiều loại đường dẫn khác nhau có thể được tạo trong Google Earth.

```

<kml xmlns#"http://www.opengis.net/kml/2.2">
  <Document>
    <name>Paths</name>
    <description>Examples of paths. Note that the tessellate tag is by default
      set to 0. If you want to create tessellated lines, they must be authored
      (or edited) directly in KML.</description>
    <Style id#"yellowLineGreenPoly">
      <LineStyle>
        <color>7f00ffff</color>
        <width>4</width>
      </LineStyle>
      <PolyStyle>
        <color>7f00ff00</color>
      </PolyStyle>
    </Style>
    <Placemark>
      <name>Absolute Extruded</name>
      <description>Transparent green wall with yellow outlines</description>
      <styleUrl>#yellowLineGreenPoly</styleUrl>
      <LineString>
        <extrude>1</extrude>
        <tessellate>1</tessellate>
        <altitudeMode>absolute</altitudeMode>
        <coordinates> -112.2550785337791,36.07954952145647,2357
          -112.2549277039738,36.08117083492122,2357
          -112.2552505069063,36.08260761307279,2357
          -112.2564540158376,36.08395660588506,2357
          -112.2580238976449,36.08511401044813,2357
          -112.2595218489022,36.08584355239394,2357
          -112.2608216347552,36.08612634548589,2357
          -112.262073428656,36.08626019085147,2357
          -112.2633204928495,36.08621519860091,2357
          -112.2644963846444,36.08627897945274,2357
          -112.2656969554589,36.08649599090644,2357
        </coordinates>
      </LineString>
    </Placemark>
  </Document>
</kml>
```

## Tham chiếu không gian trong tệp KML ##

Thông tin chứa trong bất kỳ tệp Không gian địa lý nào về Vị trí địa lý có thể có ý nghĩa khác nhau mà không có thông tin tham chiếu không gian. Theo mặc định, tham chiếu không gian của tệp KML được xác định bởi Hệ thống trắc địa thế giới năm 1984, WGS84.

## Người giới thiệu ##

* [Tham khảo KML](https://developers.google.com/kml/documentation/kmlreference)
* [Hướng dẫn dành cho nhà phát triển của Google dành cho KML](https://developers.google.com/kml/documentation/kml_tut)
* [Định dạng tệp KML](https://en.wikipedia.org/wiki/Keyhole_Markup_Language)

