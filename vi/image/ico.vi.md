{
  "date" : "2019-10-11",
  "keywords" :[ "tệp ico", "định dạng tệp ico", "tệp ico là gì", "tệp", "ví dụ ico", "phần mở rộng tệp ico","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ICO - Định dạng tệp hình ảnh",
  "description":"Tìm hiểu về định dạng tệp ICO và các API có thể tạo và mở tệp ICO.",
  "linktitle" : "ICO",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Tệp ICO là gì?

Các tệp có phần mở rộng ICO là các loại tệp hình ảnh được sử dụng làm biểu tượng đại diện cho một ứng dụng trên [Microsoft Windows](https://www.microsoft.com/en-us/windows). Chúng có kích thước, hỗ trợ màu sắc và độ phân giải khác nhau để phù hợp với yêu cầu của màn hình. Một định dạng tệp hình ảnh tương tự khác trên Microsoft Windows là [CUR](/vi/image/cur/) để biểu diễn con trỏ và xác định điểm phát sóng trong tiêu đề hình ảnh. Trên MacOS, định dạng tệp ICNS phục vụ mục đích giống như tệp ICO. Một số trang web cũng như ứng dụng trực tuyến cung cấp tính năng tạo các tệp như vậy và chuyển đổi các định dạng hình ảnh khác như [BMP](/vi/image/bmp/), [PNG](/vi/image/png/), v.v. sang định dạng tệp biểu tượng. Loại phương tiện Internet đã đăng ký IANA chính thức cho các tệp ICO là image/vnd.microsoft.icon.

## Lược Sử ##

Các biểu tượng đã được giới thiệu cùng với sự ra mắt của Microsoft Windows 1.0. Chúng có kích thước 32x32 và đơn sắc. Với sự xuất hiện của win32, hỗ trợ cho hình ảnh biểu tượng có màu sắc trung thực đã được giới thiệu với kích thước lên tới 256x256 pixel. Windows XP là hệ điều hành đầu tiên cung cấp hỗ trợ cho hình ảnh biểu tượng màu 32 bit, cho phép thêm các vùng bán trong suốt như bóng đổ, hiệu ứng khử răng cưa và giống như thủy tinh vào biểu tượng. Microsoft chỉ đề xuất kích thước biểu tượng lên tới 48 × 48 pixel cho Windows XP. Windows Vista đã thêm chế độ xem biểu tượng 256×256 pixel vào Windows Explorer, cũng như hỗ trợ định dạng [PNG](/vi/image/png/) được nén. Với người dùng sử dụng độ phân giải cao hơn và chế độ DPI cao, các định dạng biểu tượng lớn hơn (chẳng hạn như 256×256) được khuyến nghị.

## Định dạng tệp ICO ##

Một tệp ICO duy nhất bao gồm một hoặc nhiều hình ảnh nhỏ có nhiều kích cỡ và độ sâu màu. Sự hiện diện của hình ảnh có nhiều kích cỡ là để chia tỷ lệ thích hợp ở các độ phân giải màn hình khác nhau. Tất cả các giá trị trong tệp ICO/CUR được thể hiện theo thứ tự byte [little-endian](https://en.wikipedia.org/wiki/Little-endian).

Tệp ICO bao gồm tiêu đề Biểu tượng, Thư mục biểu tượng,

|Trường|Mô tả
---|---|
|Tiêu đề biểu tượng|Lưu trữ thông tin chung về tệp ICO.
|Directory[1..n]|Lưu trữ thông tin chung về mọi hình ảnh trong tệp.
|Biểu tượng #1|"Dữ liệu" thực tế cho hình ảnh đầu tiên ở định dạng AND/XOR DIB cũ hoặc PNG mới hơn
|...|
|Biểu tượng #n|Dữ liệu cho hình ảnh biểu tượng cuối cùng

### Tiêu đề ###

|Độ lệch|Kích thước (tính bằng byte)|Mục đích
---|---|---|
|0|2|Dành riêng. Phải luôn bằng 0.
|2|2|Chỉ định loại hình ảnh: 1 cho hình ảnh biểu tượng (.ICO), 2 cho hình ảnh con trỏ (.CUR). Các giá trị khác không hợp lệ.
|4|2|Chỉ định số lượng hình ảnh trong tệp.

### Danh mục ###

Thư mục chứa trong tệp ICO, được biểu diễn dưới dạng cấu trúc ICONDIR, chứa cấu trúc ICONDIRECTORY cho mỗi hình ảnh trong tệp. Điều tương tự cũng được theo sau bởi một khối liền kề của tất cả dữ liệu bitmap hình ảnh. Điều này là như hình dưới đây.

|Bù đắp|Kích thước|Mô tả
---|---|---|
|0 (0)|1|Chiều rộng, phải là 0 nếu 256 pixel
|1 (1)|1|Chiều cao, phải là 0 nếu 256 pixel
|2 (2)|1|Đếm màu, phải bằng 0 nếu có hơn 256 màu
|3 (3)|1|Dành riêng, phải là 0
|4 (4)|2|Các mặt phẳng màu khi ở định dạng .ICO, phải là 0 hoặc 1 hoặc điểm phát sóng X khi ở định dạng .CUR
|6 (6)|2|Số bit trên pixel khi ở định dạng .ICO hoặc điểm phát sóng Y khi ở định dạng .CUR
|8 (8)|4|Kích thước của dữ liệu bitmap tính bằng byte.
|12 (C)|4|Offset trong tệp.

## Người giới thiệu ##

* [ICO - Theo Wikipedia](https://en.wikipedia.org/wiki/ICO_(file_format))
* [IANA - vnd.microsoft.icon](http://www.iana.org/assignments/media-types/image/vnd.microsoft.icon)

