{
  "date" : "2019-10-11",
  "keywords" :[ "tệp qlr", "định dạng tệp qlr", "tệp qlr là gì", "tệp", "ví dụ qlr", "phần mở rộng tệp qlr","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"QLR - Tệp định nghĩa lớp QGIS",
  "description":"Tìm hiểu về định dạng tệp QLR và các API có thể tạo và mở tệp QLR.",
  "linktitle" : "QLR",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-03-14"
}

## Tệp QLR là gì?

Tệp có .qlr là tệp Định nghĩa lớp chứa con trỏ tới nguồn dữ liệu lớp. Đây là thông tin bổ sung cho thông tin kiểu [QGIS](https://www.qgis.org/en/site/) cho lớp. Có tham chiếu đến tất cả các kiểu có liên quan, tệp này được sử dụng làm nguồn duy nhất cho dữ liệu được sử dụng để nhận thông tin về kiểu. Bằng cách sử dụng các tệp QLR, thông tin về các nguồn dữ liệu có thể được đưa vào một tệp duy nhất này mà các ứng dụng khác có thể đọc được để tải thông tin kiểu dáng. Các tệp QLR có thể được mở bằng bất kỳ trình soạn thảo văn bản nào, chẳng hạn như Notepad ++.

## Định dạng tệp QLR

QLR, tương tự như [QGS](/vi/gis/qgs/), là một tệp XML chứa các con trỏ tới nguồn dữ liệu lớp ở dạng thẻ XML. Nó tương tự như tệp .lyr của ArcGIS. Các thẻ cấp cao nhất của tệp QML như trong hình bên dưới.

{{< figure src="../qlr.png" title="" >}}

## Người giới thiệu

* [QGIS](https://www.qgis.org/en/site/)
* [QLR](https://docs.qgis.org/3.16/en/docs/user_manual/appendices/qgis_file_formats.html)

