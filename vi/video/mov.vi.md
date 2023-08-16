{
  "date" : "2019-10-11",
  "keywords" :[ "tệp mov", "định dạng tệp mov", "tệp mov là gì", "tệp", "ví dụ mov", "phần mở rộng tệp mov","phần mở rộng", "định dạng", "QuickTime", "MPEG- 4" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Tệp MOV - Định dạng tệp phim QuickTime của Apple",
  "description":"Tìm hiểu về định dạng tệp MOV và API có thể tạo và mở tệp MOV.",
  "linktitle" : "MOV",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-07-29"
}

## Tệp MOV là gì?

Tệp MOV là loại tệp video, được phát triển bởi Apple Inc., chứa một hoặc nhiều bản nhạc. Mỗi bản nhạc lưu trữ một bộ phim, âm thanh, đoạn phim và phụ đề. Nó là một thùng chứa đa phương tiện có thể lưu trữ các loại thành phần phương tiện khác nhau. Định dạng video MOV tương thích với cả hệ thống Windows và Macintosh. Nó sử dụng mã MPEG-4 để nén và các bản nhạc được duy trì trong các đối tượng được gọi là nguyên tử được đặt trong cấu trúc dữ liệu phân cấp.

## Lịch sử tóm tắt về định dạng tệp MOV

Định dạng tệp MPEG-4 đã phát triển từ đặc tả Định dạng tệp QuickTime (**QTFF**) vào năm 2001. Tổ chức Tiêu chuẩn hóa Quốc tế đã phê duyệt định dạng này và các thông số kỹ thuật của hệ thống MPEG-4 Phần 1 đã được xuất bản vào năm 1999. Năm 2001, một tệp sửa đổi định dạng [MP4](/vi/video/mp4/) đã được xuất bản.

Phiên bản đầu tiên của MP4 đã được sửa đổi vào năm 2003 với tên gọi MPEG-4 Phần 14 (ISO/IEC 14496-14:2003). Năm 2004, MP4 được khái quát hóa để xác định cấu trúc chung cho tất cả các tệp phương tiện dựa trên thời gian. Do đó, bây giờ nó được sử dụng làm cơ sở cho nhiều định dạng tệp đa phương tiện khác.

## Định dạng tệp QuickTime (QTFF) - Thông tin khác

Để làm việc với đa phương tiện kỹ thuật số, QTFF có thể chứa nhiều loại dữ liệu. Đây là một định dạng ý tưởng để trao đổi phương tiện kỹ thuật số vì định dạng này xác định các tiêu chuẩn để mô tả bất kỳ loại cấu trúc phương tiện nào. Định dạng tệp bao gồm một tập hợp linh hoạt các đối tượng hướng đối tượng. Để lưu trữ phim trên đĩa, QuickTime sử dụng hai cấu trúc tức là `nguyên tử` và `nguyên tử QT`.

### Nguyên tử

Atom là đơn vị cơ bản của tệp QuickTime. Có hai trường chính trong bất kỳ nguyên tử nào trước bất kỳ trường nào khác: trường Kích thước và Loại. Trường kích thước hiển thị kích thước của nguyên tử trong khi trường loại cho biết loại dữ liệu được lưu trữ trong nguyên tử. Về bản chất, các nguyên tử có thứ bậc, nghĩa là một nguyên tử có thể chứa các nguyên tử khác mà nguyên tử này vẫn có thể chứa các nguyên tử khác. Bố cục của một nguyên tử mẫu được hiển thị trong hình ảnh sau đây.

Mỗi nguyên tử có hai phần, `tiêu đề` và `dữ liệu`. Tiêu đề chứa các trường kích thước và loại và phần dữ liệu chứa dữ liệu thực tế. Hơn nữa, mỗi lĩnh vực được giải thích dưới đây:

### Kích thước nguyên tử

Tiêu đề và nội dung của nguyên tử được biểu thị bằng một số nguyên 32 bit được gọi là kích thước của nguyên tử. Trường kích thước chứa kích thước của nguyên tử theo byte, được biểu thị bằng số nguyên không dấu 32 bit.

### Loại nguyên tử

Loại nguyên tử cũng được hiển thị bằng số nguyên 32 bit, phần lớn được coi là trường bốn ký tự có giá trị kemonic, chẳng hạn như 'moov' (0x6D6F6F76) cho nguyên tử phim hoặc 'trak' (0x7472616B) cho nguyên tử phim một nguyên tử theo dõi. Khi đã biết loại nguyên tử, nó cho phép diễn giải dữ liệu của nó.

### QT Atom và Atom Container

Các nguyên tử QT cung cấp một định dạng lưu trữ cho mục đích chung và có một tiêu đề mở rộng bao gồm các trường Kích thước, Loại, ID nguyên tử và Số lượng nguyên tử con. Các nguyên tử QT được bọc trong một thùng chứa nguyên tử, một cấu trúc dữ liệu duy nhất có tiêu đề với số lượng khóa. Có một nguyên tử gốc trong mỗi vật chứa nguyên tử là nguyên tử QT. Sơ đồ nguyên tử QT được thể hiện trong hình bên dưới.

Tiêu đề bộ chứa nguyên tử QT có dữ liệu sau:

Dành riêng: Phần tử 10 byte có giá trị 0.

Lock Count: Số nguyên 16 bit có giá trị bằng 0.

Tiêu đề nguyên tử QT có dữ liệu sau:

**Size -** Nội dung và tiêu đề nguyên tử QT được biểu thị bằng byte bởi một số nguyên 32 bit. Trong trường hợp nguyên tử lá, thì trường này chứa kích thước của một nguyên tử.

**Loại -** Loại nguyên tử được biểu thị bằng số nguyên 32 bit. Trong trường hợp đó là nguyên tử gốc, thì giá trị được đặt thành 'sean'.

**ID nguyên tử -** Đó là số nguyên 32 bit hiển thị ID nguyên tử và phải là duy nhất cho tất cả các anh chị em. Nguyên tử gốc luôn có giá trị ID nguyên tử là 1.

**Dành riêng -** Số nguyên 16 bit phải được đặt thành 0.

**Số lượng con -** Một số nguyên 16 bit cho biết số lượng nguyên tử con của một nguyên tử.

**Dành riêng -** Số nguyên 32 bit phải được đặt thành 0.

## Cấu trúc tệp của tệp MOV

Tệp MOV bao gồm các đoạn liên tiếp. Mỗi đoạn có tiêu đề 8 byte: kích thước đoạn 4 byte (big-endian, byte cao đầu tiên) và loại đoạn 4 byte - một trong các chữ ký được xác định trước: "ftyp", "mdat", "moov", "pnot ", "udta", "uuid", "moof", "free", "skip", "jP2 ", "wide", "load", "ctab", "imap", "matt", "kmat", "clip", "crgn", "sync", "chap", "tmcd", "scpt", "ssrc", "PICT". Đoạn đầu tiên thuộc loại "ftype" và có loại phụ ở độ lệch 8. MOV được xác định bởi loại phụ phải là "qt". Để soạn tệp MOV, cần lặp lại các khối cho đến khi phát hiện loại không xác định.

Đây là `ví dụ mẫu`: Kiểm tra dữ liệu nhị phân của tệp MOV mẫu, rõ ràng là nó bắt đầu bằng chữ ký **ftyp** (hex: 66 74 79 70) ở offset 4, định nghĩa Loại tệp bộ chứa QuickTime. Loại tệp phụ là **qt~_~_** (hex: 71 74 20 20) trỏ đến loại tệp MOV. Kích thước khối đầu tiên là 32 (hex: 00 00 00 20, big-endian, byte cao đầu tiên), kích thước nằm ở offset 0. Tại offset 32 (hex: 20) là chunk thứ hai, có kích thước 8 và nhập **mdat** (hệ thập lục phân: 6D 64 61 74).

Đoạn tiếp theo nằm ở offset 32+8#40 (hex: 28) và có kích thước 3.263.028 (hex: 00 31 CA 34) và gõ **mdat** (hex: 6D 64 61 74) ở offset 44 (hex : 2C). Đoạn tiếp theo nằm ở offset 40 + 3,263,028#3,263,068 (hex: 00 31 CA 5C) và có kích thước 21,189 (hex: 00 00 52 C5) và gõ **moov** (hex: 6D 6F 6F 76) tại offset 1.836.019.574 (hệ thập lục phân: 00 31 CA 60). Đây là đoạn cuối cùng, vì vậy tổng kích thước tệp là 3.263.068+21.189#3.284.257 byte.

## Làm cách nào để chuyển đổi tệp MOV?

Có rất nhiều trình phát phương tiện và phần mềm chỉnh sửa video có sẵn để chuyển đổi tệp MOV sang các định dạng tệp video phổ biến khác. Một số trình phát đa phương tiện có thể chuyển đổi tệp MOV sang các định dạng khác bao gồm:

* Trình phát đa phương tiện Videolan VLC
* Trình phát Eltima Elmedia

Một số trình phát phương tiện và trình chỉnh sửa video, bao gồm trình phát phương tiện VideoLAN VLC và Eltima Elmedia Player, có thể chuyển đổi các tệp MOV sang các định dạng khác. Những phần mềm này có thể chuyển đổi các tệp MOV sang các định dạng video sau.

* Video MPEG-4 - [MP4](/vi/video/mp4/)
* Video WebM - [WEBM](/vi/video/webm/)
* Luồng truyền tải video - [TS](/vi/video/ts/)
* Định dạng hệ thống nâng cao - [ASF](/vi/video/ts/)
* Âm thanh Ogg Vorbis - [OGG](/vi/audio/ogg/)
* Âm thanh MP3 - [MP3](/vi/audio/mp3/)
* Bộ giải mã âm thanh Lossless miễn phí - [FLAC](/vi/audio/flac/)
* Âm thanh WAVE - [WAV](/vi/audio/wav/)

## API nguồn mở cho tệp MOV

* [API phản ứng gốc để chuyển đổi MOV sang MP4](https://github.com/taltultc/react-native-mov-to-mp4)
* [API Python để sửa tệp MOV](https://github.com/nrosenstein-stuff/movrepair)
* [API Ruby để chuyển đổi MOV sang GIF](https://github.com/skygroundmedia/convert-mov-to-gif)

## Người giới thiệu

* [https://en.wikipedia.org/wiki/QuickTime_File_Format](https://en.wikipedia.org/wiki/QuickTime_File_Format)

