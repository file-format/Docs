{
  "date" : "2019-12-09",
  "keywords" :[ "tệp zip", "định dạng tệp zip", "tệp zip là gì", "tệp", "ví dụ zip", "phần mở rộng tệp zip","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ZIP",
  "description":"Tệp ZIP là gì và các API có thể tạo và mở tệp ZIP.",
  "linktitle" : "ZIP",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2019-12-09"
}

## Tệp ZIP là gì? ##

Tệp có phần mở rộng .zip là tệp lưu trữ có thể chứa một hoặc nhiều tệp hoặc thư mục. Kho lưu trữ có thể áp dụng nén cho các tệp được bao gồm để giảm kích thước tệp ZIP. Định dạng tệp ZIP đã được Phil Katz công khai vào tháng 2 năm 1989 để đạt được khả năng lưu trữ tệp và thư mục. Định dạng này được tạo thành một phần của tiện ích [PKZIP](https://www.pkware.com/pkzip), được tạo bởi PKWARE, Inc. Ngay sau khi có sẵn [thông số kỹ thuật có sẵn](https://pkware.cachefly.net/ webdocs/casestudies/APPNOTE.TXT), nhiều công ty đã biến định dạng tệp ZIP thành một phần trong các tiện ích phần mềm của họ, bao gồm Microsoft (kể từ Windows 7), Apple (Mac OS X ) và nhiều công ty khác.

## Lịch sử tóm tắt về định dạng tệp ZIP

Lịch sử của định dạng tệp ZIP bắt nguồn từ sự kiện Hiệp hội Cải tiến Hệ thống (SEA) khởi kiện PKWARE vì đã sử dụng tiện ích ARC của họ mà không có quyền đối với nhãn hiệu cũng như bản quyền về hình thức và giao diện người dùng của sản phẩm. Trước đó, Phil Katz, đã viết lại mã nguồn của SEA và phát hành PKXARC, một trình trích xuất ARC và PKARC, một trình nén tệp, dưới dạng phần mềm miễn phí cho các hệ thống dựa trên MS-DOS. Thua vụ kiện, PKWARE không thể sử dụng bất cứ thứ gì liên quan đến ARC nữa. Đây là nơi tạo ra một tệp nén mới, được đặt tên là ZIP, được tạo thành một phần của tiện ích PKZIP tại PKWARE, Inc.

Katz đã phát hành các thông số kỹ thuật định dạng tệp ZIP vào phạm vi công cộng, trong khi vẫn giữ quyền sở hữu đối với tiện ích nén và giải nén của mình, tức là PKZIP. Hệ thống nén ZIP đã (và đang) có thể lưu trữ các tệp trong một thư mục bằng thuật toán kiểm tra dự phòng theo chu kỳ 32-bit ([CRC](http://en.wikipedia.org/wiki/Cyclic_redundancy_check)) để nén tệp kích thước. Không giống như ARC, các thư mục .ZIP bao gồm một tệp thư mục đóng vai trò là sổ mã của người viết mật mã, chứa thông tin cần thiết để hiển thị các tệp nén.

## Các phương pháp nén được hỗ trợ trong ZIP

Theo thông số kỹ thuật của Định dạng tệp .ZIP, các phương pháp nén sau đây được hỗ trợ.

* Lưu trữ - ngụ ý không nén
* Co lại
* Giảm (Điều này ngụ ý các hệ số nén từ cấp 1 đến cấp 4)
* Nổ tung
* Xì hơi
* Xì hơi64
* BZIP2
* LZMA (EFS)
* Gói Wav
* PPMd phiên bản I, Rev 1

DEFLATE là phương pháp nén thường được sử dụng, là thuật toán nén ngày không mất dữ liệu sử dụng kết hợp mã hóa LZ77 và Huffman và được trình bày chi tiết trong [RFC 1951](https://tools.ietf.org/html/rfc1951).

## Thông số kỹ thuật định dạng tệp ZIP

Các tệp ZIP có khả năng lưu trữ nhiều tệp bằng các kỹ thuật nén khác nhau đồng thời hỗ trợ lưu trữ một tệp mà không cần nén. Mỗi tệp được lưu trữ/nén riêng lẻ giúp trích xuất chúng hoặc thêm tệp mới mà không cần áp dụng nén hoặc giải nén cho toàn bộ kho lưu trữ.

### Định dạng tệp ZIP tổng thể

Mỗi tệp Zip được cấu trúc theo cách sau:


|Định dạng tệp ZIP
---|
|Tiêu đề tệp cục bộ 1
|Dữ liệu tệp 1
|Mô tả dữ liệu 1
|Tiêu đề tệp cục bộ 2
|Tệp Dữ liệu 2
|Mô tả dữ liệu 2
| ....
| ....
|Tiêu đề tệp cục bộ N
|Dữ liệu tệp N
|Mô tả dữ liệu N
|Lưu trữ Tiêu đề giải mã
|Lưu trữ bản ghi dữ liệu bổ sung
|Danh bạ trung tâm

Định dạng tệp ZIP sử dụng thuật toán CRC 32 bit cho mục đích lưu trữ. Để hiển thị các tệp nén, kho lưu trữ ZIP chứa một thư mục ở cuối lưu trữ mục nhập của các tệp được chứa và vị trí của chúng trong tệp lưu trữ. Do đó, nó đóng vai trò mã hóa để đóng gói thông tin cần thiết để hiển thị các tệp nén. Trình đọc ZIP sử dụng thư mục để tải danh sách tệp mà không cần đọc toàn bộ kho lưu trữ ZIP. Định dạng giữ các bản sao kép của cấu trúc thư mục để bảo vệ tốt hơn khỏi mất dữ liệu.

Mỗi tệp trong kho lưu trữ ZIP được thể hiện dưới dạng một mục nhập riêng lẻ trong đó mỗi mục nhập bao gồm Tiêu đề tệp cục bộ theo sau là dữ liệu tệp nén. Thư mục ở cuối kho lưu trữ chứa các tham chiếu đến tất cả các mục nhập tệp này. Trình đọc tệp ZIP nên tránh đọc các tiêu đề tệp cục bộ và tất cả các loại danh sách tệp nên được đọc từ Thư mục. Thư mục này là nguồn duy nhất cho các mục nhập tệp hợp lệ trong kho lưu trữ vì các tệp cũng có thể được thêm vào cuối kho lưu trữ. Đó là lý do tại sao nếu một người đọc đọc các tiêu đề cục bộ của kho lưu trữ ZIP ngay từ đầu, thì nó cũng có thể đọc các mục không hợp lệ (đã xóa) cũng như những mục không thuộc Thư mục đang bị xóa khỏi kho lưu trữ.

Thứ tự của các mục nhập tệp trong thư mục trung tâm không nhất thiết phải trùng với thứ tự các mục nhập tệp trong kho lưu trữ.

### Mục nhập Tệp ZIP

Các mục trong tệp ZIP được sắp xếp lần lượt trong đó mỗi mục bao gồm:

* Tiêu đề tệp cục bộ
* Trường dữ liệu bổ sung tùy chọn
* Dữ liệu người dùng (nén tùy chọn/mã hóa tùy chọn)

Tiêu đề tệp cục bộ của mỗi mục biểu thị thông tin về tệp như nhận xét, kích thước tệp và tên tệp. Các trường dữ liệu bổ sung (tùy chọn) có thể chứa thông tin cho các tùy chọn mở rộng của định dạng ZIP.

#### Tiêu đề tệp cục bộ

Tiêu đề tệp cục bộ có cấu trúc trường cụ thể bao gồm các giá trị nhiều byte. Tất cả các giá trị được lưu trữ theo thứ tự byte cuối nhỏ trong đó độ dài trường tính độ dài tính bằng byte. Tất cả các cấu trúc trong tệp ZIP sử dụng chữ ký 4 byte cho mỗi mục nhập tệp. Phần cuối của chữ ký thư mục trung tâm là 0x06054b50 và có thể được phân biệt bằng chữ ký duy nhất của riêng nó. Sau đây là thứ tự thông tin được lưu trữ trong Local File Header.


|Bù đắp|Byte|Mô tả
---|---|---|
|0|4|Chữ ký tiêu đề tệp cục bộ # 0x04034b50 (được đọc dưới dạng số cuối nhỏ)
|4|2|Phiên bản cần giải nén (tối thiểu)
|6|2|Cờ bit mục đích chung
|8|2|Phương pháp nén
|10|2|Thời gian sửa đổi lần cuối của tệp
|12|2|Ngày sửa đổi cuối cùng của tệp
|14|4|CRC-32
|18|4|Kích thước nén
|22|4|Kích thước không nén
|26|2|Độ dài tên tệp (n)
|28|2|Độ dài trường bổ sung (m)
|30|n|Tên tệp
|30+n|m|Trường bổ sung

#### Tiêu đề tệp thư mục trung tâm


|Bù đắp|Byte|Mô tả
---|---|---|
|0|4|Chữ ký tiêu đề tệp thư mục trung tâm # 0x02014b50
|4|2|Phiên bản do
|6|2|Phiên bản cần giải nén (tối thiểu)
|8|2|Cờ bit mục đích chung
|10|2|Phương pháp nén
|12|2|Thời gian sửa đổi lần cuối của tệp
|14|2|Ngày sửa đổi cuối cùng của tệp
|16|4|CRC-32
|20|4|Kích thước nén
|24|4|Kích thước không nén
|28|2|Độ dài tên tệp (n)
|30|2|Độ dài trường bổ sung (m)
|32|2|Độ dài chú thích tệp (k)
|34|2|Số đĩa bắt đầu tập tin
|36|2|Thuộc tính tệp nội bộ
|38|4|Thuộc tính tệp bên ngoài
|42|4|Độ lệch tương đối của tiêu đề tệp cục bộ. Đây là số byte giữa điểm bắt đầu của đĩa đầu tiên chứa tệp và điểm bắt đầu của tiêu đề tệp cục bộ. Điều này cho phép phần mềm đọc thư mục trung tâm xác định vị trí của tệp bên trong tệp ZIP.
|46|n|Tên tệp
|46+n|m|Trường bổ sung
|46+n+m|k|Chú thích tập tin

#### Kết thúc Bản ghi Thư mục Trung tâm


|Bù đắp|Byte|Mô tả
---|---|---|
|0|4|Kết thúc chữ ký thư mục trung tâm # 0x06054b50
|4|2|Số đĩa này
|6|2|Đĩa nơi thư mục trung tâm bắt đầu
|8|2|Số bản ghi thư mục trung tâm trên đĩa này
|10|2|Tổng số bản ghi thư mục trung tâm
|12|4|Kích thước của thư mục trung tâm (byte)
|16|4|Độ lệch của điểm bắt đầu thư mục trung tâm, so với điểm bắt đầu lưu trữ
|20|2|Độ dài bình luận (n)
|22|n|Bình luận

## Người giới thiệu

* [Thông số kỹ thuật định dạng tệp ZIP của PKWARE](https://pkware.cachefly.net/webdocs/casestudies/APPNOTE.TXT)
* [Cấu trúc của tệp PKZip](https://users.cs.jmu.edu/buchhofp/forensics/formats/pkzip-printable.html)

