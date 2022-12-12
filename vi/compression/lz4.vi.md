{
  "date" : "2021-04-08",
  "keywords" :[ "tệp lz4", "định dạng tệp lz4", "tệp lz4 là gì", "tệp", "ví dụ lz4", "phần mở rộng tệp lz4","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Định dạng tệp nén LZ4 - LZ4",
  "description":"Tìm hiểu về định dạng tệp LBR và các API có thể tạo và mở tệp LZ4.",
  "linktitle" : "LZ4",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-19"
}

## Tệp LZ4 là gì?

Tệp có phần mở rộng .lz4 là tệp lưu trữ nén được tạo bằng các ứng dụng/tiện ích hỗ trợ nén [LZ4](https://en.wikipedia.org/wiki/LZ4_(compression_algorithm)). Thuật toán LZ4 tập trung vào sự đánh đổi giữa tốc độ và tỷ lệ nén. Các kho lưu trữ LZ4 đã nén có thể được tạo bằng tiện ích dòng lệnh LZ4 và có thể được giải nén bằng tiện ích tương tự.

## Định dạng tệp LZ4

Định dạng tệp LZ4, dựa trên thuật toán nén LZ4, độc lập với loại CPU, hệ điều hành, hệ thống tệp và bộ ký tự. Nó phù hợp để nén tệp và nén phát trực tuyến bằng thuật toán LZ4. Quá trình triển khai ban đầu của định dạng LZ4 được thực hiện bằng ngôn ngữ [C](/vi/programming/c/) bởi Yann Collet vào năm 2011 và có sẵn để nhà phát triển tham khảo trên [Github](https://github.com/lz4/lz4) .

### Định dạng khung LZ4

Cấu trúc chung của định dạng tệp LZ4 như hình bên dưới.

|MagicNb|F. Mô tả| Khối|(...)|Dấu cuối |C. Tổng kiểm tra|
---|---|---|---|---|---|
|4 byte| 3-15 byte||| 4 byte| 0-4 byte|

#### Con số kỳ diệu

4 byte, định dạng cuối nhỏ. Giá trị : 0x184D2204

#### Bộ mô tả khung

Bộ mô tả khung bao gồm 3 t0 15 byte và là phần quan trọng nhất của thông số kỹ thuật. Cùng với nhau, các trường Magic_Number và Frame_Descriptor được gọi là Tiêu đề khung LZ4 và kích thước của nó thay đổi trong khoảng từ 7 đến 19 byte. Nó như hình bên dưới.

|FLG| BD| (Kích thước nội dung)| (ID từ điển)| HC|
---|---|---|---|---|
|1 byte| 1 byte| 0 - 8 byte| 0 - 4 byte| 1 byte|

#### Khối dữ liệu

Mỗi khối dữ liệu tuân theo thứ tự sau.

|Kích thước khối| dữ liệu| (Tổng kiểm tra khối)|
---|---|---|
|4 byte| |0 - 4 byte|

#### Dấu cuối

Luồng khối kết thúc khi khối dữ liệu cuối cùng được theo sau bởi giá trị 32 bit 0x00000000.

#### Tổng kiểm tra nội dung

Content_Checksum xác minh tính hợp lệ của nội dung được giải mã chính xác và được thực hiện bằng kết quả của thuật toán xxHash-32. Nó xác nhận kết quả truyền thành công của tất cả các khối theo đúng thứ tự và không có bất kỳ lỗi nào.

## Người giới thiệu

* [Định dạng khung LZ4](https://github.com/lz4/lz4/blob/dev/doc/lz4_Frame_format.md)
* [Thuật toán nén LZ4 - Wikipedia](https://en.wikipedia.org/wiki/LZ4_(compression_algorithm))

