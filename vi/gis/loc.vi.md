{
  "date" : "2021-07-18",
  "keywords" :[ "LOC", "file", "extension", "file format", "GPS Location", "Waypoint" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LOC - Định dạng tệp vị trí GPS",
  "description":"Tìm hiểu về định dạng tệp LOC và các API có thể tạo và mở tệp LOC.",
  "linktitle" : "LOC",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-07-18"
}

## Tệp LỘC là gì?

Tệp có phần mở rộng .loc là tệp vị trí GPS chứa các vị trí không gian địa lý dưới dạng điểm tham chiếu. Điểm tham chiếu là một cặp giá trị Vĩ độ-Kinh độ đề cập đến một vị trí được các ứng dụng Hệ thống thông tin địa lý (GIS) sử dụng. Các chương trình lập bản đồ GPS, chẳng hạn như DeLorme Topo, sử dụng các tệp LOC để đọc và hiển thị thông tin có trong các tệp LOC này dưới dạng các lớp có thể lựa chọn của người dùng cuối. Ngoài ra, chúng được sử dụng để trao đổi dữ liệu GPS giữa các ứng dụng. Các tệp LOC có thể được mở bằng các ứng dụng như [TopoGrafix EasyGPS](https://www.easygps.com/) hiển thị nội dung của các tệp như lớp và dữ liệu được vẽ trên bản đồ ở vị trí địa lý tương ứng.

## Định dạng tệp LOC - Thông tin khác

Các tệp LOC có điểm tương đồng với các tệp [GPX](/vi/gis/gpx/) nhưng được lưu ở định dạng khác. Chúng được lưu dưới dạng tệp [XML](/vi/web/xml/) trong đó nội dung của các điểm tham chiếu và thông tin liên quan được chứa trong các thẻ có cấu trúc. Do XML là một ngôn ngữ tổng quát để trao đổi dữ liệu giữa các ứng dụng khác nhau nên điều này tạo điều kiện thuận lợi cho việc trao đổi dữ liệu LOC với các ứng dụng khác.

## Định dạng tệp LOC - Ví dụ

Sau đây là tiêu đề và văn bản của một điểm tham chiếu từ tệp LOC. Như có thể thấy, thông tin tiêu đề chứa nguồn vị trí cho dữ liệu. Điểm tham chiếu chứa thông tin như `ID` và dữ liệu nội dung liên quan được liên kết với điểm tham chiếu. Cuối cùng, điểm tham chiếu là một tập hợp các giá trị kinh độ và vĩ độ cũng như văn bản được liên kết với điểm tham chiếu cụ thể này.

```
<?xml version="1.0" encoding="UTF-8"?>

<loc version="1.0" src="Groundspeak">

<waypoint>

<name id="GCGFTA"><![CDATA[The Volunteer Cache or Find The Bridge by Eagle Son]]></name>

<coord lat="41.6965166666667" lon="-88.1080166666667"/>

<type>Geocache</type>
<link text="Cache Details">http://www.geocaching.com/seek/cache_details.aspx?wp=GCGFTA</link>

</waypoint>
```

## Người giới thiệu

* [TopGraphic EasyGPS](https://www.easygps.com/)

