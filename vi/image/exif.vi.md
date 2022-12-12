{
  "date" : "2019-10-11",
  "keywords" :[ "tệp exif", "định dạng tệp exif", "tệp exif là gì", "tệp", "ví dụ exif", "phần mở rộng tệp exif","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EXIF",
  "description":"Tìm hiểu về định dạng tệp EXIF và các API có thể tạo và mở tệp EXIF.",
  "linktitle" : "EXIF",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Tệp EXIF là gì?
EXIF là viết tắt của “Định dạng tệp hình ảnh có thể thay đổi”, định nghĩa đầu tiên được đưa ra bởi [Hiệp hội Công nghiệp Máy ảnh Nhật Bản](https://en.wikipedia.org/wiki/Japan_Electronic_Industries_Development_Association) (JCIA) vào năm 1985. Tiêu chuẩn này được quản lý bởi Japan Electronics và Hiệp hội Công nghiệp Công nghệ Thông tin (JEITA) cho đến ngày hôm nay. EXIF là một tiêu chuẩn cho các thông số kỹ thuật của định dạng hình ảnh và âm thanh chủ yếu được sử dụng bởi máy ảnh kỹ thuật số và máy quét.

Tiêu chuẩn EXIF bao gồm thông tin gắn thẻ và siêu dữ liệu với tệp hình ảnh. Siêu dữ liệu có thể chứa thông tin như kiểu máy ảnh, tốc độ màn trập, Ngày và giờ, khẩu độ, nhà sản xuất, thời gian phơi sáng, độ phân giải X, độ phân giải Y, v.v. Thông thường, dữ liệu EXIF được ẩn theo mặc định. Để xem dữ liệu EXIF, người ta phải chọn các thuộc tính xem trong ứng dụng xem ảnh. Siêu dữ liệu Exif cũng có thể bao gồm hình thu nhỏ cùng với dữ liệu kỹ thuật và hình ảnh chính trong một tệp hình ảnh.

## Lịch sử và Phiên bản ##

* Vào tháng 10 năm 1995, JEIDA đã thiết lập Phiên bản 1. Trong phiên bản này, JEIDA đã xác định cấu trúc, bao gồm định dạng dữ liệu hình ảnh và thông tin thuộc tính cũng như các thẻ cơ bản.
* Tháng 11 năm 1997, phiên bản 1.1 được giới thiệu với hầu hết các thẻ từ phiên bản 1 nhưng cũng bổ sung các điều khoản cho thông tin thuộc tính tùy chọn và thao tác định dạng.
* Tháng 6 năm 1998, Phiên bản 2 với không gian màu sRGB, hình thu nhỏ và tệp âm thanh được nén.
* Tháng 12 năm 1998, Phiên bản 2.1 với thông tin thuộc tính và lưu trữ nâng cao.
* Tháng 2 năm 2002, Phiên bản 2.2, phiên bản 2.1 cải tiến với việc bổ sung tính năng hoàn thiện bản in.
* Tháng 9 năm 2003, Phiên bản 2.21 với không gian màu tùy chọn được gọi là adobe RGB.

## Định dạng tệp EXIF

EXIF sử dụng các định dạng tệp sau với việc bổ sung siêu dữ liệu cụ thể.

1. [JPEG](/vi/image/jpeg/) - biến đổi cosin rời rạc (DCT) cho các tệp hình ảnh nén.
1. [TIFF](/vi/image/tiff/) Phiên bản 6.0 (RGB hoặc YCbCr) dành cho tệp hình ảnh không nén.
1. [RIFF](https://vi.wikipedia.org/wiki/Resource_Interchange_File_Format) [WAV](https://en.wikipedia.org/wiki/WAV) cho các tệp âm thanh (Tuyến tính [PCM](https:/ /en.wikipedia.org/wiki/Pulse-code_modulation) hoặc ITU-T [G.711](https://en.wikipedia.org/wiki/G.711) μ-Luật PCM dành cho dữ liệu âm thanh không nén và [ IMA](https://en.wikipedia.org/wiki/Interactive_Multimedia_Association)-[ADPCM](https://en.wikipedia.org/wiki/ADPCM) dành cho dữ liệu âm thanh nén).

### Điểm đánh dấu được sử dụng bởi EXIF ###

Điểm đánh dấu 0xFFE0~~0xFFEF là "Đánh dấu ứng dụng", được ứng dụng người dùng sử dụng. Ví dụ: các máy quay kỹ thuật số cũ hơn sử dụng JFIF (Định dạng trao đổi tệp JPEG) để lưu trữ hình ảnh. JFIF sử dụng Điểm đánh dấu APP0 (0xFFE0) để chèn dữ liệu cấu hình camera kỹ thuật số và hình thu nhỏ. Ngoài ra, EXIF cũng sử dụng Điểm đánh dấu ứng dụng để chèn dữ liệu, nhưng EXIF sử dụng Điểm đánh dấu APP1 (0xFFE1) để tránh xung đột với định dạng JFIF. Mọi định dạng tệp EXIF bắt đầu từ định dạng này.


|Dấu hiệu SOI|Dữ liệu APP1|Dữ liệu APP1|Dấu hiệu khác
---|---|---|---|
|FFD8|FFE1|SSSS 457869660000 TTTT......|FFXX SSSS DDDD......

Nó bắt đầu từ SOI (0xFFD8) Marker, vì vậy nó là một tệp JPEG. Sau đó, Điểm đánh dấu APP1 sẽ theo sau ngay lập tức. Tất cả dữ liệu của EXIF được lưu trữ trong vùng dữ liệu APP1 này. Phần "SSSS" ở bảng trên có nghĩa là kích thước của vùng dữ liệu APP1 (vùng dữ liệu EXIF). Xin lưu ý rằng kích thước "SSSS" cũng bao gồm kích thước của bộ mô tả. Sau "SSSS", dữ liệu APP1 bắt đầu. Phần đầu tiên là dữ liệu đặc biệt để nhận dạng EXIF hay không, ký tự ASCII "EXIF" và 2 byte 0x00 được sử dụng. Sau khu vực Điểm đánh dấu APP1, các Điểm đánh dấu JPEG khác theo sau.

### Cấu trúc dữ liệu Exif ###

Cấu trúc thô của dữ liệu EXIF (APP1) được hiển thị như bên dưới. Như đã thảo luận ở trên, dữ liệu EXIF bắt đầu từ ký tự ASCII "EXIF" và 2 byte 0x00, sau đó là dữ liệu EXIF. EXIF sử dụng định dạng TIFF để lưu trữ dữ liệu.


|FFE1|Đánh dấu APP1
---|---|
|SSSS|Dữ liệu APP1|Kích thước dữ liệu APP1
|45786966 0000|Tiêu đề Exif
|49492A00 08000000|TIFF tiêu đề
|XXXX. . . .|IFD0 (hình ảnh chính)|Danh mục
|LLLLLLLL|Liên kết đến IFD1
|XXXX. . . .|Vùng dữ liệu của IFD0
|XXXX. . . .|Exif SubIFD|Danh mục
|00000000|Kết thúc liên kết
|XXXX. . . .|Vùng dữ liệu của Exif SubIFD
|XXXX. . . .|IFD1(hình thu nhỏ)|Danh mục
|00000000|Kết thúc liên kết
|XXXX. . . .|Vùng dữ liệu của IFD1
|FFD8XXXX. . . XXXFFD9|Hình thu nhỏ

#### Tiêu đề TIFF ####

tiêu đề tệp [TIFF](/vi/image/tiff/) 8 byte chứa thông tin sau:

`Byte 0-1:` Thứ tự byte được sử dụng trong tệp. Giá trị pháp lý là:“II”(4949.H)“MM” (4D4D.H).

Ở định dạng “II”, thứ tự byte luôn từ byte có trọng số thấp nhất đến byte có trọng số cao nhất, cho cả số nguyên 16 bit và 32 bit. Đây được gọi là thứ tự byte cuối nhỏ. Ở định dạng “MM”, thứ tự byte luôn từ quan trọng nhất đến ít quan trọng nhất, cho cả số nguyên 16 bit và 32 bit. Đây được gọi là thứ tự byte lớn về cuối.

`Byte 2-3:` Một số tùy ý nhưng được chọn cẩn thận (42) xác định thêm tệp là tệp TIFF. Thứ tự byte phụ thuộc vào giá trị của Byte 0-1.

`Bytes 4-7:` Độ lệch (tính bằng byte) của IFD đầu tiên. Thư mục có thể ở bất kỳ vị trí nào trong tệp sau tiêu đề nhưng phải bắt đầu trên ranh giới từ. Cụ thể, một Thư mục tệp hình ảnh có thể theo dữ liệu hình ảnh mà nó mô tả. Người đọc phải đi theo các con trỏ đến bất cứ nơi nào chúng có thể dẫn đến. Thuật ngữ bù byte luôn được sử dụng trong tài liệu này để chỉ một vị trí đối với phần đầu của tệp TIFF. Byte đầu tiên của tệp có độ lệch là 0.

#### Thư mục tệp hình ảnh ####

Một IFD chứa thông tin về hình ảnh cũng như các con trỏ tới dữ liệu hình ảnh thực tế. Nó bao gồm 2 byte đếm số mục nhập thư mục (nghĩa là số trường), theo sau là một chuỗi các mục nhập trường 12 byte , theo sau là độ lệch 4 byte của IFD tiếp theo (hoặc 0 nếu không có). Phải có ít nhất 1 IFD trong tệp TIFF và mỗi IFD phải có ít nhất một mục nhập.

##### Mục nhập IFD #####

Mỗi Mục nhập IFD 12 byte có định dạng sau.


|Byte|Mô tả
---|---|
|0-1|Thẻ xác định trường
|2-3|Loại trường
|4-7|Số lượng của loại được chỉ định
|8-11|Phần bù giá trị, phần bù tệp (tính bằng byte) của Giá trị cho trường. Giá trị dự kiến sẽ bắt đầu trên một ranh giới từ; do đó Giá trị Offset tương ứng sẽ là một số chẵn. File offset này có thể trỏ đến bất kỳ đâu trong file, ngay cả sau dữ liệu hình ảnh

Trường TIFF là một thực thể logic bao gồm thẻ TIFF và giá trị của nó. Khái niệm logic này được triển khai dưới dạng Mục nhập IFD, cộng với giá trị thực nếu nó không khớp với phần giá trị/độ lệch, 4 byte cuối cùng của Mục nhập IFD. Thuật ngữ trường TIFF và mục nhập IFD có thể hoán đổi cho nhau trong hầu hết các ngữ cảnh.

#### Hình thu nhỏ ####

Định dạng Exif chứa hình thu nhỏ của hình ảnh (ngoại trừ Ricoh RDC-300Z). Thông thường nó nằm bên cạnh IFD1. Có 3 định dạng cho hình thu nhỏ; Định dạng JPEG (JPEG sử dụng YCbCr), định dạng RGB TIFF, định dạng YCbCr TIFF.

##### Định dạng JPEG Hình thu nhỏ #####

Nếu giá trị của Thẻ nén(0x0103) trong IFD1 là '6', định dạng hình ảnh thu nhỏ là JPEG. Hầu hết hình ảnh Exif sử dụng định dạng JPEG cho hình thu nhỏ. Trong trường hợp đó, bạn có thể lấy phần bù của hình thu nhỏ bằng Thẻ JpegIFOffset(0x0201) trong IFD1, kích thước của hình thu nhỏ bằng Thẻ JpegIFByteCount(0x0202). Định dạng dữ liệu là định dạng JPEG thông thường, bắt đầu từ 0xFFD8 và kết thúc bằng 0xFFD9. Có vẻ như định dạng JPEG và kích thước 160x120 pixel là định dạng hình thu nhỏ được khuyến nghị cho Exif2.1 trở lên.

##### Hình thu nhỏ định dạng TIFF #####

Nếu giá trị của Thẻ Nén(0x0103) trong IFD1 là '1', thì định dạng hình ảnh thu nhỏ không được nén (được gọi là hình ảnh TIFF). Điểm bắt đầu của dữ liệu hình thu nhỏ là Thẻ StripOffset(0x0111), kích thước của hình thu nhỏ là tổng của Thẻ StripByteCounts(0x0117).

## Người giới thiệu ##

* [EXIF - Theo Wikipedia](https://vi.wikipedia.org/wiki/Exif)
* [Định dạng tệp EXIF](https://www.media.mit.edu/pia/Research/deepview/exif.html)

