{
  "date" : "2019-10-11",
  "keywords" :[ "tệp tiff", "định dạng tệp tiff", "tệp tiff là gì", "tệp", "ví dụ tiff", "phần mở rộng tệp tiff","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TIFF - Định dạng tệp hình ảnh",
  "description":"Tìm hiểu về định dạng tệp TIFF và các API có thể tạo và mở tệp TIFF.",
  "linktitle" : "TIFF",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Tệp TIFF là gì?

TIFF hoặc TIF, Định dạng tệp hình ảnh được gắn thẻ, đại diện cho các hình ảnh raster được sử dụng trên nhiều loại thiết bị tuân thủ tiêu chuẩn định dạng tệp này. Nó có khả năng mô tả dữ liệu hình ảnh hai cấp độ, thang độ xám, bảng màu và đầy đủ màu sắc trong một số không gian màu. Nó hỗ trợ các lược đồ nén không mất mát cũng như không mất dữ liệu để lựa chọn giữa không gian và thời gian cho các ứng dụng sử dụng định dạng. Định dạng này không phụ thuộc vào máy và không có giới hạn như bộ xử lý, hệ điều hành hoặc hệ thống tệp.

## Lịch sử tóm tắt về định dạng tệp TIFF

Định dạng tệp TIFF ban đầu được Aldus Corporation tạo ra vào mùa thu năm 1986, sau một loạt cuộc họp với các nhà sản xuất máy quét và nhà phát triển phần mềm khác nhau. Mục đích chính của định dạng tệp TIFF là cung cấp định dạng tệp hình ảnh được quét phổ biến cho tất cả các nhà cung cấp máy quét để bàn. Bắt đầu với việc chỉ hỗ trợ định dạng hình ảnh nhị phân, định dạng này đã phát triển để hỗ trợ các hình ảnh màu và thang độ xám theo thời gian. Phiên bản ban đầu của thông số kỹ thuật định dạng tệp TIFF có thể được gắn nhãn là Reivision 3.0 vì đã có hai bản phát hành dự thảo trước đó. Bản sửa đổi lớn 5.0 đã được xuất bản vào năm 1988 bổ sung hỗ trợ cho hình ảnh màu bảng màu và nén LZW. Bản sửa đổi 6.0 của các định dạng tệp TIFF đã được xuất bản vào năm 1992 sau đó. Năm 1994, Adobe Systems đã mua lại Aldus và các thông số kỹ thuật hiện có sẵn và được duy trì bởi Adobe Systems.

## Thông số kỹ thuật định dạng tệp TIFF

Định dạng tệp TIFF có thể mở rộng và đã trải qua một số sửa đổi cho phép đưa vào lượng thông tin cá nhân hoặc mục đích đặc biệt không giới hạn. Tệp TIFF bắt đầu bằng tiêu đề 8 byte trong đó các byte được đánh số từ 0 đến N. Tệp TIFF lớn nhất có thể có độ dài 2**32 byte. Tệp bắt đầu bằng tiêu đề tệp hình ảnh 8 byte trỏ trực tiếp đến tệp hình ảnh (IFD). Một IFD chứa thông tin về hình ảnh cũng như các con trỏ tới dữ liệu hình ảnh thực tế.

### Tiêu đề tệp TIFF

Tiêu đề tệp TIFF 8 byte chứa thông tin sau:

**Byte 0-1:** Thứ tự byte được sử dụng trong tệp. Giá trị pháp lý là:“II”(4949.H)“MM” (4D4D.H).

Ở định dạng “II”, thứ tự byte luôn từ byte có trọng số thấp nhất đến byte có trọng số cao nhất, cho cả số nguyên 16 bit và 32 bit. Đây được gọi là thứ tự byte cuối nhỏ. Ở định dạng “MM”, thứ tự byte luôn từ quan trọng nhất đến ít quan trọng nhất, cho cả số nguyên 16 bit và 32 bit. Đây được gọi là thứ tự byte lớn về cuối.

**Byte 2-3:** Một số tùy ý nhưng được chọn cẩn thận (42) để xác định thêm tệp dưới dạng tệp TIFF. Thứ tự byte phụ thuộc vào giá trị của Byte 0-1.

**Bytes 4-7:** Độ lệch (tính bằng byte) của IFD đầu tiên. Thư mục có thể ở bất kỳ vị trí nào trong tệp sau tiêu đề nhưng phải bắt đầu trên ranh giới từ. Đặc biệt, một Thư mục tệp hình ảnh có thể theo dữ liệu hình ảnh mà nó mô tả. Người đọc phải đi theo các con trỏ đến bất cứ nơi nào chúng có thể dẫn đến. Thuật ngữ bù byte luôn được sử dụng trong tài liệu này để chỉ một vị trí đối với phần đầu của tệp TIFF. Byte đầu tiên của tệp có độ lệch là 0.

### Thư mục tệp hình ảnh

Một IFD chứa thông tin về hình ảnh cũng như các con trỏ tới dữ liệu hình ảnh thực tế. Nó bao gồm 2 byte đếm số mục nhập thư mục (nghĩa là số trường), theo sau là một chuỗi các mục nhập trường 12 byte , theo sau là độ lệch 4 byte của IFD tiếp theo (hoặc 0 nếu không có). Phải có ít nhất 1 IFD trong tệp TIFF và mỗi IFD phải có ít nhất một mục nhập.

#### Mục nhập IFD

Mỗi Mục nhập IFD 12 byte có định dạng sau.


|Byte|Mô tả
---|---|
|0-1|Thẻ xác định trường
|2-3|Loại trường
|4-7|Số lượng của loại được chỉ định
|8-11|Phần bù giá trị, phần bù tệp (tính bằng byte) của Giá trị cho trường. Giá trị dự kiến sẽ bắt đầu trên một ranh giới từ; do đó Giá trị Offset tương ứng sẽ là một số chẵn. Phần bù tệp này có thể trỏ đến bất kỳ đâu trong tệp, ngay cả sau dữ liệu hình ảnh

Trường TIFF là một thực thể logic bao gồm thẻ TIFF và giá trị của nó. Khái niệm logic này được triển khai dưới dạng Mục nhập IFD, cộng với giá trị thực nếu nó không khớp với phần giá trị/độ lệch, 4 byte cuối cùng của Mục nhập IFD. Thuật ngữ trường TIFF và mục nhập IFD có thể hoán đổi cho nhau trong hầu hết các ngữ cảnh.

### TIFF cơ sở ###

Baseline TIFF là cốt lõi của TIFF, yếu tố cần thiết mà tất cả các nhà phát triển TIFF chính nên hỗ trợ trong các sản phẩm của họ. Việc tuân thủ định dạng TIFF tùy thuộc vào việc tuân thủ các yêu cầu TIFF cơ bản. Các yêu cầu này được ghi lại đầy đủ trong tài liệu thông số kỹ thuật 6.0.

#### Nhiều hình ảnh trên mỗi tệp ####

Có thể có nhiều IFD trong một tệp TIFF. Mỗi IFD định nghĩa một tệp con. Một cách sử dụng tiềm năng của các tệp con là để mô tả các hình ảnh liên quan, chẳng hạn như các trang của một bản truyền fax. Không bắt buộc phải có trình đọc TIFF cơ bản để đọc bất kỳ IFD nào ngoài IFD đầu tiên.

#### Các loại hình ảnh ####

Baseline TIFF Image có các loại sau:

**Hai mặt:** Hình ảnh hai mặt chứa hai màu—đen và trắng. TIFF cho phép ứng dụng ghi dữ liệu hai mức ở định dạng trắng bằng 0 hoặc đen bằng 0. Trường ghi lại thông tin này được gọi là **PhotometricInterpretation**.

* RGB đủ màu

Thông tin diễn giải trắc quang cho hình ảnh Bilevel như sau:

Thẻ = 262 (106.H)
Loại = NGẮN
**Giá trị**

|Giá trị|Mô tả|
---|---|
|0|Đối với ảnh hai cấp độ và thang độ xám: 0 được tạo ảnh thành màu trắng. Giá trị max-mum được chụp ảnh dưới dạng màu đen. Đây là giá trị bình thường cho Compression#2|
|1|BlackIsZero. Đối với hình ảnh hai cấp độ và thang độ xám: 0 được tạo ảnh thành màu đen. Giá trị max-mum được chụp ảnh dưới dạng màu trắng. Nếu giá trị này được chỉ định cho Nén số 2, hình ảnh sẽ hiển thị và in ngược lại.|

**Thang độ xám:** Hình ảnh thang độ xám là sự tổng quát hóa của hình ảnh hai cấp độ. Hình ảnh hai cấp độ chỉ có thể lưu trữ dữ liệu hình ảnh đen trắng, nhưng hình ảnh thang độ xám cũng có thể lưu trữ các sắc thái của màu xám. Để mô tả những hình ảnh như vậy, bạn phải thêm hoặc thay đổi các trường sau. Các trường bắt buộc khác giống như các trường bắt buộc đối với hình ảnh hai mặt. Đối với hình ảnh thang độ xám, Nén # 1 hoặc 32773 (PackBits). Trong Baseline TIFF, hình ảnh thang độ xám có thể được lưu trữ dưới dạng dữ liệu không nén hoặc được nén bằng thuật toán PackBits.

Thông tin **BitsPerSample** cho hình ảnh thang độ xám như sau:

Thẻ = 258 (102.H)
Loại = NGẮN

Số bit trên mỗi thành phần. Các giá trị cho phép đối với hình ảnh thang độ xám TIFF của Đường cơ sở là 4 và 8, cho phép 16 hoặc 256 sắc thái xám riêng biệt.

**Bảng màu:** Hình ảnh bảng màu tương tự như hình ảnh thang độ xám. Chúng vẫn có một thành phần trên mỗi pixel, nhưng giá trị thành phần được sử dụng làm chỉ mục trong bảng tra cứu RGB đầy đủ. Để mô tả những hình ảnh như vậy, bạn cần thêm hoặc thay đổi các trường sau. Các trường bắt buộc khác giống như trường dành cho hình ảnh thang độ xám.
Thông tin diễn giải trắc quang cho ảnh Palette-Color như sau:

Giải thích trắc quang = 3 (Bảng màu).
ColorMapTag = 320 (140.H)
Loại = NGẮN
N = 3 * (2 Bit trên mỗi mẫu)

Trường này xác định bản đồ màu Đỏ-Lục-Xanh lam (thường được gọi là bảng tra cứu) cho ảnh màu bảng màu. Trong hình ảnh có bảng màu, giá trị pixel được sử dụng để lập chỉ mục cho bảng tra cứu RGB. Ví dụ: một pixel màu bảng màu có giá trị 0 sẽ được hiển thị theo bộ ba Đỏ, Xanh lục, Xanh lam thứ 0. Trong Bản đồ màu TIFF, tất cả các giá trị Đỏ xuất hiện trước, tiếp theo là các giá trị Xanh lục, sau đó là các giá trị Xanh lam. Trong ColorMap, màu đen được biểu thị bằng 0,0,0 và màu trắng được biểu thị bằng 65535, 65535, 65535.

**Đầy đủ màu RGB:** Trong hình ảnh RGB, mỗi pixel được tạo thành từ ba thành phần: đỏ, lục và lam. Không có ColorMap. Để mô tả một hình ảnh RGB, bạn cần thêm hoặc thay đổi các trường và giá trị sau. Các trường bắt buộc khác giống như các trường bắt buộc đối với hình ảnh bảng màu.

BitsPerSample = 8,8,8. Mỗi thành phần có độ sâu 8 bit trong hình ảnh Baseline TIFF RGB.

PhotometricInterpretation = 2 (RGB) và không có ColorMap.

Thẻ = 277 (115.H)
Loại = NGẮN
Số lượng thành phần trên mỗi pixel. Con số này là 3 đối với hình ảnh RGB, trừ khi có thêm mẫu.

## Người giới thiệu ##

* [Định dạng tệp TIFF - Wikipedia](https://en.wikipedia.org/wiki/TIFF)

