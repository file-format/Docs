{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Định dạng tệp EDB - Tệp cơ sở dữ liệu thư Exchange",
  "description":"Tìm hiểu về định dạng tệp EDB và API có thể tạo và mở tệp EDB.",
  "linktitle" : "EDB",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2020-09-16"
}

## Tệp EDB là gì?

Tệp có phần mở rộng tệp .edb là cơ sở dữ liệu hộp thư được tạo bởi Microsoft Exchange Server để lưu trữ dữ liệu liên quan đến thư. EDB, Cơ sở dữ liệu Exchange, lưu trữ các thư đang xử lý và không phải SMTP. EDB còn được gọi là tệp Cơ sở dữ liệu Công cụ lưu trữ mở rộng (ESE) và lưu trữ tệp bằng cấu trúc b-tree. Là tệp lưu trữ, các tệp EDB có thể được chuyển đổi thành các định dạng tệp lưu trữ thư khác, chẳng hạn như [PST](/vi/email/pst/) và [OST](/vi/email/ost/).

## Định dạng tệp EDB

Không có thông số kỹ thuật định dạng tệp EDB mở/chính thức nào có thể được tham chiếu. Một số tiến bộ đã được thực hiện đối với kỹ thuật đảo ngược định dạng tệp, dẫn đến việc giải mã một phần thông số kỹ thuật. Theo những điều này, một tệp EDB bao gồm:
* File Header - Chứa thông tin tiêu đề file cơ sở dữ liệu
* Các trang có kích thước cố định - Chứa cơ sở dữ liệu bao gồm các bảng và chỉ mục

### Tiêu đề tệp cơ sở dữ liệu
Tiêu đề tệp cơ sở dữ liệu nằm trong trang cơ sở dữ liệu đầu tiên và ít nhất là 668 byte. Tiêu đề tệp chứa `Phiên bản định dạng tệp` và `Loại tệp` ngoài các trường khác.

#### Loại tập tin
|Loại|Mô tả
---|---|
|0| Cơ sở dữ liệu|
|1| Phát trực tuyến|

`Lưu ý:` Không xác định được định danh cho các loại này.

#### Phiên bản định dạng tệp
Định dạng ban đầu của EDB bắt đầu vào tháng 4 năm 1997 và tiếp tục phát triển để thay đổi sau đó.

|Ngày sửa đổi|Phiên bản|Sửa đổi|mô tả
---|---|---|---|
|Tháng 4 năm 1997| 0x00000620|0x00000000| Hệ điều hành gốc định dạng Beta.|
|Tháng 5 năm 1997 |0x00000620|0x00000001| Thêm các cột trong danh mục để lập chỉ mục có điều kiện và CŨ.|
|Tháng 6 năm 1997|0x00000620|0x00000002|Thêm cờ fLocalizedText trong IDB.|
|Tháng 10 năm 1997|0x00000620|0x00000003|Thêm SPLIT_BUFFER vào các trang gốc của cây không gian.|
|Tháng 1 năm 1998|0x00000620|0x00000002|Hoàn nguyên bản sửa đổi để ESE97 vẫn tương thích về phía trước.|
||0x00000620|0x00000003|Thêm các cột được gắn thẻ mới vào danh mục ("CallbackData" và "CallbackDependencies").|
|Tháng 5 năm 1998|0x00000620|0x00000004|Hỗ trợ Giá trị siêu dài (SLV): signSLV, fSLVETồn tại trong dbheader.|
|Tháng 5 năm 1998|0x00000620|0x00000005|Cây không gian SLV mới.|
|Tháng 10 năm 1998|0x00000620|0x00000006|Bản đồ không gian SLV.|
|Tháng 12 năm 1998|0x00000620|0x00000007|IDXSEG 4 byte.|
|Tháng 1 năm 1999|0x00000620|0x00000008|Định dạng cột mẫu mới.|
|Tháng 6 năm 1999|0x00000620|0x00000009|Cột mẫu đã sắp xếp. Được sử dụng trong Windows XP SP3|
||0x00000620|0x0000000b|Chứa tiêu đề trang với tổng kiểm tra ECCĐược sử dụng trong Exchange|
||0x00000620|0x0000000c|Được sử dụng trong Windows Vista (SP0)|
||0x00000620|0x00000011|Hỗ trợ cho các trang 2 KiB, 16 KiB và 32 KiB. Tiêu đề trang mở rộng với tổng kiểm tra ECC bổ sung. Nén cột. Gợi ý khoảng trắng. Được sử dụng trong Windows 7 (SP0)|
|Tháng 5 năm 1999|0x00000623|0x00000000|Người quản lý không gian mới.|

### Tệp cơ sở dữ liệu

Tệp cơ sở dữ liệu EDB chứa lược đồ cho tất cả các bảng trong cơ sở dữ liệu. Ngoài ra, nó cũng bao gồm các bản ghi cho tất cả các bảng cơ sở dữ liệu và chỉ mục cho các bảng. Vị trí của nó được xác định bởi các định danh sau.

* Cơ sở dữ liệu JetCreate
* JetCreateDatabase2
* Cơ sở dữ liệu JetAttach
* Cơ sở dữ liệu JetAttach2

Dựa trên những điều này, trạng thái của cơ sở dữ liệu có thể được đánh giá như sau.

|Giá trị|Định danh|Mô tả
---|---|---|
|1|JET_dbstateJustCreated|Cơ sở dữ liệu vừa được tạo.|
|2|JET_dbstateDirtyShutdown|Cơ sở dữ liệu yêu cầu chạy khôi phục cứng hoặc mềm để có thể sử dụng hoặc di chuyển được. Không nên cố di chuyển cơ sở dữ liệu ở trạng thái này.|
|3|JET_dbstateCleanShutdown|Cơ sở dữ liệu ở trạng thái sạch. Có thể đính kèm cơ sở dữ liệu mà không cần bất kỳ tệp nhật ký nào.|
|4|JET_dbstateBeingConverted|Cơ sở dữ liệu đang được nâng cấp.|
|5|JET_dbstateForceDetachInternal|Giá trị này được giới thiệu trong WindowsXP|
 

## Người giới thiệu
* [Thông số kỹ thuật tệp cơ sở dữ liệu (EDB) của công cụ lưu trữ mở rộng](https://github.com/libyal/libesedb/tree/master/documentation)

