{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Muhammad Ahmad Chishti"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Định dạng tệp MKV",
  "keywords" :[ "mkv", "matroska video", "định dạng mkv", "cách phát tệp mkv", "video", "tệp", "định dạng" ],
  "description":"Tìm hiểu về định dạng tệp MKV và API có thể tạo và mở tệp MKV.",
  "linktitle" : "MKV",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2020-17-11"
}


## Tệp MKV là gì? ##

MKV (Matroska Video) là một bộ chứa đa phương tiện tương tự như định dạng [MOV](/vi/video/mov/) và [AVI](/vi/video/avi/) nhưng nó hỗ trợ nhiều rãnh âm thanh và phụ đề trong cùng một tệp. Tệp MKV là định dạng bộ chứa đa phương tiện Matroska được sử dụng cho video. MKV dựa trên Ngôn ngữ meta nhị phân mở rộng và nó hỗ trợ một số định dạng nén video và âm thanh. Sự khác biệt chính giữa MKV và các định dạng video khác là MKV là một bộ chứa chứ không phải codec. Các tệp MKV được lưu với phần mở rộng tệp .mkv. MKV có thể kết hợp âm thanh, video và phụ đề trong một tệp ngay cả khi những thành phần đó sử dụng các loại mã hóa khác nhau. Ví dụ: bạn có thể có tệp MKV chứa video H.264 và MP3 hoặc AAC cho âm thanh. MKV cũng hỗ trợ mô tả, xếp hạng, ảnh bìa và thậm chí cả điểm chương. Có một số tính năng chính mà MKV là minh chứng cho tương lai. Những tính năng này bao gồm:

- Hỗ trợ tìm kiếm nhanh.
- Khả năng chọn các luồng âm thanh và video khác nhau.
- Hỗ trợ phụ đề (mã hóa cứng và mã hóa mềm).
- Hỗ trợ siêu dữ liệu, chương và menu.
- Khả năng phát trực tuyến.
- Khả năng khôi phục các tệp bị lỗi cung cấp khả năng phát các tệp bị hỏng.

## Lược Sử ##

Tệp MKV có nguồn gốc từ năm 2002 tại Nga. Nhà phát triển chính là Lasse Kärkkäinen, người đã làm việc với người sáng lập Matroska, Steve Lhomme và một nhóm lập trình viên. MKV được phát triển như một dự án tiêu chuẩn mở, có nghĩa là nó là nguồn mở và miễn phí sử dụng. Thời gian trôi qua, định dạng này đã được cải thiện và trở thành nền tảng của định dạng đa phương tiện WebM vào năm 2010.

## Thiết kế Matroska ##

Matroska thêm các ràng buộc sau vào đặc tả EBML.

- **Dạng tài liệu** của **Tiêu đề EBML** phải là 'matroska'.
- **EBMLMaxIDLength** của **EBML Header** phải là 4.
- **EBMLMaxSizeLength** của **EBML Header** phải nằm trong khoảng từ 1 đến 8 (bao gồm).

Tất cả các phần tử cấp cao nhất được mã hóa trong 4 octet.

