{
  "date" : "2020-08-20",
  "keywords" :[ "tệp cff", "định dạng tệp cff", "tệp cff là gì", "tệp", "ví dụ cff", "phần mở rộng tệp cff","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CFF - Định dạng tệp phông chữ nhỏ gọn",
  "description":"Tìm hiểu về Định dạng tệp CFF và API để tạo và mở tệp CFF.",
  "linktitle" : "CFF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-21"
}

## Tệp CFF là gì?

Tệp có phần mở rộng .cff là Định dạng Phông chữ Nhỏ gọn và còn được gọi là Loại PostScript 1 hoặc CIDFont. CFF hoạt động như một thùng chứa để lưu trữ nhiều phông chữ cùng nhau trong một đơn vị duy nhất được gọi là Bộ phông chữ. Thiết kế của phông chữ CFF cho phép nhúng mã ngôn ngữ PostScript cho phép định dạng có tính linh hoạt và khả năng mở rộng bổ sung để sử dụng với môi trường máy in. Có thể mở và chuyển đổi các tệp phông chữ CFF bằng cách sử dụng các API chẳng hạn như [Aspose.Font](https://products.aspose.com/font).

## Định dạng tệp CFF

Các tệp CFF là các tệp nhị phân chứa bố cục dữ liệu có cấu trúc, đã xác định các loại dữ liệu, tiêu đề, tổ chức glyph và từ điển bảng. Bạn có thể tìm thêm chi tiết về những điều này trong [thông số định dạng phông chữ nhỏ gọn](https://docs.microsoft.com/en-us/typography/opentype/spec/cff).

### Bố cục dữ liệu
Bố cục dữ liệu của định dạng tệp CFF như hình bên dưới.

|Bài viết|Bình luận|
---|---|
|Tiêu đề|–|
|NameINDEX|–|
|CHỈ SỐ DICT hàng đầu|–|
|Chuỗi INDEX|–|
|CHỈ SỐ Subr toàn cầu|–|
|Mã hóa–Bộ ký tự|–|
|FDSelect|CIDFons only|
|Chuỗi ký tự INDEX|mỗi phông chữ|
|Phông chữ DICT INDEX|mỗi phông chữ, chỉ CIDFonts|
|DICT riêng|mỗi phông chữ|
|CHỈ SỐ Subr cục bộ|mỗi phông chữ hoặc mỗi DICT riêng cho CIDFonts|
|Thông báo Bản quyền và Thương hiệu|–|

### Loại dữ liệu

Các kiểu dữ liệu CFF như trong bảng sau.

|Tên|Phạm vi|Mô tả|
---|---|---|
|Card8|0 –255|số không dấu 1 byte|
|Thẻ16|0 – 65535|số không dấu 2 byte|
|Độ lệch|khác nhau|Độ lệch 1, 2, 3 hoặc 4 byte (được chỉ định bởi trường OffSize)|
|OffSize|1–4|Số không dấu 1 byte chỉ định kích thước của một hoặc nhiều trường Offset|
|SID|0 – 64999|mã định danh chuỗi 2 byte|

### Tiêu đề

Dữ liệu nhị phân bắt đầu bằng tiêu đề có định dạng được hiển thị trong bảng sau.

|Loại|Tên|Mô tả|
---|---|---|
|Card8|major|Định dạng phiên bản chính (bắt đầu từ 1)|
|Card8|minor|Định dạng phiên bản nhỏ (bắt đầu từ 0)|
|Card8|hdrSize| Kích thước tiêu đề (byte)|
|OffSize|offSize|Kích thước offset (0) tuyệt đối|

## Người giới thiệu

* [Bảng định dạng phông chữ nhỏ gọn](https://docs.microsoft.com/en-us/typography/opentype/spec/cff)
* [Định dạng tệp CFF](https://adobe-type-tools.github.io/font-tech-notes/pdfs/5176.CFF.pdf)
* [Bộ biểu đồ CFF2](https://docs.microsoft.com/en-us/typography/opentype/spec/cff2charstr)

