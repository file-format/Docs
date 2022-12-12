{
  "date" : "2019-10-11",
  "keywords" :[ "tệp geojson", "tệp geojson là gì", "tệp", "ví dụ geojson", "phần mở rộng tệp geojson","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GeoJSON - Định dạng tệp địa lý dựa trên JSON",
  "description":"Tìm hiểu về định dạng tệp GeoJSON và API có thể tạo và mở tệp GeoJSON.",
  "linktitle" : "GeoJSON",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Tệp GeoJSON là gì?

GeoJSON là một định dạng dựa trên JSON được thiết kế để thể hiện các đối tượng địa lý với các thuộc tính phi không gian của chúng. Định dạng này xác định các đối tượng JSON (Ký hiệu đối tượng JavaScript) khác nhau và cách kết hợp của chúng. Định dạng JSON đại diện cho thông tin tập thể về các đối tượng địa lý, phạm vi không gian và thuộc tính của chúng. Một đối tượng của tệp này có thể biểu thị một hình học (Điểm, LineString, Đa giác), một đối tượng địa lý hoặc tập hợp các đối tượng địa lý. Các tính năng phản ánh địa chỉ và địa điểm dưới dạng đường phố, đường chính và biên giới dưới dạng chuỗi đường và quốc gia, tỉnh và vùng đất dưới dạng đa giác. Sử dụng GeoJSON, các ứng dụng điều hướng và định tuyến di động khác nhau có thể chỉ ra phạm vi phủ sóng của các dịch vụ của họ. Một phần mở rộng của GeoJSON là TopoJSON có kích thước nhỏ hơn và mã hóa cấu trúc liên kết không gian địa lý.

## Lược Sử ##

Lực lượng Đặc nhiệm Kỹ thuật Internet (IETF), kết hợp với các tác giả định dạng, đã hình thành một [GeoJSON WG](https://datatracker.ietf.org/wg/geojson/charter/) để phát hành GeoJSON vào tháng 4 năm 2015. Thay thế cho 2008 Đặc tả GeoJSON, [RFC 7946](https://tools.ietf.org/html/rfc7946), đặc tả tiêu chuẩn mới của định dạng GeoJSON được xuất bản vào tháng 8 năm 2016.

## Định dạng tệp GeoJSON ##

### Điều phối ###

Tọa độ là yếu tố cơ bản của bất kỳ dữ liệu địa lý nào. Đây là một thứ nguyên (Kinh độ, vĩ độ) đại diện cho một số duy nhất (định dạng thập phân) và đôi khi cũng ghi lại tọa độ cho độ cao. Thời gian cũng là một chiều nhưng độ phức tạp của nó khiến việc ghi lại nó dưới dạng tọa độ trở nên khó khăn. Các tọa độ trong cả JSON GeoJSON được định dạng giống như các số.

### Chức vụ ###

Một mảng tọa độ được sắp xếp đại diện cho [vị trí](http://geojson.org/geojson-spec.html#positions). Đây là đơn vị nhỏ nhất có thể chỉ ra một điểm trên trái đất.

`[Kinh độ, vĩ độ, độ cao]`

Trước khi phát hành thông số kỹ thuật hiện tại, GeoJSON được phép ghi lại ba tọa độ cho mỗi vị trí nhưng thông số kỹ thuật mới không cho phép.

### Hình học ###

Hình học là các hình dạng đơn giản (điểm, đường cong và bề mặt) trong GeoJSON bao gồm một loại và một tập hợp các tọa độ. Điểm là hình học đơn giản nhất đại diện cho một vị trí duy nhất

`{ "loại": "Điểm", "tọa độ": [0, 0] }`

### Chuỗi Dòng ###

Ít nhất hai vị trí được kết nối được sử dụng để biểu thị một đường thẳng.

`{ "type": "LineString", "tọa độ": [[10, 30], [10, 10]] }`

Chuỗi điểm và chuỗi là hai phạm trù hình học đơn giản nhất. Cả hai loại hình học đều không bận tâm đến nhiều quy tắc hình học. Một điểm có thể được biểu diễn ở một vị trí ở bất kỳ đâu và một đường có thể có nhiều hơn một điểm, ngay cả khi các điểm đó tự cắt nhau.

### Đa giác ###

Hình học GeoJSON có vẻ phức tạp hơn đáng kể trong Đa giác. Đa giác có các khu vực bên trong và bên ngoài và có thể có các lỗ ở bên trong đó.

```
{
  "type": "Polygon",
  "Coordinates": [
    [
      [30, 10], [10, 10], [10, 0], [20, 40]
    ]
  ]
}
```

So với LineStrings, trong đa giác, danh sách tọa độ là một cấp độ khác được lồng vào nhau và có thể có các phần bị cắt giống như bánh rán.

### Cấp tọa độ ###

Ở định dạng GeoJSON, đối với thuộc tính tọa độ, có bốn mức độ sâu.

### Đặc trưng ###

Hình học là phần trung tâm của GeoJSON, do đó, dữ liệu trong thế giới thực không chỉ là những hình dạng đơn giản có bản sắc và thuộc tính. Các tính năng ghi lại hình học cũng như các thuộc tính của chúng.

```
{
  "type": "Feature",
  "geometry": {
    "type": "Point",
    "coordinates": [20, 10]
},
  "properties": {
    "name": "fortune island"
  }
}

```

Thuộc tính đối tượng có thể là một loại đối tượng [JSON](http://json.org/) chứa các ánh xạ giá trị khóa có độ sâu đơn.

### Bộ sưu tập tính năng ###

Ở cấp cao nhất của tệp GeoJSON, FeatureCollection là thứ phổ biến nhất trông giống như:

```
{
  "type": "FeatureCollection",
  "features": [
    {
      "type": "Feature",
      "geometry": {
        "type": "Point",
        "coordinates": [20, 10]
    },
      "properties": {
        "name": "null island"
  }
}
  ]
}
```

Rất nhiều gói phần mềm bản đồ và GIS hỗ trợ GeoJSON bao gồm phần mềm GeoDjango, OpenLayers và Geoforge. Nó cũng tương thích với PostGIS và Mapnik. Các dịch vụ API của bản đồ Google, yahoo và Bing cũng hỗ trợ GeoJSON.

## Người giới thiệu ##

* [macwright.org](https://macwright.org/2015/03/23/geojson-second-bite.html)
* [GeoJSON - Theo Wikipedia](https://en.wikipedia.org/wiki/GeoJSON)

