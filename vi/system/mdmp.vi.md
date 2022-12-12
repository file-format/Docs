{
  "date" : "2022-08-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Tệp MDMP - Định dạng tệp kết xuất nhỏ của Windows",
  "description":"Tìm hiểu về định dạng tệp MDMP và API có thể tạo và mở tệp MDMP.",
  "linktitle" : "MDMP",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2022-08-19"
}

## Tệp MDMP là gì?

Tệp MDMP là kết xuất bộ nhớ của ứng dụng trên Microsoft Windows được tạo khi ứng dụng đóng bất thường hoặc gặp sự cố. Nó chứa thông tin và kết xuất dữ liệu có thể được sử dụng để gỡ lỗi nguyên nhân gây ra sự cố. Các tệp MDMP có thể áp dụng trên các ứng dụng được tạo bởi bất kỳ nền tảng nào, chẳng hạn như Java, C++, .NET và các nền tảng khác. Ngoài MDMP,

Các ứng dụng có thể mở tệp MDMP bao gồm Trình gỡ lỗi Microsoft Visual Studio.

## Định dạng tệp MDMP

Các tệp MDMP được lưu dưới dạng tệp nhị phân vào đĩa và có thể được mở bằng trình gỡ lỗi Microsoft Visual Studio. Nó chứa các thông tin sau để giúp xác định lý do cho sự cố.

* Chi tiết về thông báo Dừng, các tham số của nó và dữ liệu khác
* Danh sách các trình điều khiển được nạp
* Bối cảnh bộ xử lý (PRCB) cho bộ xử lý ngừng hoạt động
* Thông tin quy trình và bối cảnh kernel (EPROCESS) cho quy trình đã dừng
* Xử lý thông tin và ngữ cảnh hạt nhân (ETHREAD) cho luồng đã dừng
* Ngăn xếp cuộc gọi chế độ hạt nhân cho luồng đã dừng

Thông tin này giúp tìm hiểu điều gì đã xảy ra, khắc phục sự cố và ngăn sự cố xảy ra lần nữa.

### Phân tích Minidump

Windows yêu cầu tệp hoán trang trên ổ đĩa khởi động để tạo tệp kết xuất bộ nhớ. Tệp hoán trang được tạo trên ổ đĩa khởi động và phải có kích thước ít nhất là 2 megabyte (MB). Tệp kết xuất được tạo khi ứng dụng gặp sự cố. Trong trường hợp xảy ra sự cố thứ hai, tệp kết xuất bộ nhớ nhỏ thứ hai được tạo trong khi tệp kết xuất trước đó được giữ nguyên. Tên của tệp kết xuất là khác biệt để tránh ghi đè.

Windows giữ một danh sách tất cả các tệp kết xuất bộ nhớ trong thư mục %SystemRoot%\Minidump. Bạn có thể phân tích các tệp MDMP bằng cách chạy chúng trong Trình gỡ lỗi Visual Studio như được liệt kê trong các bước bên dưới.

## Làm cách nào để mở tệp MDMP trong Visual Studio?

Có thể sử dụng các bước sau để mở tệp MDMP trong Visual Studio.

* Trong Visual Studio, từ menu File, chọn Open | Sụp đổ .
* Điều hướng đến tệp kết xuất mà bạn muốn mở.
* Chọn Mở.

## Tài liệu tham khảo

* [Cách đọc tệp kết xuất bộ nhớ nhỏ được tạo bởi Windows nếu xảy ra sự cố](https://docs.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump -tập tin)

