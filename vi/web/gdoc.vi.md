{
  "date" : "2022-01-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Tệp GDOC - Lối tắt Google Tài liệu",
  "description":"Tìm hiểu về tệp GDOC là gì và các API có thể tạo và mở tệp GDOC.",
  "linktitle" : "GDOC",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-01-23"
}

## Tệp GDOC là gì?

Tệp GDOC là tệp lối tắt trỏ đến một tệp nằm trên Google Drive, một dịch vụ lưu trữ tài liệu dựa trên đám mây. Khi ứng dụng khách Google Drive được cài đặt trên máy tính và tài liệu được tạo bên trong nó, ổ đĩa sẽ tạo tài liệu trong bộ lưu trữ đám mây trực tuyến và ghi [URL](/vi/web/url/) của tài liệu này vào tệp GDOC trong Google cục bộ Thư mục ổ đĩa. Khi nhấp đúp vào tệp lối tắt này, trình duyệt web mặc định sẽ mở tài liệu từ vị trí [URL](/vi/web/url/). Nếu tệp lối tắt này bị di chuyển ra khỏi thư mục này, liên kết tới tài liệu trực tuyến sẽ bị hỏng.

## Định dạng tệp GDOC - Thông tin khác

Tệp GDOC chứa lối tắt đến tài liệu trực tuyến được viết ở định dạng tệp [JSON](/vi/web/json/). Trình duyệt mở tệp GDOC sẽ đọc thông tin URL và mở tài liệu được liên kết để hiển thị miễn là người dùng đã đăng nhập vào tài khoản Google này, nơi tài liệu được lưu trữ. Các tệp GDOC không chứa nội dung của tài liệu.

### Ví dụ về tệp GDOC

Tệp GDOC có thể được mở trong trình soạn thảo văn bản và nội dung của nó trông như sau.

```
{"url": "https://docs.google.com/a/test.com/spreadsheet/ccc?key=01234567898765432123456789&usp=docslist_api", "resource_id": "spreadsheet:0A12345B678HJK9TZPL9078767"}
```

Có thể thấy, nội dung được định dạng trong JSON có URL của tài liệu và ID tài liệu được liên kết.

## Người giới thiệu

* [Google Tài liệu không mở được tệp gdoc hoặc docx](https://support.google.com/docs/thread/8408691/google-docs-not-opening-either-gdoc-or-docx-files?hl=vi )

