{
  "date" : "2019-10-11",
  "keywords" :[ "tệp bmp", "định dạng tệp bmp", "tệp bmp là gì", "tệp", "ví dụ bmp", "phần mở rộng tệp bmp","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"BMP - Định dạng tệp hình ảnh",
  "description":"Tìm hiểu về định dạng tệp BMP và các API có thể tạo và mở tệp BMP.",
  "linktitle" : "BMP",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

# Tệp BMP là gì? #

Các tệp có phần mở rộng .BMP đại diện cho các tệp Hình ảnh Bitmap được sử dụng để lưu trữ các hình ảnh kỹ thuật số bitmap. Những hình ảnh này độc lập với bộ điều hợp đồ họa và còn được gọi là định dạng tệp bitmap (DIB) độc lập với thiết bị. Tính độc lập này phục vụ mục đích mở tệp trên nhiều nền tảng như Microsoft Windows và Mac. Định dạng tệp BMP có thể lưu trữ dữ liệu dưới dạng hình ảnh kỹ thuật số hai chiều ở cả định dạng đơn sắc cũng như màu với các độ sâu màu khác nhau.

## Thông số kỹ thuật định dạng tệp BMP ##

Ảnh bitmap độc lập với thiết bị hoạt động như một công cụ trợ giúp để trao đổi ảnh bitmap giữa các thiết bị và ứng dụng. Do sự phát triển liên tục của định dạng tệp này, thông tin chứa trong các tiêu đề có thể khác nhau tùy theo phiên bản của Bitmap. Một tệp bitmap đơn bao gồm các cấu trúc có kích thước cố định cũng như có thể thay đổi theo một trình tự cụ thể.

Các cấu trúc trong tệp Bitmap được sắp xếp theo thứ tự sau:


|Kết cấu|Tùy chọn|Kích thước|Mục đích
---|---|---|---|
|Tiêu đề tệp|Không|14|Để lưu trữ thông tin chung về tệp ảnh bitmap
|DIB Header|Không|Fixed-Size|Để lưu trữ thông tin chi tiết về hình ảnh bitmap và xác định định dạng pixel
|Mặt nạ bit bổ sung|Có|12 hoặc 16 byte|Để xác định định dạng pixel
|Bảng màu|Bán tùy chọn|Kích thước thay đổi|Để xác định màu sắc được sử dụng bởi dữ liệu hình ảnh bitmap
|Gap1|Có|Kích thước thay đổi|Căn chỉnh cấu trúc
|Mảng pixel|Không|Kích thước biến|Định dạng pixel được xác định bởi tiêu đề DIB hoặc Mặt nạ bit bổ sung.
|Gap2|Có|Kích thước thay đổi|Căn chỉnh cấu trúc
|Cấu hình màu ICC|Có|Kích thước thay đổi|Để xác định cấu hình màu để quản lý màu

Khi một hình ảnh bitmap được tải vào bộ nhớ, nó sẽ trở thành cấu trúc DIB, được Windows sử dụng thông qua API GDI của nó. Tiêu đề tệp không phải là một phần của cấu trúc dữ liệu này. Màu cũng có thể bao gồm các mục nhập 16 bit tạo thành các chỉ mục cho bảng màu được tham chiếu hiện tại thay vì các định nghĩa màu RGB rõ ràng. Chúng ta hãy xem xét chi tiết một số trong số này, đặc biệt là các tiêu đề.

### Tiêu đề tệp bitmap ###

Tiêu đề tệp Bitmap tương tự như các tiêu đề tệp khác được sử dụng để xác định tệp. Vì có nhiều biến thể khác nhau đối với định dạng tệp BMP, nên 2 byte đầu tiên của định dạng tệp BMP là ký tự "B" và sau đó là ký tự "M" trong bảng mã ASCII. Tất cả các giá trị số nguyên được lưu trữ ở định dạng little-endian.

|Offset hex|Offset dec|Kích thước|Mục đích
---|---|---|---|
|00|0|2 byte|Trường tiêu đề được sử dụng để xác định tệp BMP và DIB là 0x42 0x4D ở dạng thập lục phân, giống như BM trong ASCII. Nó có thể tuân theo các giá trị có thể.* **BM** – Windows 3.1x, 95, NT, ... v.v. * **BA** – mảng bitmap cấu trúc OS/2 * **CI** – cấu trúc OS/2 biểu tượng màu * **CP** – Con trỏ màu const OS/2 * **IC** – Biểu tượng cấu trúc OS/2 * **PT** – Con trỏ OS/2
|02|2|4 byte|Kích thước của tệp BMP tính bằng byte
|06|6|2 byte|Dành riêng; giá trị thực tế phụ thuộc vào ứng dụng tạo hình ảnh
|08|8|2 byte|Dành riêng; giá trị thực tế phụ thuộc vào ứng dụng tạo hình ảnh
|0A|10|4 byte|Phần bù, tức là địa chỉ bắt đầu, của byte nơi có thể tìm thấy dữ liệu hình ảnh bitmap (mảng pixel).

#### Tiêu đề DIB (tiêu đề thông tin bitmap) ####

Thông tin chi tiết về hình ảnh được đại diện bởi tiêu đề này. Dựa trên thông tin này, ứng dụng sẽ được xác định sẽ được sử dụng để hiển thị hình ảnh trên màn hình. Tất cả các tiêu đề như vậy chứa trường DWORD (32 bit), chỉ định kích thước của chúng, để ứng dụng có thể dễ dàng xác định tiêu đề được sử dụng trong hình ảnh. Về cơ bản, điều này là do định dạng DIB đã trải qua một số phần mở rộng. Sau đây là Tiêu đề DIB với các trường được liệt kê.

#### Bảng màu ####

Bảng màu BMP là một mảng cấu trúc xác định các giá trị cường độ RGB của từng màu trong bảng màu của thiết bị hiển thị. Mỗi pixel trong dữ liệu bitmap lưu trữ một giá trị duy nhất được sử dụng làm chỉ mục trong bảng màu. Thông tin màu được lưu trữ trong phần tử tại chỉ mục đó chỉ định màu của pixel đó. Tính khả dụng của màu trong tệp bitmap thay đổi như sau:

* Một, 4 và 8-bit - dự kiến sẽ luôn chứa một bảng màu
* Mười sáu, 24 và 32 bit - không bao giờ chứa bảng màu
* Các tệp BMP mười sáu và 32 bit - chứa các giá trị mặt nạ bitfield thay cho bảng màu

#### Bộ nhớ Pixel ####

Các pixel bản đồ bit được lưu trữ dưới dạng các bit được đóng gói trong các hàng trong đó kích thước của mỗi hàng được làm tròn lên thành bội số của 4 byte (DWORD 32 bit) bằng cách đệm. Không thể tính trực tiếp tổng số byte cần thiết để lưu trữ các pixel của hình ảnh bằng cách chỉ đếm các bit. Vì có liên quan đến phần đệm nên hiệu ứng làm tròn kích thước của mỗi hàng lên bội số của 4 byte là bắt buộc. Các byte đệm (không nhất thiết phải là 0) sẽ được thêm vào cuối các hàng để tăng độ dài của các hàng lên bội số của bốn byte. Khi mảng pixel được tải vào bộ nhớ, mỗi hàng phải bắt đầu tại một địa chỉ bộ nhớ là bội số của 4.

Hình ảnh thực sự được mô tả bằng biểu diễn DWORD 32-bit của mảng pixel. Thông thường các pixel được lưu trữ "từ dưới lên", bắt đầu ở góc dưới bên trái, đi từ trái sang phải, sau đó theo từng hàng từ dưới lên trên cùng của hình ảnh. Các định dạng pixel và tác động của chúng như được liệt kê bên dưới:

* Định dạng 1 bit trên mỗi pixel (1bpp) hỗ trợ 2 màu riêng biệt (ví dụ: đen và trắng).
* Định dạng 2 bit trên mỗi pixel (2bpp) hỗ trợ 4 màu riêng biệt và lưu trữ 4 pixel trên 1 byte, pixel ngoài cùng bên trái nằm trong hai bit quan trọng nhất. Mỗi giá trị pixel là một chỉ mục 2 bit trong một bảng có tối đa 4 màu.
* Định dạng 4 bit trên mỗi pixel (4bpp) hỗ trợ 16 màu riêng biệt và lưu trữ 2 pixel trên 1 byte, pixel ngoài cùng bên trái nằm trong phần nhỏ quan trọng hơn. Mỗi giá trị pixel là một chỉ mục 4 bit trong một bảng có tối đa 16 màu.
* Định dạng 8 bit trên mỗi pixel (8bpp) hỗ trợ 256 màu riêng biệt và lưu trữ 1 pixel trên 1 byte. Mỗi byte là một chỉ mục trong một bảng có tối đa 256 màu.
* Định dạng 16 bit trên mỗi pixel (16bpp) hỗ trợ 65536 màu riêng biệt và lưu trữ 1 pixel trên mỗi WORD 2 byte. Mỗi WORD có thể xác định các mẫu alpha, đỏ, lục và lam của pixel.
* Định dạng pixel 24 bit (24bpp) hỗ trợ 16.777.216 màu riêng biệt và lưu trữ 1 giá trị pixel trên 3 byte. Mỗi giá trị pixel xác định các mẫu màu đỏ, lục và lam của pixel (8.8.8.0.0 trong ký hiệu RGBAX). Cụ thể theo thứ tự: xanh dương, xanh lá cây và đỏ (8 bit cho mỗi mẫu).
* Định dạng 32 bit cho mỗi pixel (32bpp) hỗ trợ 4.294.967.296 màu riêng biệt và lưu trữ 1 pixel cho mỗi DWORD 4 byte. Mỗi DWORD có thể xác định các mẫu alpha, đỏ, lục và lam của pixel.

## Người giới thiệu ##

* [Định dạng siêu tệp Windows](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-wmf/4813e7fd-52d0-4f42-965f-228c8b7488d2)
* [Định dạng tệp BMP](https://en.wikipedia.org/wiki/BMP_file_format)