- Mã ngôn ngữ: Matroska (phiên bản 1 đến 3) đã sử dụng mã ngôn ngữ có thể ở dạng thư mục ISO-639-2 gồm 3 chữ cái (như "fre" cho tiếng Pháp) hoặc mã quốc gia bổ sung có thể được sử dụng như "fre-ca " cho tiếng Pháp Canada. Bắt đầu từ Matroska phiên bản 4, ISO 639-2 hoặc BCP 47 CÓ THỂ được sử dụng cho mã ngôn ngữ, mặc dù BCP 47 được khuyến nghị.
- Các loại vật lý: Chúng có ý nghĩa khác nhau đối với cả tệp âm thanh và video. Ví dụ: ChapterPhysicalEquiv = 60 có nghĩa là (CD / 12" / 10" / 7" / TAPE / MINIDISC / DAT) cho âm thanh và (DVD / VHS / LASERDISC) cho video.
- Cấu trúc khối - Tiêu đề khối: Tiêu đề khối chứa thông tin về số bản nhạc, dấu thời gian, loại viền, v.v.
- Lacing: Là cơ chế tiết kiệm dung lượng khi lưu trữ dữ liệu thường dùng cho các khối dữ liệu nhỏ (frame). Có 3 kiểu thắt dây:
  - Xiph: Frame with a size multiple of 255 coded with a 0 at the end of the size. For example, The code for 765 is 255;255;255;0.
  - EBML: The frame size is coded as a difference between the previous size and this size. The first size in the lace is unsigned but others use a range shift to get a sign on each value.
  - fixed-size: The size remains the same.
- Cấu trúc SimpleBlock: Nó được lấy cảm hứng từ **Cấu trúc khối** với sự khác biệt chính là việc bổ sung các cờ **Khung hình chính** và **Có thể loại bỏ**. Ngoài ra, mọi thứ đều giống nhau.

## Cấu trúc Matroska ##

Một tài liệu Matroska phải bao gồm ít nhất một **Tài liệu EBML** sử dụng **Loại tài liệu Matroska**. Mỗi **Tài liệu EBML** phải bắt đầu bằng **Tiêu đề EBML** theo sau là **Phần tử gốc EBML** được xác định là Phân đoạn. Matroska định nghĩa một số Phần tử cấp cao nhất có thể xuất hiện trong **Phân đoạn**.

EBML sử dụng hệ thống các Thành phần để soạn Tài liệu EBML, Sau đây là danh sách các Thành phần cấp cao nhất trong tệp Matroska:

- **Tài liệu EBML**: Trình bao bọc cho toàn bộ tệp.
- **Tiêu đề EBML**: Nó chứa thông tin tiêu đề cho tệp như DocType.
- **Segment**: Phần tử trên cùng chứa tất cả các phần tử cấp cao nhất khác.
- **SeekHead**: Nó chứa vị trí của Phân đoạn của các Phần tử cấp cao nhất khác.
- **Thông tin**: Nó chứa thông tin chung về Phân đoạn.
- **Đường đi**: Thành phần thông tin cấp cao nhất với nhiều đường đi được mô tả.
- **Chương**: Nó được sử dụng để xác định các menu cơ bản và dữ liệu phân vùng.
- **Cluster**: Phần tử Cấp cao nhất chứa cấu trúc Khối.
- **Cues**: Phần tử cấp cao nhất chứa tất cả các mục cục bộ của Phân đoạn giúp tăng tốc độ tìm kiếm quyền truy cập.
- **Phần đính kèm**: Phần này chứa các tệp đính kèm.
- **Thẻ**: Phần tử này chứa siêu dữ liệu mô tả Bản nhạc, Phiên bản, Chương, Phần đính kèm hoặc toàn bộ Phân đoạn.

Bảng sau đây cho thấy cấu trúc của tài liệu Matroska với hầu hết các yếu tố được hiển thị theo thứ bậc:

| | | | | | | |
| -- | -- | -- | -- | -- | -- | -- |
| Tiêu đề EBML | | | |
| Phân khúc | Tìm Kiếm| Tìm kiếm | ID tìm kiếm |
| | | | Vị trí tìm kiếm |
| | Thông tin | Phân khúcUID | |
| | | Phân đoạnTên tệp | |
| | | TrướcUID | |
| | | TrướcTên tập tin | |
| | | Tiếp theoUID | |
| | | Tiếp theoTên tệp | |
| | | Phân khúcGia đình | |
| | | ChươngDịch | |
| | | Thang đo dấu thời gian | |
| | | Thời lượng | |
| | | NgàyUTC | |
| | | Tiêu đề | |
| | | MuxingApp | |
| | | Viết ứng dụng | |
| | Bài hát | Theo dõi Nhập cảnh | Số theo dõi |
| | | | Theo dõiUID |
| | | | Loại đường |
| | | | Tên |
| | | | Ngôn ngữ |
| | | | CodecID |
| | | | CodecPrivate |
| | | | CodecName |
| | | | Video | CờXen kẽ |
| | | | | Dòng thứ tự |
| | | | | Chế độ âm thanh nổi |
| | | | | Chế độ Alpha |
| | | | | Chiều rộng pixel |
| | | | | PixelHeight |
| | | | | Chiều rộng hiển thị |
| | | | | Chiều cao hiển thị |
| | | | | AspectRatioType |
| | | | | Màu |
| | | | Âm thanh | Tần suất lấy mẫu |
| | | | | Kênh |
| | | | | BitDepth |
| | Chương | Phiên bảnEntry | Phiên bảnUID |
| | | | BảnCờẨn |
| | | | Phiên bảnFlagDefault |
| | | | Phiên bảnCờĐặt hàng |
| | | | ChươngAtom | ChươngUID |
| | | | | ChươngStringUID |
| | | | | ChapterTimeStart |
| | | | | ChapterTimeEnd |
| | | | | ChươngCờẨn |
| | | | | ChươngDisplay | ChapString |
| | | | | | ChapNgôn Ngữ |
| | Cụm | Dấu thời gian |
| | | Dấu vết im lặng |
| | | Vị trí |
| | | TrướcKích thước |
| | | khối đơn giản |
| | | KhốiNhóm |
| | | Khối được mã hóa |
| | Cues | CuePoint | CueTime |
| | | | CueTrackPositions |
| | Tệp đính kèm | Tệp đính kèm | Mô tả tệp |
| | | | Tên tệp |
| | | | FileMimeType |
| | | | TệpUID |
| | | | Giới thiệu tệp |
| | | | FileUsedStartTime |
| | | | FileUsedEndTime |
| | Thẻ | Thẻ | Mục tiêu | TargetTypeValue |
| | | | | Loại mục tiêu |
| | | | | TagTrackUID |
| | | | | TagPhiên bảnUID |
| | | | | ThẻChươngUID |
| | | | | Thẻ Đính kèmUID |
| | | | Thẻ đơn giản | TagName |
| | | | | TagNgôn ngữ |
| | | | | TagDefault |
| | | | | TagString |
| | | | | Thẻnhị phân |
| | | | | Thẻ đơn giản |


### Sử dụng Codec ###

Nếu bạn không muốn có một trình phát đa phương tiện mới và muốn sử dụng trình phát hiện tại của mình, bạn sẽ cần cài đặt một số codec (viết tắt của nén/giải nén). Mặc dù tải xuống codec là một tùy chọn hợp lệ, nhưng bạn nên cẩn thận về nguồn gốc và chúng có thể chứa phần mềm độc hại.

## Người giới thiệu ##

- [Matroska của Wikipedia](https://en.wikipedia.org/wiki/Matroska)

