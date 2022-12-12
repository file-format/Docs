{
  "date" : "2021-04-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ISO - Định dạng tệp ảnh đĩa",
  "description":"Tệp ISO là gì và các API có thể tạo và mở tệp ISO.",
  "linktitle" : "ISO",
  "menu" : {
    "docs" : {
     "identifier": "compression-iso",
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-19"
}

## Tập tin ISO là gì?

Tệp có phần mở rộng .iso là tệp hình ảnh đĩa lưu trữ không nén, đại diện cho nội dung của toàn bộ dữ liệu trên đĩa quang chẳng hạn như CD hoặc DVD. Dựa trên tiêu chuẩn [ISO-9660](https://www.iso.org/standard/17505.html), định dạng tệp hình ảnh ISO chứa dữ liệu đĩa cùng với thông tin hệ thống tệp được lưu trữ trong đó. Khả năng của các tệp ISO chứa một bản sao chính xác của nội dung làm cho nó trở thành loại tệp hoàn hảo để tạo các bản sao của đĩa CD/DVD và chủ yếu được sử dụng để lưu trữ dữ liệu có thể khởi động để cài đặt. Hầu hết các tệp ISO được ghi vào USB/CD/DVD dưới dạng nội dung có thể khởi động để khởi động máy để cài đặt. Các tệp ISO có loại MIME application/x-iso9660-image.

## Định dạng tệp ISO

Định dạng tệp ISO không giống như các định dạng tệp tệp chứa khác mặc dù nó lưu trữ nội dung dữ liệu được chỉ định. Kho lưu trữ được tạo dưới dạng tệp nhị phân với cấu trúc chính xác của nội dung và thông tin hệ thống tệp. Định dạng tệp ISO được [ISO-9660](https://en.wikipedia.org/wiki/ISO_9660) mô tả như sau.

### Cấu trúc cấp cao nhất của tệp ISO

Cấu trúc tổng thể của tệp bao gồm:

* `Khu vực hệ thống` - 32.768 byte và không được ISO_9660 sử dụng
* `Vùng dữ liệu` - bao gồm bộ mô tả Khối lượng và các bảng Đường dẫn, thư mục và tệp

### Bộ mô tả âm lượng

Vùng dữ liệu bắt đầu với bộ mô tả âm lượng, một bộ gồm một hoặc nhiều bộ mô tả âm lượng được kết thúc bằng bộ kết thúc bộ mô tả âm lượng. Chúng hoạt động chung như một tiêu đề cho vùng dữ liệu, mô tả nội dung của nó (tương tự như khối tham số BIOS được sử dụng bởi các đĩa định dạng FAT, HPFS và NTFS).

Bộ mô tả âm lượng như hình bên dưới.

|Bộ mô tả âm lượng|
---|
|Bộ mô tả âm lượng #1|
|...|
|Bộ mô tả âm lượng #N|
|Bộ mô tả âm lượng bộ kết thúc|

#### Bộ mô tả âm lượng

Mỗi bộ mô tả âm lượng có kích thước 2048 byte và có cấu trúc như sau:

|Phần |Loại |Định danh |Phiên bản |Dữ liệu|
---|---|---|---|---|
|Kích thước |1 byte |5 byte (luôn là 'CD001') |1 byte (luôn là 0x01) |2.041 byte|

## Người giới thiệu

* [Hình ảnh đĩa quang - Wikipedia](https://en.wikipedia.org/wiki/Optical_disc_image)
* [Chữ ký tệp](https://www.garykessler.net/library/file_sigs.html)
* [ISO 9660 - Wikipedia](https://vi.wikipedia.org/wiki/ISO_9660)

