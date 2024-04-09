{
  "date" : "2023-05-17",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Tìm hiểu về định dạng tệp NMONEY và các API có thể tạo và mở tệp NMONEY.",
  "title" :"Tệp NMONEY - Định dạng tệp tài khoản Denaro",
  "linktitle" : "NMONEY",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2023-05-17"
}

## Tệp NMONEY là gì?

Tệp NMONEY là tệp cơ sở dữ liệu lưu trữ dữ liệu tài chính chứa bản ghi theo dõi các giao dịch tài chính. Nó được phát triển bởi Nickvision và được sử dụng trong phần mềm Nickvision Denaro, một ứng dụng phần mềm tài chính cá nhân. Dữ liệu được lưu trữ bên trong tệp NOMONEY bao gồm thông tin giao dịch tín dụng và ghi nợ vào tài khoản.

Các tệp NOMONEY có thể được mở bằng ứng dụng [Github](https://github.com/NickvisionApps/Denaro).

## Giới thiệu về phần mềm Denaro

Denaro ban đầu được phát triển bởi [Nickvision](https://nickvision.org/) dưới dạng một sản phẩm sau đó được chuyển đổi thành ứng dụng phần mềm nguồn mở được lưu trữ trên [Github](https://github.com/NickvisionApps/Denaro) . Kể từ đó ứng dụng chỉ được sửa đổi và cập nhật trên Github. Ứng dụng được phát triển bằng C# trong giao diện người dùng Windows với Windows App SDK (WinUI 3 tại thời điểm này).

### Tính năng được cung cấp bởi Denaro

* Quản lý đồng thời nhiều tài khoản với giao diện tab phổ biến và quen thuộc nhất
* Lọc giao dịch theo loại, nhóm hoặc ngày
* Lặp lại các giao dịch như hóa đơn xảy ra hàng tháng
* Chuyển tiền từ tài khoản này sang tài khoản khác
* Xuất dữ liệu từ tài khoản dưới dạng tệp CSV và nhập tệp CSV, OFX hoặc QIF để thêm giao dịch vào tài khoản

## Định dạng tệp Denaro - Thông tin thêm

Các tệp Denaro được lưu vào đĩa ở định dạng tệp nhị phân. Dữ liệu tài chính được lưu trữ dưới dạng tệp cơ sở dữ liệu ở định dạng tệp **.SQLITE3**. SQLITE là một tệp cơ sở dữ liệu SQL nhẹ được tạo bằng phần mềm SQLite. Nó cung cấp công cụ cơ sở dữ liệu khép kín có khả năng cung cấp cơ sở dữ liệu đầy đủ tính năng và có độ tin cậy cao. Các tệp cơ sở dữ liệu SQLite có thể được sử dụng để chia sẻ nội dung phong phú giữa các hệ thống bằng cách trao đổi các tệp này qua mạng. Các liên kết SQLite tồn tại cho các ngôn ngữ lập trình như C, [C#](/vi/programming/cs/), [C++](/vi/programming/cpp/), [Java](/vi/programming/java/), [PHP](/vi/programming/php/) và nhiều thứ khác.

## Người giới thiệu

* [Nickvision](https://nickvision.org/)
* [NIckVision - Github](https://github.com/NickvisionApps/Denaro)

