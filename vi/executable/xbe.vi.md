{
  "date" : "2021-08-31",
  "keywords" :[ "tệp xbe", "định dạng tệp xbe", "tệp xbe là gì", "tệp", "ví dụ xbe", "phần mở rộng tệp xbe","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Tìm hiểu về định dạng tệp XBE và các API có thể tạo và mở tệp XBE.",
  "title" :"XBE - Tệp gói ứng dụng iOS",
  "linktitle" : "XBE",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-08-31"
}

## Tệp XBE là gì?
Tệp có phần mở rộng .xbe là một ứng dụng thực thi từ đĩa trò chơi điện tử Xbox. Các tệp XBE là các tệp chính được thực thi trong Hệ thống Xbox và thường không được mở trên máy tính, nhưng nó có thể được mở trên PC bằng chương trình mô phỏng Xbox. Các tệp này thường được tạo bởi các nhà phát triển trò chơi và sau đó được ký bởi Microsoft. Cấu trúc tệp tương tự như tệp Windows PE, nhưng một số thay đổi quan trọng theo cài đặt XBox được áp dụng để làm cho tệp có thể chạy được trên XBox.

## Định dạng tệp XBE
Tệp XBE bao gồm một tiêu đề hình ảnh, một bộ sưu tập các tiêu đề phần, chứng chỉ, dữ liệu lưu trữ cục bộ của luồng, một bộ sưu tập các phiên bản thư viện, Microsoft bitmap và các phần chứa mã và tài nguyên.

### Tiêu đề hình ảnh
Tiêu đề hình ảnh bao gồm thông tin giải thích vị trí của các thành phần khác của tệp thực thi được đặt trong tệp và cách xử lý và tải tệp có thể chạy được.

### Bảng TLS
Bảng TLS bao gồm tất cả thông tin mà XBE cần để thiết lập lưu trữ cục bộ theo luồng đúng cách. Về cơ bản, nó là duy nhất đối với Thư mục TLS được tìm thấy trong các tệp PE32 và có thể được sao chép trực tiếp từ đó. Bảng này có thể bị bỏ qua nếu tệp XBE không sử dụng bất kỳ bộ lưu trữ luồng cục bộ nào và trường tương ứng trong tiêu đề hình ảnh được đặt thành 0.

| Bù đắp | Kích thước | Tên | Mô tả |
--------|--------|--------|------------|
| 0x0000 | 0x0004 | Dữ liệu thô Bắt đầu | Địa chỉ tuyệt đối (nghĩa là không phải RVA) bắt đầu của dữ liệu biến TLS trong hình ảnh chương trình. |
| 0x0004 | 0x0004 | Dữ liệu thô Kết thúc | Địa chỉ tuyệt đối (nghĩa là không phải RVA) của phần cuối dữ liệu biến TLS trong hình ảnh chương trình. |
| 0x0008 | 0x0004 | Địa chỉ của Index | Địa chỉ tuyệt đối (nghĩa là không phải RVA) của biến Chỉ mục TLS. |
| 0x000C | 0x0004 | Địa chỉ gọi lại | Địa chỉ tuyệt đối (nghĩa là không phải RVA) của bảng chức năng gọi lại TLS kết thúc bằng null. |
| 0x0010 | 0x0004 | Kích thước Zero Fill | Số byte sau dữ liệu thô sẽ được đặt thành 0 trong bộ nhớ. |
| 0x0014 | 0x0004 | Đặc điểm | Mô tả sự liên kết. |

### Giấy chứng nhận

Chứng chỉ là bắt buộc đối với mỗi tệp thực thi Xbox có chứa thông tin về tiêu đề:
 


- Thời gian và ngày khi chứng chỉ được tạo
- Mã tiêu đề
- Tên tiêu đề
- ID tiêu đề thay thế
- Các loại phương tiện được phép mà tệp thực thi có thể chạy từ đó (HD, DVD, CD, v.v.)
- Khu vực trò chơi
- Xếp hạng trò chơi
- Số đĩa
- Phiên bản
- Dữ liệu thô của khóa LAN được sử dụng cho Liên kết hệ thống
- Dữ liệu thô của khóa chữ ký (được sử dụng để ký các trò chơi lưu trữ)
- Phím chữ ký thay thế
- Kích thước gốc của giấy chứng nhận
- Tên dịch vụ trực tuyến (không có trong các tệp thực thi sớm)
- Cờ bảo mật thời gian chạy (không có trong các tệp thực thi sớm)
 


### Loại phương tiện được phép
Các loại phương tiện mà tệp thực thi cho phép chạy từ đó. Các giá trị sau được biết đến:
| Loại phương tiện | Giá trị |
---------------------|------------|
| CỨNG_ĐĨA | 0x00000001 |
| DVD_X2 | 0x00000002 |
| DVD_CD | 0x00000004 |
| đĩa | 0x00000008 |
| DVD_5_RO | 0x00000010 |
| DVD_9_RO | 0x00000020 |
| DVD_5_RW | 0x00000040 |
| DVD_9_RW | 0x00000080 |
| dongle | 0x00000100 |
| MEDIA_BOARD | 0x00000200 |
| KHÔNG BẢO MẬT_HARD_DISK | 0x40000000 |
| KHÔNG BẢO MẬT_MODE | 0x80000000 |
| MEDIA_MASK | 0x00FFFFFF |

### Phần
Các phần được thể hiện bằng các tiêu đề phần. Các tiêu đề của phần bắt đầu ngay sau chứng chỉ và chứa thông tin về vị trí của các phần thực trong tệp. Ít nhất hai phần luôn có trong tệp thực thi Xbox:


- .chữ


- .rdata


## Người giới thiệu



* [Xbe - XBox có thể thực thi được](https://xboxdevwiki.net/Xbe)


