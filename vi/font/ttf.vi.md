{
  "date" : "2020-08-20",
  "keywords" :[ "tệp ttf", "định dạng tệp ttf", "tệp ttf là gì", "tệp", "ví dụ ttf", "phần mở rộng tệp ttf","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TTF - Định dạng tệp phông chữ TrueType",
  "description":"Phông chữ TrueType (TTF) dựa trên thông số kỹ thuật công nghệ phông chữ kỹ thuật số được thiết kế ban đầu bởi Apple, Inc. Cả Apple và Microsoft đều sử dụng TTF trên hệ điều hành Mac và Windows.",
  "linktitle" : "TTF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-09-21"
}

## Tệp TTF là gì?

Một tệp có phần mở rộng .ttf đại diện cho các tệp phông chữ dựa trên công nghệ phông chữ thông số kỹ thuật TrueType. Ban đầu nó được thiết kế và tung ra bởi Apple Computer, Inc cho Mac OS và sau đó được Microsoft áp dụng cho Windows OS. Phông chữ TrueType cung cấp chất lượng hiển thị cao nhất trên màn hình máy tính và máy in mà không phụ thuộc vào độ phân giải. Tất cả các ứng dụng hiện đại sử dụng phông chữ đều có thể hoạt động với các tệp TTF. Các tệp phông chữ TTF có sẵn miễn phí trên internet và cũng có thể được chuyển đổi sang các định dạng tệp phông chữ khác như OTF và WOFF.

## Tóm tắt lịch sử

Được thiết kế bởi Apply Computer, Inc vào những năm 1980 cho MacOS, định dạng phông chữ TTF nhằm mục đích giải quyết một số hạn chế kỹ thuật của định dạng Loại 1 của Adobe. Apple đã hỗ trợ phông chữ TrueType trong Mac vào năm 1991. Mục tiêu thiết kế đằng sau phông chữ TTF là hiệu quả trong lưu trữ và xử lý cũng như khả năng mở rộng. Dựa trên khả năng mở rộng này, các phông chữ hiện có có thể được chuyển đổi sang định dạng TrueType.

Microsoft lần đầu tiên sử dụng phông chữ TrueType trong Windows 3.1 vào tháng 4 năm 1992 sau khi Apple đồng ý cấp phép TrueType cho Microsoft. Nó đã cải thiện cơ chế rasterization, đồng thời cải thiện hiệu quả và hiệu suất của nó.

## Thông số kỹ thuật định dạng tệp True Type

Tệp phông chữ TrueType là tệp nhị phân bao gồm một chuỗi các bảng được nối. Mỗi bảng là một chuỗi các từ và có một tên gọi là `Tag`. Mỗi thẻ thuộc loại dữ liệu uint32 và bao gồm bốn ký tự. Bảng đầu tiên trong tệp là thư mục phông chữ cho phép truy cập vào các bảng khác trong tệp phông chữ. Dữ liệu phông chữ được chứa trong các bảng khác theo sau bảng thư mục phông chữ. Vì mỗi bảng có thể truy cập được bằng thẻ của nó nên các bảng có thể xuất hiện theo bất kỳ thứ tự nào trong tệp.

Các bảng bắt buộc và tên thẻ của chúng được hiển thị trong bảng sau.

|**Thẻ**|**Bảng**|
---|---|
|'cmap'| ký tự để ánh xạ glyph |
|'glyf'| dữ liệu hình tượng |
|'đầu'| tiêu đề phông chữ |
|'hea'| tiêu đề ngang|
|'hmtx'| chỉ số ngang|
|'địa điểm'| chỉ mục đến vị trí|
|'maxp'| cấu hình tối đa|
|'tên'| đặt tên|
|'đăng'| Hậu bút|

### Loại dữ liệu
Phông chữ TrueType sử dụng số nguyên tiêu chuẩn và các loại dữ liệu bổ sung như được liệt kê trong bảng sau.

|**Loại dữ liệu** | **Mô tả** |
---|---|
|ngắnFrac| Phân số có dấu 16 bit|
|Đã sửa| Số điểm cố định có dấu 16,16-bit|
|Fword| Số nguyên có dấu 16 bit mô tả một đại lượng trong FUnits, khoảng cách nhỏ nhất có thể đo được trong không gian em.|
|uFWord| Số nguyên không dấu 16 bit mô tả một đại lượng trong FUnits, khoảng cách nhỏ nhất có thể đo được trong không gian em.|
|F2Dot14| Số cố định có dấu 16 bit với 14 bit thấp biểu thị phân số.|
|longDateTime| Định dạng bên trong dài của ngày tính bằng giây kể từ 12:00 nửa đêm, ngày 1 tháng 1 năm 1904. Nó được biểu diễn dưới dạng số nguyên 64 bit có dấu.|

### Thư mục phông chữ

Bảng đầu tiên trong phông chữ TrueType là thư mục phông chữ cung cấp quyền truy cập vào thông tin cần thiết để truy cập dữ liệu trong các bảng khác. Nó còn bao gồm:

* `Bảng phụ offset` - lưu giữ bản ghi của các bảng trong phông chữ và cung cấp thông tin offset để truy cập từng bảng trong thư mục
* `Thư mục bảng` - Chứa các mục cho mỗi bảng trong phông chữ

#### Offset SubTable
Bảng phụ offset được hiển thị bên dưới.

|**Loại**|**Tên**|**Mô tả**|
---|---|---|
|uint32| loại máy chia tỷ lệ | Một thẻ cho biết bộ chia tỷ lệ OFA được sử dụng để rasterize phông chữ này; xem ghi chú về loại máy chia tỷ lệ bên dưới để biết thêm thông tin.|
|uint16| numTables| số bàn|
|uint16| phạm vi tìm kiếm| (sức mạnh tối đa của 2 <= numTables)*16|
|uint16| mụcSelector| log2(sức mạnh tối đa của 2 <= numTables)|
|uint16| phạm viShift| numTables*16-searchRange|

#### Bảng thư mục
Thư mục bảng xuất hiện ngay sau bảng phụ bù. Cấu trúc của nó như trong bảng sau.

|**Loại**|**Tên**|**Mô tả**|
---|---|---|
|uint32| thẻ| mã định danh 4 byte|
|uint32| tổng kiểm tra| tổng kiểm tra cho bảng này |
|uint32| bù | offset từ đầu sfnt|
|uint32| chiều dài| độ dài của bảng này theo byte (độ dài thực tế không phải độ dài được đệm)|

Mỗi bảng trong tệp phông chữ phải có mục nhập thư mục bảng riêng. Các mục nhập trong một bảng phải được sắp xếp theo thứ tự tăng dần theo thẻ.


## Người giới thiệu
* [Hướng dẫn tham khảo phông chữ TrueType](https://developer.apple.com/fonts/TrueType-Reference-Manual/)
* [Tổng quan về TrueType](https://learn.microsoft.com/en-us/typography/truetype/)

