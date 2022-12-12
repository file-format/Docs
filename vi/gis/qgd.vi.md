{
  "date" : "2021-03-18",
  "author" : {
    "display_name" : "Muhammad Umar",
	"keywords" :[ "QGD", "Cơ sở dữ liệu Sqlite của Dự án QGIS", "phần mở rộng", "định dạng", "QGIS", "Cơ sở dữ liệu phụ trợ", "Tệp QGD là gì"]
},
  "draft" : "false",
  "toc" : true,
  "title" :"QGD - Cơ sở dữ liệu Sqlite của Dự án QGIS",
  "description":"Tìm hiểu về QGD là cơ sở dữ liệu sqlite của dự án QGIS và các API có thể tạo và mở tệp QGD.",
  "linktitle" : "QGD",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-03-18"
}

## Tệp QGD là gì?

Tệp có phần mở rộng .QGD thực sự là cơ sở dữ liệu sqlite được liên kết của dự án **QGIS** chứa dữ liệu phụ trợ cho dự án. Tệp QGD sẽ vẫn trống, nếu không có dữ liệu phụ trợ cho dự án.

## Chi tiết về định dạng tệp QGD

Ở chế độ cổ điển, cơ sở dữ liệu phụ trợ được lưu dưới dạng tệp có phần mở rộng .qgd dọc theo tệp xml. Hệ thống **Cơ sở dữ liệu phụ trợ** cho phép đọc và ghi dữ liệu trong hệ thống theo một cách khác. Khi tạo QGZ là vùng chứa được nén, tệp .qgd sẽ bao gồm trong .qgz.

## Cơ sở dữ liệu phụ trợ là gì?
Cơ sở dữ liệu phụ trợ thực sự là một hệ thống db dự phòng được tạo ra như một phản ứng của việc sao chép cơ sở dữ liệu đích. Cơ sở dữ liệu phụ trợ thực sự là một trường hợp cơ sở dữ liệu trùng lặp sẽ là cơ sở dữ liệu mà bạn đang sao chép vào. Ví dụ: nếu bạn thiết lập cơ sở dữ liệu dự phòng bằng cơ sở dữ liệu trùng lặp, cơ sở dữ liệu nguồn sẽ là đích và cơ sở dữ liệu dự phòng sẽ được gọi là cơ sở dữ liệu phụ trợ.


## Người giới thiệu

* [QGZ – Định dạng tệp dự án mặc định mới cho QGIS](https://oslandia.com/en/2018/06/01/qgz-a-new-default-project-file-format-for-qgis/)
* [Định dạng tệp QGIS](https://docs.qgis.org/3.16/en/docs/user_manual/appendices/qgis_file_formats.html)

