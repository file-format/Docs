{
  "date" : "2019-10-11",
  "keywords" :[ "tệp tga", "định dạng tệp tga", "tệp tga là gì", "tệp", "ví dụ tga", "phần mở rộng tệp tga","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Định dạng tệp TGA - Tệp hình ảnh đồ họa TARGA",
  "description":"Tìm hiểu về định dạng tệp TGA và các API có thể tạo và mở tệp TGA.",
  "linktitle" : "TGA",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Tệp TGA là gì?

Tệp có phần mở rộng .tga là một định dạng đồ họa raster và được tạo bởi Truevision Inc. Tệp này được thiết kế cho các bo mạch TARGA (Truevision Advanced Raster Adapter) và cung cấp hỗ trợ hiển thị Highcolor/truecolor cho các PC tương thích với IBM. Nó hỗ trợ 8, 16, 24 và 32 bit cho mỗi pixel và kênh alpha 8 bit. Nó cũng hỗ trợ nén RLE không mất dữ liệu có thể được áp dụng để giảm kích thước hình ảnh. Ảnh kỹ thuật số và kết cấu sử dụng định dạng ảnh TGA.

## Tóm tắt lịch sử

Sự hình thành định dạng tệp TGA ra đời vào năm 1984 bởi AT&T EPICenter (sau đó được trích xuất và hình thành như một thực thể độc lập được gọi là Truevision) đang làm việc để tiếp thị các công nghệ mới do AT&T phát triển cho bộ đệm khung màu. EPICenter đã làm việc trên hai thẻ đầu tiên, VDA (Bộ điều hợp hiển thị video) và ICB (bảng chụp ảnh) hoạt động trên hai loại tệp, .vda và .icb, đã được xử lý. Các định dạng tệp này đã được mã hóa và định dạng tệp cụ thể ít rộng hơn TGA đã được giới thiệu. TGA là một phần mở rộng cho những gì đã được sử dụng và cung cấp thông tin như chiều rộng, chiều cao, độ sâu pixel, bản đồ màu liên quan và nguồn gốc hình ảnh.

Phiên bản 2.0 của TGA, xuất bản năm 1989, kết hợp một số tính năng nâng cao như:

* Hình thu nhỏ
* Kênh Alpha
* Giá trị Gamma
* Siêu dữ liệu văn bản

Những người đóng góp chính cho phiên bản 2.0 của TGA bao gồm Shawn Steiner của Truevision, Kevin Fiedly và David Spoelstra.

## Thông số kỹ thuật định dạng tệp TGA TARGA

Một tệp TGA bao gồm 2 phần chính:

* Tiêu đề
* Thông tin Pixel màu

Tất cả các giá trị trong tệp TGA đều ở dạng littl-endian theo thông số định dạng.

### Tiêu đề TGA

Tiêu đề tệp TGA bao gồm 5 trường sau.

|Số trường|Độ dài |Tên trường |Mô tả|
---|---|---|---|
|1| 1 byte |độ dài ID| Độ dài của trường ID hình ảnh (0-255)|
|2| 1 byte |Loại bản đồ màu| Bản đồ màu có được bao gồm hay không (0 - biểu thị rằng không có dữ liệu bản đồ màu nào được bao gồm trong hình ảnh này. 1 - biểu thị rằng hình ảnh này có bản đồ màu.)|
|3| 1 byte |Loại hình ảnh| Loại nén và màu (0- Không bao gồm dữ liệu hình ảnh. 1- Không nén, Ảnh ánh xạ màu, 2- Không nén, Ảnh màu trung thực, 9- Mã hóa độ dài chạy, Ảnh ánh xạ màu, 11- Mã hóa độ dài chạy, Ảnh đen trắng )|
|4| 5 byte |Đặc tả bản đồ màu| Mô tả bản đồ màu |
|5| 10 byte |Đặc tả hình ảnh| Kích thước và định dạng hình ảnh|

### Dữ liệu Bản đồ Hình ảnh và Màu sắc

|Trường số. |Chiều dài |Trường |Mô tả|
---|---|---|---|
|6 |Từ trường độ dài ID hình ảnh| ID hình ảnh| Trường tùy chọn chứa thông tin nhận dạng|
|7 |Từ trường đặc tả bản đồ màu| Dữ liệu bản đồ màu| Bảng tra cứu chứa dữ liệu bản đồ màu|
|8 |Từ trường đặc tả hình ảnh| Dữ liệu hình ảnh| Được lưu trữ theo mô tả hình ảnh|

### Khu vực dành cho nhà phát triển (Tùy chọn)

TGA Phiên bản 2.0 cung cấp hỗ trợ cho các cải tiến/bổ sung bổ sung mà nhiều nhà phát triển muốn lưu trữ thêm thông tin. Thông tin là tùy chọn để nếu bộ giải mã TGA không thể giải thích nó, nó sẽ bị bỏ qua.

### Khu vực mở rộng (Tùy chọn)

|Số trường| Chiều dài| Trường |Mô tả|
---|---|---|---|
|10| 2 byte |Kích thước tiện ích mở rộng |Kích thước tính bằng byte của vùng mở rộng, luôn là 495|
|11| 41 byte| Tên tác giả |Tên tác giả. Nếu không được sử dụng, các byte phải được đặt thành NULL (\0) hoặc dấu cách|
|12| 324 byte| Bình luận tác giả| Một nhận xét, được tổ chức thành bốn dòng, mỗi dòng bao gồm 80 ký tự cộng với NULL|
|13| 12 byte| Dấu ngày/thời gian |Ngày và giờ hình ảnh được tạo|
|14| 41 byte| ID công việc||
|15| 6 byte| Thời gian làm việc| Số giờ, phút và giây dành để tạo tệp (để thanh toán, v.v.)|
|16| 41 byte| ID phần mềm |Ứng dụng đã tạo tệp.|
|17| 3 byte| Phiên bản phần mềm||
|18| 4 byte| Màu chủ đạo||
|19| 4 byte| Tỉ lệ pixel||
|20| 4 byte| Giá trị gamma||
|21| 4 byte| Độ lệch hiệu chỉnh màu |Số byte từ đầu tệp đến bảng hiệu chỉnh màu nếu có|
|22| 4 byte| Tem bưu chính | Số byte từ đầu tệp đến hình tem bưu chính nếu có|
|23| 4 byte| Độ lệch dòng quét| Số byte từ đầu tệp đến bảng dòng quét nếu có|
|24| 1 byte| Loại thuộc tính| Chỉ định kênh alpha|

### Chân trang tệp (Tùy chọn)

26 byte cuối cùng của tệp đại diện cho chân trang, nếu có nghĩa là nó có khả năng là tệp TGA phiên bản 2.

|Trường số| Chiều dài| Trường| Mô tả|
---|---|---|---|
|28| 4 byte| Phần bù mở rộng| Bù đắp theo byte từ đầu tệp|
|29| 4 byte| Nhà phát triển khu vực bù đắp| Bù đắp theo byte từ đầu tệp |
|30| 16 byte| Chữ ký| Chứa "TRUEVISION-XFILE"|
|31| 1 byte| | Chứa "."|
|32| 1 byte| | Chứa NULL|


## Người giới thiệu

* [Thông số định dạng tệp TGA 2.0](https://products.conholdate.app/viewer/view/rVqTeZPLAL/tga-file-format-specutions.pdf?default=view&preview = true.pdf)
* [TGA của Wikipedia](https://en.wikipedia.org/wiki/Truevision_TGA)

