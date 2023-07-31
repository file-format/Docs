{
  "date" : "2021-05-03",
  "keywords" :[ "SDF", "tệp sdf","tệp sdf là gì","cách mở tệp sdf", "phần mở rộng", "tệp", "định dạng tệp sdf", "Loại tệp cơ sở dữ liệu", "Định dạng tệp cơ sở dữ liệu ", "Tệp cơ sở dữ liệu" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Tìm hiểu về định dạng tệp SDF và các API có thể tạo và mở tệp SDF.",
  "title" :"SDF - Tệp cơ sở dữ liệu nhỏ gọn của máy chủ SQL",
  "linktitle" : "SDF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-05-03"
}

## Tệp SDF là gì?
Tệp có phần mở rộng .sdf chứa cơ sở dữ liệu Microsoft SQL Server Compact (SQL CE) còn được gọi là cơ sở dữ liệu quan hệ nhỏ gọn; do Microsoft sản xuất cho các ứng dụng dành cho thiết bị di động và máy tính để bàn. Nó hỗ trợ cả hệ điều hành 32 và 64 bit và toàn bộ nội dung của cơ sở dữ liệu được bao gồm trong một tệp SDF duy nhất và có thể chiếm hơn 4GB dung lượng ổ đĩa. Vì mục đích bảo mật, tệp .sdf có thể được mã hóa bằng mã hóa 128-bit. Thời gian chạy SQL CE giải quyết quyền truy cập song song của nhiều người dùng vào tệp .sdf. Có thể sao chép tệp SDF qua **QuickOnce** hoặc đơn giản là có thể sao chép tệp tới đích để triển khai hệ thống.

## Định dạng tệp SDF
Tệp SDF chứa cơ sở dữ liệu thường được gọi là cơ sở dữ liệu quan hệ nhỏ gọn. Tệp SDF chứa tất cả thông tin liên quan đến cơ sở dữ liệu và SQL Server Compact là một công cụ cơ sở dữ liệu miễn phí và nhẹ, được sử dụng để quản lý các tệp .sdf. Kích thước tệp .sdf không được vượt quá giới hạn 4 GB kích thước. Các tệp SDF không lưu trữ thông tin về các thủ tục, trình kích hoạt hoặc chế độ xem được lưu trữ. Các ứng dụng sử dụng cơ sở dữ liệu SQL CE không cần chỉ định đường dẫn đến tệp SDF trong chuỗi kết nối ADO.NET, thay vào đó, nó có thể được đề cập là |DataDirectory|\database_name.sdf, xác định thư mục dữ liệu được xác định trong bảng kê khai hợp ngữ cho ứng dụng
Quy ước đặt tên .sdf là tùy chọn và bất kỳ phần mở rộng nào cũng có thể được sử dụng để lưu tệp. Thiết lập mật khẩu cho tệp cơ sở dữ liệu là một bước tùy chọn. Để nén hoặc sửa chữa cơ sở dữ liệu, tệp phải được lưu với tùy chọn **cơ sở dữ liệu được nén/sửa chữa**.

## Người giới thiệu

* [SQL Server Compact - Wikipedia](https://en.wikipedia.org/wiki/SQL_Server_Compact)
* [Sử dụng SQL Server Compact cho các ứng dụng web ASP.NET](https://learn.microsoft.com/en-us/previous-versions/aspnet/ms247257(v=vs.110))


