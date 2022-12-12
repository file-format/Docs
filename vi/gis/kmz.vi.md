{
  "date" : "2019-10-11",
  "keywords" :[ "tệp kmz", "tệp kmz là gì", "tệp", "ví dụ kmz", "phần mở rộng tệp kmz","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"KMZ - Định dạng tệp nén KML",
  "description":"Tìm hiểu về định dạng tệp KMZ và API có thể tạo và mở tệp KMZ.",
  "linktitle" : "KMZ",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Tệp KMZ là gì?

Tệp KMZ (KML đã nén) là một đại diện của tệp [KML](/vi/gis/kml/) được nén chứa thông tin không gian địa lý có thể xem được trong các ứng dụng GIS như Google Earth. Thông tin về dấu vị trí được thể hiện trong tệp dưới dạng vĩ độ và kinh độ cùng với tên tùy chỉnh. Tệp KMZ được đóng gói duy nhất có thể được chia sẻ với những người dùng khác một cách dễ dàng. Các tệp KMZ cũng có thể bao gồm dữ liệu mô hình 3D để thể hiện địa lý của mô hình. Có thể mở tệp KMZ trong Google Maps bằng cách lưu tệp vào một vị trí trực tuyến, sau đó nhập URL vào hộp Tìm kiếm của Google Maps.

## Cấu trúc tệp ##

Nội dung của tệp MKZ bao gồm tệp KML chính và không hoặc nhiều tệp được liên kết. Nó có thể được giải nén bằng tiện ích giải nén tiêu chuẩn như WinZIP. Định dạng tệp KMZ cũng được nén vào kho lưu trữ với tỷ lệ nén là 10:1. Bạn có thể xuất trực tiếp dữ liệu từ Google Earth giống như các ứng dụng sang định dạng tệp KMZ. Tệp KML chính có tên là **doc.kml**. Trong khi đóng gói tệp KMZ, có thể thêm nhiều tệp KML vào tệp nhưng điều này sẽ không có lợi vì Google Earth tìm kiếm tệp KML đầu tiên khi mở tệp KMZ và đọc tệp đó. Nó bỏ qua bất kỳ tệp KML nào khác được tìm thấy trong kho lưu trữ. Để chắc chắn rằng tệp KML mong muốn được Google Earth đọc, chỉ nên đặt một tệp KML duy nhất bên trong tệp KMZ.

Hình ảnh, mô hình, kết cấu, tệp âm thanh và các tài nguyên khác được tham chiếu trong tệp doc.kml được đặt trong một thư mục con khác bên trong thư mục chính. Điều này cũng có thể liên quan đến một số phức tạp tùy thuộc vào số lượng tệp hỗ trợ. Liên kết đến các tài nguyên cấu thành này có thể được tham chiếu tương đối hoặc thông qua tham chiếu tuyệt đối.

### Tham chiếu tương đối ###

Khi tài nguyên được đặt dọc theo doc.kml chính bên trong thư mục con trong thư mục chính, thì tham chiếu tương đối có thể trỏ đến các tệp hỗ trợ này như trong ví dụ sau (chỉ dành cho biểu tượng).

```
<IconStyle>
  <scale>1.1</scale>
  <Icon>
    <href>files/icon_surfing.png</href>
  </Icon>
</IconStyle>
```

### Tham chiếu tuyệt đối ###

Tài nguyên có thể được tham khảo hoàn toàn là tốt. Tham chiếu tuyệt đối chứa URL đầy đủ cho tệp được liên kết. Khi các tệp được đăng trên một máy chủ trung tâm, tham chiếu tuyệt đối đảm bảo rằng những tệp này vẫn rõ ràng so với tham chiếu tương đối. Tuyệt đối không nên tham chiếu tệp cục bộ vì các liên kết này sẽ bị hỏng khi tệp được chuyển sang hệ thống mới. Một ví dụ về tham chiếu tuyệt đối như sau:

```
<Icon>
  <href>http://maps.google.com/mapfiles/kml/pushpin/ylw-pushpin.png</href>
</Icon>
```

## Xem thêm ##

* [GeoJSON](/vi/gis/geojson/)

## Người giới thiệu ##

* [Tệp Google Earth và KMZ](https://developers.google.com/kml/documentation/kmzarchives#google-earth-and-kmz-archives)

