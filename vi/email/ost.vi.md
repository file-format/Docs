{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OST - Định dạng tệp lưu trữ Outlook",
  "description":"Tìm hiểu về định dạng tệp OST và các API có thể tạo và mở tệp OST.",
  "linktitle" : "OST",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Tệp OST là gì?

OST hoặc Tệp lưu trữ ngoại tuyến biểu thị dữ liệu hộp thư của người dùng ở chế độ ngoại tuyến trên máy cục bộ khi đăng ký với Exchange Server bằng Microsoft Outlook. Nó được tạo tự động trong lần sử dụng đầu tiên của Microsoft Outlook khi kết nối với máy chủ. Sau khi tệp được tạo, dữ liệu sẽ được đồng bộ hóa với máy chủ email để nó có sẵn ngoại tuyến cũng như trong trường hợp máy chủ email bị ngắt kết nối. Các tệp OST có thể sử dụng các mục hộp thư như email, danh bạ, thông tin lịch, ghi chú, tác vụ và các dữ liệu tương tự khác. Người dùng có thể tạo email và các mục dữ liệu khác trong tệp OST ngay cả khi không có kết nối với máy chủ, nhưng chúng sẽ không được đồng bộ hóa với máy chủ. Sau khi kết nối được thiết lập, tệp cục bộ sẽ được đồng bộ hóa lại với máy chủ để cả máy chủ và bản sao cục bộ đều ở cùng một mức thông tin.

## Định dạng tệp OST

Định dạng tệp OST (Bảng Lưu trữ Ngoại tuyến) và [PST](/vi/email/pst/) (Bảng Lưu trữ Cá nhân) bao gồm định dạng Tệp Thư mục Cá nhân (PFF) tương ứng với việc lưu trữ email, danh bạ và cuộc hẹn của người dùng. Dữ liệu trong tệp PFF được lưu trữ trong little-endian với tất cả ngày và giờ được biểu thị dưới dạng FILETIME theo UTC. [MS-PST] định nghĩa hai loại PFF:

* Định dạng ANSI 32-bit
* Định dạng Unicode 64-bit

Định dạng tệp PST [thông số kỹ thuật](https://learn.microsoft.com/en-us/openspecs/office_file_formats/ms-pst/141923d5-15ab-4ef1-a524-6dce75aae546), do Microsoft cung cấp, cũng có thể áp dụng cho định dạng tệp OST miễn phí và cấp phép bằng sáng chế không thể hủy bỏ thông qua Lời hứa đặc điểm kỹ thuật mở. Nó bao gồm các yếu tố có thể phân biệt sau:

* Tiêu đề bay
* Dữ liệu tiêu đề tệp
* Nút nhánh chỉ mục
* Nút lá chỉ số
* (Tệp) chỉ số offset
* (Mục) chỉ số mô tả
* Mô tả cục bộ
* Loại bảng mục

### Thông tin tiêu đề

Cấu trúc HEADER của tệp OST nằm ở phần đầu của tệp ở độ lệch 0. Nó chứa thông tin siêu dữ liệu về tệp OST và thông tin ROOT để truy cập cấu trúc dữ liệu Lớp NDB được mô tả ở trên. Cấu trúc HEADER khác với các phiên bản Unicode và ANSI của Định dạng tệp OST.

Tiêu đề bắt đầu bằng từ ma thuật 4 byte **!BDN** được biểu thị bằng byte (0x21, 0x42, 0x44, 0x4E). Một số ma thuật 2 byte khác, **SM** (0x53, 0x4D), nằm ở offset 8 tính từ đầu tệp. Thông tin phiên bản (ANSI hoặc Unicode) nằm ở độ lệch 10 từ đầu tệp. Giá trị hex (0x17) chỉ định tệp Unicode OST trong khi 0x0E hoặc 0x0F đại diện cho định dạng tệp ANSI.

|Trường|Mô tả
---|---|
|dwMagic (4 byte)|PHẢI là "{ 0x21, 0x42, 0x44, 0x4E } ("!BDN")"
|dwCRCPartial (4 byte)|Giá trị CRC 32 bit của 471 byte dữ liệu bắt đầu từ wMagicClient (0ffset 0x0008)
|wMagicClient (2 byte)|PHẢI là "{ 0x53, 0x4D }".
|wVer (2 byte)|Phiên bản định dạng tệp. Giá trị này PHẢI là 14 hoặc 15 nếu tệp là tệp ANSI PST và PHẢI là 23 nếu tệp là tệp PST Unicode.
|wVerClient (2 byte)|Phiên bản định dạng tệp máy khách. Phiên bản tương ứng với định dạng được mô tả trong tài liệu này là 19. Người tạo tệp PST mới dựa trên tài liệu này NÊN khởi tạo giá trị này thành 19.
|bPlatformCreate (1 byte)|Giá trị này PHẢI được đặt thành 0x01.
|bPlatformAccess (1 byte)|Giá trị này PHẢI được đặt thành 0x01.
|dwReserveed (8 byte)|
|bidUnused (chỉ 8 byte Unicode)|Phần đệm không sử dụng được thêm khi định dạng tệp PST Unicode được tạo.
|bidNextP (Unicode: 8 byte; ANSI: 4 byte)|BID trang tiếp theo. Các trang có bộ đếm đặc biệt để phân bổ giá trị bidIndex. Giá trị của bidIndex cho BID cho các trang được phân bổ từ bộ đếm này.
|bidNextB (chỉ 4 byte ANSI): |Giá thầu tiếp theo. Giá trị này là bộ đếm đơn điệu cho biết BID sẽ được chỉ định cho khối được phân bổ tiếp theo. Giá trị BID tăng dần theo gia số 4. Để biết thêm chi tiết, xem phần 2.2.2.2.
|dwUnique (4 byte)|Đây là một giá trị đơn điệu tăng dần được sửa đổi mỗi khi cấu trúc HEADER của tệp PST được sửa đổi. Chức năng của giá trị này là cung cấp một giá trị duy nhất và để đảm bảo rằng các CRC HEADER khác nhau sau mỗi lần sửa đổi tiêu đề.
|rgnid[]   (128 byte)|Một mảng cố định gồm 32 NID, mỗi NID tương ứng với một trong 32 NID_TYPE có thể có (NID_TYPE, NID_TYPE_NORMAL_FOLDER, NID_TYPE_SEARCH_FOLDER, NID_TYPE_NORMAL_MESSAGE,NID_TYPE_ASSOC_MESSAGE)
|qwChưa sử dụng (8 byte)|Dung lượng chưa sử dụng; PHẢI được đặt thành không. Chỉ định dạng tệp Unicode PST.
|root (Unicode: 72 byte; ANSI: 40 byte)|Cấu trúc ROOT (mục 2.2.2.5).
|dwAlign (4 byte)|Các byte căn chỉnh không được sử dụng; PHẢI được đặt thành không. Chỉ định dạng tệp Unicode PST.
|rgbFM (128 byte)|FMap không dùng nữa. Điều này không còn được sử dụng và PHẢI được điền bằng 0xFF. Người đọc NÊN bỏ qua giá trị của các byte này.
|rgbFP (128 byte)|FPMap không dùng nữa. Điều này không còn được sử dụng và PHẢI được điền bằng 0xFF. Người đọc NÊN bỏ qua giá trị của các byte này.
|bSentinel (1 byte)|PHẢI được đặt thành 0x80.
|bCryptMethod (1 byte)|Cho biết cách dữ liệu trong tệp PST được mã hóa. PHẢI được đặt thành một trong các giá trị được xác định trước (NDB_CRYPT_NONE, NDB_CRYPT_PERMUTE, NDB_CRYPT_CYCLIC).
|rgbReserveed (2 byte)| Kín đáo; PHẢI được đặt thành không.
|bidNextB (8 byte)|Cho biết giá trị BID có sẵn tiếp theo. Chỉ định dạng tệp Unicode PST.
|bidNextB (CHỈ Unicode: 8 byte)|Giá thầu tiếp theo. Giá trị này là bộ đếm đơn điệu cho biết BID sẽ được chỉ định cho khối được phân bổ tiếp theo. Giá trị BID tăng dần theo gia số 4. Để biết thêm chi tiết, xem phần 2.2.2.2.
|dwCRCFull (4 byte)|Giá trị CRC 32 bit của 516 byte dữ liệu bắt đầu từ wMagicClient đến bidNextB, bao gồm cả. Chỉ định dạng tệp Unicode PST.
|ullReserveed (8 byte)|Reserveed; PHẢI được đặt thành không. Chỉ định dạng tệp ANSI PST.
|dwReserveed (4 byte)|Reserveed; PHẢI được đặt thành không. Chỉ định dạng tệp ANSI PST.
|rgbReserve2 (3 byte)|
|b Dành riêng (1 byte) |
|rgbReserve3 (32 byte) |

## Người giới thiệu

* Định dạng tệp [Thư mục cá nhân Outlook (.ost)](https://learn.microsoft.com/en-us/openspecs/office_file_formats/ms-pst/141923d5-15ab-4ef1-a524-6dce75aae546)
* [Thông số định dạng tệp thư mục cá nhân](https://github.com/libyal/libpff/blob/main/documentation/Personal%20Folder%20File%20(PFF)%20format.asciidoc)

