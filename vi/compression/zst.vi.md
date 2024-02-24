{
  "date" : "2022-12-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Tệp ZST - Định dạng tệp nén Zstandard",
  "description":"Tìm hiểu về định dạng tệp ZST và các API có thể tạo và mở tệp ZST.",
  "linktitle" : "ZST",
  "menu" : {
    "docs" : {
      "identifier":"compression-zst-vi",
      "parent" : "compression"
}
},
  "lastmod" : "2022-12-26"
}

## Một tập tin ZST là gì?

Tệp ZST là tệp nén được tạo bằng thuật toán nén Zstandard (zstd). Nó là một tệp nén được tạo bằng thuật toán nén không mất dữ liệu. Các tệp ZST có thể được sử dụng để nén các loại tệp khác nhau như cơ sở dữ liệu, hệ thống tệp, mạng và trò chơi. Tiêu chuẩn Z được điều chỉnh bởi [RFC 8878](https://www.rfc-editor.org/rfc/rfc8878) mô tả cơ chế nén tổng thể, loại phương tiện và mã hóa nội dung.

## Định dạng tệp ZST

Các tệp ZST được lưu trữ ở định dạng tệp nén vào đĩa. Cơ chế nén được mô tả bởi RFC 8878 đã lỗi thời RFC 8478.

## Khung ZST

Tệp ZST bao gồm một hoặc nhiều khung. Mỗi khung có thể là khung Zstandard hoặc khung có thể bỏ qua. Khung Zstandard chứa dữ liệu nén, trong khi khung có thể bỏ qua chứa siêu dữ liệu người dùng tùy chỉnh.

### Khung tiêu chuẩn Z

Một khung Zstandard có cấu trúc như sau.

|Trường|Kích thước tính bằng byte|
---|---|
|Số ma thuật |4 byte|
|Frame_Header |2-14 byte|
|Khối dữ liệu |n byte|
|[Thêm dữ liệu_Khối] ||
|[Content_Checksum] |4 byte|

### Khung có thể bỏ qua

Khung có thể bỏ qua cho phép chèn siêu dữ liệu do người dùng xác định vào luồng khung được nối. Cấu trúc của một khung có thể bỏ qua như sau.

|Magic_Number |Frame_Size |Dữ liệu người dùng|
---|---|---|
|4 byte |4 byte |n byte|

## Người giới thiệu ##

* [Nén tiêu chuẩn RFC 8878 Z](https://www.rfc-editor.org/rfc/rfc8878)


