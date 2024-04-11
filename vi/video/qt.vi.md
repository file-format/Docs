{
  "date" : "2021-02-15",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Định dạng tệp QT - Tệp phim nhanh",
  "keywords" :[ "QT", "QuickTime video", "qt format", "how to play qt files", "Quick Movie File", "QTFF", "video", "Apple" ],
  "description":"Tìm hiểu về định dạng tệp QT và các API có thể tạo và mở tệp QT.",
  "linktitle" : "QT",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-02-16"
}

## Tệp QT là gì?

Tệp có phần mở rộng .qt là tệp chứa đa phương tiện được khuôn khổ QuickTime sử dụng để lưu trữ nội dung tệp đa phương tiện. Được phát triển bởi Apple Inc. Định dạng tệp QuickTime (QTFF) là một tệp chứa đa phương tiện có chứa âm thanh, video hoặc văn bản để phát lại sau này. Đây là định dạng được lựa chọn để trao đổi phương tiện kỹ thuật số giữa các thiết bị, ứng dụng và hệ điều hành. Các tệp QT cũng được lưu ở định dạng [MOV](/vi/video/mov/) cũng được phát triển bởi Apple Inc. Một số ứng dụng có thể mở tệp QT bao gồm trình phát Apple QuickTime, trình phát phương tiện VLC và Media Player Classic với K- Gói giải mã Lite.

## Định dạng tệp QT

QTFF là hướng đối tượng, hiển thị một bộ sưu tập các đối tượng linh hoạt để dễ phân tích cú pháp và mở rộng. Mỗi bản nhạc trong tệp QT chứa luồng phương tiện được mã hóa kỹ thuật số hoặc tham chiếu dữ liệu đến luồng phương tiện nằm trong tệp khác. Cấu trúc dữ liệu phân cấp bao gồm các đối tượng được gọi là nguyên tử hoạt động như các thùng chứa theo dõi. Thông số định dạng tệp cho [Định dạng tệp QT](https://developer.apple.com/documentation/quicktime-file-format) được Apple Inc cung cấp chính thức để nhà phát triển tham khảo.

### Mô tả phương tiện

Mô tả phương tiện của tệp QuickTime được lưu trữ riêng biệt với dữ liệu phương tiện. Thông tin như số lượng bản nhạc, định dạng nén video và thông tin thời gian được lưu trữ trong mô tả phương tiện (còn được gọi là tài nguyên phim, nguyên tử phim hoặc đơn giản là phim). Dữ liệu phương tiện được tham chiếu bởi một chỉ mục trong cấu trúc phương tiện này. Dữ liệu phương tiện là dữ liệu mẫu thực tế, chẳng hạn như khung hình video và mẫu âm thanh, được sử dụng trong phim.

### Nguyên tử

Atom là đơn vị cơ bản của tệp QuickTime. Có hai trường chính trong bất kỳ nguyên tử nào trước bất kỳ trường nào khác: trường Kích thước và Loại. Trường kích thước hiển thị kích thước của nguyên tử trong khi trường loại cho biết loại dữ liệu được lưu trữ trong nguyên tử. Về bản chất, các nguyên tử có thứ bậc, nghĩa là một nguyên tử có thể chứa các nguyên tử khác và nguyên tử này vẫn có thể chứa các nguyên tử khác. Bố cục của một nguyên tử mẫu được hiển thị trong hình ảnh sau đây.

Mỗi nguyên tử có hai phần, tiêu đề và dữ liệu. Tiêu đề chứa các trường kích thước và loại và phần dữ liệu chứa dữ liệu thực tế. Hơn nữa, mỗi lĩnh vực được giải thích dưới đây:

#### Kích thước nguyên tử

Tiêu đề và nội dung của nguyên tử được biểu thị bằng một số nguyên 32 bit được gọi là kích thước của nguyên tử. Trường kích thước chứa kích thước của nguyên tử theo byte, được biểu thị bằng số nguyên không dấu 32 bit.

#### Loại nguyên tử

Loại nguyên tử cũng được hiển thị bằng số nguyên 32 bit, phần lớn được coi là trường bốn ký tự có giá trị kemonic, chẳng hạn như 'moov' (0x6D6F6F76) cho nguyên tử phim hoặc 'trak' (0x7472616B) cho nguyên tử phim một nguyên tử theo dõi. Khi đã biết loại nguyên tử, nó cho phép diễn giải dữ liệu của nó.

![alt text](../QT_Sample_Atom.png "QT File Format")

## Cấu trúc tệp ##

Các tệp QT/MOV bao gồm các đoạn liên tiếp. Mỗi đoạn có tiêu đề 8 byte: kích thước đoạn 4 byte (big-endian, byte cao đầu tiên) và loại đoạn 4 byte - một trong các chữ ký được xác định trước: "ftyp", "mdat", "moov", "pnot ", "udta", "uuid", "moof", "free", "skip", "jP2 ", "wide", "load", "ctab", "imap", "matt", "kmat", "clip", "crgn", "sync", "chap", "tmcd", "scpt", "ssrc", "PICT". Đoạn đầu tiên thuộc loại "ftype" và có loại phụ ở độ lệch 8. MOV được xác định bởi loại phụ phải là "qt". Để soạn tệp MOV, cần lặp lại các khối cho đến khi phát hiện loại không xác định.

Đây là một ví dụ mẫu: Kiểm tra dữ liệu nhị phân của tệp MOV mẫu, rõ ràng là nó bắt đầu bằng chữ ký **ftyp** (hex: 66 74 79 70) ở offset 4, định nghĩa Loại tệp chứa QuickTime. Loại tệp phụ là **qt~_~_** (hex: 71 74 20 20) trỏ đến loại tệp MOV. Kích thước khối đầu tiên là 32 (hex: 00 00 00 20, big-endian, byte cao đầu tiên), kích thước nằm ở offset 0. Tại offset 32 (hex: 20) là chunk thứ hai, có kích thước 8 và nhập **mdat** (hệ thập lục phân: 6D 64 61 74).

Đoạn tiếp theo nằm ở offset 32+8#40 (hex: 28) và có kích thước 3.263.028 (hex: 00 31 CA 34) và gõ **mdat** (hex: 6D 64 61 74) ở offset 44 (hex : 2C). Đoạn tiếp theo nằm ở offset 40 + 3,263,028#3,263,068 (hex: 00 31 CA 5C) và có kích thước 21,189 (hex: 00 00 52 C5) và gõ **moov** (hex: 6D 6F 6F 76) tại offset 1.836.019.574 (hệ thập lục phân: 00 31 CA 60). Đây là đoạn cuối cùng, vì vậy tổng kích thước tệp là 3.263.068+21.189#3.284.257 byte.

## Người giới thiệu ##

* [Định dạng tệp QT - Apple Inc.](https://developer.apple.com/documentation/quicktime-file-format)
* [Định dạng tệp QuickTime - Wikipedia](https://en.wikipedia.org/wiki/QuickTime_File_Format)

