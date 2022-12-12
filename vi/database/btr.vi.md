{
  "date" : "2021-09-06",
  "keywords" :[ "btr", "extension", "file", "file format", "Database File Type", "Database File Format", "Btrieve Database" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Tìm hiểu về định dạng tệp BTR và API có thể tạo và mở tệp BTR.",
  "title" :"BTR - Truy xuất tệp cơ sở dữ liệu",
  "linktitle" : "BTR",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-09-06"
}

## Tệp BTR là gì?

Tệp có phần mở rộng .btr là tệp cơ sở dữ liệu được tạo bởi ứng dụng cơ sở dữ liệu giao dịch [Btrieve](https://www.actian.com/). Không giống như các hệ thống quản lý cơ sở dữ liệu quan hệ (RBMS), Btrieve dựa trên Phương thức truy cập tuần tự được lập chỉ mục (ISAM), đây là một cách lưu trữ dữ liệu để truy xuất nhanh. Tệp BTR lưu trữ một tập hợp các bản ghi và được sử dụng để tạo báo cáo theo yêu cầu. Các tệp BTR có thể được mở bằng Trình quản lý cơ sở dữ liệu Btrieve phổ biến, Tiện ích bảo trì PSQL phổ biến và Trình xem BTRIEVE của phần mềm huyền thoại.

## Cấu trúc tệp BTR - Thông tin thêm

Cấu trúc dữ liệu bên trong và căn chỉnh của từng byte trong cấu trúc của tệp BTR không được cung cấp công khai. Tuy nhiên, Btriev
cung cấp [API Btrieve](https://docs.actian.com/psql/PSQLv13/index.html#page/btrieveapi%2Fbtrintro.htm) có thể dùng để đọc thông tin từ tệp BTR. Nó tương thích với các ngôn ngữ lập trình và môi trường phát triển sau đây.

* Embarcadero C/C++
* Embarcadero Delphi
* GNU C/C++
* COBOL lấy nét vi mô
*Microsoft Visual Basic
*Microsoft Visual C++
* Watcom C/C++

Truy xuất dữ liệu từ tệp BTR phụ thuộc vào tệp DDF được liên kết với nó. Nếu không có DDF, sẽ không dễ dàng truy xuất thông tin từ một tệp như vậy.

## Người giới thiệu

* [Btrieve - Wikipedia](https://en.wikipedia.org/wiki/Btrieve)
* [Giới thiệu về API Btreive](https://docs.actian.com/psql/PSQLv13/index.html#page/btrieveapi%2Fbtrintro.htm)

