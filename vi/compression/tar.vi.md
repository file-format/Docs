{
  "date" : "2019-10-11",
  "keywords" :[ "tệp tar", "định dạng tệp tar", "tệp tar là gì", "tệp", "ví dụ tar", "phần mở rộng tập tin tar","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TAR - Định dạng tệp lưu trữ Unix",
  "description":"Tìm hiểu về tệp Tar là gì và các API có thể tạo và mở tệp TAR.",
  "linktitle" : "TAR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2019-09-10"
}

## Tệp TAR là gì?

Các tệp có phần mở rộng .tar là các tệp lưu trữ được tạo bằng tiện ích dựa trên Unix để thu thập một hoặc nhiều tệp. Nhiều tệp được lưu trữ ở định dạng không nén với sự hỗ trợ thêm tệp cũng như thư mục vào kho lưu trữ. Tiện ích TAR trên Unix dựa trên Lệnh, nhưng các tệp do đó được tạo ra được hỗ trợ bởi hầu hết các hệ thống lưu trữ tệp trên hầu hết các hệ điều hành. Nó được tạo ra lần đầu tiên vào năm 1979 bởi Phòng thí nghiệm AT&T Bell và các phiên bản tiếp theo đã được xuất bản theo thời gian.

## Định dạng tệp TAR

TAR là một định dạng tệp mở với đầy đủ thông số kỹ thuật có sẵn để nhà phát triển tham khảo. Cấu trúc tệp của nó đã được chuẩn hóa trong POSIX.1-1988 và sau đó là POSIX.1-2001. Các bộ dữ liệu được tạo bởi tar giữ lại thông tin về các tham số hệ thống tệp, chẳng hạn như:

* Tên
* Dấu thời gian
* Quyền sở hữu
* Quyền truy cập tệp
* Tổ chức thư mục

Tệp Tar không có bất kỳ số ma thuật nào. Nó chứa một loạt các khối trong đó mỗi khối là BLOCKSIZE byte.

Mỗi tệp được lưu trữ được biểu thị bằng một khối tiêu đề mô tả tệp, theo sau là 0 hoặc nhiều khối cung cấp nội dung của tệp. Ở cuối tệp lưu trữ, có hai khối 512 byte chứa đầy các số 0 nhị phân dưới dạng điểm đánh dấu cuối tệp. Một hệ thống hợp lý nên viết điểm đánh dấu cuối tệp như vậy ở cuối kho lưu trữ, nhưng không được giả định rằng một khối như vậy tồn tại khi đọc một kho lưu trữ. Đặc biệt GNU tar luôn đưa ra cảnh báo nếu không gặp phải.

Các khối có thể bị chặn đối với các hoạt động I/O vật lý. Mỗi bản ghi của n khối (trong đó n được đặt bởi tùy chọn kích thước khối = 512 thành tar) được ghi bằng một thao tác "write()" duy nhất. Trên băng từ, kết quả của việc ghi như vậy là một bản ghi. Khi viết một kho lưu trữ, bản ghi cuối cùng của các khối phải được ghi ở kích thước đầy đủ, với các khối sau khối số 0 chứa tất cả các số không. Khi đọc một kho lưu trữ, một hệ thống hợp lý sẽ xử lý đúng cách một kho lưu trữ có bản ghi cuối cùng ngắn hơn phần còn lại hoặc chứa các bản ghi rác sau khối số không.

### Tiêu đề Tar

Giống như bất kỳ tiêu đề tệp nào khác, bản ghi tiêu đề tệp tar chứa siêu dữ liệu về một tệp và được hiển thị trong bảng sau.


|Độ lệch trường|Kích thước trường (Byte)|Trường
---|---|---|
|0|100|Tên tệp
|100|8|Chế độ tệp
|108|8|ID người dùng dạng số của chủ sở hữu
|116|8|ID người dùng dạng số của nhóm
|124|12|Kích thước tệp tính bằng byte (cơ số bát phân)
|136|12|Thời gian sửa đổi lần cuối ở định dạng số thời gian Unix (bát phân)
|148|8|Tổng kiểm tra cho bản ghi tiêu đề
|156|1|Chỉ báo liên kết (loại tệp)
|157|100|Tên tệp được liên kết

Các trường không sử dụng được lấp đầy bằng NUL byte. Một tiêu đề bao gồm 257 byte được đệm bằng các byte NUL để làm cho nó lấp đầy bản ghi 512 byte.

## Người giới thiệu ##

* [TAR - Theo Wikipedia](https://en.wikipedia.org/wiki/Tar_(computing))
* [Định dạng cơ bản TAR](https://www.gnu.org/software/tar/manual/html_node/Standard.html)

