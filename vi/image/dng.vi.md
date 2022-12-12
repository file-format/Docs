{
  "date" : "2019-10-11",
  "keywords" :[ "tệp dng", "định dạng tệp dng", "tệp dng là gì", "tệp", "ví dụ dng", "phần mở rộng tệp dng","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DNG - Định dạng tệp ảnh máy ảnh kỹ thuật số",
  "description":"Tìm hiểu về định dạng tệp DNG và các API có thể tạo và mở tệp DNG.",
  "linktitle" : "DNG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Tệp DNG là gì?

DNG là định dạng hình ảnh máy ảnh kỹ thuật số được sử dụng để lưu trữ các tệp thô. Nó đã được Adobe phát triển vào tháng 9 năm 2004. Về cơ bản, nó được phát triển để chụp ảnh kỹ thuật số. DNG là phần mở rộng của định dạng chuẩn [TIFF](/vi/image/tiff/)/EP và sử dụng siêu dữ liệu đáng kể. Để thao tác dữ liệu thô từ máy ảnh kỹ thuật số một cách dễ dàng linh hoạt và kiểm soát nghệ thuật, các nhiếp ảnh gia chọn các tệp thô của máy ảnh. Các định dạng JPEG và TIFF lưu trữ hình ảnh được máy ảnh xử lý, do đó, không có nhiều chỗ để thay đổi ở các định dạng như vậy.

## Lịch sử và các phiên bản của định dạng tệp DNG

Cho đến nay đã có 5 phiên bản đặc tả DNG. Phiên bản 1.0.0.0 được tung ra vào tháng 9 năm 2004 cùng với việc phát hành "2.3" (ACR và DNG Converter). Vào tháng 2 năm 2005, phiên bản 1.1.0.0 đã được xuất bản. Vào tháng 5 năm 2008, phiên bản 1.2.0.0 được phát hành và được sử dụng trong "4.4". Phiên bản 1.3.0.0 được xuất bản vào tháng 6 năm 2009. Phiên bản 1.4.0.0 xuất hiện vào năm 2012.

## Định dạng tệp DNG

Trong khi đó, các tệp thô của máy ảnh ghi lại dữ liệu chưa được xử lý hoặc được xử lý ở mức độ thấp trực tiếp từ cảm biến. Vì chúng tương tự như phim âm bản nên các định dạng thô của máy ảnh còn được gọi là "Âm bản kỹ thuật số". Lợi ích của các định dạng thô là tăng khả năng kiểm soát nghệ thuật cho người dùng cuối. Người dùng có thể điều chỉnh các dải thông số khác nhau tùy theo yêu cầu như cân bằng trắng, ánh xạ tông màu, giảm nhiễu, làm sắc nét, v.v. Mặt khác, tệp thô của máy ảnh phải được xử lý cho mọi mục đích sử dụng thông qua bất kỳ phần mềm nào hoặc thông qua trình chuyển đổi.

Vì không có sẵn định dạng tiêu chuẩn cho các tệp thô của máy ảnh nên nó đã tạo ra nhiều vấn đề cho người dùng cuối. Những vấn đề này đã được Adobe giải quyết và xác định định dạng không độc quyền cho các tệp thô của máy ảnh. Định dạng này được gọi là Phủ định kỹ thuật số hoặc DNG. DNG có thể được sử dụng bởi nhiều loại phần cứng và phần mềm để xử lý các tệp thô. Ngoài ra, DNG cũng có thể được sử dụng làm định dạng trung gian để lưu trữ hình ảnh được chụp ban đầu bằng máy ảnh có định dạng thô độc quyền của riêng chúng.

### Thông số kỹ thuật định dạng tệp DNG

Trong phần này, chúng tôi sẽ mô tả định dạng DNG dưới dạng phần mở rộng của TIFF 6.0.

* **Phần mở rộng tệp**: DNG sử dụng phần mở rộng “.DNG” hoặc “.TIF”.
* **Cây SubIFD**: DNG không hỗ trợ chuỗi SubIFD, thay vào đó, DNG khuyến nghị sử dụng cây SubIFD như đã đề cập trong thông số kỹ thuật TIFF-EP. Chất lượng và độ phân giải cao nhất có thể sử dụng NewSubFileType bằng 0, trong khi hình thu nhỏ có chất lượng thấp hơn nên sử dụng NewSubFileType bằng 1. Bạn cũng nên sử dụng IFD đầu tiên mặc dù không bắt buộc phải có hình thu nhỏ có chất lượng hoặc độ phân giải thấp.
* **Thứ tự byte**: Trình đọc DNG phải hỗ trợ thứ tự byte, cũng như đối với các tệp từ một kiểu máy ảnh cụ thể.
* **Điểm ảnh bị che **: Hầu hết các cảm biến máy ảnh đều tính toán các điểm ảnh bị che hoàn toàn ở rìa cảm biến thông qua mã hóa màu đen. Những pixel này có thể được bao gồm hoặc cắt bớt trước khi hình ảnh được lưu trữ ở định dạng DNG. Nếu các pixel bị che không được cắt bớt, thì diện tích của các pixel này phải được đề cập trong thẻ ActiveArea. Thông tin được thu thập từ các pixel này về mức độ mã hóa màu đen nên được sử dụng trước khi dữ liệu thô được lưu trữ hoặc có thể được đưa vào tệp DNG chỉ định mức độ màu đen.
* **Các pixel bị lỗi**: Trước khi lưu trữ dữ liệu thô dưới dạng DNG, các pixel bị lỗi phải được loại trừ.
* **Siêu dữ liệu**: Siêu dữ liệu có thể được đưa vào DNG theo bất kỳ cách nào sau đây:
** Bằng cách sử dụng thẻ siêu dữ liệu TIFF-EP hoặc EXIF
** Thông qua thẻ siêu dữ liệu IPTC (33723)
** Sử dụng thẻ siêu dữ liệu XMP (700)
* **Dữ liệu độc quyền**: Thông thường, các nhà cung cấp bao gồm dữ liệu độc quyền trong tệp thô để các bộ chuyển đổi của riêng họ sử dụng. DNG lưu trữ dữ liệu độc quyền của họ trong thẻ riêng, IFD riêng và trong MakerNote riêng. Các nhà cung cấp phải sử dụng thẻ DNGPrivateData và MakerNoteSafety để đảm bảo các ứng dụng chỉnh sửa tệp DNG lưu giữ dữ liệu độc quyền này.

Sau đây là một số hạn chế quan trọng và các thẻ TIFF mở rộng.

**Số bit trên mỗi mẫu**

8 đến 32 bit/mẫu được hỗ trợ. Phải có cùng độ sâu cho mỗi mẫu khi SamplesPerPixel không bằng 1. Nhưng nếu BitsPerSample không bằng 8 hoặc 16 hoặc 32, thì các bit phải được đóng gói thành byte bằng cách sử dụng FillOrder mặc định của TIFF là 1 (big-endian).

**Nén**

Hai giá trị thẻ Nén được hỗ trợ:

* Giá trị #1: Dữ liệu không nén.
* Giá trị #7: Dữ liệu nén JPEG, hoặc nén JPEG DCT cơ bản hoặc nén JPEG không mất dữ liệu.

**Giải thích trắc quang**

Các giá trị sau chỉ được hỗ trợ cho IFD hình thu nhỏ và xem trước:

* 1 = BlackIsZero. Được cho là ở trong không gian màu gamma 2.2.
* 2 = RGB. Được cho là nằm trong không gian màu sRGB.
* 6 = YCbCr. Được sử dụng cho hình ảnh xem trước được mã hóa JPEG.

Các giá trị sau được hỗ trợ cho IFD thô và được coi là không gian màu gốc của máy ảnh:

*32803#CFA (Mảng lọc màu).
* 34892 # Tuyến tínhRaw.

**Định hướng**

Thẻ định hướng được sử dụng cho các trình duyệt tệp để chúng có thể thực hiện xoay các tệp DNG không mất dữ liệu. Trình đọc DNG phải hỗ trợ tất cả các hướng có thể, bao gồm các hướng được nhân đôi.

## Các tính năng trong Phiên bản DNG mới nhất

Phiên bản DNG 1.4 tháng 10 năm 2012 có các tính năng nâng cao sau.

* Cắt người dùng mặc định
* Minh bạch
* Điểm nổi (HDR)
* Nén mất dữ liệu
* Proxy

## Người giới thiệu ##

* [Thông số kỹ thuật DNG - Bởi Adobe](https://www.kronometric.org/phot/processing/DNG/dng_spec_1.4.0.0.pdf)
* [Phủ định kỹ thuật số - Wikipedia](https://en.wikipedia.org/wiki/Digital_Negative)
* [DNG - Định dạng lưu trữ công khai cho dữ liệu thô của máy ảnh kỹ thuật số](https://helpx.adobe.com/photoshop/digital-negative.html)

