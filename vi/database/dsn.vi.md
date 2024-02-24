{
  "date" : "2023-01-17",
  "keywords" : [ "DSN", "what is a DSN file", "extension", "file", "file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "Tìm hiểu về định dạng tệp DSN và các API có thể tạo và mở tệp DSN.",
  "title" : "Định dạng tệp DSN - Tệp tên nguồn cơ sở dữ liệu",
  "linktitle" : "DSN",
  "menu" : {
    "docs" : {
      "identifier":"database-dsn-vi",
      "parent" : "database"
}
},
  "lastmod" : "2020-01-17"
}

## Tệp DSN là gì?

DSN là viết tắt của Tên nguồn dữ liệu và đây là định dạng tệp được sử dụng để lưu trữ thông tin kết nối cơ sở dữ liệu. Các tệp DSN thường được sử dụng cùng với ODBC (Kết nối cơ sở dữ liệu mở) và cho phép truy cập dễ dàng vào cơ sở dữ liệu cụ thể bằng cách cung cấp thông tin cần thiết để kết nối với nó, chẳng hạn như tên máy chủ, tên người dùng và mật khẩu. Tệp thường ở dạng văn bản thuần túy và có thể được tạo và chỉnh sửa bằng trình soạn thảo văn bản. Nó có thể được sử dụng trên nhiều hệ điều hành khác nhau như Windows, Linux và Mac.

## Làm cách nào để tạo tập tin DSN?

Phương pháp tạo tệp DSN có thể khác nhau tùy theo hệ điều hành và các công cụ có sẵn. Các bước sau đây cung cấp cái nhìn tổng quan chung về quy trình tạo tệp DSN trên hệ thống Windows.

1. Mở Quản trị viên nguồn dữ liệu ODBC bằng cách tìm kiếm Nguồn dữ liệu ODBC trong menu bắt đầu.
2. Chọn tab DSN hệ thống và nhấp vào nút Thêm.
3. Chọn trình điều khiển thích hợp cho cơ sở dữ liệu bạn muốn kết nối và nhấp vào Hoàn tất.
4. Điền thông tin cần thiết để kết nối với cơ sở dữ liệu, chẳng hạn như tên máy chủ, tên người dùng và mật khẩu.
5. Nhấp vào OK để lưu tệp DSN.

Ngoài ra, bạn có thể tạo tệp DSN theo cách thủ công bằng cách tạo tệp văn bản thuần túy có phần mở rộng .dsn và nhập thông tin kết nối cần thiết theo định dạng:

```
[ODBC]
DRIVER=driver_name
SERVER=server_name
DATABASE=database_name
UID=username
PWD=password
```

Sau đó, bạn có thể sử dụng đường dẫn của tệp này làm DSN trong mã/tập lệnh của mình để kết nối với cơ sở dữ liệu.

## Các chương trình mở tệp DSN

Tệp DSN là một tệp văn bản thuần túy lưu trữ thông tin được sử dụng để kết nối với cơ sở dữ liệu, chẳng hạn như tên máy chủ, tên người dùng và mật khẩu. Nó thường được sử dụng cùng với ODBC (Kết nối cơ sở dữ liệu mở) để cung cấp quyền truy cập dễ dàng vào cơ sở dữ liệu cụ thể.

Để mở và xem nội dung của tệp DSN, bạn có thể sử dụng bất kỳ trình soạn thảo văn bản nào như Notepad, Sublime Text, Atom, v.v. Các chương trình này sẽ cho phép bạn mở tệp DSN và xem thông tin kết nối được lưu trữ trong đó.

Tuy nhiên, để sử dụng tệp DSN để kết nối với cơ sở dữ liệu và thực hiện các thao tác như CHỌN, CHÈN, CẬP NHẬT, XÓA, v.v., một chương trình có hỗ trợ ODBC, chẳng hạn như ngôn ngữ lập trình như Python, Java, C# hoặc công cụ quản lý cơ sở dữ liệu như Microsoft Access , SQL Server Management Studio là bắt buộc. Các chương trình này có thể sử dụng thông tin trong tệp DSN để kết nối với cơ sở dữ liệu và thực hiện thao tác mong muốn.

## Người giới thiệu

* [DSN (Tên nguồn dữ liệu) là gì?](https://support.microsoft.com/en-us/topic/what-is-a-dsn-data-source-name-ae9a0c76-22fc-8a30- 606e-2436fe26e89f)



