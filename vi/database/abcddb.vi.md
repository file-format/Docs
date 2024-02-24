{
  "date" : "2023-01-09",
  "keywords" : [ "ABCDDB", "what is a ABCDDB file", "extension", "file", "file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "Tìm hiểu về định dạng tệp ABCDDB và các API có thể tạo và mở tệp ABCDDB.",
  "title" : "Định dạng tệp ABCDDB - Tệp cơ sở dữ liệu danh sách liên hệ sổ địa chỉ Apple",
  "linktitle" : "ABCDDB",
  "menu" : {
    "docs" : {
      "identifier":"database-abcddb-vi",
      "parent" : "database"
}
},
  "lastmod" : "2020-01-09"
}

## Tệp ABCDDB là gì?

Tệp có phần mở rộng **.ABCDDB** là viết tắt của Cơ sở dữ liệu danh sách liên hệ trong sổ địa chỉ Apple. Nó thuộc về ứng dụng **Sổ địa chỉ** còn được gọi là **Danh bạ**. Nó là một ứng dụng tích hợp và đi kèm với hệ điều hành iOS và macOS. Ứng dụng Danh bạ cho phép người dùng lưu và sắp xếp các thông tin liên quan đến danh bạ của mình, bao gồm các cá nhân, doanh nghiệp và tổ chức. Ứng dụng này cho phép người dùng theo dõi các chi tiết như tên, địa chỉ, số điện thoại và địa chỉ email cũng như phân loại danh bạ của họ thành các nhóm.

## Mối quan hệ với SQLite và đường dẫn điển hình

Sổ địa chỉ của Apple (còn được gọi là Danh bạ) lưu trữ thông tin liên hệ dưới dạng vCard trong thư mục siêu dữ liệu. **Tệp _ABCDDB_ thực chất là tệp dữ liệu _SQLite 3_**.

SQLite là một hệ thống quản lý cơ sở dữ liệu phổ biến được thiết kế gọn nhẹ và khép kín. Nó được sử dụng trong nhiều loại phần mềm và thiết bị khác nhau. SQLite là một loại RDBMS, nghĩa là nó lưu trữ dữ liệu trong các bảng có liên quan với nhau thông qua các khóa. Nó có thể xử lý nhiều loại dữ liệu, bao gồm số nguyên, số dấu phẩy động, chuỗi và dữ liệu nhị phân. Ngoài ra, SQLite hỗ trợ các giao dịch, cho phép người dùng thực hiện nhiều thao tác cơ sở dữ liệu cùng nhau dưới dạng một đơn vị công việc.

Tệp có phần mở rộng ABCDDB thường được lưu trữ ở đây

`~/Thư viện/Hỗ trợ ứng dụng/Sổ địa chỉ/Sổ địa chỉ-v22.abcddb`

## Sửa cơ sở dữ liệu Danh bạ bị hỏng

Trước tiên hãy sao lưu trước khi thử thực hiện việc này. Sau đó vui lòng điều hướng đến

`~/Thư viện/Hỗ trợ ứng dụng/Sổ địa chỉ`

Trong thư mục đó, bạn sẽ tìm thấy ba tệp trong đó có tệp có phần mở rộng .abcddb

- `sổ địa chỉ-v22.abcddb`
- `sổ địa chỉ-v22.abcddb-wal`
- `sổ địa chỉ-v22.abcddb-shm`

Xóa tất cả các tệp này và mở lại Danh bạ, nó sẽ bắt đầu hoạt động trở lại.

## Khôi phục cơ sở dữ liệu Sổ Địa chỉ từ Bản sao lưu

Giả sử, danh bạ cơ sở dữ liệu Sổ địa chỉ của bạn được lưu trữ trong `addressbook-v22.abcddb`

- Trước tiên hãy sao lưu dữ liệu Sổ địa chỉ của bạn và thoát khỏi tất cả các ứng dụng.
- Di chuyển tệp cơ sở dữ liệu của bạn sang thư mục con `~/Library/Application Support/AddressBook`
- Khởi chạy **Sổ địa chỉ.app**.

## Xuất dữ liệu tệp ABCDDB sang Microsoft Access

Vì tệp là tệp dữ liệu SQLite 3 nên bạn có thể xuất dữ liệu bên trong tệp abcddb sang Microsoft Access bằng trình kết nối ODBC.

Trình kết nối ODBC SQLite là thư viện phần mềm và trình điều khiển cho phép các ứng dụng hỗ trợ giao diện ODBC kết nối với cơ sở dữ liệu SQLite. Nó bao gồm một thư viện xác định giao diện ODBC và trình điều khiển chuyển giao diện này thành các lệnh gọi tới API SQLite. Để sử dụng trình kết nối ODBC SQLite, trước tiên bạn phải cài đặt nó rồi thiết lập nguồn dữ liệu ODBC trên máy tính của mình. Sau khi hoàn thành các bước này, mọi ứng dụng được trang bị hỗ trợ ODBC sẽ có thể kết nối với nguồn dữ liệu và truy xuất dữ liệu từ cơ sở dữ liệu SQLite.

## Người giới thiệu
 * [Fix corrupted Contacts database](https://discussions.apple.com/docs/DOC-10581)
 * [Cơ sở dữ liệu liên hệ dành cho Mac](https://nitroreward.weebly.com/blog/contact-database-for-mac)
 * [Làm cách nào tôi có thể mở hoặc xuất tệp abcddb trong Windows 7 Excel?](https://apple.stackexchange.com/questions/52888/how-can-i-open-or-export-a-abcddb-file-in -windows-7-excel)

