{
  "date" : "2020-01-10",
  "keywords" :[ "tệp dib", "định dạng tệp dib", "tệp dib là gì", "tệp", "ví dụ dib", "phần mở rộng tệp dib","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DIB",
  "description":"Tìm hiểu về định dạng tệp DIB và API có thể tạo và mở tệp DIB.",
  "linktitle" : "DIB",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-01-10"
}

## Tệp DIB là gì?

Ảnh bitmap không phụ thuộc vào thiết bị (DIB) là tệp ảnh raster có cấu trúc tương tự như tệp ảnh bitmap tiêu chuẩn([BMP]()/image/bmp/)). Nó chứa một bảng màu mô tả ánh xạ các màu RGB tới các giá trị pixel. Điều này cho phép DIB thể hiện hình ảnh trên bất kỳ thiết bị nào. Nó có thể được mở bằng hầu hết tất cả các ứng dụng có thể mở tệp BMP tiêu chuẩn trên Windows cũng như macOS. DIB là các tệp nhị phân và có định dạng tệp phức tạp tương tự như BMP. Hình ảnh DIB độc lập với khả năng đầu ra của thiết bị hiển thị về độ sâu màu và pixel trên mỗi inch.

## Thông số định dạng tệp DIB ##
DIB chứa thông tin về màu sắc và kích thước sau:

* Định dạng màu của thiết bị mà hình ảnh hình chữ nhật được tạo.
* Độ phân giải của thiết bị mà hình ảnh hình chữ nhật được tạo ra.
* Bảng màu cho thiết bị tạo hình ảnh.
* Một mảng bit ánh xạ bộ ba màu đỏ, lục, lam ( RGB ) thành các pixel trong hình chữ nhật.
* Mã định danh nén dữ liệu cho biết sơ đồ nén dữ liệu (nếu có) được sử dụng để giảm kích thước của mảng bit.

### Định dạng khối dữ liệu DIB ###

DIB xuất hiện trong bối cảnh khối bộ nhớ so với các tệp .DIB được lưu trữ trên đĩa. Khối bộ nhớ bao gồm cấu trúc phù hợp với thông số kỹ thuật Windows API cho DIB. DIB thực tế bao gồm:
* Một tiêu đề
* Bảng màu
* Dữ liệu điểm ảnh

Trên thực tế, làm việc với dữ liệu bảng màu, tiêu đề và hình ảnh được thực hiện như thể chúng là ba khối bộ nhớ riêng biệt. Một tay cầm cho khối bộ nhớ chung này được gán bằng GlobalAlloc và được gọi là HDIB, được sử dụng để trích xuất và làm việc với dữ liệu tiêu đề, bảng màu và pixel.

### Cấu trúc ###
Thông tin chứa trong DIB được biểu diễn bằng các cấu trúc khác nhau. Bao gồm các:

BITMAPInfo - Xác định thông tin kích thước và màu sắc cho một DIB
```
typedef struct tagBITMAPINFO {
  BITMAPINFOHEADER bmiHeader;
  RGBQUAD          bmiColors[1];
} BITMAPINFO, *LPBITMAPINFO, *PBITMAPINFO;
```
Nó bao gồm một BITMAPINFOHEADER:

```
typedef struct tagBITMAPINFOHEADER {
  DWORD biSize;
  LONG  biWidth;
  LONG  biHeight;
  WORD  biPlanes;
  WORD  biBitCount;
  DWORD biCompression;
  DWORD biSizeImage;
  LONG  biXPelsPerMeter;
  LONG  biYPelsPerMeter;
  DWORD biClrUsed;
  DWORD biClrImportant;
} BITMAPINFOHEADER, *PBITMAPINFOHEADER;
```
theo sau là hai hoặc nhiều cấu trúc RGBQAD.

```
typedef struct tagRGBQUAD {
  BYTE rgbBlue;
  BYTE rgbGreen;
  BYTE rgbRed;
  BYTE rgbReserved;
} RGBQUAD;
```
### Bit dữ liệu ###
|Bit|Mô tả|
---|---|
|Định dạng 1 bit (đơn sắc)|Ảnh bitmap đơn sắc bao gồm hai màu (đen và trắng). Do số lượng màu hạn chế này, các ảnh bitmap này chiếm ít dung lượng hơn trên đĩa. BitBitCount trả về true hoặc false để thể hiện cả hai màu. Hầu hết các ứng dụng hoàn toàn bỏ qua bảng màu nếu bitBitCount==1.
|Định dạng 4 bit (VGA hoặc 16 màu)|Mỗi byte dữ liệu hình ảnh đại diện cho hai pixel và bitBitCount==4. Các bit này đại diện cho màu của pixel theo thứ tự giảm dần.
|Định dạng 8 bit (256 màu)|Định dạng 8 bit này có thể biểu thị tối đa 256 màu. Mỗi byte trong mảng dữ liệu bitmap của hình ảnh đại diện cho một pixel. Giá trị của byte đó là số lượng mục nhập bảng màu được sử dụng từ 256 mục nhập được biểu thị bằng bmciColors.
|Định dạng 24 bit (TrueColor)|Các bản đồ bit này có thể có tối đa 2^24 màu (biBitCount == 24). Mỗi chuỗi ba byte trong mảng dữ liệu bản đồ bit biểu thị cường độ tương đối của ba màu chính của một pixel. Màu sắc được mô tả là các giá trị nằm trong khoảng từ 0 đến 255 và được lưu trữ trong ba byte theo thứ tự Xanh lam, Xanh lục và Đỏ. Đây là một sự khác biệt quan trọng, bởi vì hầu hết các tham chiếu đến màu sắc trong Windows sử dụng thứ tự ngược lại: Đỏ/Lục/Xanh lam, vì vậy hãy nghĩ "BGR" khi làm việc với hình ảnh TrueColor thay vì "RGB". Một bảng màu có thể được chỉ định để tăng tốc quá trình vẽ cho Windows, trong trường hợp đó, biClrUsed sẽ không bằng 0. Nhưng như bạn có thể thấy, bảng màu này không cần thiết vì bản thân dữ liệu pixel đã chứa thông tin màu.
|Định dạng 32 bit|Hình ảnh 32 bit có tối đa 2^24 màu (biBitCount == 24).

## Người giới thiệu ##
* [Bản đồ bit độc lập với thiết bị - Bởi Microsoft](https://docs.microsoft.com/en-us/windows/win32/gdi/device-independent-bitmaps)

