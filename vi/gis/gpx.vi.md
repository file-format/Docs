{
  "date" : "2019-10-11",
  "keywords" :[ "tệp gpx", "tệp gpx là gì", "tệp", "ví dụ gpx", "phần mở rộng tệp gpx","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GPX - Định dạng tệp trao đổi GPX",
  "description":"Tìm hiểu về định dạng tệp GPX và API có thể tạo và mở tệp GPX.",
  "linktitle" : "GPX",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Tệp GPX là gì?

Các tệp có phần mở rộng GPX đại diện cho định dạng Trao đổi GPS để trao đổi dữ liệu GPS giữa các ứng dụng và dịch vụ web trên internet. Đây là một định dạng tệp XML có trọng lượng nhẹ chứa dữ liệu GPS, tức là các điểm tham chiếu, tuyến đường và đường đi sẽ được nhập và tô đỏ bởi nhiều chương trình. Định dạng tệp GPX mở và được hỗ trợ bởi nhiều ứng dụng và thiết bị GPS. Dữ liệu GPS từ các tệp như vậy có thể được tải để hiển thị trên các ứng dụng bản đồ cho mục đích không gian địa lý.

## Định dạng tệp GPX ##

Tệp GPX bao gồm dữ liệu vị trí kinh độ và vĩ độ, giá trị độ cao và các thông tin mô tả khác có thể khác. Dữ liệu vị trí được biểu thị bằng độ thập phân và độ cao được biểu thị bằng mét. Thời gian trong tệp GPX là Giờ phối hợp quốc tế (UTC) sử dụng định dạng ISO 8601. Lợi ích của việc sử dụng tệp GPX như sau:

* GPX cho phép bạn trao đổi dữ liệu với danh sách chương trình ngày càng tăng dành cho Windows, MacOS, Linux, Palm và PocketPC.
* GPX có thể được chuyển đổi thành các định dạng tệp khác bằng cách sử dụng một trang web đơn giản hoặc chương trình chuyển đổi.
* GPX dựa trên tiêu chuẩn XML, vì vậy nhiều chương trình mới mà bạn sử dụng (ví dụ: Microsoft Excel) có thể đọc các tệp GPX.
* GPX giúp mọi người trên web dễ dàng phát triển các tính năng mới sẽ hoạt động ngay lập tức với các chương trình yêu thích của bạn.

[Lược đồ GPX](https://www.topografix.com/GPX/1/1/gpx.xsd) hiển thị biểu diễn cho định dạng tệp GPX để tham khảo.

### Dữ liệu cần thiết ###

Sau đây là dữ liệu cần thiết là một phần của tệp GPX để thể hiện dữ liệu GPS.

* **Điểm tham chiếu**: Điểm tham chiếu là tọa độ WGS84 (GPS) của một điểm và biểu thị lớp tính năng của loại OGR wkbPoint
* **Routes**: Đại diện cho một lớp tính năng của loại OGR wkbLineString. Nó bao gồm một danh sách các điểm theo dõi, là các điểm tham chiếu hiển thị các điểm rẽ hoặc chặng dẫn đến đích
* **Đường đi**: Đường đi đại diện cho lớp tính năng của loại OGR wkbMultiLineString. Nó được tạo thành từ ít nhất một đoạn chứa các điểm tham chiếu trong một danh sách các điểm được sắp xếp theo thứ tự mô tả một đường dẫn. Nó bao gồm một danh sách các điểm theo dõi đại diện cho một tuyến đường GPS liên tục.

### Tệp Ví dụ GPX ###

Tệp GPX sau đây hiển thị tổ chức dữ liệu GPS trong tệp GPX và có thể cung cấp ý tưởng hay về nội dung của tệp GPX.

```
<gpx xmlns#"http://www.topografix.com/GPX/1/1" xmlns:gpxx#"http://www.garmin.com/xmlschemas/GpxExtensions/v3" xmlns:gpxtpx#"http://www.garmin.com/xmlschemas/TrackPointExtension/v1" creator#"Oregon 400t" version#"1.1" xmlns:xsi#"http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation#"http://www.topografix.com/GPX/1/1 http://www.topografix.com/GPX/1/1/gpx.xsd http://www.garmin.com/xmlschemas/GpxExtensions/v3 http://www.garmin.com/xmlschemas/GpxExtensionsv3.xsd http://www.garmin.com/xmlschemas/TrackPointExtension/v1 http://www.garmin.com/xmlschemas/TrackPointExtensionv1.xsd">
  <metadata>
    <link href#"http://www.garmin.com">
      <text>Garmin International</text>
    </link>
    <time>2009-10-17T22:58:43Z</time>
  </metadata>
  <trk>
    <name>Example GPX Document</name>
    <trkseg>
      <trkpt lat#"47.644548" lon#"-122.326897">
        <ele>4.46</ele>
        <time>2009-10-17T18:37:26Z</time>
      </trkpt>
      <trkpt lat#"47.644548" lon#"-122.326897">
        <ele>4.94</ele>
        <time>2009-10-17T18:37:31Z</time>
      </trkpt>
      <trkpt lat#"47.644548" lon#"-122.326897">
        <ele>6.87</ele>
        <time>2009-10-17T18:37:34Z</time>
      </trkpt>
    </trkseg>
  </trk>
</gpx>
```

## Người giới thiệu ##

* [Định dạng tệp GPX](http://www.topografix.com/gpx.asp)
* [GPX - Theo Wikipedia](https://en.wikipedia.org/wiki/GPS_Exchange_Format)

