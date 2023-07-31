{
  "date" : "2020-08-20",
  "keywords" :[ "tệp otf", "định dạng tệp otf", "tệp otf là gì", "tệp", "ví dụ otf", "phần mở rộng tệp otf","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OTF - Định dạng tệp phông chữ TrueType",
  "description":"Tìm hiểu về định dạng tệp OTF và các API có thể tạo và mở tệp OTF.",
  "linktitle" : "OTF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-09-21"
}

## Tệp OTF là gì?

Tệp có phần mở rộng .otf đề cập đến định dạng phông chữ OpenType. Định dạng phông chữ OTF có thể mở rộng hơn và mở rộng các tính năng hiện có của định dạng [TTF](/vi/font/ttf/) cho kiểu chữ kỹ thuật số. Được phát triển bởi Microsoft và Adobe, OTF kết hợp các tính năng của định dạng phông chữ PostScript và TrueType. Điều này làm cho định dạng OTF phù hợp với các hệ thống viết đa số và đó là lý do tại sao nó được sử dụng thống nhất trên các nền tảng máy tính lớn. Định dạng phông chữ OpenType được hỗ trợ bởi Mac OS X và Windows 2000 trở lên.

## Tóm tắt lịch sử

Yêu cầu về phông chữ OpenType bắt nguồn từ yêu cầu về định dạng phông chữ biểu cảm hơn có thể xử lý kiểu chữ đẹp. Ngoài ra, nó nhằm mục đích đáp ứng các yêu cầu về hành vi phức tạp của nhiều hệ thống chữ viết trên thế giới. Microsoft đã cố gắng cấp phép cho công nghệ đánh máy tiên tiến của Apple, được gọi là GX Typography, vào đầu những năm 1990. Điều này không diễn ra suôn sẻ và kết quả là Microsoft bắt đầu cải tiến công nghệ phông chữ TrueType của riêng mình vào năm 1994. Các sửa đổi cũng bao gồm để giới thiệu một định dạng phông chữ phù hợp hơn cũng đáp ứng các tính năng của định dạng phông chữ Loại 1 (PostScript) của Adobe.

Adobe, vào năm 1996, đã tham gia cùng Microsoft trong nỗ lực thay thế cả TrueType của Apple và các định dạng phông chữ Loại 1 của chính họ. Điều này dẫn đến sự kết hợp của cả hai định dạng phông chữ cơ bản để khắc phục những hạn chế và thêm các phần mở rộng mới. Công nghệ mới này được giới thiệu cùng năm với tên **OpenType**.

## Thông số kỹ thuật định dạng tệp OTF

Thông số kỹ thuật OTF được Microsoft công khai và có thể được tham khảo từ quan điểm của nhà phát triển. Giống như TTF, nó sử dụng cùng một cấu trúc bộ chứa 'sfnt' và tương thích với các thông số kỹ thuật của TrueType. Dữ liệu bên trong tệp phông chữ OpenType được sử dụng cho các mục đích khác nhau, chẳng hạn như tính toán bố cục văn bản, xác định các nét tượng trưng dưới dạng đường viền TrueType hoặc Định dạng Phông chữ Nhỏ gọn (CFF), cung cấp các tài liệu SVG hoặc bitmap đơn sắc hoặc màu dưới dạng mô tả nét vẽ thay thế và thông tin siêu dữ liệu.

### Các kiểu dữ liệu OTF
Các tệp OTF sử dụng các loại dữ liệu sau, tất cả đều có trong Big Endian.

|Kiểu dữ liệu| Mô tả|
---|---|
|uint8| Số nguyên không dấu 8 bit.|
|int8| Số nguyên có dấu 8 bit.|
|uint16| Số nguyên không dấu 16-bit.|
|int16| Số nguyên có dấu 16-bit.|
|uint24| Số nguyên không dấu 24-bit.|
|uint32| Số nguyên không dấu 32-bit.|
|int32| Số nguyên có dấu 32 bit.|
|Đã sửa| Số điểm cố định có chữ ký 32 bit (16.16)|
|FWORD| int16 mô tả số lượng trong đơn vị thiết kế phông chữ.|
|UFWORD| uint16 mô tả số lượng trong đơn vị thiết kế phông chữ.|
|F2DOT14| Số cố định có dấu 16 bit với phân số 14 bit thấp (2,14).|
|LONGDATETIME| Ngày và giờ được biểu thị bằng số giây kể từ 12:00 nửa đêm, ngày 1 tháng 1 năm 1904, UTC. Giá trị được biểu thị dưới dạng số nguyên 64 bit có dấu.|
|Thẻ| Mảng gồm bốn uint8 (độ dài = 32 bit) được sử dụng để xác định bảng, trục biến thể thiết kế, tập lệnh, hệ thống ngôn ngữ, tính năng hoặc đường cơ sở|
|Chênh lệch16| Độ lệch ngắn cho một bảng, giống như uint16, độ lệch NULL = 0x0000|
|bù đắp32| Độ lệch dài cho một bảng, giống như uint32, độ lệch NULL = 0x00000000|
|Phiên bản16Dot16| Giá trị 32 bit được đóng gói với các số phiên bản chính và phụ. (Xem Bảng số phiên bản.)|

### Thư mục bảng OTF

Một tệp OTF bắt đầu bằng một thư mục bảng. Thư mục này là tập hợp cấp cao nhất của các bảng trong tệp phông chữ. Tùy thuộc vào số lượng phông chữ trong một tệp, thư mục bảng có thể được đặt ở các vị trí khác nhau trong tệp. Ví dụ, trong trường hợp tệp phông chữ chỉ có một phông chữ, thư mục bảng bắt đầu từ byte 0 của tệp. Trong trường hợp có nhiều bộ sưu tập Phông chữ OpenType,
thư mục bảng bắt đầu được chỉ định trong TTCHeader.

|Loại |Tên |Mô tả|
---|---|---|
|uint32 |sfntVersion| 0x00010000 hoặc 0x4F54544F ('OTTO')|
|uint16| numTables |Số lượng bảng|
|uint16| phạm vi tìm kiếm |Lũy thừa tối đa của 2 nhỏ hơn hoặc bằng numTables, nhân 16 ((2\**floor(log2(numTables))) * 16, trong đó “**” là toán tử lũy thừa).|
|uint16 |entrySelector Log2 của lũy thừa tối đa 2 nhỏ hơn hoặc bằng numTables (log2(searchRange/16), bằng với floor(log2(numTables))).|
|uint16 |rangeShift |numTables nhân 16, trừ phạm vi tìm kiếm ((numTables * 16) - phạm vi tìm kiếm).|
|bảng ghi| tableRecords[numTables] |Mảng bản ghi bảng—một mảng cho mỗi bảng cấp cao nhất trong phông chữ|


### Bản ghi bảng

Đối với mỗi bảng cấp cao nhất trong phông chữ, có một Bản ghi bảng bao gồm các trường sau.

|Loại| Tên| Mô tả|
---|---|---|
|Thẻ| bảngTag| Định danh bảng.|
|uint32| tổng kiểm tra| Tổng kiểm tra cho bảng này.|
|bù đắp32| bù | Offset từ đầu file font.|
|uint32| chiều dài Chiều dài của bảng này.|

Mỗi bảng trong tệp phông chữ OpenType được biểu thị bằng các tên được gọi là thẻ bảng. Tất cả các bản ghi trong mảng phải được sắp xếp theo thứ tự tăng dần theo thẻ.

## Người giới thiệu
* [Thông số kỹ thuật phông chữ OpenType của Microsoft](https://learn.microsoft.com/en-us/typography/opentype/spec/overview)
* [Tổng quan về TrueType](https://learn.microsoft.com/en-us/typography/truetype/)

