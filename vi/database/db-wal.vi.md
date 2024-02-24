{
  "date" : "2023-01-16",
  "keywords" : [ "DB-WAL", "what is a DB-WAL file", "extension", "file", "file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "Tìm hiểu về định dạng tệp DB-WAL và các API có thể tạo và mở tệp DB-WAL.",
  "title" : "Định dạng tệp DB-WAL - Tệp nhật ký ghi trước cơ sở dữ liệu SQLite",
  "linktitle" : "DB-WAL",
  "menu" : {
    "docs" : {
      "identifier":"database-db-wal-vi",
      "parent" : "database"
}
},
  "lastmod" : "2020-01-16"
}

## Tệp DB-WAL là gì?

Phần mở rộng tệp .db-wal được liên kết với SQLite, một hệ thống quản lý cơ sở dữ liệu quan hệ nguồn mở phổ biến. Định dạng tệp WAL (viết tắt của Write-Ahead Log) là một định dạng thay thế cho nhật ký khôi phục truyền thống được SQLite sử dụng. Nó cung cấp khả năng kiểm soát đồng thời nhiều hơn, cho phép nhiều quy trình đọc cơ sở dữ liệu cùng một lúc, trong khi vẫn cung cấp khả năng khôi phục sự cố. Tệp .db-wal được sử dụng để lưu trữ các thay đổi được thực hiện đối với cơ sở dữ liệu chưa được chuyển sang tệp cơ sở dữ liệu chính (có phần mở rộng .db).

## Định dạng WAL chung

Ở định dạng tệp WAL (Nhật ký ghi trước), các thay đổi được thực hiện đối với cơ sở dữ liệu trước tiên được ghi vào tệp WAL trước khi được chuyển sang tệp cơ sở dữ liệu chính. Điều này cho phép truy cập đồng thời hơn vào cơ sở dữ liệu, vì nhiều quy trình có thể đọc từ cơ sở dữ liệu trong khi các thay đổi đang được thực hiện. Ngoài ra, định dạng tệp WAL cung cấp khả năng khôi phục sau sự cố, cho phép cơ sở dữ liệu được khôi phục về trạng thái trước đó trong trường hợp tắt máy đột ngột.

## Sự khác biệt giữa định dạng DB-WAL và WAL

Cả hai định dạng tệp .db-wal và WAL đều được liên kết với SQLite, một hệ thống quản lý cơ sở dữ liệu quan hệ nguồn mở phổ biến. Tuy nhiên, có một sự khác biệt tinh tế giữa hai.

Tệp .db-wal về cơ bản là tệp WAL, nhưng có phần mở rộng tệp khác. Tệp .db-wal được sử dụng để lưu trữ các thay đổi được thực hiện đối với cơ sở dữ liệu chưa được cam kết với tệp cơ sở dữ liệu chính (có phần mở rộng .db), trong khi định dạng tệp WAL được sử dụng để lưu trữ nhật ký ghi trước của các thay đổi cơ sở dữ liệu .

Nói cách khác, tệp .db-wal là một loại tệp WAL cụ thể được cơ sở dữ liệu SQLite sử dụng để lưu trữ các thay đổi được thực hiện đối với cơ sở dữ liệu chưa được cam kết với tệp cơ sở dữ liệu chính. Định dạng tệp WAL là thuật ngữ chung cho loại định dạng tệp này.

Vì vậy, WAL là thuật ngữ chung cho định dạng tệp, .db-wal là cách triển khai cụ thể của định dạng tệp WAL được cơ sở dữ liệu SQLite sử dụng.

## Người giới thiệu
* [Định dạng tệp chế độ WAL](https://www.sqlite.org/walformat.html)

* [Ghi nhật ký ghi trước](https://www.sqlite.org/wal.html)


