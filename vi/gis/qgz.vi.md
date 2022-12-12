{
  "date" : "2021-03-18",
  "keywords" :[ "tệp qgz", "định dạng tệp qgz", "tệp qgz là gì", "tệp", "ví dụ qgz", "phần mở rộng tệp qgz","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"QGZ - Dự án nén lượng tử GIS",
  "description":"Tìm hiểu về định dạng tệp QGZ vốn chỉ là một QGS nén và các API có thể tạo và mở tệp QGZ.",
  "linktitle" : "QGZ",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-03-18"
}

## Tệp QGZ là gì?

Định dạng tệp **QGZ** là tệp lưu trữ nén chứa tệp [QGS](https://docs.fileformat.com/gis/qgs/) và tệp QGD. Trong khi đó, tệp QGD là cơ sở dữ liệu sqlite của dự án qgis bao gồm dữ liệu phụ trợ cho dự án. Nếu không có dữ liệu phụ, tệp QGD sẽ vẫn trống.

## Chi tiết về định dạng tệp QGZ

QGZ được giới thiệu là một biến thể mới của **định dạng tệp dự án QGIS 3**. Định dạng này là một vùng chứa được nén cho tệp xml QGS. Nếu người dùng chọn QGD là định dạng tùy chọn, thì trong trường hợp này, bộ chứa có lợi để lưu trữ cơ sở dữ liệu lưu trữ phụ trợ.

Ở chế độ cổ điển, cơ sở dữ liệu phụ trợ được lưu dưới dạng tệp có phần mở rộng .qgd dọc theo tệp xml. Khi chọn vùng chứa đã nén, tệp .qgd sẽ bao gồm trong .qgz, Nó chỉ tạo điều kiện thuận lợi cho người dùng mà không gặp vấn đề gì, người dùng không thể xóa hoặc quên sao chép khi chia sẻ tệp dự án!


## Người giới thiệu

* [QGZ – Định dạng tệp dự án mặc định mới cho QGIS](https://oslandia.com/en/2018/06/01/qgz-a-new-default-project-file-format-for-qgis/)
* [Định dạng tệp QGIS](https://docs.qgis.org/3.16/en/docs/user_manual/appendices/qgis_file_formats.html)

