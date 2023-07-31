{
  "date" : "2020-08-20",
  "keywords" :[ "tệp cff2", "định dạng tệp cff2", "tệp cff2 là gì", "tệp", "ví dụ cff2", "phần mở rộng tệp cff2","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CFF2 - Định dạng tệp phông chữ nhỏ gọn phiên bản 2",
  "description":"Tìm hiểu về Định dạng tệp CFF2 và API để tạo và mở tệp CFF2.",
  "linktitle" : "CFF2",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-21"
}

## Tệp CFF2 là gì?

Định dạng tệp CFF2 là phiên bản 2.0 của định dạng tệp CFF và cho phép lưu trữ hiệu quả các đường viền và siêu dữ liệu hình tượng tương tự như định dạng tệp CFF. CFF2 khác với CFF ở chỗ nó được dự định sử dụng trong ngữ cảnh phông chữ OpenType dưới dạng bảng 'sfnt' với thẻ CFF2. Nó không thể được sử dụng như một chương trình độc lập và phụ thuộc vào dữ liệu trong các bảng OpenType khác.

## Định dạng tệp CFF2

[Thông số định dạng tệp CFF2](https://learn.microsoft.com/en-us/typography/opentype/spec/cff2) chứa thông tin chi tiết về bố cục dữ liệu nội bộ, loại dữ liệu, bảng và thông tin nội bộ khác về định dạng tệp. Nó có thể được giới thiệu để tham khảo của nhà phát triển. Một số chi tiết về những điều này như sau.

### Bố cục dữ liệu

Dữ liệu nhị phân của định dạng tệp CFF2 được tổ chức hợp lý dưới dạng một số cấu trúc dữ liệu riêng biệt. Bố cục trong dữ liệu nhị phân như trong bảng sau.

|Bài viết |Bình luận|
---|---|
|Tiêu đề |Vị trí cố định|
|Đầu DICT| Vị trí cố định|
|CHỈ SỐ Subr toàn cầu| Vị trí cố định|
|Biến thể |Cửa hàng|
|FDSelect |Chỉ hiển thị nếu có nhiều hơn một Phông chữ DICT trong Phông chữ DICT INDEX.|
|Phông chữ DICT INDEX ||
|Mảng phông chữ DICT| Bao gồm trong Phông chữ DICT INDEX.|
|DICT riêng tư| Một cho mỗi Phông chữ DICT.|

Chỉ có ba cấu trúc đầu tiên dựa trên các vị trí cố định. Phần còn lại đạt được thông qua hiệu số và thứ tự của chúng có thể được thay đổi.

### Loại dữ liệu

Định dạng tệp CFF2 sử dụng các loại dữ liệu sau.

|Tên |Phạm vi |Mô tả|
---|---|---|
|uint8 |0 đến 255 |số không dấu 8 bit|
|uint16 |0 đến 65535| số không dấu 16-bit|
|uint32 |0 đến 4294967295| Số không dấu 32-bit|
|độ lệch |khác nhau| Độ lệch 1, 2, 3 hoặc 4 byte (được chỉ định bởi trường OffSize trong bảng Chỉ mục)|
|OffSize |1 đến 4| Số không dấu 1 byte chỉ định kích thước của một hoặc nhiều trường Offset|

Nó lưu trữ tất cả dữ liệu số nhiều byte và các trường bù theo thứ tự byte lớn về cuối. Định dạng CFF2 không có byte đệm vì nó không tôn trọng bất kỳ hạn chế căn chỉnh nào.

### Dữ liệu DICT

Các tệp CFF2 chứa dữ liệu từ điển phông chữ dưới dạng các cặp khóa-giá trị ở định dạng mã thông báo nhỏ gọn. Các khóa từ điển được mã hóa dưới dạng toán tử 1 hoặc 2 byte và các giá trị từ điển được mã hóa dưới dạng toán hạng số có kích thước thay đổi. Có ba cấu trúc sử dụng định dạng Dữ liệu DICT: `Top DICT`, `Font DICT` và `Private DICT`. Một số loại toán hạng số nguyên có kích thước khác nhau được xác định và được mã hóa như trong bảng sau (byte đầu tiên của toán hạng là b0, byte thứ hai là b1, v.v.).

|Kích thước |phạm vi b0 |Phạm vi giá trị |Tính toán giá trị|
---|---|---|---|
|1 |32 đến 246| -107 đến +107 |b0 - 139|
|2 |247 đến 250| +108 đến +1131 |(b0 - 247) * 256 + b1 + 108|
|2 |251 đến 254| -1131 đến -108| -(b0 - 251) * 256 - b1 - 108|
|3 |28| -32768 đến +32767| b1 << 8 | b2|
|5 |29| -(2^31) đến +(2^31 - 1)| b1 << 24 \| b2 << 16 \| b3 << 8 \| b4|

### Tiêu đề

Dữ liệu nhị phân bắt đầu bằng tiêu đề có định dạng được hiển thị trong Bảng bên dưới.

|Loại |Tên |Mô tả|
---|---|---|
|uint8| phiên bản chính| Định dạng phiên bản chính. Đặt thành 2.|
|uint8| nhỏPhiên bản| Định dạng phiên bản nhỏ. Đặt thành 0.|
|uint8| kích thước tiêu đề| Kích thước tiêu đề (byte).|
|uint16| topDictLength| Độ dài của cấu trúc DICT hàng đầu theo byte.|

## Người giới thiệu

* [Định dạng tệp CFF2](https://learn.microsoft.com/en-us/typography/opentype/spec/cff2)

