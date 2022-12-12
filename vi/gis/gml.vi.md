{
  "date" : "2019-10-11",
  "keywords" :[ "tệp gml", "tệp gml là gì", "tệp", "ví dụ gml", "phần mở rộng tệp gml","tiện ích mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GML - Định dạng tệp ngôn ngữ đánh dấu địa lý",
  "description":"Tìm hiểu về định dạng tệp GML và API có thể tạo và mở tệp GML.",
  "linktitle" : "GML",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Tệp GML là gì?

GML là viết tắt của Language Markup Language dựa trên các đặc tả XML được phát triển bởi Open Geospatial Consortium (OGC). Định dạng được sử dụng để lưu trữ các tính năng dữ liệu địa lý để trao đổi giữa các định dạng tệp khác nhau. Nó đóng vai trò là ngôn ngữ mô hình hóa cho các hệ thống địa lý cũng như định dạng trao đổi mở cho các giao dịch địa lý trên internet.

## Định dạng tệp GML ##

Như với hầu hết các ngữ pháp dựa trên XML, ngữ pháp có hai phần – lược đồ mô tả tài liệu và tài liệu cá thể chứa dữ liệu thực tế. Tài liệu GML được mô tả bằng Lược đồ GML. Điều này cho phép người dùng và nhà phát triển mô tả các tập dữ liệu địa lý chung có chứa các điểm, đường và đa giác. Sử dụng lược đồ ứng dụng, người dùng có thể tham khảo đường, đường cao tốc và cầu thay vì điểm, đường và đa giác.

Cần lưu ý rằng GML không nên được giải thích để biểu thị dữ liệu không gian trên bản đồ. Việc trình bày nội dung GML khác với mục đích mà GML được tạo ra. Nói tóm lại, GML tương tự như XML ở chỗ nó chỉ được sử dụng để giữ các nội dung không gian có thể được sử dụng bởi các ứng dụng ánh xạ cho mục đích hiển thị.

### Hình thành nội dung trong GML ###

GML biểu thị dữ liệu không gian bằng cách sử dụng các tính năng là danh sách các thuộc tính và hình học. Một Thuộc tính có tên, loại và mô tả giá trị. Hình học bao gồm các khối xây dựng hình học cơ bản như:

* điểm
* dòng
* đường cong
* bề mặt và
* đa giác

Các phiên bản tương lai của GML được lên kế hoạch để hỗ trợ hình học 3D cũng như các mối quan hệ cấu trúc liên kết giữa các tính năng.

Mã hóa GML đã cho phép các tính năng khá phức tạp. Ví dụ, một tính năng có thể bao gồm các tính năng khác. Do đó, một tính năng đơn lẻ như sân bay có thể bao gồm các tính năng khác như đường lăn, đường băng, móc treo và nhà ga hàng không. Hình học của một đối tượng địa lý cũng có thể bao gồm nhiều yếu tố hình học. Do đó, một tính năng phức tạp về mặt hình học có thể bao gồm sự kết hợp của các loại hình học bao gồm điểm, chuỗi đường và đa giác.

### Ví dụ ###

GML 1.0 và 2.0 mã hóa các đối tượng Đa giác, Điểm và LineString như sau:

```
<gml:Polygon>
         <gml:outerBoundaryIs>
                 <gml:LinearRing>
                         <gml:coordinates>0,0 100,0 100,100 0,100 0,0</gml:coordinates>
                 </gml:LinearRing>
        </gml:outerBoundaryIs>
     </gml:Polygon>
     <gml:Point>
        <gml:coordinates>100,200</gml:coordinates>
     </gml:Point>
     <gml:LineString>
        <gml:coordinates>100,200 150,300</gml:coordinates>
     </gml:LineString>
```

## Người giới thiệu ##

* [Thông số GML](http://www.opengeospatial.org/standards/gml)
* [GML - Theo Wikipedia](https://en.wikipedia.org/wiki/Geography_Markup_Language)

