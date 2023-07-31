{
  "date" : "2021-06-21",
  "keywords" :[ "UDL", "phần mở rộng", "tệp udl", "định dạng tệp udl", "Loại tệp cơ sở dữ liệu", "Định dạng tệp cơ sở dữ liệu", "tệp udl là gì" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Tìm hiểu về định dạng tệp UDL và API có thể tạo và mở tệp UDL.",
  "title" :"UDL - Tệp liên kết dữ liệu chung của Microsoft",
  "linktitle" : "UDL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-06-21"
}

## Tệp UDL là gì?
Tệp có phần mở rộng .udl được gọi là tệp Liên kết dữ liệu chung của Microsoft; chỉ định các thuộc tính kết nối; được các ứng dụng Windows sử dụng để thiết lập kết nối với cơ sở dữ liệu. Tệp UDL chứa chuỗi kết nối cho nguồn dữ liệu OLE DB; với tên người dùng và mật khẩu và các thuộc tính chuỗi kết nối thiết yếu. Để tránh chỉ định trực tiếp các thuộc tính bằng tay trong chuỗi kết nối, có thể sử dụng hộp thoại Thuộc tính liên kết dữ liệu để lưu thông tin kết nối trong tệp .udl như một giải pháp thay thế.

## Định dạng tệp UDL
Về cơ bản, tệp UDL (Liên kết dữ liệu chung) là một tệp văn bản đơn giản bao gồm một chuỗi kết nối cơ sở dữ liệu với các thuộc tính hoặc thuộc tính cụ thể. Khi tệp UDL được tạo, nó có thể được kiểm tra bằng cách sử dụng SQL Server Management Studio để xác minh kết nối.

### Thuộc tính chuỗi kết nối
Các thuộc tính sau có thể được đặt trong UDL để đảm bảo kết nối phù hợp:

- **Tên máy chủ**: vị trí của máy chủ chứa cơ sở dữ liệu mà bạn muốn truy cập.
- **Tùy chọn xác thực**
- **Xác thực Windows**: Xác thực với SQL Server bằng thông tin đăng nhập tài khoản Windows của người dùng hiện đang đăng nhập.
- **Xác thực máy chủ SQL**: Xác thực bằng ID đăng nhập và mật khẩu.
- **Active Directory - Tích hợp**: Xác thực tích hợp với danh tính Azure Active Directory; cũng có thể được sử dụng để xác thực Windows với SQL Server.
- **Active Directory - Mật khẩu**: Xác thực ID người dùng và mật khẩu với danh tính Azure Active Directory.
- **Active Directory - Universal có hỗ trợ MFA**: Xác thực tương tác với danh tính Azure Active Directory.
- **Active Directory - Dịch vụ chính**: Xác thực bằng dịch vụ chính của Azure Active Directory.
- **SPN máy chủ**: Nếu bạn sử dụng kết nối đáng tin cậy, bạn có thể chỉ định tên chính của dịch vụ (SPN) cho máy chủ.
- **Tên người dùng**: Nhập ID người dùng để sử dụng để xác thực khi bạn đăng nhập vào nguồn dữ liệu.
- **Mật khẩu**: Nhập mật khẩu để sử dụng để xác thực khi bạn đăng nhập vào nguồn dữ liệu.
- **Mật khẩu trống**: Khi được chọn, cho phép nhà cung cấp được chỉ định sử dụng mật khẩu trống trong chuỗi kết nối.
- **Cho phép lưu mật khẩu**: Cho phép lưu mật khẩu cùng với chuỗi kết nối.
- **Sử dụng mã hóa mạnh cho dữ liệu**: dữ liệu truyền qua kết nối sẽ được mã hóa.
- **Chứng chỉ máy chủ tin cậy**: Chứng chỉ của máy chủ sẽ được xác thực.
- **Database**: Tên cơ sở dữ liệu mà bạn muốn truy cập.
- **Đính kèm tệp cơ sở dữ liệu dưới dạng tên cơ sở dữ liệu**: Chỉ định tên của tệp chính cho cơ sở dữ liệu có thể đính kèm.

## Người giới thiệu ##

* [Các thành phần truy cập dữ liệu của Microsoft](https://en.wikipedia.org/wiki/Microsoft_Data_Access_Components#Universal_data_link)
* [Cấu hình Liên kết dữ liệu chung (UDL)](https://learn.microsoft.com/en-us/sql/connect/oledb/help-topics/data-link-pages?view=sql-server-ver15)

