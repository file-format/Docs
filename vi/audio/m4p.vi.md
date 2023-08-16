{
  "date" : "2021-06-09",
  "keywords" :[ "m4p", "mp3", "tệp", "phần mở rộng", "định dạng", "định dạng tệp m4p là gì", "nhạc", "định dạng tệp m4p", "M4b so với MP3", "đặc tả định dạng tệp m4p "],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Tìm hiểu về định dạng tệp M4P và các API có thể tạo, chuyển đổi và mở tệp M4P.",
  "title" :"M4P - Định dạng tệp sách nói MPEG-4",
  "linktitle" : "M4P",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-06-09"
}

## Tệp M4P là gì?
Tệp có phần mở rộng .m4p là tệp âm thanh thường có sẵn tại Apple iTunes store để tải xuống. Nói cách khác, chúng ta có thể nói rằng M4P là tệp AAC nhưng được bảo vệ chống sao chép bằng cách sử dụng Quản lý quyền kỹ thuật số (DRM). Điều đó có nghĩa là chỉ có thể phát các tệp M4P trên các hệ thống hoặc thiết bị được ủy quyền. Thông thường các tệp M4P dành riêng cho các thiết bị đa phương tiện của Apple. Vì vậy, những tệp này chỉ có thể được phát trên Apple macbook, podcast, điện thoại thông minh như iPhone 6 hoặc iPhone 7.

## Định dạng tệp M4P
M4P là viết tắt của MPEG 4 Protected (âm thanh) và nó mã hóa âm thanh bằng codec âm thanh nâng cao (AAC) và bảo vệ tệp khỏi việc sử dụng tệp trái phép. Định dạng tệp này thường được coi là định dạng tệp âm thanh của iTunes Music Store. Apple sử dụng hệ thống Quản lý quyền kỹ thuật số FairPlay (DRM) để bảo vệ các tệp M4P. FairPlay DRM dựa trên công nghệ do Veridisc phát triển. Cơ chế bảo vệ của nó hoạt động bằng cách mã hóa luồng âm thanh AAC bằng mã hóa AES. Người dùng nhận được khóa chính được gán cho tài khoản của mình để giải mã. Định dạng tệp này được giới thiệu để thay thế định dạng tệp MP3, vì MP3 ban đầu không được dự định là tệp âm thanh mà là lớp III trong tệp video MPEG 1 hoặc 2.


## Thông số kỹ thuật định dạng tệp M4P

Tương tự như [M4A](/vi/audio/m4a/), các tệp M4P cũng bao gồm các đoạn liên tiếp. Mỗi đoạn có tiêu đề 8 byte và được chia thành:
- Kích thước chunk 4 byte (big-endian, byte cao trước)
- Loại chunk 4 byte - một trong các chữ ký được xác định trước: "mdat", "moov", "pnot", "moof", "udta", "uuid", "free", "skip", "ftyp", "jP2 ", "wide", "load", "imap", "matt", "chap", "kmat", "clip", "crgn", "sync", "tmcd", "PICT", "scpt ", "ctab", "ssrc".

Tương tự như M4A, đoạn đầu tiên trong M4P sẽ thuộc loại "ftype" và có loại phụ ở độ lệch 8. M4P được xác định bởi loại phụ phải là "M4P_".

Lặp lại các đoạn, cho đến khi phát hiện thấy đoạn không xác định, Nó sẽ soạn tệp M4P (âm thanh MPEG-4).

## Người giới thiệu ##

* [MPEG-4 Phần 14 - Theo Wikipedia](https://en.wikipedia.org/wiki/MPEG-4_Part_14)
* [Ví dụ khôi phục và định dạng âm thanh MPEG-4 Phần 14 (M4A,M4B,M4P)](https://www.file-recovery.com/m4a-signature-format.htm)

