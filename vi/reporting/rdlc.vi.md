{
  "date" : "2021-03-02",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RDLC - Ngôn ngữ định nghĩa báo cáo phía máy khách",
  "keywords" :[ "rdlc", "ngôn ngữ định nghĩa báo cáo", "định dạng mkv", "XSD", "phía máy khách ngôn ngữ định nghĩa báo cáo"],
  "description":"Tìm hiểu về định dạng tệp RDLC là biểu diễn XML của định nghĩa báo cáo Dịch vụ báo cáo SQL Server.",
  "linktitle" : "RDLC",
  "menu" : {
    "docs" : {
      "parent" : "reporting"
}
},
  "lastmod" : "2021-03-02"
}

## Tệp RDLC là gì? ##

RDLC là viết tắt của Phía máy khách ngôn ngữ định nghĩa báo cáo. Trên thực tế, đây là phần mở rộng của tệp báo cáo được tạo bằng công nghệ báo cáo của Microsoft. Phiên bản SQL Server 2005 của Report Designer được sử dụng để tạo các tệp này. Điều khiển **ReportViewer** ở phía máy khách có thể thực thi trực tiếp các báo cáo RDLC.

## Tệp RDL VS RDLC
|.rdl tập tin |.rdlc tập tin|
---|---|
|Tệp RDL được tạo bởi phiên bản Trình thiết kế báo cáo SQL Server 2005|Tệp RDLC được tạo bởi phiên bản Visual Studio 2005 của Trình thiết kế báo cáo|
|Nó được sử dụng trong SQL Server Reporting Services|Nó được sử dụng trong Visual Studio|
|Đó là báo cáo từ xa|Đó là báo cáo cục bộ|
|Cần một phiên bản Dịch vụ Báo cáo để chạy nó|Không cần một phiên bản Dịch vụ Báo cáo|

## Tạo tệp định nghĩa báo cáo khách hàng (.rdlc)
Điều khiển ReportViewer được sử dụng để chạy các tệp định nghĩa báo cáo máy khách (.rdlc) bằng cách sử dụng khả năng xử lý tích hợp sẵn của điều khiển. Máy khách báo cáo rằng bạn chạy trong chế độ xử lý cục bộ có thể được tạo dễ dàng trong dự án ứng dụng của bạn. Sau đây là các cách tiếp cận để tạo báo cáo:

- Sử dụng **Trình hướng dẫn báo cáo** để tạo định nghĩa báo cáo khách hàng mới (.rdlc).

- Tạo tệp định nghĩa báo cáo khách hàng (.rdlc) mới bằng cách sử dụng Visual Studio.

- Tạo định nghĩa báo cáo theo chương trình.


Bạn chỉ có thể xem trước báo cáo bằng cách chạy nó trong điều khiển **ReportViewer**. Xin lưu ý rằng bạn có thể mở và chỉnh sửa định nghĩa báo cáo bất kỳ lúc nào, sau đó xây dựng hoặc triển khai ứng dụng để kiểm tra kết quả.

## Người giới thiệu ##

- [Tạo tệp định nghĩa báo cáo khách hàng (.rdlc)](https://learn.microsoft.com/en-us/previous-versions/visualstudio/visual-studio-2010/ms252067(v=vs.100))

