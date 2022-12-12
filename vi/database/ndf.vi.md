{
  "date" : "2020-11-11",
  "keywords" :[ "NDF", "phần mở rộng", "tệp", "định dạng tệp", "Loại tệp cơ sở dữ liệu", "Định dạng tệp cơ sở dữ liệu", "Tệp cơ sở dữ liệu" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Tìm hiểu về định dạng tệp MDF và API có thể tạo và mở tệp NDF.",
  "title" :"Định dạng tệp NDF - Tệp cơ sở dữ liệu chính của máy chủ SQL",
  "linktitle" : "NDF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## Tệp NDF là gì?

Tệp có phần mở rộng .ndf là tệp cơ sở dữ liệu thứ cấp được [Microsoft SQL Server](https://en.wikipedia.org/wiki/Microsoft_SQL_Server) sử dụng để lưu trữ dữ liệu người dùng. NDF là tệp lưu trữ thứ cấp vì máy chủ SQL lưu trữ dữ liệu do người dùng chỉ định trong tệp lưu trữ chính được gọi là [MDF](/vi/database/mdf/). Tệp dữ liệu NDF là tùy chọn và do người dùng xác định để quản lý lưu trữ dữ liệu trong trường hợp tệp MDF chính sử dụng tất cả dung lượng được phân bổ. Nó thường được lưu trữ trên đĩa riêng biệt và có thể lây lan sang nhiều thiết bị lưu trữ. Sự hiện diện của tệp MDF là cần thiết để mở tệp NDF.

## Định dạng tệp NDF

Định dạng tệp NDF không khác gì [MDF](/vi/database/mdf) và sử dụng các trang làm đơn vị lưu trữ dữ liệu cơ bản. mỗi trang bắt đầu với tiêu đề 96 byte bao gồm:

* Mã trang
* Loại kết cấu
* Số lượng hồ sơ trong các trang
* Con trỏ tới trang trước và trang sau

### Cấu trúc tệp NDF

Tệp MDF có cấu trúc dữ liệu sau.

* Trang 0: Tiêu đề
* Trang 1: PFS đầu tiên
* Trang 2: GAM đầu tiên
* Trang 3: SGAM đầu tiên
* Trang 4: Chưa sử dụng
* Trang 5: Chưa sử dụng
* Trang 6: DCM đầu tiên
* Trang 7: BCM đầu tiên

#### Tiêu đề tệp NDF

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

## Trang tệp dữ liệu

Các trang trong tệp dữ liệu SQL Server bắt đầu từ số không (0) và tăng dần theo tuần tự. Mỗi tệp được nhận dạng bằng một số ID tệp duy nhất. ID tệp và cặp số trang xác định duy nhất một trang trong cơ sở dữ liệu. Một ví dụ hiển thị số trang trong cơ sở dữ liệu, như trong hình ảnh sau đây.

{{< figure src="../ndf.png" alt="Định dạng tệp cơ sở dữ liệu NDF" >}}

Ví dụ này hiển thị số trang trong cơ sở dữ liệu có tệp dữ liệu chính 4 MB và tệp dữ liệu phụ 1 MB.

## Người giới thiệu

* [Tệp cơ sở dữ liệu và nhóm tệp](https://docs.microsoft.com/en-us/sql/relational-databases/databases/database-files-and-filegroups?redirectedfrom=MSDN&view=sql-server-ver15)
* [Tách và đính kèm cơ sở dữ liệu - SQL Server](https://docs.microsoft.com/en-us/sql/relational-databases/databases/database-detach-and-attach-sql-server?view=sql-server -ver15)
* [Phân tích giải phẫu tệp dữ liệu máy chủ SQL](https://blog.pythian.com/analyzing-sql-server-data-file-anatomy/)

