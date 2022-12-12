{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PST - Định dạng tệp lưu trữ thông tin cá nhân của Outlook",
  "description":"Tìm hiểu về định dạng tệp PST và API có thể tạo và mở tệp PST.",
  "linktitle" : "PST",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Tệp PST là gì?

Các tệp có phần mở rộng .pst đại diện cho Tệp Lưu trữ Cá nhân Outlook (còn được gọi là Bảng Lưu trữ Cá nhân) lưu trữ nhiều thông tin người dùng. Thông tin người dùng được lưu trữ trong các loại thư mục khác nhau bao gồm email, mục lịch, ghi chú, danh bạ và một số định dạng tệp khác. Các tệp PST được sử dụng để lưu trữ dữ liệu gửi email ngoại tuyến mà sau này có thể được tải và xem trong các ứng dụng khác nhau.

## Định dạng tệp PST Thông số kỹ thuật

Định dạng tệp PST [thông số kỹ thuật](https://msdn.microsoft.com/en-us/library/ff385210(v#office.12).aspx) có sẵn từ Microsoft dưới dạng giấy phép bằng sáng chế miễn phí và không thể hủy ngang thông qua Lời hứa về đặc điểm kỹ thuật mở .

### Loại Định dạng PST

Các định dạng tệp PST được phân loại thành hai loại dựa trên mã hóa của loại tệp. Các tệp PST được mã hóa ANSI là các định dạng tệp cũ hơn và chỉ được hỗ trợ bởi Outlook 2002 và các phiên bản cũ hơn. Những tệp như vậy có giới hạn kích thước tối đa là 2 GB (2^^31^^ Byte) và không hỗ trợ Unicode. Loại định dạng tệp hiện đại hơn, dựa trên mã hóa Unicode, loại bỏ giới hạn kích thước tệp và có thể đạt kích thước dữ liệu tối đa là 50GB.

### Tổ chức hợp lý của định dạng tệp PST

Cơ sở của định dạng tệp PST là B-Tree giữ cho dữ liệu được sắp xếp và cho phép tìm kiếm, truy cập tuần tự, chèn, xóa, v.v. trong thời gian logarit. Cấu trúc tổng thể của tệp PST được tổ chức thành ba lớp.

![Logical layers of a PST file](/vi/email/PST-1.png "Logical layers of a PST file")

`Lớp cơ sở dữ liệu nút (NDB)` - Lớp cơ sở dữ liệu nút nằm ở cấp thấp hơn của tệp PST và bao gồm cơ sở dữ liệu về các nút. Các nút này thực sự đại diện cho các cơ sở lưu trữ cấp thấp hơn của định dạng tệp PST. Lớp NDB bao gồm tiêu đề, thông tin phân bổ tệp, khối và BTree (Node BTree và Block BTree) từ quan điểm lưu trữ. Các nút và khối của Lớp NDB được liên kết thông qua BID dữ liệu, đây là một trong bốn thuộc tính của tham chiếu Nút, tức là NID (ID nút), NID gốc, BID dữ liệu (BID khối) và BID nút con.

`Lớp Danh sách, Bảng và Thuộc tính -` Lớp LTP cung cấp hiểu biết logic về các khái niệm cấp cao hơn trên NDB. Bên cạnh các yếu tố khác, lớp LTP chủ yếu bao gồm Ngữ cảnh thuộc tính (PC) và Ngữ cảnh bảng (TC). PC là tập hợp các thuộc tính, trong khi TC đại diện cho ma trận hai chiều của tập hợp các thuộc tính so với sự hiện diện của các thuộc tính này. Để triển khai PC và TC hiệu quả, lớp LTP sử dụng hai loại cấu trúc dữ liệu sau trên Nút NDB:

* Heap On Node (HN) - cho phép phân bổ phụ luồng dữ liệu của một nút thành các đoạn nhỏ, có kích thước thay đổi.
* BTree on Heap (BTH) - BTH cung cấp một cách thuận tiện và thiết thực để tìm kiếm thông qua các PC dữ liệu, được mô tả ở trên, được triển khai dưới dạng BTH và đó là lý do tại sao nó được triển khai bằng cách xây dựng bên trong cấu trúc HN.

`Lớp nhắn tin -` Các quy tắc cấp cao hơn và logic nghiệp vụ để làm việc với các tệp PST được triển khai ở lớp này. Kết quả đầu ra logic của lớp này là các đối tượng Thư mục, đối tượng Thư, đối tượng Tệp đính kèm và Thuộc tính có thể thực hiện được bằng cách kết hợp các lớp LTP và NDB. Các quy tắc và yêu cầu cần tuân theo khi sửa đổi nội dung PST cũng được xác định tại lớp này.

### Tổ chức vật lý của định dạng tệp PST

Mức độ tổ chức tệp cao của tệp PST được thể hiện trong hình bên dưới. Đây chỉ là tổng quan về các khái niệm khác nhau từ các thành phần logic của tệp PST.

![Physical organization of the PST file format](/vi/email/PST-2.png "Physical organization of the PST file format")


#### Thông tin tiêu đề PST

Cấu trúc HEADER của tệp PST nằm ở phần đầu của tệp ở độ lệch 0. Nó chứa thông tin siêu dữ liệu về tệp PST và thông tin ROOT để truy cập cấu trúc dữ liệu Lớp NDB được mô tả ở trên. Cấu trúc HEADER khác với các phiên bản Unicode và ANSI của Định dạng tệp PST.

Tiêu đề bắt đầu bằng từ ma thuật 4 byte **!BDN** được biểu thị bằng byte (0x21, 0x42, 0x44, 0x4E). Một số ma thuật 2 byte khác, **SM** (0x53, 0x4D), nằm ở offset 8 tính từ đầu tệp. Thông tin phiên bản (ANSI hoặc Unicode) nằm ở độ lệch 10 từ đầu tệp. Giá trị hex (0x17) chỉ định tệp Unicode PST trong khi 0x0E hoặc 0x0F đại diện cho định dạng tệp ANSI.

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
|rgnid[] (128 byte)|Một mảng cố định gồm 32 NID, mỗi NID tương ứng với một trong 32 NID_TYPE có thể có (NID_TYPE, NID_TYPE_NORMAL_FOLDER, NID_TYPE_SEARCH_FOLDER, NID_TYPE_NORMAL_MESSAGE,NID_TYPE_ASSOC_MESSAGE)
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

### Bảo vệ dữ liệu ###

Để bảo mật, các tệp PST cũng có thể được bảo vệ bằng mật khẩu, yêu cầu ứng dụng tải phải áp dụng mật khẩu trước khi có thể xem được. Mật khẩu áp dụng cho tệp PST được lưu trữ trong kho lưu trữ tin nhắn. Tuy nhiên, điều này không cung cấp khả năng bảo vệ dữ liệu mạnh mẽ vì mật khẩu có thể bị xóa bằng các công cụ có sẵn. Ngoài ra, mật khẩu do người dùng chỉ định không được sử dụng như một phần của khóa để mã hóa và giải mã các thuật toán mật mã. Do đó, không có lợi ích gì trong việc bảo vệ dữ liệu khỏi bị truy cập bởi các bên không được ủy quyền. Việc lưu trữ mật khẩu dưới dạng hàm băm CRC-32 của chuỗi gốc cũng khiến nó trở thành một phương pháp yếu để bảo mật dữ liệu trước cách tiếp cận vũ phu.

## Người giới thiệu ##

* Định dạng tệp [Thư mục cá nhân Outlook (.pst)](https://msdn.microsoft.com/en-us/library/ff385210(v#office.12).aspx)
* [Thông số định dạng tệp thư mục cá nhân](https://github.com/libyal/libpff/blob/master/documentation/Personal%20Folder%20File%20(PFF)%20format.asciidoc)

