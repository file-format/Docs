{
  "date" : "2019-12-16",
  "keywords" :[ "OTS", "file", "extension", "file format", "Excel", "Spreadsheet" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Tìm hiểu về định dạng tệp OTS và các API có thể tạo và mở tệp OTS.",
  "title" :"OTS - Định dạng Tệp Mẫu Bảng tính Tài liệu Mở",
  "linktitle" : "OTS",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2021-01-19"
}

## Tệp OTS là gì?

Tệp có phần mở rộng .ots là tệp Mẫu Bảng tính Tài liệu Mở được tạo bằng phần mềm ứng dụng Calc có trong Apache OpenOffice. Phần mềm ứng dụng Calc tương tự như Excel có sẵn trong Microsoft Office. Định dạng tệp OTS được sử dụng để tạo các mẫu có chứa các cài đặt xác định trước liên quan đến kiểu, phông chữ, dữ liệu, bố cục bảng tính và định dạng. Các tệp OTF có `ứng dụng kiểu mime/vnd.oasis.opendocument.spreadsheet-template`. Các tệp mẫu này có thể được sử dụng làm điểm bắt đầu để tạo và lưu các tệp dữ liệu thực được lưu ở [Định dạng tệp ODS](/vi/bảng tính/ods/). Các tệp OTS có thể được sử dụng với các ứng dụng như OpenOffice và LibreOffice.

## Định dạng tệp OTS

Các tệp OTS được lưu ở định dạng tệp dựa trên XML OpenDocument của OASIS bao gồm một tập hợp nhiều tài liệu phụ với một gói dưới dạng tệp lưu trữ [ZIP](/vi/compression/zip/). Mỗi kho lưu trữ zip lưu trữ một phần của tài liệu hoàn chỉnh và mỗi tài liệu phụ lưu trữ một khía cạnh cụ thể của tài liệu. Ví dụ: một tài liệu con chứa thông tin về kiểu dáng và một tài liệu con khác chứa nội dung của tài liệu. Một tài liệu ODF điển hình có các thành phần sau:

### OTS Content.xml

Tệp content.xml chứa nội dung thực của tài liệu. Tuy nhiên, điều này không bao gồm dữ liệu nhị phân như hình ảnh.
```
<text:h style-name="Heading_2">This is a title</text:h>
<text:p style-name="Text_body"/>
<text:p style-name="Text_body">
   This is a paragraph. The formatting information is
   in the Text_body style. The empty text:p tag above
   is a blank paragraph (an empty line).
</text:p>
```

### Styles.xml của Định dạng tệp OTS

Tệp style.xml chứa thông tin về kiểu dáng và được sử dụng nhiều để định dạng và bố cục. Các loại phong cách bao gồm:

* Kiểu đoạn văn
* Kiểu trang
* Phong cách nhân vật
* Kiểu khung
* Danh sách phong cách

### Meta.xml

Tệp meta.xml chứa thông tin về siêu dữ liệu tệp như Tác giả, Ngày sửa đổi lần cuối, v.v.
```
<meta:creation-date>2003-09-10T15:31:11</meta:creation-date>
<dc:creator>Daniel Carrera</dc:creator>
<dc:date>2005-06-29T22:02:06</dc:date>
<dc:language>es-ES</dc:language>
<meta:document-statistic
      table-count="6" object-count="0"
      page-count="59" paragraph-count="676"
      image-count="2" word-count="16701"
      character-count="98757"/>
```
### Settings.xml

Tệp `settings.xml` bao gồm các cài đặt cấp độ tài liệu như hệ số thu phóng và vị trí con trỏ.

## Người giới thiệu ##

* [Đặc tả OpenDocument 1.2](https://www.oasis-open.org/standards#opendocumentv1.2)
* [OpenDocument - Bởi Wikipedia](https://vi.wikipedia.org/wiki/OpenDocument)

