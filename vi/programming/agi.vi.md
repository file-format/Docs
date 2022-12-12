{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Tệp AGI - Định dạng tệp giao diện cổng Asterisk",
  "description":"Tìm hiểu về định dạng tệp AGI với ví dụ và các API có thể tạo và mở tệp AGI.",
  "linktitle" : "AGI",
  "menu" : {
    "docs" : {
      "identifier": "programming-agi",
      "parent" : "programming"
}
},
  "lastmod" : "2022-10-30"
}

## Tệp AGI là gì?

Tệp AGI là tệp tập lệnh được sử dụng bởi hệ thống điện thoại nguồn mở, Asterisk. Nó chứa thông tin có thể được sử dụng để tự động hóa các quy trình và sơ đồ quay số Asterisk. Sử dụng các tệp tập lệnh AGI, các kết nối có thể được thiết lập với cơ sở dữ liệu quan hệ như PostgreSQL hoặc MySQL. Ngoài ra, các tập lệnh AGI cũng có thể được sử dụng để truy cập các tài nguyên bên ngoài khác. Các tập lệnh AGI có thể chuyển quyền kiểm soát của dialplan sang một tập lệnh AGI bên ngoài, cho phép Asterisk thực hiện các tác vụ phức tạp.

## Định dạng tệp AGI - Thông tin khác

Các tệp tập lệnh AGI được lưu dưới dạng tệp văn bản và có thể được mở trong bất kỳ trình soạn thảo văn bản nào để thực hiện thay đổi.

### Mẫu giao tiếp AGI tiêu chuẩn

Tập lệnh AGI tải các biến và giá trị của chúng được Asterisk gửi tới. Một cái nhìn chung của các biến này là như sau.

```
agi_request: test.py
agi_channel: Zap/1-1
agi_language: en
agi_callerid:
agi_context: default
agi_extension: 123
agi_priority: 2
```

Các biến này được theo sau bởi một dòng trống được gửi bởi Asterisk, cho thấy rằng tập lệnh AGI có thể kiểm soát kế hoạch quay số ngay bây giờ.

### Ngôn ngữ lập trình cho các tệp AGI Script

Các tập lệnh AGI thường có thể được viết bằng Perl, [PHP](/vi/programming/php/), [C](/vi/programming/c/), Pascal hoặc Bourne Shell.

## Người giới thiệu

* [Asterisk AGI Script](https://www.oreilly.com/library/view/asterisk-the-future/9780596510480/ch09.html)

