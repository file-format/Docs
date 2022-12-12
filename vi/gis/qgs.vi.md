{
  "date" : "2019-10-11",
  "keywords" :[ "tệp qgs", "định dạng tệp qgs", "tệp qgs là gì", "tệp", "ví dụ qgs", "phần mở rộng tệp qgs","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"QGS - Định dạng tệp dự án QGIS",
  "description":"Tìm hiểu về định dạng tệp QGS và API có thể tạo và mở tệp QGS.",
  "linktitle" : "QGS",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## Tệp QGS là gì?

Tệp có phần mở rộng .qss là tệp dự án được tạo bằng [QGIS](https://www.qgis.org/en/site/), đây là một ứng dụng GIS đa nền tảng mã nguồn mở. Tất cả các cài đặt dự án như thuộc tính lớp và dữ liệu phụ trợ cho dự án. Nó được tạo khi một dự án bản đồ được lưu vào đĩa. Nó thực sự là một tệp cấu hình giữ lại thông tin như con trỏ tới dữ liệu GIS, thông tin kiểu dáng về các lớp và tiêu đề dự án. Các tệp QGS có thể được mở bằng phần mềm QGIS có sẵn miễn phí để tải xuống.

## Định dạng tệp QGS

Các tệp QGS ở định dạng [XML](/vi/web/xml/) và lưu trữ dữ liệu dự án dưới dạng thẻ XML. Tệp QGS chứa thông tin như:

* Tên dự án
* dự án CRS
* cây lớp
* cài đặt chụp nhanh
* quan hệ
* phạm vi canvas bản đồ
* mô hình dự án
* truyền thuyết
* bến cảng mapview (2D và 3D)
* các lớp có liên kết đến bộ dữ liệu cơ bản (nguồn dữ liệu) và các thuộc tính lớp khác bao gồm phạm vi, SRS, liên kết, kiểu, trình kết xuất, chế độ hòa trộn, độ mờ, v.v.
* tài sản dự án

### Thẻ XML cấp cao nhất của QGS

{{< figure src="../qgstoplevel.png" title="" >}}

### Thẻ lớp dự án cấp cao nhất mở rộng

{{< figure src="../qgstoplevel.png" title="" >}}

## Người giới thiệu

* [QGIS](https://www.qgis.org/en/site/)

