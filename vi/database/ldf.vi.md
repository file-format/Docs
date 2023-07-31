{
  "date" : "2020-11-11",
  "keywords" :[ "LDF", "phần mở rộng", "tệp", "định dạng tệp", "Loại tệp cơ sở dữ liệu", "Định dạng tệp cơ sở dữ liệu", "Tệp cơ sở dữ liệu" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Tìm hiểu về định dạng tệp LDF và API có thể tạo và mở tệp LDF.",
  "title" :"LDF - Định dạng tệp cơ sở dữ liệu chính của máy chủ SQL",
  "linktitle" : "LDF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## Tệp LDF là gì?

Tệp có phần mở rộng .ldf là tệp nhật ký được duy trì bởi Microsoft SQL Server, một hệ thống quản lý cơ sở dữ liệu quan hệ (RDBMS). Tất cả các giao dịch được thực hiện trên các tệp cơ sở dữ liệu chính ([MDF](/vi/database/mdf/))(chẳng hạn như chèn, cập nhật, xóa) đều được ghi lại trong tệp LDF. Các tệp LDF là các thành phần quan trọng của bất kỳ cơ sở dữ liệu nào. Trong trường hợp lỗi hệ thống, tệp nhật ký được sử dụng để khôi phục cơ sở dữ liệu về trạng thái nhất quán. Tệp nhật ký giao dịch có thể tăng kích thước nếu các giao dịch không được cam kết đầy đủ. Các tệp LDF có thể được mở bằng ứng dụng phần mềm Microsoft SQL Server.

## Hoạt động được ghi trong tệp LDF

Tệp nhật ký SQL ghi lại các thao tác sau:

* Thời điểm bắt đầu và kết thúc mỗi giao dịch.

* Mỗi lần sửa đổi dữ liệu dữ liệu (chèn, cập nhật hoặc xóa). Điều này cũng bao gồm các thay đổi bởi các thủ tục được lưu trữ trong hệ thống hoặc các câu lệnh ngôn ngữ định nghĩa dữ liệu (DDL) đối với bất kỳ bảng nào, kể cả các bảng hệ thống.

* Mọi phạm vi và phân bổ hoặc phân bổ trang.

* Tạo hoặc xóa bảng hoặc chỉ mục.

## Định dạng tệp LDF

Tệp LDF bao gồm các bản ghi giao dịch SQL Server được sắp xếp dưới dạng chuỗi bản ghi nhật ký. Mỗi bản ghi nhật ký có một số thứ tự nhật ký (LSN) cao hơn LSN của bản ghi trước đó. Các chuỗi được nối với nhau trong tệp. Do các máy tính tốc độ cao hiện đại, các bản ghi có thể được chèn vào nơi LSN2 tồn tại trong tệp nhật ký trước LSN1. Do các thao tác được ghi lại theo trình tự, thay đổi được mô tả bởi LSN2 được thực hiện sau bản ghi nhật ký LSN1. Các bản ghi cho một giao dịch cụ thể được liên kết ngược lại bằng cách sử dụng các con trỏ được sử dụng và tăng tốc độ khôi phục của giao dịch.
 

## Người giới thiệu

* [Tệp cơ sở dữ liệu và nhóm tệp](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-files-and-filegroups?view=sql-server-ver15)
* [Hướng dẫn quản lý và kiến trúc nhật ký giao dịch](https://learn.microsoft.com/en-us/sql/relational-databases/sql-server-transaction-log-architecture-and-man Quản lý-guide?view=sql- máy chủ-ver15)

