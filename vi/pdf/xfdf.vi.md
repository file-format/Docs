{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Định dạng tệp XFDF - Tệp XFDF là gì?",
  "description":"Tìm hiểu về tệp XFDF và các API có thể tạo và mở tệp XFDF.",
  "linktitle" : "XFDF",
  "menu" : {
    "docs" : {
      "parent" : "pdf"
}
},
  "lastmod" : "2019-09-10"
}

## Tệp XFDF là gì?

Tệp có phần mở rộng .xfdf là Định dạng Dữ liệu Biểu mẫu XML được tạo bằng phần mềm Adobe Acrobat. Giống như [FDF](/vi/pdf/fdf/), XFDF chứa phần mô tả phần tử biểu mẫu và giá trị của chúng ở định dạng XML. Điều này có thể bao gồm tên và giá trị của các trường văn bản trong biểu mẫu PDF. XFDF được lưu ở định dạng mà con người có thể đọc được và có thể được đọc theo chương trình bằng các ngôn ngữ lập trình như C#.

## Định dạng tệp XFDF - Thông tin khác

Các tệp XFDF được lưu ở định dạng tệp XML, đây là định dạng phổ biến được sử dụng để nhập và xuất dữ liệu. Cấu trúc tệp XFDF bao gồm tiêu đề, theo sau là giá trị trường và dữ liệu phần tử như được hiển thị bên dưới.

|Thành phần|Thuộc tính|Nội dung|
---|---|---|
|\<XFDF> ||Phần tử trên cùng|
|\<fields> ||Tất cả các giá trị trường cho mẫu này|
|<field (T)> |tên |Tên trường|
|<value (V)> |giá trị |giá trị trường|

## Người giới thiệu

* [Hỗ trợ định dạng FDF bởi Acrobat](https://helpx.adobe.com/coldfusion/developing-applications/working-with-documents-charts-and-reports/assembling-pdf-documents/fdf-format-support-for -acroforms.html)
* [Tài nguyên dành cho nhà phát triển Adobe](https://opensource.adobe.com/dc-acrobat-sdk-docs/)

