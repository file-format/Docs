{
  "date" : "2020-11-11",
  "keywords" :[ "MDF", "phần mở rộng", "tệp", "định dạng tệp", "Loại tệp cơ sở dữ liệu", "Định dạng tệp cơ sở dữ liệu", "Tệp cơ sở dữ liệu" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Tìm hiểu về định dạng tệp MDF và các API có thể tạo và mở tệp MDF.",
  "title" :"Định dạng tệp MDF - Tệp cơ sở dữ liệu chính của máy chủ SQL",
  "linktitle" : "MDF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## Tệp MDF là gì?

Tệp có phần mở rộng .mdf là Tệp cơ sở dữ liệu chính được [Microsoft SQL Server](https://en.wikipedia.org/wiki/Microsoft_SQL_Server) sử dụng để lưu trữ dữ liệu người dùng. Nó có tầm quan trọng hàng đầu vì tất cả dữ liệu được lưu trữ trong tệp này. Tệp MDF lưu trữ dữ liệu người dùng trong cơ sở dữ liệu quan hệ ở dạng cột, hàng, trường, chỉ mục, dạng xem và bảng. SQL Server cho phép đặt cài đặt autogrow và autoshrink để có tác động tích cực đến hiệu suất của cơ sở dữ liệu. Các tệp MDF có thể được tải và đính kèm vào cơ sở dữ liệu bằng Microsoft SQL Server. Các tệp MDF có loại ứng dụng/octet-stream mime.

## Định dạng tệp MDF

Đơn vị lưu trữ dữ liệu cơ bản trong SQL Server là một trang. Một trang lưu trữ được chỉ định cơ sở dữ liệu được chia thành các trang logic được đánh số từ 0 đến n. Một trang đơn bắt đầu với tiêu đề 96 byte bao gồm ID trang, loại cấu trúc thuộc về trang, số lượng bản ghi trong trang và con trỏ tới trang trước và trang tiếp theo.

### Cấu trúc tệp

Tệp MDF có cấu trúc dữ liệu sau.

* Trang 0: Tiêu đề
* Trang 1: PFS đầu tiên
* Trang 2: GAM đầu tiên
* Trang 3: SGAM đầu tiên
* Trang 4: Chưa sử dụng
* Trang 5: Chưa sử dụng
* Trang 6: DCM đầu tiên
* Trang 7: BCM đầu tiên

#### Tiêu đề tệp

Trang số 0 của tất cả các tệp chứa tiêu đề lưu trữ siêu dữ liệu về tệp.

#### Không gian trống của trang (PFS)
PFS xác định trạng thái phân bổ và xác định dung lượng trống.

* Bit 1: Cho biết trang đã được cấp phát hay chưa.
* Bit 2: Cho biết trang có thuộc phạm vi hỗn hợp hay không.
* Bit 3: Cho biết trang này là trang IAM.
* Bit 4: Cho biết trang này chứa bản ghi ma
* Bits 5 đến 7: Giá trị ba bit kết hợp, cho biết độ đầy của trang như sau:
* 0: Trang trống
* 1: Trang đầy 1–50%
* 2: Trang đầy 51–80%
* 3: Trang đầy 81–95%
* 4: Trang đầy 96–100%

## Người giới thiệu

* [Tệp cơ sở dữ liệu và nhóm tệp](https://docs.microsoft.com/en-us/sql/relational-databases/databases/database-files-and-filegroups?view=sql-server-ver15)
* [Tách và đính kèm cơ sở dữ liệu - SQL Server](https://docs.microsoft.com/en-us/sql/relational-databases/databases/database-detach-and-attach-sql-server?view=sql-server -ver15)
* [Phân tích giải phẫu tệp dữ liệu máy chủ SQL](https://blog.pythian.com/analyzing-sql-server-data-file-anatomy/)

