{
"ngày": "2023-09-05",
  "keywords": [
"máy bay phản lực",
"tập tin máy bay phản lực",
"tập tin máy bay phản lực là gì",
"Tệp cơ sở dữ liệu JET Microsoft Access",
"cách mở tập tin máy bay phản lực",
"tài liệu",
"phần mở rộng tập tin máy bay phản lực",
"sự mở rộng"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Định dạng tệp JET - Tệp cơ sở dữ liệu Microsoft JET",
  "description":"Tìm hiểu về định dạng JET và các API có thể tạo và mở tệp JET.",
  "linktitle": "JET",
  "menu": {
    "docs": {
      "identifier": "database-jet",
      "parent": "database"
}
},
"lastmod": "2023-09-05"
}

## Một tập tin JET là gì?

Tệp cơ sở dữ liệu JET, còn được gọi là tệp cơ sở dữ liệu Microsoft Access, là định dạng tệp được sử dụng bởi Microsoft Access, một hệ thống quản lý cơ sở dữ liệu phổ biến (DBMS). JET là viết tắt của Joint Engine Technology, tên ban đầu của công cụ cơ sở dữ liệu mà Microsoft Access đã sử dụng. Các phiên bản Access sau này đã sử dụng các công cụ cơ sở dữ liệu khác nhau nhưng thuật ngữ "cơ sở dữ liệu JET" vẫn thường được sử dụng để chỉ cơ sở dữ liệu Access.

Dưới đây là một số điểm chính về tệp cơ sở dữ liệu JET:

- **Phần mở rộng tệp:** Các tệp cơ sở dữ liệu JET thường có phần mở rộng tệp là ".mdb" cho các phiên bản Access cũ hơn (Access 2003 trở về trước) và ".accdb" cho các phiên bản mới hơn (Access 2007 trở về trước). Tệp ".mdb" sử dụng công cụ cơ sở dữ liệu JET cũ hơn, trong khi tệp ".accdb" sử dụng công nghệ ACE (Access Database Engine) mới hơn.

- **Cơ sở dữ liệu quan hệ:** Cơ sở dữ liệu JET là cơ sở dữ liệu quan hệ, nghĩa là chúng lưu trữ dữ liệu trong các bảng có mối quan hệ xác định giữa chúng. Người dùng có thể tạo, sửa đổi và truy vấn dữ liệu bằng SQL (Ngôn ngữ truy vấn có cấu trúc) hoặc thông qua giao diện đồ họa Access.

- **Lưu trữ dữ liệu:** Cơ sở dữ liệu JET có thể lưu trữ nhiều loại dữ liệu, bao gồm văn bản, số, ngày tháng, hình ảnh, v.v. Họ cũng có thể xử lý các cấu trúc dữ liệu phức tạp và mối quan hệ giữa các bảng.

- **Truy cập nhiều người dùng:** Cơ sở dữ liệu JET hỗ trợ quyền truy cập nhiều người dùng, cho phép nhiều người dùng làm việc với cơ sở dữ liệu cùng một lúc, mặc dù có thể có những hạn chế về khả năng mở rộng và hiệu suất đối với các ứng dụng quy mô lớn.

- **Tích hợp:** Cơ sở dữ liệu Access có thể được tích hợp với các ứng dụng Microsoft Office khác như Excel và Outlook, giúp người dùng thuận tiện trao đổi dữ liệu giữa các chương trình khác nhau.

## Thông tin về cơ sở dữ liệu JET

**Lịch sử động cơ JET:**

Công cụ cơ sở dữ liệu JET (Công nghệ động cơ chung) ban đầu được Microsoft phát triển vào đầu những năm 1990 để sử dụng trong Microsoft Access. Công cụ này được thiết kế để trở thành một giải pháp cơ sở dữ liệu nhẹ, hướng đến máy tính để bàn, có thể được tích hợp vào nhiều sản phẩm khác nhau của Microsoft.

**Các thành phần của Cơ sở dữ liệu JET**

- **Bảng:** Cơ sở dữ liệu JET lưu trữ dữ liệu trong bảng, là tập hợp các bản ghi được sắp xếp thành hàng và cột.
- **Truy vấn:** Người dùng có thể tạo truy vấn để trích xuất, lọc và thao tác dữ liệu từ các bảng bằng SQL (Ngôn ngữ truy vấn có cấu trúc).
- **Biểu mẫu:** Access cung cấp công cụ thiết kế biểu mẫu cho phép người dùng tạo biểu mẫu hiển thị và nhập dữ liệu tùy chỉnh.
- **Báo cáo:** Người dùng có thể tạo báo cáo chuyên nghiệp từ dữ liệu được lưu trữ trong cơ sở dữ liệu.
- **Macro và VBA:** Người dùng có thể tự động hóa các tác vụ và thêm chức năng tùy chỉnh bằng cách sử dụng macro hoặc bằng cách viết mã VBA.

**Loại dữ liệu**

Cơ sở dữ liệu JET hỗ trợ nhiều loại dữ liệu, bao gồm:

- **Văn bản:** Để lưu trữ các ký tự chữ và số.
- **Số:** Dành cho giá trị số.
- **Ngày/Giờ:** Dành cho giá trị ngày và giờ.
- **Bản ghi nhớ:** Dành cho văn bản hoặc ghi chú dài hơn.
- **Siêu liên kết:** Dành cho các liên kết web và địa chỉ email.
- **Đính kèm:** Để lưu trữ tập tin và tệp đính kèm.

## Làm cách nào để mở tập tin JET?

Các chương trình mở hoặc tham chiếu tệp JET bao gồm

- Microsoft Access 365 (Dùng thử miễn phí)

## Các tập tin JET khác

- [JET - Cài đặt gói tiệc Jackbox](/vi/settings/jet/)


## Người giới thiệu
* [Truy cập công cụ cơ sở dữ liệu](https://en.wikipedia.org/wiki/Access_Database_Engine)

