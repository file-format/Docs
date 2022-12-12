{
  "date" : "2022-05-06",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Định dạng tệp TCX- Tệp XML của Trung tâm đào tạo",
  "description":"Tìm hiểu về định dạng tệp TCX và các API có thể tạo và mở tệp TCX.",
  "linktitle" : "TCX",
  "menu" : {
    "docs" : {
      "identifier":"gis-tcx",
      "parent" : "gis"
}
},
  "lastmod" : "2022-05-06"
}

## Tệp TCX là gì?

Tệp TCX (XML của Trung tâm đào tạo) là định dạng trao đổi dữ liệu được sử dụng để chia sẻ dữ liệu giữa các thiết bị thể dục. Nó được giới thiệu vào năm 2008 với sản phẩm Trung tâm đào tạo của Garmin. Dữ liệu tập luyện như nhịp tim, nhịp chạy, nhịp xe đạp, lượng calo và thời gian vòng chạy được lưu trữ ở định dạng [XML](/vi/web/xml/) bên trong tệp TCX. Ngoài ra, dữ liệu tóm tắt về bài tập luyện cũng được bao gồm trong tệp TCX. Tệp TCX tương tự như tệp [FIT](/vi/gis/fit/) được tạo bằng thiết bị đeo thể thao của Garmin.

## Định dạng tệp TCX - Thông tin khác

Các tệp TCX được lưu vào đĩa dưới dạng tệp XML với mỗi bản ghi được lưu dưới dạng một hoạt động. Một hoạt động bao gồm tất cả dữ liệu của một bài tập như thời gian, thời gian vòng chạy, Id, nhịp tim, cường độ, nhịp và thông tin bản nhạc chứa các cặp vị trí cùng với dấu thời gian cho vị trí vĩ độ đó tương tự như [GPX] (/vi/gis/gpx/).

### Phiên bản định dạng tệp TCX

Có hai phiên bản của định dạng này với lược đồ XML riêng do Garmin lưu trữ. Sau đây là một vài trong số họ:

* https://www8.garmin.com/xmlschemas/TrainingCenterDatabasev2.xsd
* https://www8.garmin.com/xmlschemas/UserProfileExtensionv1.xsd
* https://www8.garmin.com/xmlschemas/ActivityExtensionv2.xsd


## Giao thức dữ liệu TCX

Phiên bản nhanh của định dạng TCX XML có sẵn trên Github dưới dạng [TcxDataProtocol](https://github.com/FitnessKit/TcxDataProtocol).

## Người giới thiệu ##

* [XML Trung tâm đào tạo](https://en.wikipedia.org/wiki/Training_Center_XML)
* [Trình xem TCX](http://www.whiterocksoftware.com/2019/02/tcx-viewer.html)

