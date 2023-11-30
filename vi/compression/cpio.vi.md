{
  "date" : "2023-05-10",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Tệp CPIO - Định dạng tệp lưu trữ Unix CPIO",
  "description":"Tìm hiểu để biết tệp CPIO là gì và các API có thể tạo và mở tệp CPIO.",
  "linktitle" : "CPIO",
  "menu" : {
    "docs" : {
      "identifier" : "compression-cpio",
      "parent" : "compression"
}
},
  "lastmod" : "2023-05-10"
}

## Tập tin CPIO là gì?

Tệp CPIO là tệp lưu trữ được tạo ở định dạng Copy In Copy Out (CPIO) của Unix. Nó tương tự như định dạng tệp TAR, ngoại trừ việc nó không bị nén. Tệp CPIO có thể lưu trữ tệp thiết bị, liên kết tượng trưng và thuộc tính tệp mở rộng.

## Định dạng tệp CPIO

Kho lưu trữ CPIO được tạo dưới dạng tệp nhị phân mà con người không thể đọc được. Nó lưu trữ bộ sưu tập các tập tin và thư mục. Nội dung của kho lưu trữ CPIO được xác định bằng thông tin siêu dữ liệu như tên tệp, quyền, quyền sở hữu và dấu thời gian. Thông tin siêu dữ liệu này cũng được lưu trữ trong tệp lưu trữ để hệ thống truy cập sau.

## Định dạng của Lưu trữ CPIO

Tệp CPIO bao gồm một hoặc nhiều tệp thành viên được nối. Mỗi tệp trong kho lưu trữ bao gồm một tiêu đề tùy chọn, theo sau là nội dung tệp như được đề cập trong tiêu đề. Kho lưu trữ chứa một tiêu đề khác ở cuối được mô tả bằng một tệp trống có tên TRAILER!!.

### Các loại kho lưu trữ CPIO

Có hai loại kho lưu trữ CPIO. Những điều này chỉ khác nhau ở phong cách của tiêu đề.

* Lưu trữ ASCII - Các kho lưu trữ CPIO này có tiêu đề có thể in được và trở thành một phần của kho lưu trữ CPIO nếu bản thân kho lưu trữ bao gồm các tệp ASCII
* Lưu trữ nhị phân - Các kho lưu trữ CPIO này có tiêu đề nhị phân.

## Làm việc với Lưu trữ CPIO

### Làm thế nào để tạo kho lưu trữ CPIO?

Bạn có thể tạo CPIO trên các hệ thống giống Unix bằng lệnh **cpio**. Lệnh sau sẽ tìm tất cả các tệp và thư mục trong thư mục hiện tại và các thư mục con của nó. Đầu ra này sau đó được chuyển tới lệnh cpio để tạo ra một kho lưu trữ CPIO mới có tên archive.cpio.

```
find . -depth -print | cpio -ov > archive_cpio.cpio
```
### Làm cách nào để trích xuất tệp từ kho lưu trữ CPIO?

Lệnh sau trích xuất các tập tin từ kho lưu trữ hiện có.

```
cpio -id < archive_cpio.cpio
```
Nó sẽ đọc tệp archive.cpio từ đầu vào tiêu chuẩn và trích xuất các tệp vào thư mục hiện tại.


## Người giới thiệu

* [CPIO - Bởi Wikipedia](https://en.wikipedia.org/wiki/Cpio)
* [Định dạng tệp CPIO](https://www.ibm.com/docs/en/zos/2.2.0?topic=formats-cpio-format-cpio-archives)

