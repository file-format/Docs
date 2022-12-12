{
  "date" : "2019-10-11",
  "keywords" :["xoml", "Tệp", "Phần mở rộng", "Định dạng tệp", "Phần mở rộng tệp", "Ngôn ngữ đánh dấu đối tượng mở rộng"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XOML - Định dạng tệp quy trình làm việc của Windows",
  "description":"Tìm hiểu về định dạng tệp XOML và API có thể tạo và mở tệp XOML.",
  "linktitle" : "XOML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Tệp XOML là gì?

XOML là từ viết tắt của Extensible Object Markup Language và là định dạng tuần tự hóa cho các đối tượng quy trình công việc của Windows Workflow Foundation. Dựa trên **[XAML](/vi/web/xaml/)**, nó chủ yếu được sử dụng để tạo giao diện người dùng ở dạng **[XML](/vi/web/xml/)** đơn giản. Chúng được sử dụng để khai báo quy trình làm việc cho giao diện người dùng và được biên dịch cùng với tệp riêng chứa logic triển khai. Nó chứa một cấu trúc dựa trên cây xác định một nút quy trình công việc gốc, các phần tử phụ lồng nhau và các đoạn mã được nhúng. Khi một quy trình công việc mới được tạo bằng Visual Studio cho .NET, nó có một tùy chọn để bạn chọn xem nó sẽ ở định dạng Mã hay định dạng Mã được phân tách. Trong trường hợp bạn chọn cái sau, IDE sẽ tạo hai tệp cho bạn; một ở định dạng XOML (bao gồm cài đặt và bố cục quy trình công việc) và một ở định dạng [.CS](/vi/programming/cs/)/[.VB](/vi/programming/vb/) nơi chứa mã lập trình.

