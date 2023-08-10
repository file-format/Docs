{
  "date" : "2021-04-21",
  "keywords" :[ "tệp hạt đậu", "định dạng tệp hạt đậu", "tệp hạt đậu là gì", "tệp", "ví dụ hạt đậu", "phần mở rộng tệp hạt đậu","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PEA - Định dạng tệp lưu trữ PeaZip",
  "description":"Tìm hiểu về định dạng tệp PEA và API có thể tạo và mở tệp PEA.",
  "linktitle" : "PEA",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-21"
}

## Tệp PEA là gì?

Tệp có phần mở rộng .pea, viết tắt của Pack, Encrypt và Authenticate, là tệp lưu trữ [zip](/vi/compression/zip/) được tạo bằng ứng dụng phần mềm lưu trữ [PeaZip](https://peazip.github.io/). Nó có tính năng nén và đầu ra nhiều khối lượng, đồng thời cung cấp mô hình bảo mật linh hoạt thông qua Mã hóa và mật mã được xác thực. Điều này cung cấp cả quyền riêng tư và xác thực dữ liệu. Tiện ích PeaZip có sẵn dưới dạng công cụ nguồn mở có thể được biên dịch cho các hệ điều hành khác nhau theo yêu cầu.

## Định dạng tệp PEA

[Thông số định dạng tệp PEA](https://peazip.github.io/pea_help.pdf) được cung cấp công khai để nhà phát triển tham khảo. Lưu trữ PEA là các tệp nhị phân với mô hình bảo mật linh hoạt và kiểm tra tính toàn vẹn dự phòng, từ tổng kiểm tra đến hàm băm mạnh về mặt mật mã. Điều này xác định ba cấp độ giao tiếp khác nhau để kiểm soát:

* Luồng - luồng dữ liệu đầu ra thực tế được hình thành bởi nhiều tệp đầu vào và có thể được ghi vào nhiều ổ đĩa đầu ra
* Đối tượng - các tệp và thư mục đầu vào được gửi tới kho lưu trữ .pea
* Tập - tệp lưu trữ đầu ra có thể được kéo dài theo kích thước do người dùng xác định

Mỗi một trong số này là tùy chọn và có thể được kết hợp theo yêu cầu của người dùng. Định dạng tệp PEA có thể lưu trữ một luồng chứa các đối tượng không giới hạn. Mỗi luồng có kích thước tối đa 2^64 byte.

Các tệp PEA cung cấp tùy chọn kiểm tra tính toàn vẹn và mã hóa được xác thực bằng AES ở chế độ EAX hoặc HMAC, hoặc Twofish và Serpent ở chế độ EAX.

### Tiêu đề Lưu trữ PEA

Tiêu đề lưu trữ là 10 byte và được cấu trúc như sau.

|Byte|Mô tả|
---|---|
|1 | Trường byte ma thuật để định hướng định dạng tệp: $EA|
|1 | Số phiên bản|
|1 | Số sửa đổi|
|1 | Sơ đồ điều khiển âm lượng|
|1 | Khai báo hệ điều hành nơi xây dựng luồng|
|1 | Khai báo mã hóa ngày giờ của hệ điều hành|
|1 | Khai báo mã ký tự tên đối tượng|
|1 | Khai báo loại CPU (được mã hóa bằng 7 bit) và tuổi thọ (tính bằng msb)|
|1 | Dành để sử dụng trong tương lai|

## Người giới thiệu

* [Thông số định dạng tệp PEA](https://peazip.github.io/pea_help.pdf)
* [Định dạng tệp PEA](https://peazip.github.io/pea-file-format.html#.pea_specifications)

