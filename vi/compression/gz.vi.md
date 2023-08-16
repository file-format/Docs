{
  "date" : "2019-10-11",
  "keywords" :[ "tệp gz", "định dạng tệp gz", "tệp gz là gì", "tệp", "ví dụ gz", "phần mở rộng tệp gz","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Định dạng tệp GZ - Tệp lưu trữ nén GNU",
  "description":"Tìm hiểu về tệp GZ là gì và các API có thể tạo và mở tệp GZ.",
  "linktitle" : "GZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2019-09-10"
}

## Tệp GZ là gì?

Tệp GZ là một kho lưu trữ nén được tạo bằng thuật toán nén [gzip](https://en.wikipedia.org/wiki/Gzip) (GNU zip) tiêu chuẩn. Nó có thể chứa nhiều tệp nén, thư mục và sơ khai tệp. Định dạng này ban đầu được phát triển để thay thế các định dạng nén trên hệ thống UNIX. và vẫn là một trong những loại lưu trữ phổ biến nhất trên hệ thống Linux. Các ứng dụng như [WinZip](https://www.winzip.com/en/) có thể mở các tệp GZ để xem nội dung của nó trên cả Windows và MacOS.

## Định dạng tệp GZ - Thông tin khác

Gzip sử dụng thuật toán [DEFLATE](https://en.wikipedia.org/wiki/DEFLATE) để nén tệp lưu trữ và khác với định dạng tệp lưu trữ [ZIP](/vi/compression/zip/) trong việc áp dụng thuật toán nén trên toàn bộ tệp lưu trữ thay vì các tệp riêng lẻ. Thông số kỹ thuật định dạng tệp GZIP phiên bản 4.3 do Lực lượng Đặc nhiệm Kỹ thuật Internet (IETF) xuất bản chứa thông tin chi tiết về định dạng tệp. Định dạng tệp bao gồm:

* Tiêu đề tệp
* Tiêu đề tùy chọn
* Dữ liệu nén
* Chân trang tệp

## Tiêu đề tệp GZ ##

Tiêu đề tệp GZ bao gồm 10 byte như sau:

|Bù đắp|Kích thước|Giá trị|Mô tả
---|---|---|---|
|0|2|0x1f 0x8b|Số ma thuật xác định loại tệp
|2|1| |Phương pháp nén * 0-7 (Dành riêng) * 8 (Xả hơi)
|3|1| |Cờ tập tin
|4|4| |dấu thời gian 32-bit
|8|1| |Cờ nén
|9|1| |ID hệ điều hành

### Cờ tệp ###

|Giá trị|Định danh|Mô tả
---|---|---|
|0x01|FTEXT|Nếu được đặt, dữ liệu không nén cần được coi là văn bản thay vì dữ liệu nhị phân. Cờ này gợi ý chuyển đổi cuối dòng cho các tệp văn bản đa nền tảng nhưng không thực thi nó.
|0x02|FHCRC|Tệp chứa tổng kiểm tra tiêu đề (CRC-16)
|0x04|FEXTRA|Tệp chứa các trường bổ sung
|0x08|FNAME|Tệp chứa chuỗi tên tệp gốc
|0x10|FCOMMENT|Tệp chứa bình luận
|0x20| |dành riêng
|0x40| |dành riêng
|0x80| |dành riêng

### Hệ điều hành ###

|Giá trị|Mô tả
---|---|
|0|Hệ thống tập tin FAT (MS-DOS, OS/2, NT/Win32)
|1|Amiga
|2|VMS (hoặc OpenVMS)
|3|Unix
|4|VM/CMS
|5|Điều khoản dịch vụ Atari
|6|Hệ thống tập tin HPFS (OS/2, NT)
|7|Macintosh
|8|Hệ thống Z
|9|CP/M
|10|TOPS-20
|11|Hệ thống tập tin NTFS (NT)
|12|QĐOS
|13|RỦI RO Acorn
|255|không rõ

## Tiêu đề tùy chọn GZ ##

Các tiêu đề bổ sung tùy chọn là những tiêu đề được biểu thị bằng cờ tệp và bao gồm thông tin như tên tệp gốc, các trường bổ sung, nhận xét và tổng kiểm tra tiêu đề.

## Dữ liệu nén ##

Phần này chứa dữ liệu được nén bằng thuật toán nén DEFLATE.

## Chân trang tệp GZ ##

Chân trang tệp có kích thước 8 byte và chứa thông tin sau.

|Bù đắp|Kích thước|Mô tả
---|---|---|
|0|4|Tổng kiểm tra (CRC-32)
|4|4|Giá trị kích thước dữ liệu không nén theo byte

## Người giới thiệu ##

* [gzip - Wikipedia](https://en.wikipedia.org/wiki/Gzip)
* [RFC1952: Đặc tả định dạng tệp GZIP](https://datatracker.ietf.org/doc/html/rfc1952), bởi IETF.

