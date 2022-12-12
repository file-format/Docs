{
  "date" : "2021-04-26",
  "keywords" :[ "m4a", "mp3", "tệp", "phần mở rộng", "định dạng", "định dạng tệp m4a là gì", "âm nhạc", "định dạng tệp m4a", "M4A so với MP3", "đặc tả định dạng tệp m4a "],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Tìm hiểu về định dạng tệp M4A và các API có thể tạo, chuyển đổi và mở tệp M4A.",
  "title" :"M4A - Tệp âm thanh MPEG-4",
  "linktitle" : "M4A",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-04-26"
}

## Tệp M4A là gì?

**Định dạng tệp M4A** là tệp âm thanh được tạo bằng cách sử dụng AAC (Mã hóa âm thanh nâng cao) được gọi là nén mất dữ liệu. Từ M4A viết tắt là MPEG 4 Audio. Các tệp âm thanh này thường có phần mở rộng tệp .m4a. Điều này đặc biệt đúng với nội dung không được bảo vệ. Nó có thể lưu trữ nhiều loại nội dung âm thanh khác nhau, chẳng hạn như sách nói, bài hát và podcast. M4A thường được nhận ra là định dạng nâng cao hơn MP3, định dạng này thường không được thiết kế chỉ dành cho âm thanh. Nó chỉ là một lớp âm thanh trong các tệp video MPEG 1 hoặc 2.

Định dạng M4A được mã hóa bởi FairPlay Digital Rights Management khi được bán qua iTunes Store sử dụng tiện ích mở rộng .m4p. iPhone của Apple sử dụng âm thanh MPEG-4 cho nhạc chuông nhưng những tệp âm thanh đó sử dụng phần mở rộng .m4r.


## M4A so với MP3

Cả M4A và [MP3](https://docs.fileformat.com/audio/mp3/) đều là định dạng tệp chỉ có âm thanh.

**M4A**: Tốt hơn MP3 về chất lượng và kích thước khi được mã hóa ở cùng tốc độ bit. Phần mở rộng tệp .m4a rất phổ biến vì chúng đã được Apple sử dụng để sử dụng trong iTunes Music Store. M4A là một tệp âm thanh được nén bằng công nghệ MPEG-4; một thuật toán để nén mất dữ liệu. Về cơ bản, nó được liên kết với “Lớp âm thanh MPEG-4”, các tệp có phần mở rộng .m4a là lớp âm thanh của phim MPEG-4. Nó được dự định sẽ vượt qua MP3 và trở thành tiêu chuẩn mới trong nén âm thanh. Nó rất gần với MP3 theo nhiều cách nhưng được giới thiệu là có chất lượng tốt hơn với cùng kích thước tệp hoặc thậm chí nhỏ hơn. Định dạng M4A lần đầu tiên được giới thiệu bởi Apple. Loại định dạng cũng được nhận ra là Bộ mã hóa không mất dữ liệu của Apple (ALE).

Do đó, hiện tại M4A không thể đạt được thành công chủ đạo của MP3 vì định dạng âm thanh nói chung chưa thể phát được. Bằng cách nào đó, nó chỉ giới hạn ở MacOS, iPod và các sản phẩm khác của Apple.

**Mp3**: Định dạng âm thanh kỹ thuật số nổi tiếng nhất. Nó cũng là một trong những định dạng nén đầu tiên xuất hiện và trở nên rất phổ biến đối với những người yêu âm nhạc. Thành công chính của nó nhanh đến mức loại tệp này có khả năng được phát phổ biến và với hầu hết mọi thứ, phần cứng hoặc phần mềm. Theo nghĩa chung, M4A sẽ tạo ra chất lượng âm thanh tốt hơn, nhưng nhiều người sẽ tranh luận rằng, dù đúng hay sai thì sự khác biệt về âm thanh cũng không thể phân biệt được và sẽ rất lãng phí thời gian khi cố gắng chuyển đổi tệp MP3 thành tệp M4A. Cuối cùng, việc chuyển đổi sẽ khiến bạn mất đi chất lượng âm thanh ban đầu.

## Thông số định dạng tệp M4A

Các tệp M4A bao gồm các khối liên tiếp. Mỗi đoạn có tiêu đề 8 byte và được chia thành:
- Kích thước chunk 4 byte (big-endian, byte cao trước)
- Loại khối 4 byte - một trong các chữ ký được xác định trước: "ftyp", "mdat", "moov", "pnot", "udta", "uuid", "moof", "free", "skip", "jP2 ", "wide", "load", "ctab", "imap", "matt", "kmat", "clip", "crgn", "sync", "chap", "tmcd", "scpt ", "ssrc", "PICT".

Đoạn đầu tiên sẽ thuộc loại "ftype" và có một loại phụ ở độ lệch 8. M4A được xác định bởi loại phụ phải là "M4A_", đối với loại phụ M4B phải là "M4B_" và đối với loại phụ M4P phải là "M4P_".

Lặp lại các đoạn, cho đến khi phát hiện thấy đoạn không xác định, Nó sẽ soạn tệp M4A (âm thanh MPEG-4).

## Người giới thiệu ##

* [MPEG-4 Phần 14 - Theo Wikipedia](https://en.wikipedia.org/wiki/MPEG-4_Part_14)
* [Ví dụ khôi phục và định dạng âm thanh MPEG-4 Phần 14 (M4A,M4B,M4P)](https://www.file-recovery.com/m4a-signature-format.htm)

